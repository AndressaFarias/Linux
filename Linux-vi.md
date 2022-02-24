# Comandos vi
 [esc]      | Sai do modo de edição 

 [esc] x    | Apaga caractere atual  

 [esc] 4x   | Pode ser passado o parâmetro da quantidade de caracteres a serem deletados: 

 `$`        | Vai para o fim da linha 

 `/<string>`| <string> é a palavra que deve ser localizada 
            | n  avança para próxima ocorrência da string localizada
            | N volta para a ocorrência anterior 

`:q`        | Sai  

`:w`        | Salva

 `0`        | Vai para o início da linha 

 `a`        | Ativa a edição a partir do próximo caractere 

 `A`        |  Insere no fim da linha 

`dd`        | Apaga a linha completa (mesmo que o cursos esteja no meio da linha) 
              Tb pode ser passado por parâmetro a quantidade de linha a serem removidas

 `i`        | Ativa a edição no caractere atual 

`gg`        | Vai para o início do arquivo 

`G`         |  Vai para a última linha do arquivo

`<num> G`   | Vai para a linha indicada 

`p`         | Cola a linha 


`yy`        | Copia a linha 

`<num> yy`  | Copiar num linhas 