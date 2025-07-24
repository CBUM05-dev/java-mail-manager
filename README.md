# MailManager

MailManager is a Java-based email management application designed to provide features typically missing from standard email services (Gmail, Yahoo, Hotmail, etc.), such as automatic classification, mailing lists, XML archiving, advanced search, multi-account handling, and mobile communication (SMS/Email).

## Key Features
- Send and receive emails (IMAP/SMTP)

- Mailing list management for grouped and scheduled sending

- Automatic classification of messages (spam, priority)

- XML archiving and multi-criteria search

- Multi-account email support

- Mobile notifications (SMS and push)

## Requirements

- Java 8 or higher

- External libraries (JAR files) in the lib/ folder: JavaMail, SMS API, etc.

- Accessible IMAP/SMTP server for email services

## Installation
1. Clone the repository:

\`\`\`bash
   git clone https://votre-repo/MailManager.git
   \`\`\`

2. Compile the project:

\`\`\`bash
   javac -cp "lib/*" -d out src/java/com/mailmanager/**/*.java
   \`\`\`
   
## Project Structure
\`\`\`text
├── .gitignore
├── README.md                              ← Fichier de documentation
├── lib/                                   ← JAR externes (JavaMail, SMS API…)
└── src/
    └── java/
        └── com/mailmanager/
            ├── MailManagerApp.java        ← Point d’entrée de l’application
            │
            ├── email/                      ← Tâche 1 : Envoi & réception
            │   ├── EmailReceiverService.java  ← réception des emails
            │   ├── EmailSenderService.java    ← envoi des emails
            │   └── EmailClient.java           ← connexion IMAP/SMTP
            │
            ├── mailing/                    ← Tâche 2 : Listes de diffusion
            │   ├── MailingListService.java
            │   └── SubscriberService.java
            │
            ├── classification/            ← Tâche 3 : Classification automatique
            │   ├── SpamClassifier.java
            │   └── PriorityClassifier.java
            │
            ├── archive/                   ← Tâche 4 : Archivage & recherche
            │   ├── ArchiveService.java
            │   └── SearchService.java
            │
            ├── accounts/                  ← Tâche 5 : Multi-boîtes email
            │   └── AccountService.java
            │
            ├── notification/              ← Tâche 6 : Notification mobile
            │   ├── SMSService.java
            │   └── PushNotificationService.java
            │
            └── util/                      ← Outils partagés
                ├── ConfigLoader.java
                └── LogManager.java
\`\`\`

## Running the Application

\`\`\`bash
java -cp "lib/*:out" com.mailmanager.MailManagerApp
\`\`\`

## License
This project is licensed under the MIT License.
