# Dado Blindado

Prepare a revisão de texto, Word e PDF antes de compartilhar.

O plugin monta um roteiro de revisão por formato (texto, Word ou PDF) e por foco (contatos, nomes e endereços, contexto identificável) e informa os limites do Dado Blindado. Na página pública, sem cadastro, você pode marcar trechos com o pincel, conferir possíveis identificadores e exportar uma cópia revisada.

**Importante:** o original é escolhido e processado no navegador. O servidor MCP não recebe documentos nem anonimiza conteúdo pelo chat. Não faz OCR nem altera o PDF original; exporta TXT ou Word revisado. A revisão humana é necessária e não há garantia de anonimização irreversível.

## Como funciona

O plugin conecta o Claude ao servidor MCP remoto do Dado Blindado (sem autenticação), que expõe duas ferramentas somente-leitura:

- `preparar_revisao_local` — monta o roteiro de revisão conforme formato e foco e fornece o endereço do editor público.
- `consultar_formatos_e_limites` — informa formatos aceitos, limites e funcionamento do processamento local.

Editor público: https://dadoblindado.jhonata-emerick.workers.dev

## Instalação

A partir deste repositório (marketplace próprio):

```
claude plugin marketplace add comeca-ai/dado-blindado
claude plugin install dado-blindado@jhoneme-plugins
```

Ou, para uma sessão única:

```
claude --plugin-dir ./dado-blindado
```

No claude.ai/Cowork, o servidor também pode ser adicionado diretamente como conector personalizado usando a URL:
`https://anonimizador-plugin.jhonata-emerick.workers.dev/dado-blindado/mcp`

## Privacy Policy

Política de privacidade: https://anonimizador-plugin.jhonata-emerick.workers.dev/privacidade

- **Coleta de dados:** o servidor MCP não recebe documentos, texto original, identificadores, nomes de arquivo ou links de documentos. As ferramentas recebem apenas o formato escolhido e categorias gerais de foco.
- **Uso e armazenamento:** o processamento do documento ocorre localmente no navegador do usuário, na página pública do editor.
- **Compartilhamento com terceiros:** nenhum conteúdo de documento é enviado ou compartilhado com terceiros pelo MCP.
- **Retenção:** o MCP não armazena conteúdo de documentos.
- **Contato:** https://anonimizador-plugin.jhonata-emerick.workers.dev/suporte

## Suporte e termos

- Suporte: https://anonimizador-plugin.jhonata-emerick.workers.dev/suporte
- Termos de serviço: https://anonimizador-plugin.jhonata-emerick.workers.dev/termos
