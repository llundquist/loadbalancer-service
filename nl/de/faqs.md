---

copyright:
  years: 2017
lastupdated: "2017-08-21"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Häufig gestellte Fragen (FAQs)

Dieser Abschnitt enthält Antworten auf einige häufig gestellte Fragen zum IBM Bluemix-Service für die Lastausgleichsfunktion. 

## Wie viele virtuelle Ports können mit dem Service für die Lastausgleichsfunktion maximal definiert werden? 

Beim erstmaligen Erstellen eines neuen Service für die Lastausgleichsfunktion können Sie bis zu zwei virtuelle Ports definieren. Nach der Erstellung des Service können weitere virtuelle Ports definiert werden. Maximal sind 10 virtuelle Ports zulässig.  

## Wie viele Recheninstanzen können der Lastausgleichsfunktion maximal zugeordnet werden? 

50.

## Kann ich eine rein interne private Lastausgleichsfunktion erstellen, auf die nur von internen Clients zugegriffen werden kann?   

Derzeit ist dies nicht möglich. Dem Service, der von der IBM Bluemix-Lastausgleichsfunktion gehostet wird, ist ein vollständig qualifizierter Domänennamen zugewiesen, auf den vom öffentlichen Internet aus zugegriffen werden kann.  

## Wie lauten die Standardeinstellungen und zulässigen Werte für die unterschiedlichen Parameter für die Statusprüfung? 

Die Standardeinstellungen und zulässigen Werte werden nachfolgend aufgelistet: 

* **Intervall für Statusprüfung:** Die Standardeinstellung ist 5 Sekunden, der zulässige Bereich liegt zwischen 2 und 60 Sekunden. 
* **Antwortzeitlimit für Statusprüfung:** Die Standardeinstellung ist 2 Sekunden, der zulässige Bereich liegt zwischen 1 und 59 Sekunden. 
* **Maximale Neuversuche:** Die Standardeinstellung ist 2 Neuversuche, der zulässige Bereich liegt zwischen 1 und 10 Neuversuchen. 

**Hinweis:** Der Wert für das Antwortzeitlimit für die Statusprüfung muss immer niedriger als der interne Wert für die Statusprüfung sein.  

## Kann ich mit diesem Service Recheninstanzen verwenden, die sich in fernen Rechenzentren befinden?  

Es wird empfohlen, dass sich der Service für die Lastausgleichsfunktion und die Recheninstanzen lokal in demselben Rechenzentrum befinden. In der grafischen Benutzerschnittstelle des Service für die Lastausgleichsfunktion werden Recheninstanzen von anderen fernen Rechenzentren nicht angezeigt. In der grafischen Benutzerschnittstelle sind jedoch die Recheninstanzen aus anderen Rechenzentren in derselben Stadt eingeschlossen (also Rechenzentren, deren Namen die ersten drei Buchstaben gemeinsam haben, wie zu zum Beispiel `GERxx`). In der API-Schnittstelle können Sie jedoch Recheninstanzen in einem beliebigen fernen Rechenzentrum hinzufügen.  

## Welche TLS-Version wird mit der SSL-Auslagerung unterstützt? Welche Verschlüsselungen werden unterstützt? 

Vom Bluemix-Service für die Lastausgleichsfunktion wird TLS 1.2 mit SSL-Terminierung unterstützt.  

In der folgenden Liste werden die unterstützten Verschlüsselungen (in der Reihenfolge ihrer Priorität) aufgeführt:   

* ECDHE-RSA-AES256-GCM-SHA384 
* ECDHE-RSA-AES256-SHA384 
* DHE-RSA-AES256-GCM-SHA384 
* DHE-RSA-AES256-SHA256 
* AES256-GCM-SHA384 
* AES256-SHA256 
* ECDHE-RSA-AES128-GCM-SHA256 
* ECDHE-RSA-AES128-SHA256 
* DHE-RSA-AES128-GCM-SHA256 
* DHE-RSA-AES128-SHA256 
* AES128-GCM-SHA256 
* AES128-SHA256 

## Kann ich meine SSL-Verschlüsselungsliste anpassen? 

Derzeit ist dies nicht möglich. 

## Wie viele Instanzen des Service für die Lastausgleichsfunktion kann ich für mein Konto erstellen?  

Derzeit können Sie bis zu 20 Serviceinstanzen erstellen. Wenn Sie mehr Instanzen benötigen, wenden Sie sich an den IBM Support.  


