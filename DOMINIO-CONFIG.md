# Configuração do Domínio imavyagent.com.br no Vercel

## Passo 1: No Vercel (após fazer deploy)

1. Acesse seu projeto no Vercel
2. Vá em **Settings** > **Domains**
3. Digite: `imavyagent.com.br`
4. Clique em **Add**
5. O Vercel mostrará os registros DNS necessários

## Passo 2: No seu provedor de domínio (Registro.br ou onde comprou)

Configure os seguintes registros DNS:

### Opção A - Usando A Record (Recomendado)
```
Tipo: A
Nome: @
Valor: 76.76.21.21
TTL: 3600
```

```
Tipo: CNAME
Nome: www
Valor: cname.vercel-dns.com
TTL: 3600
```

### Opção B - Usando CNAME (Alternativa)
```
Tipo: CNAME
Nome: @
Valor: cname.vercel-dns.com
TTL: 3600
```

```
Tipo: CNAME
Nome: www
Valor: cname.vercel-dns.com
TTL: 3600
```

## Passo 3: Aguarde a propagação

- Propagação DNS leva de 5 minutos a 48 horas
- Geralmente funciona em 15-30 minutos
- Verifique em: https://dnschecker.org

## Passo 4: SSL Automático

O Vercel configurará SSL (HTTPS) automaticamente após a verificação do domínio.

## Verificar se funcionou

Acesse: https://imavyagent.com.br

---

**Onde comprou o domínio?**
- Registro.br: https://registro.br
- GoDaddy: https://godaddy.com
- Hostinger: https://hostinger.com.br
- Locaweb: https://locaweb.com.br
