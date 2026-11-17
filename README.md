# Connecto · Conector Firebird

Instaladores do conector que liga o banco Firebird da loja à Connecto. O pacote traz o Node 22 embutido; o servidor não precisa de Node, git nem npm.

> Os arquivos ficam na **[Release mais recente](https://github.com/tryconnecto/conector-firebird/releases/latest)**, não na lista de código. Os comandos abaixo baixam de lá automaticamente.

| Sistema | Download direto |
| --- | --- |
| Windows Server 2012 R2+ (x64) | [firebird-graphql-agent-win-x64.zip](https://github.com/tryconnecto/conector-firebird/releases/latest/download/firebird-graphql-agent-win-x64.zip) |
| Linux x64 | [firebird-graphql-agent-linux-x64.tar.gz](https://github.com/tryconnecto/conector-firebird/releases/latest/download/firebird-graphql-agent-linux-x64.tar.gz) |
| Linux arm64 | [firebird-graphql-agent-linux-arm64.tar.gz](https://github.com/tryconnecto/conector-firebird/releases/latest/download/firebird-graphql-agent-linux-arm64.tar.gz) |

## Instalar ou atualizar

**Windows Server 2012 R2 ou superior** — abra o PowerShell **como administrador** e cole:

```powershell
[Net.ServicePointManager]::SecurityProtocol='Tls12'; iex ((New-Object Net.WebClient).DownloadString('https://github.com/tryconnecto/conector-firebird/releases/latest/download/install-windows.ps1'))
```

**Linux com systemd** (x64 ou arm64):

```bash
curl -fsSL https://github.com/tryconnecto/conector-firebird/releases/latest/download/install-linux.sh | sudo sh
```

O instalador baixa a última versão, confere o SHA-256 e pergunta os dados do banco Firebird, o endereço público e a senha do usuário `admin`. No fim mostra o endereço do painel e o Client ID/Secret para cadastrar na Connecto.

Rodar o mesmo comando de novo atualiza para a versão mais nova e mantém configuração, credenciais e autorizações.

## Depois de instalado

```
fga help
```

No Windows, use um Prompt de Comando como administrador; no Linux, `sudo fga …`.

Downloads manuais de cada versão: [Releases](https://github.com/tryconnecto/conector-firebird/releases).
