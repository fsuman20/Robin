<div align="center">
    <img src="https://github.com/user-attachments/assets/c1c60261-dc4f-4ab1-9155-ac0ff9e472f5" alt="Bez naslova (1500 x 1125 piks)" width="500"/>
</div>


# ROBIN

Ovaj projekt se fokusira na izradu i implementaciju chatbot sustava temeljenog na velikim jezičnim modelima (LLM) u okviru Fakulteta organizacije i informatike (FOI), specifično za preddiplomske studije. Projekt uključuje razvoj i evaluaciju modela, te njihovu moguću integraciju u aplikacijsko okruženje.

## Uvod

ROBIN (**ROB**otska **IN**teligencija) je napredni chatbot sustav dizajniran za pružanje podrške studentima i osoblju Fakulteta organizacije i informatike (FOI). Koristeći najnovije tehnologije obrade prirodnog jezika i strojnog učenja, ROBIN ima za cilj poboljšati korisničko iskustvo pružanjem točnih i relevantnih informacija o fakultetskim programima, procedurama i resursima.

## Struktura Projekta

Projekt je organiziran u nekoliko ključnih modula:

- **chat.py**: Glavni modul za pokretanje chatbota. Ovaj modul upravlja interakcijom s korisnikom, obrađuje upite i generira odgovore.
- **api.py**: Modul za rukovanje API zahtjevima i interakcijama. Omogućuje integraciju chatbota s drugim sustavima i aplikacijama.
- **evaluation-metrics.py**: Skripta za evaluaciju performansi modela. Koristi se za mjerenje točnosti, relevantnosti i koherentnosti odgovora chatbota.
- **model_utils.py**: Pomoćne funkcije za rad s modelima. Sadrži utility funkcije za inicijalizaciju, učitavanje i konfiguraciju jezičnih modela.
- **config.py**: Konfiguracijske postavke za projekt. Centralizira sve postavke i parametre projekta na jednom mjestu.
- **document_processor.py**: Modul za obradu dokumenata i ulaznih podataka. Priprema i indeksira dokumentaciju fakulteta za korištenje u chatbotu.

## Zahtjevi

Za pokretanje ovog projekta potrebno je imati instalirane sljedeće Python pakete:

- Flask
- llama-index
- openai
- numpy
- scikit-learn
- nltk

Točne verzije paketa i dodatne ovisnosti možete pronaći u datoteci `requirements.txt`.

## Instalacija

1. Klonirajte ovaj repozitorij:
    ```bash
    git clone https://github.com/vaše-korisničko-ime/ROBIN.git
    ```

2. Uđite u direktorij projekta:
    ```bash
    cd ROBIN
    ```

3. Instalirajte potrebne pakete:
    ```bash
    pip install -r requirements.txt
    ```

4. Konfigurirajte API ključeve:
   Otvorite `config.py` i unesite svoj OpenAI API ključ i LlamaParse API ključ.

## Korištenje

### Pokretanje Chatbota

Za pokretanje chatbota u interaktivnom načinu rada, koristite sljedeću naredbu:

```bash
python chat.py
```

Ovo će pokrenuti konzolno sučelje gdje možete postavljati pitanja i dobivati odgovore od ROBIN-a.

### Pokretanje API-ja

Ako želite chatbot pokrenuti kao API putem Flask-a, koristite sljedeću naredbu:

```bash
python api.py
```

Ovo će pokrenuti Flask server, obično na `http://127.0.0.1:5000`. Možete slati POST zahtjeve na `/query` endpoint s JSON tijelom koje sadrži `query` polje.

### Obrada Dokumenata

Prije prve uporabe chatbota, potrebno je obraditi i indeksirati dokumente. To možete učiniti pokretanjem:

```bash
python document_processor.py
```

Ovo će stvoriti indeks koji chatbot koristi za generiranje odgovora.

## Evaluacija

Za evaluaciju izgrađenog modela koristite sljedeću naredbu:

```bash
python evaluation-metrics.py
```

Ovo će pokrenuti niz testnih slučajeva i generirati izvješće o performansama modela, uključujući metrike poput relevantnosti, koherentnosti i BLEU score-a.

## Prilagodba

ROBIN je dizajniran da bude fleksibilan i prilagodljiv. Možete prilagoditi ponašanje chatbota modificiranjem `SYSTEM_PROMPT` u `config.py`. Također možete dodati nove dokumente u `documents` direktorij i ponovno pokrenuti `document_processor.py` za ažuriranje baze znanja.


## Licenca

Ovaj projekt je licenciran pod [MIT licencom](LICENSE).

## Kontakt

Za sva pitanja ili sugestije, molimo vas da otvorite issue u ovom repozitoriju ili na mail fsuman20@student.foi.hr.
