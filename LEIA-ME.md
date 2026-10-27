# Painel Digimon — instalador para Windows (Electron)

Empacota o app (www/index.html) num instalador .exe. A compilação roda no GitHub Actions.

## Gerar o instalador
1. Crie um repositório NOVO no GitHub (separado do projeto do APK).
2. Envie o conteúdo desta pasta: `main.js`, `package.json`, `.gitignore`, `LEIA-ME.md`, `build` e `www`.
3. Crie a receita à mão: Add file > Create new file, nome `.github/workflows/build-exe.yml`,
   e cole o conteúdo do arquivo de mesmo nome que está dentro do zip.
4. Aba Actions > Gerar EXE > Run workflow (também roda sozinha a cada envio).
5. Quando ficar verde (uns 3 a 6 minutos), baixe `painel-digimon-exe` em Artifacts.
   O zip traz dois arquivos:
   - PainelDigimon-Instalador-1.0.0.exe: instala no computador, com atalhos.
   - PainelDigimon-Portatil-1.0.0.exe: roda direto, sem instalar.

## Aviso do Windows
O instalador não tem assinatura paga, então o SmartScreen pode mostrar
"O Windows protegeu o seu PC". Clique em "Mais informações" e depois em "Executar assim mesmo".

## Atualizar
Troque `www/index.html` pela versão nova, envie ao repositório e rode o workflow de novo.
