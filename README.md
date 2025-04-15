# 📲 Disparo e Validação de QR Code via WhatsApp

Automação completa usando **n8n**, **Evolution API**, **Google Sheets** e **Supabase** para envio de convites com QR Code via WhatsApp e validação de presença em eventos.

---

## 🚀 Visão Geral

Este projeto automatiza o processo de envio de mensagens personalizadas com QR Code em PDF para convidados, permitindo a confirmação de presença por meio de uma página web dedicada.

- ✅ Envio automático via WhatsApp
- 🧾 PDF personalizado com QR Code
- 🌐 Página de confirmação de presença
- 📊 Controle de status via planilha

---

## 🛠️ Tecnologias

- [n8n](https://n8n.io/) – Orquestração da automação
- [Google Sheets](https://www.google.com/sheets/about/) – Base de contatos
- [Evolution API](https://evolutionapi.com.br/) – Envio de mensagens/documentos via WhatsApp
- [PDFShift](https://pdfshift.io/) – Conversão HTML para PDF
- [Supabase](https://supabase.com/) – Backend para validação dos QR Codes
- [qrserver.com](https://goqr.me/api/) – Geração de QR Code

---

## 💡 Como Funciona

1. **Disparo de mensagens**  
   - A planilha é lida pelo n8n.
   - A cada 10 segundos, é enviada uma mensagem com texto personalizado via Evolution API.
   - O status da mensagem é atualizado na planilha.

2. **Geração e envio de QR Code**  
   - Quando o usuário responde “SIM”, um webhook é acionado.
   - Um QR Code é gerado com um código único.
   - Um convite em PDF é gerado e enviado por WhatsApp.

3. **Validação da presença**  
   - Ao escanear o QR Code, o usuário acessa a página:  
     [Página de Confirmação](https://evilasioferreira.github.io/qr-code/)
   - A presença é confirmada e registrada na base.

---

## 📎 Arquivos

- `disparo_qrCode.json` – Workflow n8n exportado
- `planilha_base.txt` – Estrutura da base de contatos
- `fluxo.png` – Fluxo visual da automação
- `README.md` – Este documento

---

## ✨ Demonstração

**Link da Página de Confirmação:**  
[https://evilasioferreira.github.io/qr-code/](https://evilasioferreira.github.io/qr-code/)

---

## 📬 Contato

Criado por [@evilasioferreira](https://github.com/evilasioferreira) – sinta-se à vontade para abrir uma issue ou contribuir!
