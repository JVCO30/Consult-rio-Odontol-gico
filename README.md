# Sorrir Odontologia — Landing Page

Landing page de uma página só (single file) para um consultório odontológico **fictício**, criada para fins de demonstração/portfólio.

🔗 **Site publicado:** https://jvco30.github.io/Consult-rio-Odontol-gico/

## Arquivos

```
sorrir-odontologia.html   # página completa (HTML + CSS + JS em um único arquivo)
README.md                 # este arquivo
```

Não há dependências externas de build. O arquivo `sorrir-odontologia.html` pode ser aberto diretamente em qualquer navegador ou hospedado em qualquer serviço de arquivos estáticos (Netlify, Vercel, GitHub Pages, cPanel, etc.).

## O que tem na página

- **Header fixo** com navegação e menu mobile (hambúrguer)
- **Hero** com chamada principal e estatísticas
- **Sobre** — bio da dentista fictícia (Dra. Camila Andrade) com foto
- **Serviços** — 5 especialidades em linhas alternadas
- **Como funciona** — fluxo de atendimento em 4 etapas
- **Depoimento** de paciente
- **Diferenciais** do consultório
- **Contato** — endereço, telefone/WhatsApp, e-mail, horários, mapa ilustrativo e formulário de agendamento
- **Footer** com dados de contato e navegação

## Conteúdo fictício usado

Todos os dados abaixo são inventados e devem ser substituídos por dados reais antes de qualquer uso em produção:

| Campo | Valor no template |
|---|---|
| Clínica | Sorrir Odontologia |
| Dentista | Dra. Camila Andrade — CRO-MG 28.451 |
| Endereço | Rua das Acácias, 245 — Centro, Teófilo Otoni, MG |
| Telefone | (33) 3203-4521 |
| WhatsApp | (33) 99001-2233 |
| E-mail | contato@sorrirodonto.com.br |
| Horário | Seg–sex 8h–18h · Sáb 8h–12h |

Use Ctrl+F (ou Cmd+F) no arquivo HTML para localizar e trocar cada um desses valores.

## ⚠️ O formulário de agendamento não envia dados

O formulário na seção "Contato" é **apenas visual**: ao clicar em enviar, um JavaScript local mostra uma mensagem de confirmação na tela, mas nenhuma informação é transmitida para e-mail, banco de dados ou qualquer serviço. Para receber os pedidos de verdade, escolha uma opção antes de publicar o site:

1. **WhatsApp** — trocar a ação do formulário para montar uma mensagem e abrir `https://wa.me/55SEUNUMERO?text=...` com os dados preenchidos.
2. **mailto** — abrir o cliente de e-mail do visitante com os dados no corpo da mensagem (simples, porém menos confiável em celulares).
3. **Serviço de formulários** (Formspree, Getform, Google Forms embutido etc.) — envia os dados para um endpoint externo e notifica por e-mail ou salva em planilha.

## Sobre a imagem na seção "Sobre"

A ilustração usada nessa seção foi enviada pelo usuário e está embutida diretamente no HTML como uma imagem codificada em base64 (`data:image/jpeg;base64,...`). Isso mantém o arquivo autocontido (sem depender de links externos), mas deixa o HTML consideravelmente maior e menos legível nesse trecho. Para trocar a imagem:

1. Substitua o conteúdo do atributo `src` da tag `<img>` dentro de `.sobre-photo` por outra imagem (outra base64, ou um link `https://` se for hospedar em um site com imagens externas permitidas).
2. Ou remova a tag `<img>` e volte a usar uma ilustração em SVG (mais leve).

## Personalização rápida

- **Cores**: todas as cores estão centralizadas nas variáveis CSS dentro de `:root` no topo do `<style>` (`--teal-700`, `--gold-600`, `--ivory`, etc.). Também há uma variante para modo escuro automático.
- **Fontes**: `Fraunces` (títulos) e `Work Sans` (texto), carregadas do Google Fonts no `<head>`.
- **Textos**: todo o conteúdo está direto no HTML, sem sistema de templates — basta editar o texto entre as tags.
- **Ícones e ilustrações**: são todos SVG desenhados à mão no próprio arquivo, sem bibliotecas externas.

## Publicando o site

Qualquer serviço de hospedagem de site estático funciona, por exemplo:

- Netlify / Vercel: arraste o arquivo `sorrir-odontologia.html` (renomeando para `index.html`) para o painel de deploy.
- GitHub Pages: suba o arquivo como `index.html` num repositório e ative o Pages nas configurações.
- Hospedagem tradicional: envie o arquivo por FTP/cPanel como `index.html`.

## Aviso

Este é um projeto de demonstração. Nome do consultório, dentista, CRO, endereço, telefone e e-mail são fictícios e não correspondem a nenhuma pessoa ou estabelecimento real.