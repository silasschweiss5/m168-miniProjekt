# m169-miniProjekt

---

+ Als erstes habe ich das [Dockerfile](./Dockerfile) erstellt. Dabei habe ich mich extra für httpd damit ich so wenig befehl in das [Dockerfile](./Dockerfile) Schreiben muss.
+ Als nächtest habe ich das image **website** erstellt. <pre><code>docker build website . </code></pre>
+ Als Letztes habe ich den Docker gestartet: <pre><code>docker run -d --name web -p 8080:80 -v /home/vmadmin/Desktop/Logs/:usr/local/apache2/logs/ -v /home/vmadmin/Desktop/website/:usr/local/apache2/htdocs/</code></pre>
