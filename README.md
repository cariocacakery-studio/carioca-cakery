# Carioca Cakery — pacote de produção

Stack: React + Vite + Supabase + Vercel.

Já incluído: home, cardápio, galeria, formulário de encomenda, validação de 7 dias, WhatsApp, cadastro/login, área do cliente, pedidos/status, painel da dona, agenda/pedidos, clientes, editor do site, criação/ocultação de categorias, upload de fotos, banco Postgres e políticas RLS.

## Regras comerciais incorporadas
- 7 dias de antecedência para novos pedidos.
- Mudança de sabor até 3 dias antes, mediante disponibilidade.
- Alteração de data somente mediante consulta prévia.
- Sem devolução; cancelamento vira crédito por 30 dias.
- Uso do crédito com novo pedido de pelo menos 5 dias de antecedência.
- Quitação até 3 dias antes da retirada/entrega.
- 50% na reserva + 50% até 3 dias antes.
- Pix ou cartão (+6%).
- Entrega: disponibilidade e valor pelo WhatsApp.

## Para publicar
1. Crie um projeto Supabase.
2. Rode `supabase/schema.sql` no SQL Editor.
3. Crie a conta da dona com Cariocacakery@gmail.com.
4. Pegue o UUID da conta e rode: `update public.profiles set role='admin' where id='UUID_DA_DONA';`
5. Crie um projeto Vercel e importe esta pasta/repositório.
6. Configure `VITE_SUPABASE_URL` e `VITE_SUPABASE_PUBLISHABLE_KEY`.
7. Faça o deploy e depois conecte o domínio na Vercel.

Nunca coloque a service role key do Supabase no frontend.
