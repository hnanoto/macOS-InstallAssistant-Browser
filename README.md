# macOS-InstallAssistant-Browser

## Português
Navegue, filtre e baixe InstallAssistant (PKG/DMG) direto dos catálogos oficiais da Apple. Foco em praticidade para encontrar a versão/build certa com rapidez.

### ✨ O que o app faz
- Consolida itens "InstallAssistant" de múltiplos catálogos da Apple.
- Filtros por Canal (Release, Beta, Developer/Seed) e Tipo (PKG/DMG).
- Exibe Título, Versão, Build, Data, Catálogo, URL e Tamanho (quando disponível).
- Copiar URL ou Baixar o pacote diretamente.

### 📥 Download
Vá na aba Releases deste repositório e baixe o arquivo mais recente:  
`macOS-InstallAssistant-Browser.zip` (ou `.dmg` quando disponível)  
Requisitos: macOS 13 ou superior.

### 🧩 Instalação
1. Extraia o `.zip` (se aplicável).
2. Arraste `macOS-InstallAssistant-Browser.app` para `/Applications`.
3. Abra o app.

Se o macOS bloquear a abertura (Gatekeeper):
- Primeiro tente clicar com o botão direito → **Abrir** (duas vezes na primeira execução), ou
- **Configurações do Sistema ▸ Privacidade e Segurança ▸ Abrir assim mesmo.**

Se ainda assim não abrir (quarentena do download), use o Terminal:

```bash
# Remover o atributo de quarentena do app
sudo xattr -dr com.apple.quarantine "/Applications/macOS-InstallAssistant-Browser.app"

# (Opcional) Garantir permissão de execução
chmod -R a+x "/Applications/macOS-InstallAssistant-Browser.app"
```

Dica: para conferir a integridade do arquivo baixado, compare o SHA-256 publicado na Release:

```bash
shasum -a 256 ~/Downloads/macOS-InstallAssistant-Browser.zip
```

### ▶️ Como usar
1. Abra o app e aguarde o carregamento dos catálogos.
2. Use os filtros (Canal/Tipo) para refinar a lista.
3. Selecione um item para **Copiar URL** (área de transferência) ou **Baixar** (do servidor da Apple).

### 🧭 Fluxograma (como funciona)
flowchart TD
    A[Iniciar app] --> B[Carregar catálogos oficiais<br/>swscan.apple.com]
    B --> C[Extrair produtos InstallAssistant]
    C --> D[Normalizar itens e remover duplicados]
    D --> E[Aplicar filtros (Canal/Tipo/Build)]
    E --> F{Ação do usuário}
    F -->|Copiar URL| G[URL copiada p/ área de transferência]
    F -->|Baixar| H[Download direto do servidor Apple]
    F -->|Ver detalhes| I[Mostrar metadados: Versão/Build/Data/Catálogo/Tamanho]
    H --> J[Salvar arquivo no local escolhido]


### ❓ FAQ
**Por que aparece Tamanho "N/A"?**  
Alguns catálogos não informam `SizeBytes`. O download continua funcional.

**URL retornou 403/404.**  
O item pode ter sido removido/alterado pela Apple. Atualize a lista e tente novamente.

### 🔒 Privacidade
- Não coleta nem envia dados pessoais.
- As URLs de download apontam para domínios oficiais da Apple.

### ⚖️ Aviso
- O app apenas navega e baixa arquivos hospedados pela Apple.
- Respeite os Termos de Licença da Apple e a legislação aplicável.
- Uso destinado a testes, suporte e fins educacionais.

### 💬 Suporte
- Dúvidas, sugestões e feedback: abra uma Issue aqui no repositório.
- Comunidade: Hackintosh and Beyond (YouTube/Discord).

## English
Browse, filter, and download InstallAssistant (PKG/DMG) directly from Apple's official catalogs. Focused on practicality to quickly find the correct version/build.

### ✨ What the app does
- Consolidates "InstallAssistant" items from multiple Apple catalogs.
- Filters by Channel (Release, Beta, Developer/Seed) and Type (PKG/DMG).
- Displays Title, Version, Build, Date, Catalog, URL, and Size (when available).
- Copy the URL or download the package directly.

### 📥 Download
Go to the **Releases** tab of this repository and grab the latest file:  
`macOS-InstallAssistant-Browser.zip` (or `.dmg` when available)  
Requirements: macOS 13 or later.

### 🧩 Installation
1. Extract the `.zip` (if applicable).
2. Drag `macOS-InstallAssistant-Browser.app` to `/Applications`.
3. Open the app.

If macOS blocks the launch (Gatekeeper):
- First, try right-click → **Open** (twice on first run), or
- **System Settings ▸ Privacy & Security ▸ Open Anyway.**

If it still doesn't open (download quarantine), use Terminal:

```bash
# Remove the quarantine attribute from the app
sudo xattr -dr com.apple.quarantine "/Applications/macOS-InstallAssistant-Browser.app"

# (Optional) Ensure execute permission
chmod -R a+x "/Applications/macOS-InstallAssistant-Browser.app"
```

Tip: verify the integrity of the downloaded file by comparing the SHA-256 published in the Release:

```bash
shasum -a 256 ~/Downloads/macOS-InstallAssistant-Browser.zip
```

### ▶️ Usage
1. Open the app and wait for the catalogs to load.
2. Use the filters (Channel/Type) to refine the list.
3. Select an item to **Copy URL** (to the clipboard) or **Download** (from Apple's server).

### 🧭 Flowchart (how it works)
flowchart TD
  A([Iniciar app]) --> B[Carregar catálogos oficiais\nswscan.apple.com]
  B --> C[Extrair produtos InstallAssistant]
  C --> D[Normalizar itens e remover duplicados]
  D --> E[Aplicar filtros: Canal/Tipo/Build]
  E -->|Copiar URL| G[URL copiada para a área de transferência]
  E -->|Baixar| H[Download direto do servidor Apple]
  E -->|Ver detalhes| I[Mostrar metadados: Versão/Build/Data/Catálogo/Tamanho]
  H --> J[Salvar arquivo no local escolhido]


### ❓ FAQ
**Why does Size show "N/A"?**  
Some catalogs do not provide `SizeBytes`. The download still works.

**The URL returned 403/404.**  
The item may have been removed or changed by Apple. Refresh the list and try again.

### 🔒 Privacy
- Does not collect or send personal data.
- Download URLs point to Apple's official domains.

### ⚖️ Disclaimer
- The app only browses and downloads files hosted by Apple.
- Respect Apple's License Terms and applicable laws.
- Intended for testing, support, and educational purposes.

### 💬 Support
- Questions, suggestions, and feedback: open an Issue here in the repository.
- Community: Hackintosh and Beyond (YouTube/Discord).

