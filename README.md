IT4biz Training
========

Updated: 20 Jan 2014

Downloads Pentaho BI Suite

Links Pentaho:
http://sourceforge.net/projects/pentaho/

PRD 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Report%20Designer/5.0.1-stable/

PDI 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Data%20Integration/5.0.1-stable/

PME 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Pentaho%20Metadata/5.0.1-stable/

BI Server 5.0.1 Stable
http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.0.1-stable/

PSW 3.6.1 Stable
http://sourceforge.net/projects/mondrian/files/schema%20workbench/3.6.1-stable/

PAD 5.0.1 Stable
http://sourceforge.net/projects/mondrian/files/aggregation%20designer/5.0.1-stable/

PDS 4.0.0 Stable
http://sourceforge.net/projects/pentaho/files/Design%20Studio/4.0.0-stable/

Links Mondrian:
http://sourceforge.net/projects/mondrian/

Mondrian 3.6.1
http://sourceforge.net/projects/mondrian/files/mondrian/mondrian-3.6.1/

Infos:

BI Server 5.0.1
http://localhost:8080/
user: admin
password: password

Administration
Home -> Administration

Pentaho BI Server 5.0.1CE MySQL installation guide
http://anonymousbi.wordpress.com/2013/12/15/pentaho-bi-server-5-0-1ce-mysql-installation-guide/

Personalização básica para colocar em produção
1) Alterar o logo da página inicial do BI Server 5.0.1

Na pasta:
biserver-ce-5.0.1-stable/biserver-ce/pentaho-solutions/system/common-ui/resources/themes/images/

Edite a imagem:
puc-login-logo.png

Caminho completo (Arquivo):
biserver-ce-5.0.1-stable/biserver-ce/pentaho-solutions/system/common-ui/resources/themes/images/puc-login-logo.png

Caminho completo (Web):
http://localhost:8080/pentaho/content/common-ui/resources/themes/images/puc-login-logo.png

Reiniciar o BI Server caso necessário.

2) Remover o Botão Login as an Evaluator

Na pasta:
biserver-ce-5.0.1-stable/biserver-ce/tomcat/webapps/pentaho/jsp

Editar o arquivo PUCLogin.jsp

Comentar o código abaixo:

<code>

<div id="eval-users-toggle-container">
            <%
              if (showUsers) {
            %>
            <div id="eval-users-toggle" onClick="toggleEvalPanel()">
              <div><%=Messages.getInstance().getString("UI.PUC.LOGIN.EVAL_LOGIN")%></div>
                <div id="eval-arrow" class="closed"></div>
            </div>

            <%
            } else {
            %>
            &nbsp;
            <%
              }
            %>
</div>

</code>

Ficando:

<code>
<!--		  
		  IT4biz - Remove o Botão Login as an Evaluator
		  
          <div id="eval-users-toggle-container">
            <%
              if (showUsers) {
            %>
            <div id="eval-users-toggle" onClick="toggleEvalPanel()">
              <div><%=Messages.getInstance().getString("UI.PUC.LOGIN.EVAL_LOGIN")%></div>
                <div id="eval-arrow" class="closed"></div>
            </div>

            <%
            } else {
            %>
            &nbsp;
            <%
              }
            %>
          </div>

-->

</code>

Não é necessário reiniciar

3) Editar a imagem de fundo da tela de login:

/Applications/Pentaho/biserver-ce-5.0.1-stable/biserver-ce/pentaho-solutions/system/common-ui/resources/themes/crystal

arquivo:
login-crystal-bg.jpeg

4) Alterar a tela interna (Home)

biserver-ce-5.0.1-stable/biserver-ce/tomcat/webapps/pentaho/mantle/home/content/welcome/index.html

Ou 

biserver-ce-5.0.1-stable/biserver-ce/tomcat/webapps/pentaho/mantle/home/index.jsp


http://www.science.co.il/Language/Locale-codes.asp

Links visualizadores OLAP:

Saiku Chart Plus
http://it4biz.github.io/SaikuChartPlus/

Saiku
http://meteorite.bi/saiku

Pivot4J
http://mysticfall.github.io/pivot4j/
http://www.pivot4j.org/

Pivot
http://jpivot.sourceforge.net/

STPivot
https://code.google.com/p/stpivot/

OLAP4J
http://www.olap4j.org/

http://www.science.co.il/Language/Locale-codes.asp


          
          


