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

### PostgreSQL — Em andamento
- `psql` client instalado (versão 16.13)
- Conectou no banco `sousou_perfumes` via `docker exec -it postgres-sousou psql -U sousou_user -d sousou_perfumes`
- **Tabelas criadas:** `categorias`, `produtos`
- **Faltam criar:** `clientes`, `pedidos`, `itens_pedido`
- Depois: INSERT + SELECT + JOIN

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

# Stack de Hardware

- **Atual:** ThinkPad T480 — roda Docker, PostgreSQL (container), VS Code, navegador. Aguenta o aprendizado.
- **Futuro (2+ anos):** MacBook Air M2 16GB — laptop definitivo pro trabalho de automação. Silencioso, bateria infinita, potente.
- **Não comprar:** MacBook Neo (8GB RAM única, chip A18 Pro de celular, sem Thunderbolt — fraco pra Docker + dev).

# Sessões

## Sessão 1 — Git (11/06/2026)
- Instalou/configurou Git no Fedora
- Aprendeu: `init`, `add`, `commit -m`, `status`, `branch -m`, `push`
- Criou repositório local e remoto (GitHub)
- Entendeu: staging area, commits, `--` vs `-`, `origin`
- Criou primeiro README.md com Nano

## Sessão 2 — Git SSH + PostgreSQL + Filosofia (12/06/2026)
- Aprendeu o que é SSH e pra que serve
- Gerou chave com `ssh-keygen -t ed25519`
- Adicionou chave pública no GitHub via navegador
- Trocou remote de HTTPS pra SSH
- Fez `git push` funcionar com SSH
- Removeu containers antigos (`postgres_local`, `n8n_local`) e recriou `postgres-sousou` manualmente
- Instalou `psql` (postgresql16) no Fedora
- Conectou no banco `sousou_perfumes` via `psql`
- Criou tabelas: `categorias` (id, nome) e `produtos` (id, nome, preco, estoque, categoria_id)
- Entendeu: PRIMARY KEY, SERIAL, VARCHAR, DECIMAL, NOT NULL, DEFAULT, REFERENCES (foreign key), diferença NULL vs zero
- Entendeu lógica de relacionamento entre tabelas (categorias → produtos)
- Discutiu visão de vida: liberdade geográfica, shape, empreendedorismo em automação, trabalho remoto em dólar
- Atualizou AGENTS.md com regras de ensino, filosofia de vida, stack de hardware, e estado atual

# Filosofia de Vida

- **Ferramenta de trabalho:** cabe num retângulo com botões dentro de uma mochila. Trabalhar de qualquer lugar — café na frente da praia, hostel, casa da mãe.
- **Único luxo:** MacBook Air M2. Não quer carro caro (Polo 2010 sedan — espaçoso, seguro, confortável, não chama atenção), não quer status material.
- **Grana é pra saúde e experiência:** prefere gastar 100k em alimentação de qualidade do que em um carro de luxo.
- **Alimentação:** banana, kiwi, peixes (salmão), carne vermelha, ovos, mel cru, sucos naturais (laranja, uva), ostras, aveia, churrasco pra família.
- **Shape + mente:** academia, jiu-jitsu, confiança, cortisol baixo. Aprender idiomas (francês, árabe, japonês) por prazer, matemática por diversão, filosofia, livros gerais.
- **Vida social:** ser o gostosão do grupo, flerte gostoso, aproveitar os 20 anos, festas, viajar Brasil, conhecer pessoas pelo caminho.
- **Família:** aliviar carga da mãe, levar irmão Dudu (3 anos) pra aventuras. Loja da mãe (Sousou Perfumes) faturando 50k+/mês.
- **Modelo de negócio:** automatizar o próprio negócio primeiro → SaaS + freela em dólar → contratar 2 pessoas (redes + produção de automações). Meta de ~R$ 20k+/mês com clientes gringos.
- **Propósito:** ajudar pessoas e montar o próprio negócio. Não quer ser "funcionário de TI" — quer ser resolvedor de problemas com liberdade.

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
