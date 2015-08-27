IT4biz Training
========

##Tradução do Pentaho:
http://community.pentaho.com/marketplace/language-packs/
https://github.com/webdetails/pentahoLanguagePacks
http://blog.professorcoruja.com/2009/06/traducao-pentaho-bi-server-20-e-30-para.html
https://code.google.com/p/brazilianportuguesetranslationofpentaho/

##Pentaho Marketplace
https://github.com/pentaho/marketplace-metadata
https://github.com/pentaho/marketplace-metadata/blob/master/marketplace.xml

##Links Mondrian:
http://sourceforge.net/projects/mondrian/

##Infos:

##BI Server 5.0.1
http://localhost:8080/
user: admin
password: password

Administration
Home -> Administration

##Pentaho BI Server 5.0.1CE MySQL installation guide
http://anonymousbi.wordpress.com/2013/12/15/pentaho-bi-server-5-0-1ce-mysql-installation-guide/

##Personalização básica para colocar em produção
https://github.com/it4biz/training/blob/master/pentaho-5.0-personalizacao.txt
http://www.science.co.il/Language/Locale-codes.asp

##Links visualizadores OLAP:

###Saiku Chart Plus
http://it4biz.github.io/SaikuChartPlus/

###Saiku
http://meteorite.bi/saiku

###Pivot4J
http://mysticfall.github.io/pivot4j/
http://www.pivot4j.org/

###Pivot
http://jpivot.sourceforge.net/

###STPivot
https://code.google.com/p/stpivot/

###OLAP4J
http://www.olap4j.org/


##Como logar sem pedir usuario e senha no Pentaho BI Server 5.0.1?

Até a versão 4.8 funciona colocar userid=admin&password=password em qualquer URL.

A partir da versão 5.0.1 somente é aceito na página Home conforme exemplo abaixo:
Home aceita
http://localhost:8080/pentaho/Home?userid=admin&password=password

Direto no Relatório não aceita userid e password
http://172.16.1.6:8080/pentaho/api/repos/:public:IT4biz:Reports:ClientsReport.prpt/viewer?ts=1390324489461&userid=admin&password=password

Infos:
http://jira.pentaho.com/browse/BISERVER-10354
http://jira.pentaho.com/browse/BISERVER-10708


## MDX

```
 select NON EMPTY(TopCount({Descendants([Produto].[Todos] ,[Produto].[Nome do Produto])}, 5, [Measures].[Valor])) on ROWS,
 NON EMPTY({[Measures].[Valor]}) on Columns
 from [Vendas]
 WHERE {${filtroAnoVendasParameter}}

```

```
export CATALINA_OPTS="-Xms2g -Xmx2g -XX:MaxPermSize=256m -Dsun.rmi.dgc.client.gcInterval=3600000 -Dsun.rmi.dgc.server.gcInterval=3600000"
```

## Recomendações Pentaho (Hardware)
http://infocenter.pentaho.com/help/index.jsp?topic=%2Fsupported_components%2Freference_supported_components.html

##Alterar a versão do JDK no Mac OX
export JAVA_HOME=$(/usr/libexec/java_home -v 1.7)

https://coderwall.com/p/esa4sg

Pentaho Plug-ins (Obrigatórios)
Pentaho Marketplace
Community Dashboards Framework
Community Data Access
Community Dashboard Editor
Community Graphics Generator
Sparkl - Pentaho Application Builder
Saiku Analytics
Saiku Chart Plus


Recomendados
D3 Component Library
Pivot4J Analytics
Change Password
Portuguese (Brazilian variant) Language Pack Installer

-i = case insensitive
ps -ef | grep -i pentaho

##SQLeonardo
http://sqleonardo.altervista.org/index.htm

##PRD with MongoDB
http://wiki.pentaho.com/display/BAD/Create+a+Report+with+MongoDB

## Mondrian Documentation
http://mondrian.pentaho.com/documentation/xml_schema.php

hideMemberIf	String	Never	 Condition which determines whether a member of this level is hidden. If a hierarchy has one or more levels with hidden members, then it is possible that not all leaf members are the same distance from the root, and it is termed a ragged hierarchy.
Allowable values are: Never (a member always appears; the default); IfBlankName (a member doesn't appear if its name is null, empty or all whitespace); and IfParentsName (a member appears unless its name matches the parent's.


IBM InfoSphere DataStage
http://www-03.ibm.com/software/products/pt/ibminfodata

dtCarga (Campo utilizado para saber quando foi feito a carga)

SQL Server
select
getDate() as dtCarga
from suaTabela

PostgreSQL
select
now() as dtCarga
from nomeesquema.nometabela


SELECT p.intProcessoId
      ,dtaAbertura
      , convert(datetime,convert(varchar, dtaAbertura,103),103) as dtaAberturaConvertida
      ,p.intMunicipioComarcaId



##Pentaho BIServer api doc
http://javadoc.pentaho.com/bi-platform500/webservice500/index.html



1) JDK 1.7

Instalar JDK 1.7 da Oracle e Configurar a variável JAVA_HOME.

