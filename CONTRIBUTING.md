# Sobre este repositório
Este projeto é composto de diversos microsserviços, cada um em seu próprio repositório. Neste há a junção de todos eles através de [git submodules](https://www.git-scm.com/book/en/v2/Git-Tools-Submodules).
Como diz explica a documentação no link: 

> Submodules allow you to keep a Git repository as a subdirectory of another Git repository. This lets you clone another repository into your project and keep your commits separate. 

Com a utilização de submodules se fazem necessários o uso de outros comandos git além dos mais comuns. Este documento explicará mais sobre a estrutura apresentada aqui, e como funciona o git flow para explorá-la e contribuir com ela. Informações mais detalhadas sobre os comandos podem ser encontrados no mesmo link citado no início.

## Os repositórios separados
- `backend`: https://github.com/Eric-Mendes/smart-plant
- `mobile_app`: https://github.com/rabbitvictor/smartfactoryapp 
- `web_app`: ...

## Clonando este repositório
Ao rodar o `git clone` normalmente, você obterá as pastas de cada submodule, mas não os arquivos. Para obter seus arquivos você precisa rodar dois comandos a mais: `git submodule init` e `git submodule update`. Juntando tudo temos
```bash
git clone git@github.com:Eric-Mendes/smart-factory.git
git submodule init
git submodule update
```

## Atualizando os submodules com as mudanças do repositório remoto
Vá até a pasta correspondente e rode `git fetch`.
```bash
# Para atualizar com os commits mais recentes do backend, por exemplo
cd backend
git fetch
cd ..
```

Também é possível atualizar (mandar código para) o repositório remoto através deste, porém como foge do objetivo aqui - que é apenas ter uma visão melhor do todo - não será detalhado neste documento.
