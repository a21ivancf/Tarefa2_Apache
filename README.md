Necesitaremos ter un nome  DNS. 

Configuramos un servidor virtual para www.omeusitio.lan. Descomprime o arquivo omeusitio.lan.tar.gz en  e fai que se monte en /opt/web/oumeusitio.lan

A configuración do host virtual é a seguinte:

1. O directorio raíz de documentos debe ser /opt/web/omeusitio.lan/htdocs, e debe permitir o uso de ficheiros .htaccess relacionados coa autenticación e información de ficheiros. Tamén queremos habilitar a opción para amosar un listado do contido do directorio no caso de se introduza un directorio na URL e que non exista ningún dos ficheiros especificados como de procura nese caso. Indica cal é a configuración do sitio virtual e explícaa detalladamente.

    !["imaxen"](./images/ej1/ej1.1.png)

    !["imaxen"](./images/ej1/ej1.2.png)

2. No directorio imaxes, queremos permitir so que se descarguen os ficheiros con extensións .jpg, jpeg, bmp, gif, png e tiff. Todos os demais deberían esta bloqueados.  Explica o resultado obtido unha vez accedido cun navegador web á URL http://www.omeusitio.lan/imaxes tendo en conta o contido do directorio imaxes. Comproba se se pode acceder explicitamente ao ficheiro .pdf que hai dentro dese directorio.

    !["imaxen"](./images/ej2/ej2.1.png)

    !["imaxen"](./images/ej2/ej2.2.png)

    !["imaxen"](./images/ej2/ej2.3.png)

    !["imaxen"](./images/ej2/ej2.4.png)

    !["imaxen"](./images/ej2/ej2.5.png)

    !["imaxen"](./images/ej2/ej2.6.png)

    !["imaxen"](./images/ej2/ej2.7.png)

    !["imaxen"](./images/ej2/ej2.8.png)

3. No directorio datos queremos bloquearlle o acceso aos clientes que teñan enderezo na rede 192.168.58.128/25 mediante ficheiros .htaccess. Indica o contido dese ficheiro, e tamén comproba con un cliente dentro desa subrede e outro fora se se pode acceder ou non a ese directorio.

    !["imaxen"](./images/ej3/ej3.1.png)

    !["imaxen"](./images/ej3/ej3.2.png)

    !["imaxen"](./images/ej3/ej3.3.png)

    !["imaxen"](./images/ej3/ej3.4.png)

    !["imaxen"](./images/ej3/ej3.5.png)

4. No directorio traballadores, queremos habilitar a autenticación Basic, e para elo crearemos os usuarios ana e eva. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Amosa a configuración, a ventá de acceso no navegador e a liña do log onde se ve o nome do usuario que fixo login.

    !["imaxen"](./images/ej4/ej4_1.png)

    !["imaxen"](./images/ej4/ej4_2.png)

    !["imaxen"](./images/ej4/ej4_3.png)

    !["imaxen"](./images/ej4/ej4_4.png)

    !["imaxen"](./images/ej4/ej4_5.png)

    !["imaxen"](./images/ej4/ej4_6.png)

    !["imaxen"](./images/ej4/ej4_7.png)

5. No directorio directivos, queremos habilitar a autenticación Digest, e para elo crearemos os usuarios xan e lois. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Escolleremos como nome de dominio (realm) “directivos”. Amosa a configuración, a ventá de acceso no navegador e a liña do log onde se ve o nome do usuario que fixo login.

6. No directorio contas, usando ficheiros .htaccess, queremos permitir o acceso a certos grupos de usuarios usando autenticación Basic. Gardaremos a lista de usuarios nun ficheiro en /opt/web/omeusitio.lan/ que debería ter un nome que impida ser accedido accidentalmente. Poderán acceder o usuario manolo e os membros do grupo directivos (matias, anton) que sexan a súa vez membros do grupo accionistas (anton, maría, olga) e que non sexan a súa vez membros do grupo temporais (matias, olga, xaime)

7. Indica como se faría para impedirlle o acceso á URL http://www.omeusitio.lan/secure aos clientes que teñan un enderezo IP que comece por 172.16 e aos que teñan un nome cuxo dominio sexa apache.lan

8. Indica como farías para configurar o acceso ao directorio reservado da seguinte maneira: Para poder acceder, ten que cumprirse que o usuario sexa manolo, ou pertencer ao grupo admin e máis administradores e a súa vez estar no grupo vendas ou comerciais, e que baixo ningún concepto se pertenza ao grupo temporais ou interinos ou que o enderezo IP sexa 192.168.58.99