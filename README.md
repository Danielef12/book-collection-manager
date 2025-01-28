# Book Collection Manager 📚

**Book Collection Manager** è una semplice applicazione web sviluppata con Flask che consente agli utenti di gestire una collezione di libri. Questo progetto include funzionalità per aggiungere, modificare e rimuovere libri, ed è stato pensato come esempio pratico per esplorare Flask, SQLAlchemy e operazioni CRUD.

---

## Funzionalità principali 🌟
- **Visualizza la lista dei libri**: Mostra tutti i libri salvati nel database con i relativi dettagli (titolo, autore, valutazione).
- **Aggiungi un libro**: Modulo semplice per inserire nuovi libri nella collezione.
- **Modifica la valutazione di un libro**: Possibilità di aggiornare la valutazione di un libro esistente.
- **Elimina un libro**: Funzionalità per rimuovere un libro dalla collezione.

---



## Tecnologie utilizzate 🛠️
- **Flask**: Framework web leggero e flessibile.
- **Flask-SQLAlchemy**: Estensione di Flask per l'integrazione con il database.
- **SQLAlchemy ORM**: Per definire e interagire con il modello di database.
- **SQLite**: Database leggero per la persistenza dei dati.
- **HTML**: Per il rendering delle pagine tramite template.

---

---

## Come eseguire il progetto 🚀

1. **Clona il repository**:
    ```bash
    git clone https://github.com/Danielef12/book-collection-manager.git
    cd book-collection-manager
    ```

2. **Crea un ambiente virtuale e installa le dipendenze**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # Su Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3. **Avvia l'applicazione**:
    ```bash
    python app.py
    ```

4. **Apri nel browser**:
    Visita [http://127.0.0.1:5000](http://127.0.0.1:5000).

---

## Esempio di codice

Ecco come è stato definito il modello per la tabella `Book` utilizzando SQLAlchemy ORM:

```python
class Book(db.Model):
    id: Mapped[int] = mapped_column(Integer, primary_key=True)
    title: Mapped[str] = mapped_column(String(250), unique=True, nullable=False)
    author: Mapped[str] = mapped_column(String(250), nullable=False)
    rating: Mapped[float] = mapped_column(Float, nullable=False)
```
## Obiettivi didattici 🎯
Questo progetto è stato sviluppato per:

- Approfondire l'uso di Flask e SQLAlchemy.
- Imparare a creare applicazioni CRUD (Create, Read, Update, Delete).
- Gestire l'interazione con un database relazionale.
- Utilizzare template HTML per il rendering dinamico delle pagine.

