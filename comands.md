

# Comandos para monitorar diretórios

## Versão do git:
```
git --version
```


## Vê o que tem dentro do diretório
```
ls
```


Inicia um repositório (este diretório e tudo o que tiver dentro) e cria a branch MASTER - que pode ser renomeada com o comando ```$ git branch -m <name>```
```
git init
```


Mostra as infos do diretório
```
git status
```


Adiciona arquivos no git para serem monitorados. Também usar o comando sempre que for enviar (salvar) alterações
```
git add (file - nome do arquivo)
```


Adiciona todos os arquivos da pasta atual no git para serem monitorados
```
git add .
```


Para comitar as alterações efetuadas - mensagem sempre entre aspas duplas. Ou ver na lateral do terminal o que tem para salvar, comitar e sincronizar (com o github)
```
git commit -m "blablabla"
```


Mostra o resumo do que foi feito, salvo e comitado
```
git log
```


Mostra o resumo do que foi feito, salvo e comitado em apenas 1 linha
```
git log --oneline
```


Mostra o resumo do que foi feito, salvo e comitado, com mais informações
```
git log -p
```


 Sai da tela do log e volta para editar no terminal
```
q
```


## Git log cheatsheet - para ver mais comandos e filtrar o que será mostrado no resuno do log
https://devhints.io/git-log



## Para ignorar um documento ou pasta - criar o arquivo .gitignore e dentro dele salvar o nome do que quer que seja ignorado - nome-do-doc ou nome-da-pasta/  ou * nome-da-pasta. Tem que add este arquivo no repositório e comitar



Sobe 1 diretório
```
cd ..
```


Vai para o diretório escolhido
```
cd (nome-da-pasta)
````


Cria um repositório puro, que só contem as alterações dos arquivos. Vai gerar um endereço do repositorio criado. Ex. /Users/klebernogueira/Desktop/Loulou/Alura/servidor-curso-git/
```
git init --bare
```


Cria um repositório remoto com o endereço que quiser - pode ser um remoto na propria maquina, no hub, etc
```
git remote add (nome-que-quiser) (endereço do repositório remoto)
```


Mostra o endereço do repositório remoto e que busca (fecth) e envia (push) dados para este caminho
```
git remote -v
```

Cria uma nova pasta
```
mkdir nome-da-pasta-a-criar
```


Clona os arquivos do repositório para este lugar que está sendo indicado
```
git clone /nome-pra-onde-vai-mandar
```


Renomear repositório remoto
```
git remote rename nome-antigo nome-novo
```


Envia arquivos pro repositório
```
git push nome-do-repositório-que-quer-mandar master
```


Busca arquivos pro repositório
```
git pull nome-do-repositório-que-quer-trazer master
```

