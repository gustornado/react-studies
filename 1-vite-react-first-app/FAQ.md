# Possíveis Questionamentos
Recaptulação rápida para perguntas que podem surgir na cabeça caso eu veja esse estudo no futuro. Também porque tomei algumas decisões.

## O que é Reactjs?
Framework JavaScript para criação de frontend

## Por que Reactjs e não outro framework (e.g. Angular, Vue)?
Escolhi Reactjs, também por sua popularida, mas principalmente por existir o React Native. O React Native é uma linguagem paralela ao Reactjs mas para desenvolvimento mobile.

Dessa forma, ao aprender desenvolvimento web, estarei caminhando para o desenvolvimento mobile simultaneamente.

## O que é Vite?
É um startpack para projetos Reactjs. 

Até onde sei, o Reactjs não é só uma biblioteca, mas todo um ecossistema de bibliotecas que trabalham em conjunto para entregar um frontend. Então instalar parte por parte toda vez é trabalhoso ([como instalar parte a parte](https://blog.bitsrc.io/create-react-app-without-create-react-app-b0a5806a92)).

Por isso existem pacotes como Vite e create-react-app. Eles compilam essas bibliotecas e disponibilizam uma aplicação funcional apenas com um comando.

## Por que Vite e não create-react-app?
Achei o Vite mais clean. 

O react-react-app instala muita coisa e fica muita sujeira em um projeto que acabou de começar. 

## Recomendo instalar `nvm` para controle de versões do Node
Para listar todas as versões do node:
```sh
nvm ls-remote
```

Para instalar e usar a últimar versão LTS na máquina:
```sh
nvm install --lts
nvm use --lts
```