Ver video de como instalar o JDK 1.6, favor instalar o JDK 1.7

https://www.youtube.com/watch?v=9hnmyQUYbro

OBS: NÃO INSTALAR O JDK 1.8!!!

2) PostgreSQL 9.3 ou superior

http://www.postgresql.org/download/

3) Descarregar e descompactar os arquivos

Pentaho BI Server 5.3 Stable
http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.3/biserver-ce-5.3.0.0-213.zip/download

PRD 5.3.0 Stable
http://sourceforge.net/projects/pentaho/files/Report%20Designer/5.3/prd-ce-5.3.0.0-213.zip/download

PDI 5.3 Stable
http://sourceforge.net/projects/pentaho/files/Data%20Integration/5.3/pdi-ce-5.3.0.0-213.zip/download

PSW 3.9.0 Stable
http://sourceforge.net/projects/mondrian/files/schema%20workbench/3.9.0/psw-ce-3.9.0.0-213.zip/download

PAD 5.3.0 Stable
http://sourceforge.net/projects/mondrian/files/aggregation%20designer/5.3/pad-ce-5.3.0.0-213.zip/download


```

{
    "emptyTable":"Não há dados disponíveis",
    "info":"Mostrando _START_ a _END_ de _TOTAL_ registros",
    "infoEmpty":"Mostrando 0 a 0 de 0 registros",
    "infoFiltered":"(filtrado de _MAX_ registros)",
    "infoPostFix":"",
    "thousands":".",
    "lengthMenu":"Mostrar _MENU_ registros",
    "loadingRecords":"Carregando...",
    "processing":"Processando...",
    "search":"Filtro:",
    "zeroRecords":"Nenhum registro encontrado",
    "paginate": {
        "first":"Primeiro",
        "last":"Último",
        "next":"Próximo",
        "previous":"Anterior"
    }
}

```

## SQL Query 

```
SELECT
     "dw"."dim_produtos"."desc_produto",
     SUM("dw"."fato_vendas"."m_valor") as soma_valor_vendas
FROM
     "dw"."fato_vendas" 
INNER JOIN "dw"."dim_produtos"
	ON "dw"."dim_produtos"."sk_produto" = "dw"."fato_vendas"."sk_produto"  
GROUP BY
	"dw"."dim_produtos"."desc_produto"
ORDER BY
	2 DESC

```

## MDX Query w/ Filter

```
WITH
SET [~FILTER] AS
    {${filter_productParameter}}
SET [~ROWS] AS
    {[Clientes.Cliente].[Nome do Cliente].Members}
SELECT
NON EMPTY {[Measures].[Valor]} ON COLUMNS,
NON EMPTY [~ROWS] ON ROWS
FROM [Vendas com o PSW]
WHERE [~FILTER]
```

## Consulta SQL Vendas por Produto filtrando por cliente

```

SELECT
     "dw"."dim_produtos"."desc_produto",
     SUM("dw"."fato_vendas"."m_valor") as soma_valor_vendas
FROM
     "dw"."fato_vendas" 
INNER JOIN "dw"."dim_produtos"
	ON "dw"."dim_produtos"."sk_produto" = "dw"."fato_vendas"."sk_produto"  
WHERE 	
     "dw"."fato_vendas"."sk_clientes" = ${p_cliente}
GROUP BY
	"dw"."dim_produtos"."desc_produto"
ORDER BY
	2 DESC

```

## Consulta SQL com os Clientes
```

SELECT
    distinct "dw"."dim_clientes"."nome_cliente",
    "dw"."dim_clientes"."sk_clientes"
FROM
     "dw"."dim_clientes" 
order by 1

```


## Consulta SQL Produtos, Clientes, Estado, Cidade e Valor


```

SELECT
     "dw"."dim_produtos"."desc_produto",
     "dw"."dim_clientes"."nome_cliente",
     "dw"."dim_clientes"."estado",
     "dw"."dim_clientes"."cidade",
     SUM("dw"."fato_vendas"."m_valor") as soma_valor_vendas
FROM
     "dw"."fato_vendas" 
INNER JOIN "dw"."dim_produtos"
    ON "dw"."dim_produtos"."sk_produto" = "dw"."fato_vendas"."sk_produto"  
INNER JOIN "dw"."dim_clientes"
    ON "dw"."dim_clientes"."sk_clientes" = "dw"."fato_vendas"."sk_clientes"  
GROUP BY
      "dw"."dim_produtos"."desc_produto"
    , "dw"."dim_clientes"."nome_cliente"
    , "dw"."dim_clientes"."estado"
    , "dw"."dim_clientes"."cidade"
ORDER BY
    5 DESC
    
    
```


	
## Tipos de FormatString	

```
#,###;(#,###)
#,###.00;(#,###.00)
¤ #,###;(¤ #,###)
¤ #,###.00;(¤ #,###.00)
#.#%;(#.#%)
MMM-dd-yyyy
MM-dd-yy
yyyy-MMM-dd
yy-MM-dd

```

