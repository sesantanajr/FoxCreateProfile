# Script PowerShell para Perfis e Atalhos do Firefox

## Visão Geral

Este script PowerShell automatiza a criação de dois perfis do Firefox chamados "Estudos" e "Trabalho", e gera atalhos para esses perfis na área de trabalho e no menu Iniciar. O script garante que a instalação do Firefox seja encontrada no sistema e cria os perfis e atalhos somente se o Firefox estiver disponível.

## Funcionalidades

- **Detecção Automática da Instalação do Firefox**: O script procura o executável do Firefox nos caminhos de instalação comuns.
- **Criação de Perfis**: Cria automaticamente os perfis "Estudos" e "Trabalho" no Firefox.
- **Criação de Atalhos**: Gera atalhos para ambos os perfis na área de trabalho e no menu Iniciar com os argumentos apropriados para abrir o Firefox com o perfil especificado.

## Vantagens

- **Eficiência**: Automatiza tarefas repetitivas, economizando tempo e reduzindo a chance de erro humano.
- **Conveniência**: Facilita a troca entre diferentes perfis do Firefox usando atalhos.
- **Personalização**: Personalize os nomes dos perfis e os locais dos atalhos conforme necessário.

## Detalhes do Script

### Função Find-FirefoxInstallation

Esta função tenta localizar a instalação do Firefox no sistema. Primeiro, verifica se o Firefox está disponível no PATH do sistema. Se não encontrado, verifica os diretórios de instalação padrão.

### Função Create-FirefoxProfile

Esta função cria um novo perfil do Firefox usando o executável do Firefox. Ela recebe um nome de perfil como parâmetro.

### Função Create-Shortcut

Esta função cria um atalho com os parâmetros especificados, incluindo nome, caminho de destino, argumentos, localização do ícone e local do atalho.

## Uso

1. **Baixe o Script**: Salve o script no seu computador.
2. **Execute o Script**: Abra o PowerShell com privilégios administrativos e execute o script.
3. **Verifique os Atalhos**: Verifique a área de trabalho e o menu Iniciar para os atalhos recém-criados.

### Exemplo de Execução

```powershell
# Salve o script em um arquivo, por exemplo, CreateFirefoxProfiles.ps1
# Abra o PowerShell como Administrador e execute o script
.\CreateFirefoxProfiles.ps1
```

## Requisitos

- **Sistema Operacional**: Windows 10 ou Windows 11
- **PowerShell**: Versão 5.1 ou superior
- **Firefox**: Instalado no sistema

## Notas

- Se o Firefox não for encontrado no sistema, o script exibirá uma mensagem indicando que o Firefox não está disponível.
- Personalize os nomes dos perfis e os locais dos atalhos no script conforme necessário.

## Contribuindo

Sinta-se à vontade para fazer um fork deste repositório e enviar pull requests para melhorias ou funcionalidades adicionais. 
