# Perfil do Aluno

- Nome: Vitor (vitorpielec)
- Idade: 19 anos
- Cidade: Porto Alegre - RS
- Mora com: Mãe e irmão de 3 anos
- Experiência: Vendedor na Stanley (Shopping Iguatemi) — diferencial em atendimento
- Estilo de aprendizado: Aprende fazendo, odeia teoria. Precisa de contexto e problema real.
- Objetivo de vida: Liberdade geográfica e financeira — viajar Brasil, festas, shape, conhecer gente
- Estilo: Empreendedor de automações, não CLT tradicional
- Metas paralelas: shape na academia, jiu-jitsu, confiança, cortisol baixo
- Família: aliviar carga da mãe, levar irmão Dudu (3 anos) pra aventuras
- Prova real: loja da mãe vendeu R$ 20 mil em UM dia (quinta) — negócio valida a necessidade de automação
- Modelo de negócio desejado: SaaS + freela em dólar + investimentos, sem faculdade formal
- Futuro: contratar 2 pessoas (redes + produção de automações)

# Projeto Real da Mãe

- Loja: Sousou Perfumes (Nuvemshop)
- Problemas:
  - Confirma pagamento manualmente no celular
  - Imprime etiquetas uma por uma (MelhorEnvio, Loggi, Correios, Jadlog)
  - Duas etiquetas por caixa (frente + declaração de conteúdo)
  - Não tem disparo de email (carrinho abandonado, confirmação)
  - Processo 100% manual e repetitivo

# Stack de Aprendizado (ordem de prioridade)

1. n8n
2. PostgreSQL
3. Python
4. APIs (HTTP, JSON, REST, webhooks)
5. Git
6. Docker

# Projetos

## Projeto 1: Estoque Alerta (em andamento)

Sandbox para aprender as 7 tecnologias. Sistema de monitoramento de estoque com alertas automáticos.

### Git — Completo
- `git init`, `add`, `commit -m`, `status`, `branch -m main`
- README.md criado e commitado
- Repositório no GitHub: vitorpielec/estoque-alerta
- `git push` via `gh repo create` (HTTPS), depois trocou pra SSH
- Chave SSH gerada e adicionada no GitHub pra autenticar
- `git remote remove origin` + `git remote add origin git@github.com:vitorpielec/estoque-alerta.git`
- Usa lazygit como atalho visual (já sabe os comandos base)
- 3 commits no total (README inicial, AGENTS.md, regras de ensino)

### Docker — Parcial
- Sabe rodar container Docker manualmente (`docker run --name ... -d postgres:16-alpine`)
- Container **postgres-sousou** rodando (PostgreSQL 16 Alpine, banco `sousou_perfumes`, user `sousou_user`)
- Porta 5432 mapeada pro host
- Entende diferença de container vs imagem
- Imagem n8n baixada mas container nunca iniciado
- Não usa docker-compose ainda

### PostgreSQL — Instalado mas não usado ainda
- `psql` client instalado (versão 16.13)
- AINDA NÃO conectou no banco
- NENHUMA tabela criada ainda
- Próximo passo: `\l`, `\c`, CREATE TABLE, INSERT, SELECT

### Python — Não iniciado
- Python 3.14.5 instalado no sistema
- Nenhum script criado
- Nenhuma lib instalada (nem venz criado)

### n8n — Não iniciado
- Imagem Docker `docker.n8n.io/n8nio/n8n:latest` baixada
- Container nunca foi rodado

### APIs — Não iniciado

# Problemas de Infra Conhecidos

- **api.github.com bloqueado pela rede** (timeout) — `github.com` funciona normalmente. Solução: usar SSH em vez de HTTPS para Git.
- **Sem placa de vídeo dedicada** (ThinkPad T480) — Ollama não roda bem

# Sessões

## Sessão 1 — Git (11/06/2026)
- Instalou/configurou Git no Fedora
- Aprendeu: `init`, `add`, `commit -m`, `status`, `branch -m`, `push`
- Criou repositório local e remoto (GitHub)
- Entendeu: staging area, commits, `--` vs `-`, `origin`
- Criou primeiro README.md com Nano

## Sessão 2 — Git SSH + Infra (12/06/2026)
- Aprendeu o que é SSH e pra que serve
- Gerou chave com `ssh-keygen -t ed25519`
- Adicionou chave pública no GitHub via navegador
- Trocou remote de HTTPS pra SSH
- Fez `git push` funcionar com SSH
- Removeu containers antigos (`postgres_local`, `n8n_local`) e recriou `postgres-sousou` manualmente
- Instalou `psql` (postgresql16) no Fedora
- Adicionou regras de ensino no AGENTS.md
- Atualizou AGENTS.md pro estado atual de aprendizado

# Regras para o Professor (IA)

- **Explicar CADA comando antes de mandar executar** — Vitor está aprendendo, não adianta mandar código sem explicar. Pra cada comando: o que faz, cada parte (flags, argumentos), o que vai acontecer depois de rodar.
- **Nunca pular etapas** — ir passo a passo, confirmar antes de avançar
- **Contexto real sempre** — mostrar como cada coisa se conecta com o problema da loja da mãe
- **Preferir comandos que mostram resultado visual** (ex: SELECT no psql, listar tabelas) em vez de comandos silenciosos

# Notas Importantes

- Vitor pode usar tanto terminal puro quanto lazygit
- Não tem placa de vídeo dedicada (ThinkPad T480) — Ollama não roda bem
- Prefere soluções que não dependam de assinatura paga
- Tópico existencial: sente que mercado de tech/IA tem muito oportunista, quer ser resolvedor de problemas, não "influencer de tech"
- O e-commerce completo de perfumes com Next.js iniciado em /tmp/opencode/perfumes/ é um projeto extra que pode ser explorado depois (NÃO é o foco atual)
