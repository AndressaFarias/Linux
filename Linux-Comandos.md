### ****
| Comando   | Descrição|
|---------  |----------|
| >                         | Adiciona ao arquivo sobrescrevendo o que havia nele antes |
| >>                        | Adiciona ao fim do arquivo |
| cat <arq>                 | Recebe o nome do arquivo como argumento e imprime seu conteúdo | 
| cat <arquivo?.txt>        | ? - busca um caractere não determinado  |
| cat <arquivo*.txt>        | * - substitui n caracteres não determinados  |
| cat *.txt                 |  * - substitui n caracteres não determinados |
| cat <arquivo> -n          | Retorna també a numeração das linhas |
| cd                        | Muda de diretório.
| cd ~/workspace            | Podemos também passar para o comando cd o caminho absoluto. Ou podemos usar um atalho para a home do usuário e fazer |
| clear                     | Limpa terminal                    |
| cp origem destino         | Para arquivos. Cópia de diretório precisa ser recursiva | 
| date "+%d/%m%Y"           | Date + formatação da data a ser exibida. Mais informações de formatação pode ser verificada com o comando date --help |
| echo                      | Exibe um mensagem                 | 
| echo "msg" > nomeArquivo  | Enia a mnaem pr um arquivo        |
| head <arquivo>            | Por default retorna as 10 primeiras linhas                                |
| head <arquivo> -n num     | -n especifica uma quantidade especifica de linhas a serem retornadas      |
| less                      | Vai abrindo o arquivo aos poucos                                          |
| locate <string>           | Busca em todo o sistema os arquivos que tenham string em seu nome         |
| ls                        | Lista arquivos e diretórios                                               |
| ls -l                     | Para listar de forma detalhada                                            |
| ls -a                     | Para listar os arquivos e diretórios incluindo arquivos ocultos           |
| ls *                      | Retorna o que há dentro dos diretórios presentes no diretório consultado  |

| man <cmd>                 | Manual dos comandos               |
| man + "q"                 | Para sair o manual                |
| mkdir                     | Criar diretório                   | 
| mv <origem> <destino>     |                                   |
| passwd                    | Faz alteração de senha do usuário corrente no sistema     S|
| $  sudo passwd            | Para alterar a senha do user root deve executar o comando |

 
| pwd                       | Descobrir qual o diretório        | 
| rm                        | Remove arquivo                    | 
| rmdir                     | Remove diretório vazio            | 
| tail <arquivo>            | Retorna as 10 ultimas linhas, por default |
| tail <arquivo> -n num     | -n retorna uma quantidade especifica de linhas |
| tar -cz <arquivo/diretorio> > <novoarquivo>.tar.gz | Para compactar os arquivos. O parâmetro -c indica ao comando tar que desejamos criar um novo arquivo.|
| tar –xzf <nomeArquivo.tar.gz> | O comando _tar_ apenas empacota vários arquivos em um único arquivo, sem realizar compactação, e por isso passamos o parâmetro **-z** para indicar que queremos, além de criar um único arquivo, realizar um processo de compactação utilizando o formato .gz. Quando compactamos podemos reduzir o tamanho. O parâmetro **-f** indica que compactaremos para um arquivo. |
| tar –xz < <nomeArquivo>.tar.gz| Para descompactar                                 |
| tar –xzf nomeArquivo.tar.gz   | Podemos adicionar a fla -v = verbose              |
| touch <arquivo>               | Atualiza a data do arquivo                        |
| whoami                        | Retorna o usuário que está logado                 |
| unzip -q                      | Para reduzir os logs                              |
| unzip -l                      | Para listar os arquivos dentro do arquivo zipado  |
| wc                            | Utilizado para contar o número de palavras, caracteres e linhas que um arquivo possui.    |
| wc –w                         | Indica que devem ser contabilizadas apenas o número de palavras que existe em um arquivo. |
| wc –w *.txt  (palavras)       | Indica que devem ser contabilizadas todas as palavras do diretório em que o comando foi executado. |
| wc –C *.txt  (caracteres)      | Indica que devem ser contabilizadas todos os caracteres do diretório em que o comando foi executado. |
| wc –L *.txt  (lihas)           | Indica que devem ser contabilizadas todas as linhas do arquivo em que o comando foi executado.
| which <programa>              | Busca onde está localizado o "executável" do programa. | 
| zip <nomeDestino.zip> <arqOriginal.zip> -rq | Zip recursivo não verboso           | 

### **Comandos Relacionados a *Programas,Processos e Pacotes*** 

 

### **Comandos relacionados ao Acesso Remoto**
### ****
| Comando                           | Descrição|
|---------                          | ---------|
| `sudo apt-get install ssh`        | Para acessar remotamente um servidor Linux é preciso ter instalado o ssh | 
| `ssh <usuario>@<ipDoServidor>`    | Teste de instalação | 
| `ssh -X <usuario>@<ipDoServidor>` |  //para que a interface gráfica esteja habilitada  


### Comandos relavionados a edião de texto
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
    Busca por várias strings
        `cat <arquiv> | grep -E "<String1|string2|string3>"`
    Saida para outro arquivo
        `cat <arquivo> | grep '<string_a_ser_localizada>'> NomeArquivo`
        `cat Teste_linhas-Com-Erro | awk '{print $152}'`
        `cat Teste_linhas-Com-Erro | awk '{print $1}'`
        `cat Teste_linhas-Com-Erro | awk '{print $3}'`
        `cat arquivo | grep -E "palavra1|palavra2"`
        A opção `-E` descrita no grep acima é usada para fazer uma busca estendida. 
        Pode-se usar apenas egrep no lugar de grep -E que será obtido o mesmo resultado

**DIVISÃO DE UM ARQUIVO**
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