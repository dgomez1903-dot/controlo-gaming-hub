# Controlo de obrigações — Gaming Hub

Site estático. Uma pasta por mês, cada uma com o seu `index.html`.

```
/
├── index.html        ← lista de meses (editar o array MESES)
├── README.md
└── 2026-08/
    └── index.html    ← painel de agosto/2026
```

## Publicar (GitHub Pages)

1. Criar conta em github.com.
2. **New repository** → nome `controlo-gaming-hub` → **Public** → **Create**.
3. **uploading an existing file** → arrastar `index.html`, `README.md` e a pasta `2026-08` → **Commit changes**.
4. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, pasta `/ (root)` → **Save**.
5. Esperar 1–2 minutos. O endereço fica `https://<utilizador>.github.io/controlo-gaming-hub/`.

## Acrescentar um mês novo

1. No repositório, entrar em `2026-08`, abrir `index.html`, botão **Raw**, guardar o ficheiro.
2. Editar os valores no ficheiro guardado: as constantes `OBS`, `FORN`, `EMPS`, `NOTES`, a data em `TODAY` e a chave `KEY` (mudar para `gaminghub:092026:v1`, senão o mês novo herda as marcações do anterior).
3. **Add file → Create new file**, escrever `2026-09/index.html` no nome, colar o conteúdo, **Commit**.
4. Abrir o `index.html` da raiz e juntar a linha do mês novo ao array `MESES`.

## Atenção à confidencialidade

Um site em GitHub Pages é **sempre público**, mesmo quando o repositório é privado (e no plano gratuito o repositório tem obrigatoriamente de ser público). Qualquer pessoa com o endereço vê salários e nomes.

Duas saídas:

- **Tirar os dados pessoais**: apagar a secção da folha e deixar só o total. O resto do painel não expõe nada sensível.
- **Pôr autenticação**: publicar em Cloudflare Pages em vez de GitHub Pages e ligar o Cloudflare Access, que exige código enviado por email antes de abrir a página. É gratuito até 50 utilizadores, mas precisa de um domínio próprio gerido na Cloudflare.
