# 🚀 PASSO A PASSO COMPLETO - Deploy iMavyAgent

## PARTE 1: FAZER DEPLOY NO VERCEL (15 minutos)

### Passo 1: Criar conta no Vercel
1. Acesse: https://vercel.com
2. Clique em **Sign Up** (Cadastrar)
3. Escolha **Continue with GitHub**
4. Faça login com sua conta do GitHub
5. Autorize o Vercel a acessar seus repositórios

### Passo 2: Importar o projeto
1. Na tela inicial do Vercel, clique em **Add New...** > **Project**
2. Procure por: `imavyAgent`
3. Clique em **Import** ao lado do repositório
4. Deixe tudo como está (não precisa mudar nada)
5. Clique em **Deploy**
6. Aguarde 1-2 minutos (vai aparecer fogos de artifício quando terminar)

### Passo 3: Copiar o link temporário
1. Após o deploy, você verá algo como: `imavyagent.vercel.app`
2. Clique no link para testar seu site
3. **PRONTO! Seu site já está no ar!**

---

## PARTE 2: CONECTAR SEU DOMÍNIO (20 minutos)

### Passo 4: Adicionar domínio no Vercel
1. No painel do Vercel, clique no seu projeto `imavyAgent`
2. Clique na aba **Settings** (Configurações)
3. No menu lateral, clique em **Domains** (Domínios)
4. Digite: `imavyagent.com.br`
5. Clique em **Add**
6. O Vercel vai mostrar uma mensagem de erro (é normal!)
7. **DEIXE ESSA PÁGINA ABERTA** - você vai precisar dela

### Passo 5: Configurar DNS no Registro.br (ou onde comprou)

#### Se comprou no REGISTRO.BR:
1. Acesse: https://registro.br
2. Faça login com seu CPF e senha
3. Clique em **Meus Domínios**
4. Clique em `imavyagent.com.br`
5. Clique em **Editar Zona DNS** ou **DNS**
6. Clique em **Adicionar Novo Registro**

**Adicione o PRIMEIRO registro:**
- Tipo: `A`
- Nome: `@` (ou deixe em branco)
- Dados/Valor: `76.76.21.21`
- TTL: `3600` (ou deixe padrão)
- Clique em **Salvar** ou **Adicionar**

**Adicione o SEGUNDO registro:**
- Tipo: `CNAME`
- Nome: `www`
- Dados/Valor: `cname.vercel-dns.com`
- TTL: `3600` (ou deixe padrão)
- Clique em **Salvar** ou **Adicionar**

#### Se comprou em OUTRO LUGAR (GoDaddy, Hostinger, Locaweb):
1. Faça login no painel do seu provedor
2. Procure por: **DNS**, **Gerenciar DNS** ou **Zona DNS**
3. Adicione os mesmos registros acima (A e CNAME)

### Passo 6: Verificar no Vercel
1. Volte para a página do Vercel que você deixou aberta
2. Clique em **Refresh** ou **Verify** (pode demorar alguns minutos)
3. Quando aparecer um ✓ verde, está pronto!

### Passo 7: Adicionar www também (opcional mas recomendado)
1. Ainda na página de Domains do Vercel
2. Clique em **Add** novamente
3. Digite: `www.imavyagent.com.br`
4. Clique em **Add**
5. Pronto! Agora funciona com e sem www

---

## PARTE 3: TESTAR SE FUNCIONOU

### Aguarde a propagação (15-30 minutos)
- Pode levar até 48h, mas geralmente funciona em 15-30 minutos

### Teste seu site:
1. Abra o navegador em modo anônimo (Ctrl + Shift + N)
2. Acesse: https://imavyagent.com.br
3. Acesse: https://www.imavyagent.com.br

### Verificar propagação DNS:
- Acesse: https://dnschecker.org
- Digite: `imavyagent.com.br`
- Clique em **Search**
- Quando aparecer verde em vários países, está funcionando!

---

## ✅ CHECKLIST FINAL

- [ ] Conta criada no Vercel
- [ ] Projeto importado do GitHub
- [ ] Deploy realizado com sucesso
- [ ] Domínio adicionado no Vercel
- [ ] Registro A configurado (76.76.21.21)
- [ ] Registro CNAME configurado (cname.vercel-dns.com)
- [ ] Site acessível em https://imavyagent.com.br
- [ ] SSL (cadeado verde) funcionando

---

## 🆘 PROBLEMAS COMUNS

**"Não consigo fazer login no Vercel"**
- Use a opção "Continue with GitHub"
- Certifique-se que está logado no GitHub

**"Não encontro meu repositório no Vercel"**
- Clique em "Adjust GitHub App Permissions"
- Autorize o acesso ao repositório imavyAgent

**"Domínio não funciona após 1 hora"**
- Verifique se os registros DNS estão corretos
- Aguarde até 48h para propagação completa
- Use https://dnschecker.org para verificar

**"Aparece 'Not Found' ou erro 404"**
- Certifique-se que o arquivo index.html está na raiz do projeto
- Faça um novo deploy no Vercel

**"SSL não funciona (sem cadeado)"**
- Aguarde alguns minutos após adicionar o domínio
- O Vercel gera o certificado SSL automaticamente

---

## 📞 PRECISA DE AJUDA?

Me avise em qual passo você está travado que eu te ajudo!
