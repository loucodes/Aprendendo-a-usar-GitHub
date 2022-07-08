

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


Renomea repositório remoto
```
git remote rename nome-antigo nome-novo
```


Envia arquivos pro repositório (local ou hub - vc escolhe)
```
git push nome-do-repositório-que-quer-mandar master
```


Busca arquivos pro repositório
```
git pull nome-do-repositório-que-quer-trazer master
```

Para mandar pro github, cria um repositório lá, coloca descrição e etc. Vai gerar um endereço https com o comando para colar no terminal.
```
git remote add origin https://github.com/loucodes/Aprendendo-a-usar-GitHub.git
```


Cria uma nova branch e já faz o checkout para esta nova
```
git checkout -b nome-da-nova-branch
```


Faz checkout para outra branch
```
git checkout nome-da-branch
```


Mostra lista coms branchs disponíveis
```
git branch
```


Unifica as branchs e envia o que foi trabalhado em uma branch para a branch master
```
git merge nome-da-branch-que-vai-unir-com-master
```


Atualiza e reposiciona os comits trabalhados numa branch para a master sem gerar um novo commit (une os trabalhos, colocando os commits numa posição de continuidade antes da master - mas dentro dela) )
```
git rebase nome-da-branch-a-reposicionar
```


Descarta alterações no arquivo que ainda não foram marcadas para comitar
```
git restore <file>...
```


Descarta alterações no arquivo que já foram marcadas para comitar, mas não foram commitadas efetivamente
```
git reset HEAD nomedoarquivo
git checkout --nomedoarquivo
```


Descarta alterações no arquivo que já foram commitadas (ver o hash do commit em git log)
```
git revert hash-do-commit
```


Salva as alterações em um aquivo temporário, sem precisar commitar
```
git stash
```


Lista os docs salvos no aquivo temporário
```
git stash list
```


Resgata as alterações salvas no arquivo temporário (resgata o 0, ou 1, ou 2, etc...)
```
git stash apply 0
```


Apaga do temporário
```
git stash drop
```


Resgata a última alteração e já apaga do temporário, realiza o merge com as modificações que já temos e aplica aquelas que já estavam salvas lá
```
git stash pop
```


Volta no estágio que estava no commit indicado
```
git checkout hash-co-commit-indicado
```


Cria nova branch a partir do commit indicado
```
git checkout -b novo-branch
```


Mostra a diferença entre 2 commits
```
git diff hash-do-commit..hash-do-outro-commit
```


Mostra a diferença para o que ainda não foi commitado
```
git diff
```


Cria uma tag do projeto (versão a ser lançada)
```
git tag -a nome-da-versão
```


Cria uma tag do projeto (versão a ser lançada) com uma mensagem
```
git tag -a nome-da-versão -m "mensagem para descrever"
```


Mostra as tags disponíveis
```
git tag
```


Envia tag pro repositório (local ou hub - vc escolhe)
```
git push nome-do-repositório-que-quer-mandar nome-da-versão
```