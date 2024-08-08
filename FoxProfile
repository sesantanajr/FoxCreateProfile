# Função para encontrar a instalação do Firefox
function Find-FirefoxInstallation {
    $firefoxPath = (Get-Command firefox -ErrorAction SilentlyContinue).Source
    if (-not $firefoxPath) {
        # Tentativa de encontrar Firefox no caminho padrão de instalação
        $defaultPaths = @(
            "C:\Program Files\Mozilla Firefox\firefox.exe",
            "C:\Program Files (x86)\Mozilla Firefox\firefox.exe"
        )
        foreach ($path in $defaultPaths) {
            if (Test-Path $path) {
                $firefoxPath = $path
                break
            }
        }
    }
    if (-not $firefoxPath) {
        Write-Host "Firefox não encontrado no sistema."
        return $null
    }
    return $firefoxPath
}

# Função para criar um perfil do Firefox
function Create-FirefoxProfile {
    param (
        [string]$ProfileName
    )
    $firefoxPath = Find-FirefoxInstallation
    if ($firefoxPath) {
        Start-Process -FilePath $firefoxPath -ArgumentList "-CreateProfile `"$ProfileName`"" -NoNewWindow -Wait
        Write-Host "Perfil '$ProfileName' criado com sucesso."
    }
}

# Função para criar um atalho
function Create-Shortcut {
    param (
        [string]$Name,
        [string]$TargetPath,
        [string]$Arguments,
        [string]$IconLocation,
        [string]$ShortcutLocation
    )
    $shell = New-Object -ComObject WScript.Shell
    $shortcut = $shell.CreateShortcut("$ShortcutLocation\$Name.lnk")
    $shortcut.TargetPath = $TargetPath
    $shortcut.Arguments = $Arguments
    $shortcut.IconLocation = $IconLocation
    $shortcut.Save()
}

# Caminhos para atalhos
$desktop = [System.Environment]::GetFolderPath('Desktop')
$startMenu = [System.Environment]::GetFolderPath('StartMenu')

# Criar perfis
Create-FirefoxProfile -ProfileName "Estudos"
Create-FirefoxProfile -ProfileName "Trabalho"

# Criar atalhos
$firefoxPath = Find-FirefoxInstallation
if ($firefoxPath) {
    Create-Shortcut -Name "Firefox Student" -TargetPath $firefoxPath -Arguments '-P "Estudos"' -IconLocation $firefoxPath -ShortcutLocation $desktop
    Create-Shortcut -Name "Firefox Work" -TargetPath $firefoxPath -Arguments '-P "Trabalho"' -IconLocation $firefoxPath -ShortcutLocation $desktop
    Create-Shortcut -Name "Firefox Student" -TargetPath $firefoxPath -Arguments '-P "Estudos"' -IconLocation $firefoxPath -ShortcutLocation $startMenu
    Create-Shortcut -Name "Firefox Work" -TargetPath $firefoxPath -Arguments '-P "Trabalho"' -IconLocation $firefoxPath -ShortcutLocation $startMenu

    Write-Host "Perfis e atalhos criados com sucesso."
} else {
    Write-Host "Não foi possível criar atalhos porque o Firefox não foi encontrado."
}
