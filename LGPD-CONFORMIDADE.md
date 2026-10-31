# SmartComanda – LGPD, versão simples

> Guia técnico, não é parecer jurídico. Peça a um advogado ou consultor de proteção de dados que revise o aviso e os prazos.

## O que o sistema faz
- **Aviso de privacidade e aceite** no app do cliente (primeira visita). Chat, encomenda e avaliação só funcionam após o aceite. O aceite guarda versão e data, sem nome nem telefone (`consentimentos` no Firebase).
- **Link "Política de Privacidade" e "Meus direitos"** no rodapé do app. Os direitos do titular são atendidos por **contato direto** (WhatsApp ou e-mail da empresa, cadastrados na aba Desenvolvedor), em até 15 dias.
- **Botão "Apagar dados deste aparelho"** no app do cliente.
- **QR Code gerado no navegador**: o link da comanda não vai mais para site de terceiros.
- **Segurança**: login da equipe, regras do banco por perfil, cliente só acessa a própria comanda.

## Como atender um pedido de titular (sem aba LGPD)
1. Confirme a identidade da pessoa (nome e WhatsApp da comanda).
2. **Acesso/cópia**: consulte o CRM e o Histórico (por mesa ou por cliente) e envie as informações.
3. **Correção**: edite o cliente no CRM.
4. **Exclusão**: remova o cliente no CRM e peça ao responsável técnico para apagar, no Firebase, os registros dessa pessoa em `encomendas`, `feedbacks`, `historico` e `chats_arquivo`.
5. Anote a data do pedido e da resposta (planilha ou caderno).

## Retenção manual
- Defina o prazo com o contador (aba Desenvolvedor > Retenção de dados pessoais).
- A cada trimestre, apague ou anonimize no Firebase os dados pessoais mais antigos que o prazo.

## Incidentes (vazamento, acesso indevido, perda de dados)
Anote data, o que aconteceu, dados afetados e medidas tomadas, e consulte logo o jurídico sobre a comunicação à ANPD e aos titulares (prazo regulamentar curto).

## Registro simplificado das operações
| Dado | Finalidade | Base legal (validar com o jurídico) | Onde fica |
|---|---|---|---|
| Nome, WhatsApp, e-mail | Atender a comanda e encomendas | Execução de contrato | PC e Firebase |
| Aniversário (opcional) | Cumprimentar o cliente | Consentimento | PC |
| Itens, valores, tempo | Cobrança e controle financeiro | Contrato / obrigação legal | PC e Firebase |
| Chat | Atender chamados | Execução de contrato | Firebase |
| Avaliações e comentários | Melhorar o atendimento | Consentimento | Firebase |
| Identificador anônimo | Segurança do acesso | Legítimo interesse | Firebase |

## O que depende da empresa
1. Preencher encarregado/canal do titular e retenção na aba Desenvolvedor.
2. Revisão jurídica do aviso e das bases legais.
3. O banco está em `us-central` (transferência internacional). Prefira `southamerica-east1` e aceite os termos de processamento de dados do Google.
4. Apagar os clientes fictícios de exemplo antes de usar em produção.
5. Treinar a equipe, usar senhas individuais e desativar acessos de quem saiu.
6. Guardar os backups em local seguro.
