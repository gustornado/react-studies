# Criando o primeiro app Reactjs + Vite
Neste estudo estarei criando o primeiro app Reactjs + Vite (no Codespaces)

## Pré-requisitos
- node

## Instalação do Vite
```sh
npm create vite
```
Ao rodar o comando acima será necessário responder algumas perguntas para que seja instalado corretamente:
- **Projet Name:** será o nome da pasta onde tudo será instalado. Se colocar "." tudo será instalado na pasta atual.
- **Framework:** escolha React
- **Variant:** TypeScript ou JavaScript. O SWC (Speedy Web Compiler) é como se fosse o novo Babel, ou seja, escolha se precisar suportar navegadores mais antigos.

E pronto! Vite está instalado.

Agora só entrar na pasta e rodar `npm install` para baixar os módulos e `npm run dev` para iniciar o React + Vite

## Rodando aplicação no Codespace do GitHub
Ao rodar `npm run dev` não funciona no Codespaces. Isso acontece por alguma configuração default.

Para rodar, é necessário alterar no `packages.json` a parte de scripts de:
```json
"scripts": {
    "dev": "vite"
    ...
}
```

para:
```json
"scripts": {
    "dev": "vite --host"
    ...
}
```
Essas instruções foram achadas [neste link](https://dev.to/kkoziarski/react-vite-github-codespaces-5529).

Também dá para procurar direto na [documentação oficial do Vite](https://vitejs.dev/config/server-options.html)
