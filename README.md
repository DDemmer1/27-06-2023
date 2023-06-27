# 27-06-2023
SS23 - Maven

### 📝 Aufgabe:

In dieser Aufgabe wird der Umgang mit Maven geübt. Dazu wird ein einfaches Email-Programm erstellt.


- Erstellt in Eclipse ein neues ```Maven Project```
- Fügt ```Simple Java Mail``` als dependency in eure ```pom.xml``` ein
```
  <dependency>
    <groupId>org.simplejavamail</groupId>
    <artifactId>simple-java-mail</artifactId>
    <version>8.1.2</version>
  </dependency>
```


- Sendet euch selbst eine Email (z.B an eure uni-mail) anhand des "Basic Usage" Beispiels in der [Simple Java Mail Doucumentation](https://www.simplejavamail.org/features.html#section-basic-usage)
- [Infos zum Uni Mail Server](https://rrzk.uni-koeln.de/accounts-kommunikation/e-mail/e-mail-einstellungen)
- 💡 Wenn ihr mit einem VPN im Uni Netz seit könnnt ihr dazu diesen smtp server ohne Login verwenden (ansonsten ist ein Login mit euren smail Daten notwendig)
   - Server: smtp.uni-koeln.de 
   - Port: 25

```
Email email = EmailBuilder.startingBlank()
    .from("Michel Baker", "m.baker@mbakery.com")
    .to("mom", "jean.baker@hotmail.com")
    .to("dad", "StevenOakly1963@hotmail.com")
    .withSubject("My Bakery is finally open!")
    .withPlainText("Mom, Dad. We did the opening ceremony of our bakery!!!")
	.withHTMLText("<p>Mom, Dad. We did the opening ceremony of <strong>our bakery</strong>!!!</p>")
    .buildEmail();

MailerBuilder
  .withSMTPServer("server", 25, "username", "password")
  .buildMailer()
  .sendMail(email);
```



### ℹ️ Resourcen:
Hier noch ein paar nützliche 📃Artikel, 🖊️Threads und 🎥Videos

- [📃 Simple Java Mail](https://www.simplejavamail.org/features.html#section-basic-usage)
- [📃 Maven Repository - Set compiler source](https://maven.apache.org/plugins/maven-compiler-plugin/examples/set-compiler-source-and-target.html)
