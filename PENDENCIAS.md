# Pendências — Funil Pele de Pêssego (Portugal)

## Falta fazer

- [ ] **Trocar o checkout principal (9,90 €).** O botão ainda vai para a Cakto brasileira
      (`https://pay.cakto.com.br/3fohws3_1108935`), que cobra em reais. Criar um checkout em euro
      e trocar o link em `assets/funnel-v2-DnV_0Dgs.js` (variável `Xn=`).
- [ ] **Configurar o pós-compra do checkout principal** para mandar a cliente para `/upsell/`.
- [ ] **Criar o checkout do upsell (14,90 €)** e colocar o link em `upsell/index.html`
      (variável `CHECKOUT_UPSELL`). Enquanto estiver vazia, o botão "Sim" mostra um aviso.
      Se o gateway tiver upsell de 1 clique, usar o script dele no lugar do link.
- [ ] **Configurar o pós-compra do upsell** para mandar para `/obrigado/`.
- [ ] **Conferir a página `/obrigado/`**: ela diz que o acesso chega por e-mail e é pela app
      Pele de Pêssego. Ajustar se a entrega for diferente.
- [ ] **Ligar a UTMify ao gateway** (webhook de vendas) para as vendas aparecerem com origem.
- [ ] **Evento de compra (Purchase) no pixel**: vem do gateway/UTMify. Conferir se está a chegar
      no Gerenciador de Eventos com valor em EUR.

## Já feito (23/10/2026)

- Preços em euro: 9,90 € (antes R$37), 0,47 €/dia, bónus e valores de referência convertidos.
- Script da UTMify em todas as páginas.
- Pixel `1110951577989683` em todas as páginas (substituiu o `4829206560640375` que vinha no funil).
- Botão de compra: dispara `InitiateCheckout` (9,90 EUR) e repassa as UTMs da URL para o checkout.
- Upsell `/upsell/`: Ritual Pescoço de Cisne™ por 14,90 € (de 39 €), com saída para `/obrigado/`.
- Página `/obrigado/`.
