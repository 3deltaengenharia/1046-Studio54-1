3DELTA ENGENHARIA — VISUALIZADOR IFC POR QR CODE
================================================

ARQUIVOS PRINCIPAIS
- index.html       página do visualizador
- app.js           lógica 3D
- logo-3delta.jpg  identidade visual
- modelo.ifc       IFC exibido pela página

COMO ATUALIZAR O MODELO SEM TROCAR O QR
1. Exporte a nova revisão do IFC.
2. No servidor/hospedagem, substitua somente o arquivo "modelo.ifc" pelo novo IFC.
3. Mantenha exatamente o nome "modelo.ifc".
4. O endereço da página continua o mesmo, portanto o QR Code continua o mesmo.
5. O visualizador usa uma URL sem cache para buscar sempre a versão atual.

IMPORTANTE
- O QR Code deve apontar para a URL da pasta/página publicada, por exemplo:
  https://modelo.3deltaengenharia.com.br/h741/
- O usuário da obra NÃO precisa de app nem login.
- É necessário acesso à internet.
- Este modelo IFC tem aproximadamente 49 MB. Em celulares, o primeiro carregamento pode ser pesado.
- Para produção com muitos acessos, vale converter automaticamente IFC -> .frag para carregamento muito mais rápido.

TESTE LOCAL
Não abra o index.html com duplo clique, pois navegadores podem bloquear a leitura do IFC local.
Na pasta do site, rode um servidor HTTP. Exemplo, com Python instalado:

  python -m http.server 8080

Depois abra:
  http://localhost:8080

HOSPEDAGEM
Funciona como site estático em serviços como Cloudflare Pages, GitHub Pages, Netlify ou hospedagem própria.
Para uso em obra, recomenda-se domínio/subdomínio fixo e HTTPS.
