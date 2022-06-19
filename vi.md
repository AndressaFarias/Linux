# Comandos vi

setas       | modo de navegar no arquivo

`i`         | Ativa a edição no caractere atual 

[esc]       | Sai do modo de edição

`:w`        | Salva

`:q`        | Sai

`a`         | Ativa a edição a partir do próximo caractere 

[esc] x     | Apaga caractere atual

[esc] 4 x   | Pode ser passado o parâmetro da quantidade de caracteres a serem deletados: 

`dd`        | Apaga a linha completa (linha em que o cursor está, mesmo que le esteja no meio da linha) 
              Tb pode ser passado por parâmetro a quantidade de linha a serem removidas

`A`         |  Insere no fim da linha 

`G`         | Vai para a últiam linha do arquivo

`0 G`        | Vai para a linha 0 do arquivo - `5G`vai para a linha 5 do arquivo

`$`         | Vai para o fim da linha;

`0`         | Vai para o início da linha;

 `/<string>`| <string> é a palavra que deve ser localizada 
            | `n` avança para próxima ocorrência da string localizada
            | `N` volta para a ocorrência anterior 

`yy`        | copia a linha inteira

`<num> yy`  | copia <num>

`p`         | cola a linha

`<num> p>`  | irá colar <num> vezes o conteudo copiado

