# Permissões Linux

As informações sobre permissões são listadas nos primeiros caracteres da saída ls –l.

O primeiro caractere, indica que se trata de um arquivo ou diretório, se tiver um `d` refere-se a um diretório. 

Há três tipos de permissões

r - leitura
w - escrita
x - execução

O primeiro conjunto de três caracteres representa as permissões do **dono do arquivo**; 
O segundo conjunto de três caracteres representa as permissões do **grupo**;
E o terceiro conjunto de três caracteres representa as permissões dos **outros usuários**.

As permissões são dadas para cada grupo :: [dono][grupo][outrosUsuarios] 

Podendo ser diferentes para cada grupo 

`chmod +x <programa>`

Fornece a todos os usuários poderão executar o programa. 
Também pode ser executado o `+r` e o `+w`;

Remove de todos os usuários e grupos a permissão de execução. 
Também pode ser executado –r e -w 

`chmod o-rx`  

Remove dos "outros usuários" as permissões de read e execute 

Para remover as permissões do usuário dono: u 
Para remover as permissões do grupo de usuários: g 

Para remover as permissões de um arquivo/diretório, é preciso estar logado como o dono do arquivo/diretório que terá as permissões alteradas. 