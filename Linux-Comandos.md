# Ajuda
Para saber mais sobre os comandos:
`man <comando>`
`<commando> --help`

# Globbing
* : zero ou mais caracteres
? : substitiu um / ou mais caracteres


#  Arquivo - Compactação e descompactação tar
| `tar -czf <arquivo>.tar.gz <ORIGEM_arquivo|diretorio>` | Para compactar os arquivos. O parâmetro `-c` indica ao comando tar que desejamos criar um novo arquivo. O parâmetro `-z` indica que queremos zipar, além de criar um único arquivo, realizar um processo de compactação utilizando o formato .gz. O parâmetro `-f` indica que compactaremos para um arquivo |
| `tar –xzf <nomeArquivo.tar.gz>` | Descompacta o arquivo |
| `tar –vxzf nomeArquivo.tar.gz`  | Podemos adicionar a flag -v = verbose |


#  Arquivo - Criando e abrindo ZIP
| `unzip -l`                        | Lista os arquivos dentro do arquivo zipado, sem descompactar |
| `unzip -q`                        | Para reduzir os logs |
| `zip <nomeDestino.zip> <arqs>`    | Zip de um arquivo |
| `zip -r <nomeDestino.zip> <dir/>` | Zip de diretório e seus aequivos |
| `zip <nomeDestino.zip> <arqOriginal.zip> -rq` | Zip recursivo não verboso           | 


#  Arquivos - Leitura
| `cat <arq>`           | Recebe o nome do arquivo como argumento e imprime seu conteúdo |
| `cat <arquivo> -n`    | Retorna também a numeração das linhas   |
| `cat <arquivo?.txt>`  | `?` - busca um caractere não determinado, vai ler todos os arquivos |
| `cat <arquivo*.txt>`  | `*` - substitui _n_ caracteres não determinados |
| `cat *.txt`           | `*` - substitui _n_ caracteres não determinados |

| `more` |
| `head <arquivo>`            | Por default retorna as 10 primeiras linhas  |
| `head <arquivo> -n <num>`   | `-n` especifica uma quantidade especifica de linhas a serem retornadas  |
| `less <arquivo> `           | Vai abrindo o arquivo aos poucos    |
| `tail <arquivo>`            | Retorna as 10 ultimas linhas, por default   |
| `tail <arquivo> -n num`     | `-n` retorna uma quantidade especifica de linhas    |
 tail -n 5 syslog | grep systemd > log5.txt

#  Arquivos - Manipulação
| `cp origem destino`       | Faz uma cópia do arquivo (origem) com o nome/local `destino` |
| `cp -r origem destino`    | Faz uma cópia do diretório (origem) com o nome/local `destino` |
| `mv <origem> <destino>`   | Renomeia o arquivo (origem) para o um novo nome (destino) |
| `mv <origem> <destino/>`  | Move o arquivo (origem) para o um novo local (destino) |
| `rm <nomeArq>`            | Remove arquivo |
| `rm -r <dir/>`            | Remove o diretório e tudo que tem nele |
| `touch <arquivo.ext>`     | Atualiza a data do arquivo, sem alterar o conteudo |   

# Diretórios
| `pwd`             | Descobrir qual o caminho do diretório em que estou |
| `ls`              | Lista arquivos e diretórios |
| `ls *`            | Retorna o que há dentro dos diretórios presentes no diretório consultado  |
| `ls -a`           | Para listar os arquivos ocultos |
| `ls -l`           | Para listar de forma detalhada |
| `ls -la`          | Para listar os arquivos e diretórios incluindo arquivos ocultos |
| `cd`              | Muda de diretório. Se digitado sem parametro, vai para a home do usuário |
| `cd ~/workspace`  | Também passar para o comando cd o caminho absoluto. Ou podemos usar esse atalho para a home do usuário |
| `mkdir <nomeDir>` | Criar diretório |
| `mkdir -p <nomeDir1>/<nomeDir2>/<nomeDir3>` | Criar um diretório com diversos subdiretórios |
| `rmdir <dir/>`    | Remove diretório VAZIO |


# Impressão em Tela
| `echo <string>` | Exibe uma mensagem no terminal | 


# Pesquisa 
| `find -maxdepth <num>` | vai limitar quantos niveis irá entrar para faezr a busca |
| `finde . -amin -5`  | vai retornar os arquivos a partir do direotiro informado que foram alterados nos ultimos 5 minutos
| `find <dir> -atime -2` | vai retornar os arquivos que foram alterados nos ultimos dois dias |
| `find <dir> -size +100M` | vai retornar os arquivos com mais de 100 Mega 


# Redirecionando saída
| `echo "msg" > nomeArquivo`    | Envia a saida para um arquivo |
|  `>`                          | Adiciona ao arquivo sobrescrevendo o que havia nele antes |
|  `>>`                         | Adiciona ao fim do arquivo |


