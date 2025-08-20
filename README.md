# macOS-InstallAssistant-Browser
macOS-InstallAssistant-Browser
Navegue, filtre e baixe InstallAssistant (PKG/DMG) direto dos catálogos oficiais da Apple.
Foco em praticidade para encontrar a versão/build certa com rapidez.
✨ O que o app faz
Consolida itens “InstallAssistant” de múltiplos catálogos da Apple.
Filtros por Canal (Release, Beta, Developer/Seed) e Tipo (PKG/DMG).
Exibe Título, Versão, Build, Data, Catálogo, URL e Tamanho (quando disponível).
Copiar URL ou Baixar o pacote diretamente.
📥 Download
Vá na aba Releases deste repositório e baixe o arquivo mais recente:
macOS-InstallAssistant-Browser.zip (ou .dmg quando disponível)
Requisitos: macOS 13 ou superior.
🧩 Instalação
Extraia o .zip (se aplicável).
Arraste macOS-InstallAssistant-Browser.app para /Applications.
Abra o app.
Se o macOS bloquear a abertura (Gatekeeper)
Primeiro tente clicar com o botão direito → Abrir (duas vezes na primeira execução)
ou Configurações do Sistema ▸ Privacidade e Segurança ▸ Abrir assim mesmo.
Se ainda assim não abrir (quarentena do download), use o Terminal:
# Remover o atributo de quarentena do app
sudo xattr -dr com.apple.quarantine "/Applications/macOS-InstallAssistant-Browser.app"

# (Opcional) Garantir permissão de execução
chmod -R a+x "/Applications/macOS-InstallAssistant-Browser.app"
Dica: para conferir a integridade do arquivo baixado, compare o SHA-256 publicado na Release:
shasum -a 256 ~/Downloads/macOS-InstallAssistant-Browser.zip
▶️ Como usar
Abra o app e aguarde o carregamento dos catálogos.
Use os filtros (Canal/Tipo) para refinar a lista.
Selecione um item para Copiar URL (área de transferência) ou Baixar (do servidor da Apple).
🧭 Fluxograma (como funciona)

```mermaid
flowchart TD
    A([Iniciar app]) --> B[Carregar catálogos oficiais<br/>swscan.apple.com]
    B --> C[Extrair produtos InstallAssistant]
    C --> D[Normalizar itens e remover duplicados]
    D --> E[Aplicar filtros (Canal/Tipo/Build)]
    E --> F{Ação do usuário}
    F -->|Copiar URL| G[URL copiada p/ área de transferência]
    F -->|Baixar| H[Download direto do servidor Apple]
    F -->|Ver detalhes| I[Mostrar metadados: Versão/Build/Data/Catálogo/Tamanho]
    H --> J[Salvar arquivo no local escolhido]
    classDef start fill:#b3e5fc,stroke:#333,stroke-width:1px;
    classDef decision fill:#ffe0b2,stroke:#333,stroke-width:1px;
    class A start;
    class F decision;
```

*O diagrama mostra o fluxo de funcionamento do app.*  
*The diagram shows how the app works.*

🧭 Flowchart (how it works)

```mermaid
flowchart TD
    A([Launch app]) --> B[Load official catalogs<br/>swscan.apple.com]
    B --> C[Extract InstallAssistant products]
    C --> D[Normalize items and remove duplicates]
    D --> E[Apply filters (Channel/Type/Build)]
    E --> F{User action}
    F -->|Copy URL| G[URL copied to clipboard]
    F -->|Download| H[Direct download from Apple's server]
    F -->|View details| I[Show metadata: Version/Build/Date/Catalog/Size]
    H --> J[Save file to chosen location]
    classDef start fill:#b3e5fc,stroke:#333,stroke-width:1px;
    classDef decision fill:#ffe0b2,stroke:#333,stroke-width:1px;
    class A start;
    class F decision;
```

*O diagrama mostra o fluxo de funcionamento do app.*  
*The diagram shows how the app works.*
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
