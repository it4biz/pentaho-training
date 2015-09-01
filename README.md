###IT4biz Training

If you are here, it is because you want to learn more about Pentaho.

If so you will probably participate in a IT4biz course.

Here are the steps you need to follow to get ready to start the Training.

## Download all the softwares and unzip them all in a folder called Pentaho

If you want to download the CE(Community Edition) please go direct to sourceforge.net instead of the website Pentaho.com.

Until today (August, 11, 2015) the last stable version of Pentaho is the 5.4 version.

Downloads Pentaho BI Suite CE (Community Edition)<BR>

Links Pentaho BA Suite:<BR>
http://sourceforge.net/projects/pentaho/<BR>

BI Server 5.4.0.1-130 Stable<BR>
http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.4/biserver-ce-5.4.0.1-130.zip/download<BR>

PRD 5.4.0.1-130 Stable<BR>
http://sourceforge.net/projects/pentaho/files/Report%20Designer/5.4/prd-ce-5.4.0.1-130.zip/download<BR>

PDI 5.4.0.1-130 Stable<BR>
http://sourceforge.net/projects/pentaho/files/Data%20Integration/5.4/pdi-ce-5.4.0.1-130.zip/download<BR>

PSW 3.10.0.1-130 Stable<BR>
http://sourceforge.net/projects/mondrian/files/schema%20workbench/3.10.0/psw-ce-3.10.0.1-130.zip/download<BR>

PAD 5.4.0.1-130 Stable<BR>
http://sourceforge.net/projects/mondrian/files/aggregation%20designer/5.4/pad-ce-5.4.0.1-130.zip/download<BR>

## Install JDK 1.7

Install on your computer the JDK 1.7 and config the JAVA_HOME.

DO NOT INSTALL JDK 1.6 OR 1.8.
ONLY JDK 1.7

See the video below to help you with the installation.<BR>
https://www.youtube.com/watch?v=9hnmyQUYbro

## Install PostgreSQL 9.3 or superior

Download PostgreSQL in the link below:<BR>

http://www.postgresql.org/download/<BR>


## pentahoLanguagePacks

Visit the links below to learn more about it.<BR>

http://community.pentaho.com/marketplace/language-packs/<BR>

https://github.com/webdetails/pentahoLanguagePacks<BR>

http://blog.professorcoruja.com/2009/06/traducao-pentaho-bi-server-20-e-30-para.html<BR>

https://code.google.com/p/brazilianportuguesetranslationofpentaho/<BR>

## Pentaho Marketplace

https://github.com/pentaho/marketplace-metadata<BR>

## Infos:

BA Server 5.4.0.1-130<BR>
http://localhost:8080/<BR>
user: admin<BR>
password: password<BR><BR>

Administration<BR>
Home -> Administration<BR>

##OLAP viewer

Saiku Chart Plus<BR>
http://it4biz.github.io/SaikuChartPlus/<BR>

Saiku<BR>
http://meteorite.bi/saiku<BR>

Pivot4J<BR>
http://mysticfall.github.io/pivot4j/<BR>
http://www.pivot4j.org/<BR>

Pivot<BR>
http://jpivot.sourceforge.net/<BR>

STPivot<BR>
https://code.google.com/p/stpivot/<BR>

OLAP4J<BR>
http://www.olap4j.org/<BR>

Hardware recommendations for the Pentaho Server<BR>
http://infocenter.pentaho.com/help/index.jsp?topic=%2Fsupported_components%2Freference_supported_components.html

##Pentaho Plug-ins (Mandatory)
* Pentaho Marketplace
* Community Dashboards Framework
* Community Data Access
* Community Dashboard Editor
* Community Graphics Generator
* Sparkl - Pentaho Application Builder
* Saiku Analytics
* Saiku Chart Plus
* Pentaho CE Audit
* Pentaho Performance Monitoring

##Pentaho Plug-ins (recommended)
* D3 Component Library
* Pivot4J Analytics
* Change Password
* Portuguese (Brazilian variant) Language Pack Installer

##Pentaho BIServer api doc
http://javadoc.pentaho.com/bi-platform500/webservice500/index.html

## Pentaho CE 5.4 on production with PostgreSQL

https://github.com/wmarinho/docker-pentaho<BR>
https://github.com/wmarinho/pentaho5-installer<BR>
http://forums.pentaho.com/showthread.php?165218-Pentaho-Rapid-Deployment-with-Docker<BR>
https://www.rowellbelen.com/docker-pentaho-ba-server-ce/<BR>
https://hub.docker.com/r/bytekast/docker-pentaho-ce-5.3/<BR>
https://hub.docker.com/r/wmarinho/pentaho-biserver/<BR>

## Proxy / BI Server

Add -Dhttp.proxyHost=proxy.trt7.local -Dhttp.proxyPort=9090 -Dhttps.proxyHost=proxy.trt7.local -Dhttps.proxyPort=9090

```
IF "%BITS%" == "64" (
  set CATALINA_OPTS=-Xms3g -Xmx3g -XX:MaxPermSize=256m -Dsun.rmi.dgc.client.gcInterval=3600000 -Dsun.rmi.dgc.server.gcInterval=3600000 -Dhttp.proxyHost=proxy.trt7.local -Dhttp.proxyPort=9090 -Dhttps.proxyHost=proxy.trt7.local -Dhttps.proxyPort=9090
) ELSE (
  set CATALINA_OPTS=-Xms3g -Xmx3g -XX:MaxPermSize=256m -Dsun.rmi.dgc.client.gcInterval=3600000 -Dsun.rmi.dgc.server.gcInterval=3600000 -Dhttp.proxyHost=proxy.trt7.local -Dhttp.proxyPort=9090 -Dhttps.proxyHost=proxy.trt7.local -Dhttps.proxyPort=9090
)

```

## Change Port / BI Server

Edit the file biserver-ce-5.4.0.1-130\biserver-ce\tomcat\conf\server.xml


```
	<!-- porta alterada de 8080 para 80 -->
	
    <Connector URIEncoding="UTF-8" port="80" protocol="HTTP/1.1" 
               connectionTimeout="20000" 
               redirectPort="8443" />

```

Edit the file \biserver-ce-5.4.0.1-130\biserver-ce\tomcat\webapps\pentaho\WEB-INF\web.xml


```

  <context-param>
    <param-name>fully-qualified-server-url</param-name>
    <param-value>http://localhost/pentaho/</param-value>
  </context-param>
  

```

## DW Config 


```
#DW Config
DW_HOST=localhost
DW_DATABASE=dw
DW_PORT=5432
DW_USERNAME=postgres
DW_PASSWORD=Encrypted 2be98afc78aa7f2e21a1da345d078bdce

```
## Matt Casters talking about PDI/Kettle at FEA/USP
http://www.portalfea.fea.usp.br/videos/o-comeco-de-tudo-pentaho-data-integration-parte-4

http://www.portalfea.fea.usp.br/videos/pentaho-day-2014-parte-1
