# Pendências — Funil Pele de Pêssego (Portugal)

## Falta fazer

- [ ] **Configurar o pós-compra do checkout principal** (KorexPay) para mandar a cliente para
      `https://botox-silk.vercel.app/upsell/`.
- [ ] **Criar o checkout do upsell (14,90 €)** e colocar o link em `upsell/index.html`
      (variável `CHECKOUT_UPSELL`). Enquanto estiver vazia, o botão "Sim" mostra um aviso.
      Se o gateway tiver upsell de 1 clique, usar o script dele no lugar do link.
- [ ] **Configurar o pós-compra do upsell** para mandar para `https://botox-silk.vercel.app/obrigado/`.
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
- Checkout principal trocado para `https://korexpay.lovable.app/pay?product=botox`.
- Imagens convertidas para WebP (largura máx. 1080 px): 47,6 MB → 4,1 MB. Originais em
  `funil-portugal/Pele-de-Pessego-imagens-originais` (fora do repositório).
