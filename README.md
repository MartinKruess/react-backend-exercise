# React Webseite, Backend API´s und MongoDB

## Einleitung

In dieser Übung geht es darum die bisher gerlernten Backend-Skills mit einem frontend zu verbinden. Das Lesen und Schreiben von Daten in Verbindung mit einem Login gehört zu den Grundlagen vieler Webseiten.

Der Übungsaufbau wird wie folgt sein:
Diese Aufgabe sollte nicht länger als 3h dauern.
Ihr fangt alleine oder in gruppen an an der Aufgabe zu arbeiten.
Ein wichtiger Punkt ist es, dass ihr versucht alleine anzufangen ohne jegliche Hilfe.
Nach 30 Minuten würde ich im Hauptraum für Fragen und Livecoding zur Verfügung stehen.

## Backend (geschätzt: 30-45 min)

- Erstelle ein NodeJS Backend mit Express, Cors und Mongoose
- Baue eine get und eine Post API für `articles` mit folgenden Funktionen
  - showArticles
  - addArticle
- erstelle ein allgemeines `productSchema` für die Article aus der `article.js`:
- Erstelle zusätzlich ein `articleSchema` mit den Individuellen ArticleData aus `article.js`
- Der Titel jedes Articls soll automatisch aus dem type, producer, der version und Form zusammengestezt werden Beispiel:(Kühlschrank: Miele K 12023 S-3 Standgerät)
- Teste dein Backend indem du die **ersten beiden Article** aus `article.js` mit Thunder-Client in der Datenbank speicherst und sie anschließend ausgibst

## Frontend (geschätzt: 45-1h 45 min)

- Deine Webseite sollte aus zwei Seiten bestehen, die durch eine Navigation erreichbar sind.

  - gebe im router die unterschiedlichen Pfade an
  - Seite 1 sollte beim Laden der Seite alle gespeicherten Articles aus dem backend fetchen und in Cards ausgeben (fetch im useEffect)
  - Kontrolliere ob die zwei gespeicherten Articles korrekt auf der Seite angezeigt werden

  - Seite 2 sollte ein Formular beinhalten über das neue Article in der DB gespeicht werden können (fetch onClick)
  - Füge die letzten beiden Article über das Frontend zur Datenbank hinzu und kontrolliere dies erneut auf der Startseite.

## Benötigte Skills

- useState
- useEffect
- fetch
- JSX
- CSS

## Bonus (geschätzt: 20-45 min)

Baue deine Webseite so um, dass nur ein eingeloggter User neue Article hinzufügen kann.

- Baue eine neue Seite für ein Login Formular
- Erstelle eine privatRoute für addArticle, so das nur eingeloggte Benutzer einen neuen Article anlegen können
- Überprüfe die Logindaten (password) mit bcrypt
  - Ist der User vorhanden?
  - Stimmt das passwort überein?
- Schicke ein userObject mit dem Usernamen und status: true zurück an das Frontend.
- Speichere dieses Object im useContext, damit du die Daten auch auf unterseiten verwenden kannst.
- speichere die Daten im localStorage damit die Seite auch nach einem Refresh noch funktioniert.

  ### Benötigte Skills

  - bcrypt
  - useContext
  - localStorage
  - ternary
