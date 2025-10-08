### Datenbank
- Typen
	- Mongodb
	- SQL
- Struktur
	- Haupt Table mit Verlinkung zu fragen
		- ID
		- Name
		- Verlinkung
	- Pro Fragenset ein table
		- ID
		- Frage
		- Antworten seperiert von | 
		- Richtig seperiert von |

```mermaid
erDiagram
	GAME {
	}
	
	QUIZ {
		int id PK
		String name
	}
	
	FRAGEN {
		int id PK
		int q_id FK
		String frage
		String antworten
		String Correkt
	}
	
	SPIELER {
	}
	
	GAME ||--|| QUIZ : hat
	GAME ||--o{ SPIELER : hat
	QUIZ ||--o{ FRAGEN : hat
```

