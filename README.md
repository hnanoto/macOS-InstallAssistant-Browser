# macOS-InstallAssistant-Browser

Navigate, filter and download InstallAssistant (PKG/DMG) directly from Apple's official catalogs.  
Navegue, filtre e baixe InstallAssistant (PKG/DMG) direto dos catálogos oficiais da Apple.  
Foco em praticidade para encontrar a versão/build certa com rapidez.

**Summary / Resumo**  
Requires macOS 13 or later. Supports browsing InstallAssistant packages for macOS versions available in Apple's catalogs (High Sierra and newer).  
Requer macOS 13 ou superior. Suporta pacotes InstallAssistant das versões do macOS disponíveis nos catálogos da Apple (High Sierra em diante).

## ⚡ Quick Start / Início rápido

### English
1. Download the latest release from the **Releases** tab.
2. Launch `macOS-InstallAssistant-Browser.app`.
3. Use filters to find an installer and copy the URL or download.

### Português
1. Baixe a versão mais recente na aba **Releases**.
2. Abra `macOS-InstallAssistant-Browser.app`.
3. Use os filtros para localizar um instalador e copie a URL ou baixe.

✨ O que o app faz
Consolida itens “InstallAssistant” de múltiplos catálogos da Apple.
Filtros por Canal (Release, Beta, Developer/Seed) e Tipo (PKG/DMG).
Exibe Título, Versão, Build, Data, Catálogo, URL e Tamanho (quando disponível).
Copiar URL ou Baixar o pacote diretamente.
📥 Download
Vá na aba Releases deste repositório e baixe o arquivo mais recente:
macOS-InstallAssistant-Browser.zip (ou .dmg quando disponível)
🧩 Installation / Instalação

#### English
1. Extract the `.zip` if needed and drag `macOS-InstallAssistant-Browser.app` to `/Applications`.
2. Open the app.
3. If macOS blocks the app (Gatekeeper):
   - Right‑click and choose **Open** (twice on first run), or
   - System Settings ▸ Privacy & Security ▸ **Open Anyway**.
4. If quarantine still prevents launching, run:
   ```
   sudo xattr -dr com.apple.quarantine "/Applications/macOS-InstallAssistant-Browser.app"
   ```
   Optional: ensure execute permission:
   ```
   chmod -R a+x "/Applications/macOS-InstallAssistant-Browser.app"
   ```

#### Português
1. Extraia o `.zip` (se necessário) e arraste `macOS-InstallAssistant-Browser.app` para `/Applications`.
2. Abra o app.
3. Se o macOS bloquear a abertura (Gatekeeper):
   - Clique com o botão direito e escolha **Abrir** (duas vezes na primeira execução) ou
   - Configurações do Sistema ▸ Privacidade e Segurança ▸ **Abrir assim mesmo**.
4. Se ainda assim não abrir (quarentena do download), execute:
   ```
   sudo xattr -dr com.apple.quarantine "/Applications/macOS-InstallAssistant-Browser.app"
   ```
   Opcional: garantir permissão de execução:
   ```
   chmod -R a+x "/Applications/macOS-InstallAssistant-Browser.app"
   ```

Tip / Dica: para conferir a integridade do arquivo baixado, compare o SHA-256 publicado na Release:
```
shasum -a 256 ~/Downloads/macOS-InstallAssistant-Browser.zip
```
▶️ Como usar
Abra o app e aguarde o carregamento dos catálogos.
Use os filtros (Canal/Tipo) para refinar a lista.
Selecione um item para Copiar URL (área de transferência) ou Baixar (do servidor da Apple).
🧭 Fluxograma (como funciona)
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
❓FAQ
Por que aparece Tamanho “N/A”?
Alguns catálogos não informam SizeBytes. O download continua funcional.
URL retornou 403/404.
O item pode ter sido removido/alterado pela Apple. Atualize a lista e tente novamente.
🔒 Privacidade
Não coleta nem envia dados pessoais.
As URLs de download apontam para domínios oficiais da Apple.
⚖️ Aviso
O app apenas navega e baixa arquivos hospedados pela Apple.
Respeite os Termos de Licença da Apple e a legislação aplicável.
Uso destinado a testes, suporte e fins educacionais.
💬 Suporte
Dúvidas, sugestões e feedback: abra uma Issue aqui no repositório.
Comunidade: Hackintosh and Beyond (YouTube/Discord).