# Sistema
| `whoami`          | Retorna o usuário que está sendo usado |
| `date "+%d/%m/%Y"` | Date + formatação da data a ser exibida. Mais informações de formatação pode ser verificada com o comando date --help |


# Terminal
| `clear` | Limpa terminal (CTRL + l tem a mesma função) |
| `sort`| irá ordenar a saida. pode ser usado para ordenar a saida de um outro comando, exemplo `cat <arquivo> | sort`|



# ---- --------------- REVISADO --------------------------




















## Manipulação de Arquivos

| locate <string>           | Busca em todo o sistema os arquivos que tenham string em seu nome     |


| wc                            | Utilizado para contar o número de palavras, caracteres e linhas que um arquivo possui.    |
| wc –w                         | Indica que devem ser contabilizadas apenas o número de palavras que existe em um arquivo. |
| wc –w *.txt  (palavras)       | Indica que devem ser contabilizadas todas as palavras do diretório em que o comando foi executado. |
| wc –C *.txt  (caracteres)      | Indica que devem ser contabilizadas todos os caracteres do diretório em que o comando foi executado. |
| wc –L *.txt  (lihas)           | Indica que devem ser contabilizadas todas as linhas do arquivo em que o comando foi executado.







| man <cmd>                 | Manual dos comandos               |
| man + "q"                 | Para sair o manual                |
| passwd                    | Faz alteração de senha do usuário corrente no sistema     |
| $  sudo passwd            | Para alterar a senha do user root deve executar o comando |
                          |

| which <programa>              | Busca onde está localizado o "executável" do programa. | 


# **Comandos relacionados ao Acesso Remoto**
| Comando                           | Descrição|
|---------                          | ---------|
| `sudo apt-get install ssh`        | Para acessar remotamente um servidor Linux é preciso ter instalado o ssh | 
| `ssh <usuario>@<ipDoServidor>`    | Teste de instalação | 
| `ssh -X <usuario>@<ipDoServidor>` |  //para que a interface gráfica esteja habilitada  


# Comandos relacionados a edição de texto
**Busca pela palavra na posição x**
    `cat <nome-do-arquivo> | awk '{print $<posição-da-palavra}'`
        `print $1 -> Exibe a primeira coluna;`
        `print $2 -> Exibe a segunda coluna e assim por diante;`
        `print $NF ->Exibe a última coluna.`

**Verifica o caracter em uma posição especifica**
    Seleção de uma coluna
        `$ cut -c152 Teste_linhas-Com-Erro`
    Seleção de uma faixa de colunas
        `$ cut -c141-155 Teste_linhas-Com-Erro`
         cat logs | cut -d “ “ -f6- > logs1
    Busca por várias strings
        `cat <arquiv> | grep -E "<String1|string2|string3>"`
        `cat <arquiv> | grep -E "^<string>"` vai buscar a string que esteja no inicio da palavra
        `cat <arquiv> | grep -E "<string>$"` vai buscar a string que esteja no fim da palavra

    Saida para outro arquivo
        `cat <arquivo> | grep '<string_a_ser_localizada>'> NomeArquivo`
        `cat Teste_linhas-Com-Erro | awk '{print $152}'`
        `cat Teste_linhas-Com-Erro | awk '{print $1}'`
        `cat Teste_linhas-Com-Erro | awk '{print $3}'`
        `cat arquivo | grep -E "palavra1|palavra2"`
        A opção `-E` descrita no grep acima é usada para fazer uma busca estendida. 
        Pode-se usar apenas egrep no lugar de grep -E que será obtido o mesmo resultado
        `-i` ignore Case
    `grep <string> <arquivo> `| pesquisa no arquivo indicado a string informada

    | irá redirecionar a saida de um comando para outro, exemplo : `cat /etc/passwd | grep andressa `


# **DIVISÃO DE UM ARQUIVO**
    `split --lines=<NumeroDeLinhas> <Arquivo>`
        Syntax to extract .tar.gz file
        The syntax is as follows:
            `tar [options] file.tar.gz`
            `tar [options] file.tar.gz pattern`
            `tar -xf file.tar.gz`
            `tar -xvf file.tar.gz`
            `tar -zxvf file.tar.gz`
            `tar -zxvf file.tar.gz file1 file2 dir1 dir2`

### MaiS

* Comando **tar**
Para descompactar o arquivo .tar.gz, substituímos o -c que usamos antes por -x, para indicar que iremos extrair os arquivos. 
O f indica que lemos de um arquivo. E o z, que o arquivo está compactado. 
O parâmetro z na verdade é ignorado na extração, no man fala que só funciona no creation mode. 
Logo poderíamos fazer: tar -xf work.tar.gz 
tar –cjf nomeDoArquiv.tar.bz2 diretorio/ 
Outro algoritmo de compactação bzip2,é mais lento para gerar a compactação, mas gera arquivos menores. 


Apache-Tomcat-configurar-porta