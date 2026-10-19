# Vibe Music para Android

Este projeto cria um aplicativo Android instalável que abre `https://vibe-music.hatchable.site` em uma WebView segura. O site continua hospedado no Hatchable: o login, as APIs, o banco de dados, o chat global e o histórico permanecem no backend atual, sem copiar credenciais ou banco para o APK.

## Gerar o APK pelo GitHub Actions

1. Crie um repositório GitHub vazio e envie todos os arquivos desta pasta para a branch `main`.
2. Abra a aba **Actions** do repositório e habilite os workflows, se o GitHub pedir.
3. Execute **Build Vibe Music APK** com **Run workflow** (ou aguarde o build após o push).
4. Quando terminar, abra a execução e baixe o artefato **Vibe-Music-APK**.
5. Extraia o ZIP do artefato e instale `app-debug.apk` no Android. Se solicitado, permita instalar apps dessa fonte.

## Observações importantes

- O APK é um invólucro Android para o site online; não é uma cópia offline completa do serviço.
- É necessário internet para acessar o site e o backend.
- O seletor de arquivos do Android é habilitado para recursos de upload de capa.
- O player, a conta e os dados continuam sujeitos às capacidades do site e do navegador WebView do Android. Recursos que dependam de suporte especial do navegador precisam ser testados no aparelho.
- Este fluxo gera um APK de depuração instalável. Para distribuição pública, o ideal é configurar assinatura de release e testar em aparelhos reais.
