# smart-factory
Projeto de uma fábrica inteligente para a matéria de MC855 do IC - Unicamp (2s2022).

Aqui pretendemos obter dados _near-real-time_ de sensores diversos - como de temperatura, umidade, luminosidade, etc. - manter um histórico destas medições, apresentá-las visualmente em um web app, e mandar anomalias nelas através de um app mobile.

## Tech stack
- [`Thingsboard`](https://thingsboard.io/) para lidar com a parte IoT;
- `Kotlin` para o mobile app;
- `Python` para o backend;
- [`Anvil Works`](https://anvil.works/) para o web app.

Mais informações podem ser encontradas nos repositórios de origem de cada parte deste projeto.

## Rodando o projeto
Usaremos docker para um ambiente local, e simularemos um ambiente multihost para simular um ambiente de produção. Importante notar que **NÃO USAREMOS CLOUD**, dado a sensibilidade do contexto produtivo de qualquer fábrica. 

Suba todos os containeres de cada microsserviço apenas com o comando
```bash
docker compose up -d
```
Após isto você encontrará o backend no endereço `localhost:8000` e o web app (frontend) no endereço `localhost:3030`.

Não se esqueça de derrubar todos os containeres ao final, rodando o comando abaixo
```bash
docker compose down
```