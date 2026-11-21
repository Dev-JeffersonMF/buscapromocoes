<div align="center">

# 🔥 BuscaPromoções

[![Versão](https://img.shields.io/badge/versão-1.4.0-brightgreen)](https://github.com/Dev-JeffersonMF/buscapromocoes/releases)
[![Android](https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white)](https://github.com/Dev-JeffersonMF/buscapromocoes/releases)
[![Catálogo](https://img.shields.io/badge/catálogo-848%20ofertas-orange)](https://github.com/Dev-JeffersonMF/buscapromocoes)
[![Licença](https://img.shields.io/badge/licença-uso%20pessoal-red)](LICENCA.md)

**Ofertas do Mercado Livre 🛒 com links de afiliado e compra organizada em uma fila.**

[**📥 Baixar APK mais recente**](https://github.com/Dev-JeffersonMF/buscapromocoes/releases/latest)

</div>

---

## 📲 Sobre o app

O **BuscaPromoções** reúne centenas de promoções do **Mercado Livre** em uma vitrine rápida, com:

- 🔎 Busca por nome, loja ou categoria
- 🏷️ Filtro por loja (**Todos / Mercado Livre**)
- 🌙 Modo claro e escuro
- 🎟️ Cupons (quando disponíveis)
- 🛒 **Carrinho próprio** com compra **sequencial** (um produto por vez)
- 🔗 Links de **afiliado** — você compra nos apps oficiais e o autor recebe uma comissão
- 📡 Catálogo atualizado em tempo real via **Firebase Realtime Database**
- 🔄 Atualização **OTA** (o app baixa melhorias ao abrir)

> ⚠️ O BuscaPromoções **não é um app de compras** e não processa pagamentos. Todas as compras acontecem dentro dos aplicativos oficiais das lojas, com a sua conta e o seu login.

---

## ✨ Novidades

### 🚧 v1.4.0 — em preparação (próximo build)

- 🩹 **Corrigido:** o modal do produto não travava mais a tela nem desfocava o fundo; agora ele abre na frente, com fundo escurecido e fecha com **✕**, **toque fora** ou **botão voltar**
- 🛒 **Novo:** carrinho interno com botão **➕** no card e no detalhe do produto
- 🧭 **Novo:** compra **sequencial** — o app agrupa os itens por loja, abre um produto por vez e espera você voltar para seguir para o próximo
- ✅ **Novo:** painel de progresso da compra com **"Concluído"**, **"Próximo"** e **"Cancelar"**
- 📦 **Atualizado:** catálogo com **848 ofertas**, todas do **Mercado Livre**
- 🏷️ **Novo:** categoria ⚡ **Pokémon** (6 ofertas) e remoção da categoria ⚽ Figurinha da Copa
- 📱 **Novo: modo autônomo** — os **848 produtos vão dentro do APK**: a vitrine funciona sem Firebase, sem internet e sem login
- ➕ **Novo:** tela **Novo produto** — cole o link, busque o preço automaticamente, escolha a imagem e salve **no aparelho** (marcado com 📱); opcionalmente envie também ao Firebase
- 🔑 **Novo:** **Esqueci minha senha** no painel admin (envia o link de redefinição do Firebase Authentication)
- 📄 **Novo:** página com changelog, emojis, avisos de afiliado e licença contra pirataria
- 🔒 **Novo:** `AndroidManifest` com `<queries>` para detectar corretamente o app do Mercado Livre no Android 11+

### ✅ v1.3.0 — release atual

- ♻️ Refatoração e melhoria da qualidade do código
- 🔔 Sistema de notificação de atualização **in-app** (opcional)
- 🏗️ Infraestrutura preparada para a versão da Play Store
- 🐞 Correções de bugs menores

<details>
<summary><b>📜 Versões anteriores</b></summary>

- **v1.02** — vitrine 3D, cupons, filtros por loja e painel admin
- **v1.01** — primeiro release com catálogo Firebase

</details>

---

## 🛒 Como funciona a compra sequencial

O app abre **um produto por vez** no app do Mercado Livre. O fluxo é:

1. Você toca em **➕** nos produtos que quer e eles entram no carrinho do BuscaPromoções, em uma fila.
2. Toque em **🧾 Comprar tudo**.
3. O app verifica se o app do Mercado Livre está instalado e abre **um produto de cada vez**.
4. Dentro da loja, **adicione o item ao carrinho** com a sua conta (é necessário estar logado).
5. Quando você voltar ao BuscaPromoções, o app detecta o retorno e mostra: **➡️ Próximo produto** ou **✅ Concluído**.
6. Você confirma o retorno e o app segue para o próximo produto.
7. No final, você vê um resumo e o carrinho é limpo.

> 💡 **Importante:** as lojas não oferecem um link público para "adicionar ao carrinho e ir para o pagamento". Por isso o app abre cada produto e você confirma a adição dentro do app oficial. Isso evita erros, compras duplicadas e garante que os links de afiliado sejam registrados corretamente.

---

## 📱 Modo autônomo — funciona sem Firebase

A partir da v1.4.0 o catálogo completo (**848 ofertas**) vem **embarcado no APK**.
O app carrega essa lista na hora, sem depender de rede, e só tenta atualizar do
Firebase em segundo plano. Se o Firebase estiver fora do ar, você continua vendo
e usando todos os produtos normalmente.

### Adicionar produtos sem login

Toque no **➕** no topo da vitrine (ou no **＋** do card) para abrir a tela **Novo produto**:

1. **Cole o link** de afiliado — a loja é detectada automaticamente (Mercado Livre)
2. Toque em **🔍 Buscar preço pelo link** — o app tenta preencher preço e preço original
3. Escolha a **imagem** da galeria, ajuste nome, descrição e **categoria**
4. Toque em **💾 Salvar no aparelho**

O produto aparece na vitrine com o selo **📱** e fica salvo no seu aparelho.
Se você estiver logado no painel admin, também pode tocar em **☁️ Salvar também no Firebase**.

> 🔑 **Esqueceu a senha do admin?** Na tela de login, toque em **🔑 Esqueci minha senha**.
> O Firebase envia o link de redefinição para o e-mail cadastrado (não é mais preciso
> apagar o usuário e criar outro). Se esse e-mail não existir mais no Firebase
> Authentication, crie um novo usuário no Console e use o link de recuperação.

---

## 💰 Links de afiliado

Os links do catálogo já contêm o rastreamento de afiliado do autor (**Mercado Livre**). Ao finalizar uma compra, o autor recebe uma comissão — **sem custo extra para você**.

Produtos adicionados manualmente no painel admin usam os IDs configurados em `.env`:

```env
EXPO_PUBLIC_AFILIADO_ML_ID=SEU_ID
```

---

## 🏆 Catálogo e "mais vendidos"

O catálogo é servido pelo **Firebase Realtime Database** (`/catalogo`) e hoje conta com
**848 ofertas** (todas do 🛒 Mercado Livre), organizadas por categoria.

Para escolher os produtos que mais vendem, a fonte oficial é o **hub de afiliados**:

- 🛒 [Mercado Livre Afiliados — Hub](https://www.mercadolivre.com.br/afiliados/hub?is_affiliate=true#menu-user)

Esse painel exige login e tem proteção anti-bot, por isso a seleção dos "mais
vendidos" é feita com sessão logada e os links de afiliado são capturados pelos
bookmarklets incluídos no repositório privado. O pipeline completo está em
`scripts/README.md`:

```bash
python3 scripts/login-ml-afiliado.py     # login único no ML
python3 scripts/baixar-catalogo.py
python3 scripts/importar-produtos.py     # lê produtos-novos.json
python3 scripts/melhorar-catalogo.py
python3 scripts/publicar-catalogo.py --dry-run
python3 scripts/publicar-catalogo.py
```

> 🔑 A publicação exige o **Database Secret** do Firebase (fora do APK). Nunca
> commite `.env`, `chave.json`, sessões de afiliado nem o `catalogo.json`.

---

## 📥 Instalação (APK)

1. Baixe o APK em [**Releases**](https://github.com/Dev-JeffersonMF/buscapromocoes/releases/latest)
2. Libere **Fontes desconhecidas**:
   - **Android 8+:** Configurações → Apps → Acesso especial → Instalar apps desconhecidos → permita o navegador/gerenciador usado
   - **Android 7:** Configurações → Segurança → Fontes desconhecidas
3. (Opcional) Play Store → avatar → **Play Protect** → desative a verificação **temporariamente**
4. Instale o `buscapromocoes-v1.x.x.apk` e **reative o Play Protect** depois

**Requisitos:** Android 7.0 (API 24)+ e internet.

---

## 🔐 Privacidade

- O app **não coleta dados pessoais**, não pede login e não lê suas compras
- Seus dados de login ficam **somente no app oficial do Mercado Livre**
- O catálogo, os cupons e os links são públicos e servidos pelo Firebase
- O app registra apenas erros técnicos anônimos (para melhorar a estabilidade)

---

## ⚖️ Licença e avisos legais

O código e os arquivos deste repositório são de autoria de **Dev-JeffersonMF** e são fornecidos para **uso pessoal, não comercial**.

**É permitido:**

- ✅ Usar o app e baixar o APK para uso próprio
- ✅ Compartilhar o link oficial deste repositório
- ✅ Estudar o código para fins educacionais

**É PROIBIDO:**

- 🚫 Vender, alugar, sublicenciar ou redistribuir o app ou APKs modificados
- 🚫 Publicar o APK em lojas, sites ou canais que não sejam os oficiais do autor
- 🚫 Remover ou trocar os **links de afiliado** para desviar comissões
- 🚫 Falsificar releases, versões, telas ou a identidade do autor
- 🚫 Usar o código para criar produto concorrente ou comercial
- 🚫 Fazer engenharia reversa com fins comerciais ou maliciosos

O autor não se responsabiliza por uso indevido, alterações não autorizadas ou instalações de fontes não oficiais. **Pirataria e uso improprio não são tolerados.** Veja o texto completo em [`LICENCA.md`](LICENCA.md).

A marca Mercado Livre pertence ao seu respectivo dono. Este projeto não é afiliado oficial da empresa.

---

## 🆘 Suporte

Encontrou um problema? Abra uma [**Issue**](https://github.com/Dev-JeffersonMF/buscapromocoes/issues) com:

- 📱 Modelo do aparelho e versão do Android
- 🔢 Versão do app
- 📝 Passo a passo para reproduzir

---

<div align="center">

Feito com 🔥 por **Dev-JeffersonMF**

[⬆️ Voltar ao topo](#-buscapromoções)

</div>
