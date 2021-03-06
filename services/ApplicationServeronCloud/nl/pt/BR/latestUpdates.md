---

copyright:
  years: 2015, 2016

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Atualizações mais recentes
{: #latest_updates}
Última atualização: 17 de agosto de 2016
{: .last-updated}

Uma lista das atualizações mais recentes para o serviço.

## 17 de agosto de 2016: WebSphere Application
Server for {{site.data.keyword.Bluemix_notm}} atualizado

* Feito upgrade dos binários do WebSphere Application Server for Bluemix de 8.5.5.9 para 8.5.5.10
* Resolvidas as [várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window} que afetam o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}, incluindo:
  * As vulnerabilidades do Apache Struts que afetam o WebSphere Application Server e o console de administração do WebSphere Application Server Hypervisor Edition.
  * Uma potencial negação de vulnerabilidade de serviço com o IBM WebSphere Application Server ao usar serviços de SIP.
  * Várias vulnerabilidades que podem afetar o IBM HTTP Server usado pelo WebSphere Application Server.
  * Uma vulnerabilidade que permite o redirecionamento do tráfego HTTP com aplicativos CGI que pode afetar o IBM HTTP Server (IHS). Essa vulnerabilidade é conhecida como "HTTPOXY".
  * Uma vulnerabilidade de divulgação de informações no IBM WebSphere Application Server.
  * Uma potencial vulnerabilidade de restrição de segurança ao efetuar bypass no IBM WebSphere Application Server que ocorre apenas em ambientes que têm ativada a propriedade customizada HttpSessionIdReuse do contêiner de web.


## 24 de junho de 2016: atualizado o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}

* Incluída a capacidade para os clientes escolherem entre a V8.5 e a V9.0 quando você cria uma nova instância do *Traditional ND* ou do *Traditional WebSphere*.
* Feito upgrade dos binários do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} para que novas instâncias do WebSphere Application Server Liberty (Planos Core e ND) tenham o fix pack 16.0.0.2 instalado. 16.0.0.2 é o próximo fix pack depois de 8.5.5.9. A partir de 16.0.0.2, todos os recursos opcionais autorizados do Liberty suportados para esses planos são instalados por padrão.
* Tratadas [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window} que afetam o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}, incluindo:
  * Uma vulnerabilidade XML External Entity Injection (XXE) no Apache Standard Taglibs que afeta o IBM WebSphere Application Server.
  * Um potencial para segurança menor que a esperada ao usar o recurso Descoberta de API do perfil Liberty do WebSphere Application Server e os documentos do Swagger.
  * Uma vulnerabilidade potencial de divulgação de informações no Admin Center do IBM WebSphere Application Server Liberty.
  * Uma vulnerabilidade potencial de divisão de resposta HTTP no IBM WebSphere Application Server.
  * Vulnerabilidades do OpenSSL divulgadas em 3 de maio de 2016 pelo Projeto OpenSSL.

## 13 de junho de 2016: atualizado o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}

* Incluída capacidade para que os clientes construam, provisionem, gerenciem e excluam instâncias da máquina virtual por meio da criação de um aplicativo ou script que use APIs RESTful do WebSphere Application Server for Bluemix.
* Incluída função que permite que um cliente tenha um número fixo de instâncias INTERROMPIDAS com não mais de 10 endereços IP ou 64 GB de memória. Agora os clientes são cobrados por instâncias acumuladas no estado INTERROMPIDO a uma taxa reduzida de 5%.

## 26 de abril de 2016: atualizado o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}

* Tratadas [vulnerabilidades de segurança em potencial](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window} no WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} se FIPS 140-2 estiver ativado e múltiplas vulnerabilidades no Samba - incluindo Badlock.
* Integrada a manutenção de serviços diversos.

## 15 de abril de 2016: atualizado o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}

* Feito upgrade dos binários do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} de 8.5.5.8 para 8.5.5.9
* Tratada uma vulnerabilidade [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window} no Liberty for Java para IBM {{site.data.keyword.Bluemix_notm}} que afeta consumidores que usam o cliente OpenID Connect (OIDC).
* Integrada a manutenção de serviços diversos.

## 19 de fevereiro de 2016: atualizado o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}}
* Incluída uma opção para clientes com aplicativos de uso intensivo de memória para "dimensionar corretamente" seu ambiente com máquinas virtuais maiores. Os clientes podem selecionar o tamanho do recurso específico de um determinado componente do WebSphere Application Server ou de um único sistema com máquinas virtuais de até 32 GB de RAM.
* Feito upgrade dos binários do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} de 8.5.5.7 para 8.5.5.8
* Tratadas múltiplas vulnerabilidades no IBM SDK Java Technology Edition que afetam o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} que são geralmente referidas como [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}.
* Tratada uma vulnerabilidade [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window} que afeta consumidores da saída do provedor OAuth.
* Integrada a manutenção de serviços diversos.

## 11 de dezembro de 2015: o WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} foi atualizado
* O nome oficial do produto mudou de IBM Application Server on Cloud for {{site.data.keyword.Bluemix_notm}} para IBM WebSphere Application Server for
{{site.data.keyword.Bluemix_notm}}
* Incluídos novos recursos no plano do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} Network Deployment. O plano consiste em um ambiente de célula do WebSphere Application Server Network Deployment com duas ou mais máquinas virtuais. Esses novos recursos permitem que os
usuários configurem um ambiente em cluster para alta disponibilidade, failover e escalabilidade.
* Incluídos novos recursos no plano do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} Liberty Core. O plano inclui
o uso de um Liberty Collective, que é um domínio administrativo para um grupo de perfis Liberty
(servidores) e consiste em duas ou mais máquinas virtuais
* Feito upgrade dos binários do WebSphere Application Server for {{site.data.keyword.Bluemix_notm}} de 8.5.5.6 para 8.5.5.7
* Tratada uma [vulnerabilidade do Apache Commons Collections](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window} para manipular a desserialização
do objeto Java.
* Tratada uma vulnerabilidade que poderia permitir um [ataque
de divisão de resposta HTTP](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}.
* Integrada a manutenção de serviços diversos.

## 15 de outubro de 2015: Atualizado o Application Server on Cloud
* Incluídos os dois novos planos a seguir:
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* Manutenção de serviços diversos
