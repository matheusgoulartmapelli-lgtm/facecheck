# FaceCheck — Como rodar no VS Code

App de controle de presença por reconhecimento facial (câmera do navegador).

## O que você precisa instalar (uma vez só)

1. **Node.js 20 ou mais novo** — baixe em https://nodejs.org (versão LTS).
2. **VS Code** — https://code.visualstudio.com

## Passo a passo

Abra o terminal do VS Code (menu **Terminal → New Terminal**) e rode:

```bash
# 1. Instalar as dependências (só na primeira vez; se der erro, use exatamente assim)
npm install --legacy-peer-deps

# 2. Iniciar o app
npm run dev
```

Depois abra no navegador o endereço que aparecer, normalmente:

```
http://localhost:5173
```

Para parar o app, aperte `Ctrl + C` no terminal.

## Observações importantes

- **Câmera:** o navegador só libera a câmera em `localhost` ou em sites com HTTPS — rodando por `localhost` funciona normalmente. Na primeira vez, permita o acesso à câmera.
- **Banco de dados:** o app já está conectado ao mesmo banco usado na versão online (as chaves de acesso público já vêm no arquivo `.env`). Cadastros, presenças e pessoas aparecem nos dois lugares.
- **Login:** use a mesma conta que você criou na versão online. A primeira conta criada vira Administrador.
- **Reconhecimento facial:** na primeira leitura de rosto, o app baixa os modelos de reconhecimento pela internet (alguns segundos).
- **Arquivo `.env`:** não compartilhe nem suba para o GitHub contendo o arquivo `.env` junto com o código? — Neste projeto o `.env` só contém chaves **públicas** (do lado do navegador), então é seguro, mas por costume mantenha-o fora do git (já está no `.gitignore`).

## Scripts disponíveis

| Comando | O que faz |
| --- | --- |
| `npm run dev` | Roda o app em modo desenvolvimento |
| `npm run build` | Gera a versão de produção |
| `npm run test` | Roda os testes |
| `npm run lint` | Verifica erros no código |
