```markdown
# Firefox Profile Creator

Este script PowerShell foi desenvolvido para criar dois perfis personalizados do Firefox (Estudos e Trabalho) e adicionar atalhos para esses perfis tanto na área de trabalho quanto no menu Iniciar do Windows 10 e 11.

## Funcionalidades

- **Criação de Perfis Personalizados:** Cria dois perfis separados no Firefox: "Estudos" e "Trabalho".
- **Criação de Atalhos:** Adiciona atalhos para os perfis na área de trabalho e no menu Iniciar.
- **Detecção Automática do Firefox:** O script detecta automaticamente a instalação do Firefox no sistema operacional.
- **Compatibilidade:** Compatível com Windows 10 e Windows 11.

## Como Usar

1. **Download do Script:** Faça o download do script `FirefoxProfile.ps1`.
2. **Executar o Script:** Execute o script no PowerShell com privilégios administrativos para garantir que ele tenha permissão para criar atalhos no menu Iniciar.

```powershell
powershell.exe -ExecutionPolicy Bypass -File .\FirefoxProfile.ps1
```

## Pré-requisitos

- **PowerShell:** Certifique-se de ter o PowerShell instalado e atualizado.
- **Firefox:** O Firefox deve estar instalado no sistema. O script tenta localizar a instalação do Firefox nos caminhos de instalação padrão.

## Detalhes Técnicos

### Funções do Script

- **Find-FirefoxInstallation:** Função que tenta localizar a instalação do Firefox no sistema, verificando os caminhos padrão de instalação.
- **Create-FirefoxProfile:** Função que cria um perfil do Firefox com o nome especificado.
- **Create-Shortcut:** Função que cria um atalho para o perfil do Firefox na localização especificada (área de trabalho ou menu Iniciar).

### Estrutura do Script

1. **Detecção do Firefox:** O script verifica se o Firefox está instalado no sistema, tentando localizá-lo nos caminhos padrão de instalação.
2. **Criação de Perfis:** Se o Firefox for encontrado, o script cria dois perfis: "Estudos" e "Trabalho".
3. **Criação de Atalhos:** O script cria atalhos para esses perfis na área de trabalho e no menu Iniciar.

## Vantagens

- **Automação:** Automatiza a criação de perfis e atalhos do Firefox, economizando tempo.
- **Personalização:** Permite a criação de perfis personalizados para diferentes usos (estudos e trabalho).
- **Facilidade de Uso:** Simples de executar, basta rodar o script no PowerShell.
- **Compatibilidade:** Funciona em várias versões do Windows (10 e 11).

## Contribuição

Sinta-se à vontade para contribuir com melhorias para este script. Você pode criar issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**Autor:** Sérgio Sant'Ana Júnior
**Contato:** [seu-email@exemplo.com](mailto:seu-email@exemplo.com)
```

Este README fornece uma visão geral completa do que o script faz, como usá-lo, suas vantagens e detalhes técnicos importantes. Sinta-se à vontade para ajustá-lo conforme necessário e adicionar mais detalhes específicos ao seu projeto.
