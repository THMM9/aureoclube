# Segurança e backup — Áureo Clube

## Segurança aplicada
- Área administrativa removida da versão pública.
- Endpoint antigo de backend removido.
- Formulário de coleta de nome, telefone e e-mail removido.
- Consultas comerciais direcionadas ao WhatsApp oficial.
- JavaScript servido apenas pelo próprio domínio (`script-src 'self'`).
- Nenhum script de terceiros.
- Política CSP para bloquear frames, plugins e formulários.
- Referrer desativado.
- Resultados compartilhados no fragmento `#` do endereço.
- Preferências, carrinho e favoritos permanecem no navegador.

## Backup automático
O workflow `.github/workflows/backup-diario.yml` é executado diariamente às 06:17 UTC
(aproximadamente 03:17 no horário de Brasília), podendo sofrer pequeno atraso da fila do GitHub Actions.

Cada execução cria:
1. um `git bundle` com o histórico restaurável;
2. um `.tar.gz` com os arquivos do projeto;
3. um artefato mantido por 30 dias no GitHub Actions.

Também pode ser executado manualmente em:
GitHub → Actions → Backup diário do Áureo Clube → Run workflow.
