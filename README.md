# Geo Mania — site de download

Site independente do aplicativo Android, em português, com download da versão 0.6.0, apresentação dos três jogos, Camo e instruções de instalação.

## Executar localmente

Com Node.js instalado: `node preview.mjs`. Abra http://localhost:4173.

## Estrutura

- `dist/`: site estático pronto para publicação.
- `dist/downloads/GeoMania-0.6.0-debug.apk`: APK de demonstração (Android 8+).
- `.openai/hosting.json`: configuração da publicação com Sites.

SHA-256 do APK: `b4f968aec89790387e01a4fe17050956da5db4b5b7b9c954e93fc0ea08034efe`.

Para atualizar, substitua o APK e ajuste versão, tamanho e hash em `dist/index.html`. Não há dados pessoais, serviços de cadastro ou analytics no site. As fontes tipográficas vêm do Google Fonts, com alternativas locais.

O aplicativo está em um repositório separado: https://github.com/lucasDev88/GeoMania.
