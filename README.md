# m169-miniProjekt

---

+ Als erstes habe ich das [Dockerfile](./Dockerfile) erstellt. Dabei habe ich mich extra für httpd damit ich so wenig befehl in das [Dockerfile](./Dockerfile) Schreiben muss.

+ Als nächtest habe ich das image **website** erstellt. <pre><code>docker build -t website . </code></pre>

+ Als nächstes habe ich auf dem Desktop den Ordner **Logs** erstellt(für die Container Log Dateien) zudem habe ich meine Webseite aus dem ersten Lehrjahr in einem Ordner auf dem Desktop namens **website** gespeichert.

+ Als Letztes habe ich den Docker gestartet: <pre><code>docker run -d --name web -p 8080:80 -v /home/vmadmin/Desktop/Logs/:usr/local/apache2/logs/ -v /home/vmadmin/Desktop/website/:usr/local/apache2/htdocs/</code></pre> 
    + -d = Starte den Container im Hintergrund
    + --name = definiert den Namen des Container
    + -p = Leitet den Port 8080 auf Container
    + -v:
        + 1: Verbindet den **Logs** Ordner auf dem Desktop mit dem im Conatiner
        + 2: Verbindet den **website** Ordner auf dem Desktop mit dem Ordner **htdocs** im Conatiner

+ Mit dem Browser und unter **localhost:8080** kann man nun auf den Container und die Webseite zugreifen.
