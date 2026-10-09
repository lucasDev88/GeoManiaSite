# Geo Mania — site de download

Site independente do aplicativo Android, em português, com download da versão 0.6.0, apresentação dos três jogos, Camo e instruções de instalação.

## Executar localmente

Com Node.js instalado: `node preview.mjs`. Abra http://localhost:4173.

## Estrutura

- `dist/`: site estático pronto para publicação.
- `dist/downloads/GeoMania-0.6.0-debug.apk`: APK de demonstração (Android 8+).
- `.openai/hosting.json`: configuração da publicação com Sites.
- `vercel.json`: configuração para publicar na Vercel, sem instalação de dependências ou build.

## Publicar na Vercel

1. Na Vercel, escolha **Add New → Project** e importe `lucasDev88/GeoManiaSite`.
2. Use a branch `main` e mantenha **Root Directory** na raiz do repositório (não selecione `dist`).
3. O `vercel.json` configura automaticamente **Framework Preset: Other**, **Output Directory: dist** e desativa os comandos de build e instalação. Não é preciso configurar variáveis de ambiente.
4. Clique em **Deploy**. Após conectar o GitHub, novos pushes para a branch de produção geram novas publicações.

O site é HTML/CSS/JavaScript estático. O APK já está dentro de `dist/downloads`, e o botão utiliza um caminho relativo, funcionando no domínio fornecido pela Vercel ou em um domínio personalizado. Os cabeçalhos de download do APK estão definidos no `vercel.json`; a Vercel não utiliza o arquivo `dist/_headers` da hospedagem anterior.

A configuração em `.openai/hosting.json` foi mantida como registro da hospedagem anterior e não é usada pela Vercel. Não há necessidade de framework, servidor ou funções.

Documentação: https://vercel.com/docs/project-configuration/vercel-json

SHA-256 do APK: `b4f968aec89790387e01a4fe17050956da5db4b5b7b9c954e93fc0ea08034efe`.

Para atualizar, substitua o APK e ajuste versão, tamanho e hash em `dist/index.html`. Não há dados pessoais, serviços de cadastro ou analytics no site. As fontes tipográficas vêm do Google Fonts, com alternativas locais.

O aplicativo está em um repositório separado: https://github.com/lucasDev88/GeoMania.
