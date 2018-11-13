# Webseiten

Autor: Filek  
Datum: 13. November 2018

## Übersicht

Dieser Artikel enthält technische Informationen zu folgenden Webseiten:

1. Marketing-Seite <https://www.manessia.ch/>
2. Info-Seite <https://info.manessia.ch/>
3. Knowledge-Base <https://kb.manessia.ch/>

## Marketing-Seite (publik)

Die öffentliche [Manessia-Marketingseite](https://www.manessia.ch/) dient der Information und zur Anwerbung des interessierten Publikums und beruht auf folgendem Stack:

- Jekyll als static site generator. Der Code ist unter version control auf Fileks privatem [Github-Repo](https://github.com/thiemo/manessia-jekyll) abgelegt.
- Deployment via Netlify. Ein push in das master repo löst einen page build und deployment aus.
- Der dynamische Veranstaltungskalender ist fremdgehosted bei Tockify und wird auch dort gepflegt. Login bei Filek.
- Die Scripts für das call to action popup auf der Startseite sowie das Chat-Fenster werden erst beim Deployment bei Netlify in das generierte HTML eingefügt; sie können auf der Netlify-Weboberfläche editiert werden.

AH Troll managt unsere Second-Level-Domain auf Switchplus. Die Nameserver zeigen auf Netlify, dort kann der DNS für etwaige third-level-Domains und für die MX-Einträge (zeigen aktuell auf Google Apps) administiert werden (Zugangsdaten bei Filek).

## Info-Seite (intern)

Als zweites gibt es noch die "interne" Seite <https://info.manessia.ch/>, wo die Statuten, Couleurordnung, Comment, sowie Fuxenheft und (erst einige) Kanten publiziert sind. Der technische Aufbau ist wie folgt:

- vuepress als static site generator
- Github-Repo: <https://github.com/thiemo/infomanessia> (privat)
- auto deployment bei push via Netlify

Ein Passwortschutz ist nicht implementiert, momentan ist es eine "authentification by obscurity": Die Subdomain ist nicht publik und die robots.txt verbietet den Suchmaschinencrawlern ein indexieren. Dies ist zwar unbefriedigend, aber ein basic auth bei Netlify würde mit ca 20 Dollar pro Jahr zu Buche schlagen.

## Knowledge Base (intern)

Als drittes gibt es die Knowledge-Base, die du gerade liest, <https://kb.manessia.ch/>, basierend auf dem static site tool MkDocs.