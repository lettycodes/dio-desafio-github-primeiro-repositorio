Alguns dos comandos mais utilizados no terminal do Git, o Git Bash.

# git config
A primeira coisa que você deve fazer quando instalar o Git é definir o seu nome de usuário e endereço de e-mail. Isso é importante porque todos os commits no Git utilizam essas informações, e está imutavelmente anexado nos commits que você realiza:

    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com
    
Relembrando, você só precisará fazer isso uma vez caso passe a opção --global, pois o Git sempre usará essa informação para qualquer coisa que você faça nesse sistema. Caso você queira sobrepor estas com um nome ou endereço de e-mail diferentes para projetos específicos, você pode executar o comando sem a opção --global quando estiver no próprio projeto.

# git init
Esse é o comando que você irá utilizar para criar um novo projeto de git. O comando irá criar um repositório novo em branco e, a partir daí, será possível armazenar seu código fonte, alterar, salvaguardar alterações etc.
Exemplo:

    $ git init
    
Se você já possui um repositório anterior ou deseja criar um repositório com um nome em específico, você pode passar o nome como parâmetro do comando:

    $ git init <O nome do seu repositório>

# git clone

Clonando um Repositório Existente
Você clona um repositório com git clone [url]. Por exemplo, caso você queria clonar a biblioteca Git do Ruby chamada Grit, você pode fazê-lo da seguinte forma:

    git clone git://github.com/schacon/grit.git
    
# git add
Esse comando Git adiciona os arquivos especificados de código ao seu repositório, sejam arquivos novos ou arquivos anteriores que foram alterados. Oferece diferentes possibilidades de sintaxe.

Exemplo:

    $ git add seu_arquivo (esse comando irá adicionar o arquivo em específico ao repositório)

ou

    $ git add * (esse comando irá adicionar todos os arquivos novos e/ou modificados ao repositório)
    
# git commit
É fundamental se estabelecer uma diferença entre git add e git commit:

- git add adiciona seus arquivos modificados à fila para serem submetidos a um commit posteriormente. Os arquivos não passaram por um commit.

- O git commit executa o commit dos arquivos que foram adicionados e cria uma nova revisão com um log. Por outro lado, se você não adicionar nenhum arquivo, o git não fará o commit de nada.

É possível combinar as duas ações em um único comando: $ git commit -a.

Também é possível adicionar uma mensagem para a execução de um commit. Exemplo:

    $ git commit -m “seu comentário”
    
# git status
A principal ferramenta utilizada para determinar quais arquivos estão em quais estados é o comando:

    git status
    
# git push
Esse comando serve para subir suas modificações para um repositório remoto conectado anteriormente com git remote.

Exemplo:

    $ git push -u <nome_curto> <nome_do_branch>

É importante especificar a origem e o upstream antes de usar o git push. Veja o exemplo:

    $ git push –set-upstream <nome_curto> <nome_do_branch>

# git pull
O comando Git pull baixa o conteúdo (não os metadados) do que foi alterado no repositório remoto para o seu repositório local e imediatamente atualiza seu contreúdo para a última versão.

Exemplo:

    $ git pull <URL>
    
