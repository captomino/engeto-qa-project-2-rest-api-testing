# Testování REST API
![Project Status](https://img.shields.io/badge/status-⏳_Awaiting%20Review-orange)


## O projektu
Projekt je zaměřen na **testování REST API aplikace pro správu studentů** dostupné na adrese [https://test-app.engeto.cz/students](https://test-app.engeto.cz/students). Testování pokrývá metody **GET, POST, PUT a DELETE**, ověřování autentizace a autorizace, validaci vstupních dat, kontrolu konzistence s databází a základní bezpečnostní scénáře.

Rozsah testování má **modelový charakter** a nepředstavuje plně vyčerpávající testovací sadu. Projekt byl realizován v rámci **ENGETO Testing Akademie**.

**Výstupy projektu:**
- **PDF report** (`report.pdf`) – shrnutí testování, výsledky a bug report  
- **Excel soubor** (`details.xlsx`) – testovací scénáře, výsledky a evidence chyb  


## Použité nástroje
- **Postman (v12.4.2)**  – exekuce API requestů a testování endpointů   
- **DBeaver (v24.3.4.0)** – ověření dat a konzistence v databázi
- **Microsoft Excel** – evidence testovacích scénářů, výsledků a bug reportu
- **Textový editor** – úprava a finalizace PDF reportu  

## Struktura projektu
```plaintext
engeto-qa-project-2-rest-api-testing/
├─ report.pdf
├─ details.xlsx
└─ README.md
```

## Testování

Testování zahrnovalo:

- autentizační a autorizační testy  
- CRUD operace (GET, POST, PUT, DELETE)
- validační testy (email, ID, povinná pole)  
- bezpečnostní testy  

V rámci těchto oblastí byly provedeny pozitivní i negativní scénáře.

Každý testovací případ obsahuje:

- ID a název testu
- endpoint a metodu
- vstupní podmínky a kroky
- očekávaný a skutečný výsledek
- stav (PASS / FAIL)

> Detailní scénáře a výsledky jsou uvedeny v `details.xlsx` (listy `testCases` a `testResults`).


## Výsledky testů

- **Celkem testů:** 28  
- **Neúspěšné:** 13  

**Hlavní zjištění:**
- nefunkční DELETE (záznam není odstraněn z DB)
- nedostatečná validace vstupů (email, ID, povinná pole)
- nekonzistentní HTTP status kódy
- potenciální zranitelnost vůči SQL injection

> Kompletní výsledky a bug report viz `details.xlsx` (listy `testResults` a `bugReport`).


## Doporučení

- odstranit chyby s vysokou závažností
- sjednotit validační a autentizační logiku
- dodržovat konvence HTTP status kódů
- posílit ochranu proti vstupním útokům (např. SQL injection)


## Omezení projektu

- testování je manuální (bez automatizace)
- testováno na sdílené testovací instanci
- výsledky mohou být ovlivněny stavem databáze

## Možná rozšíření

- automatizace testů (Postman Collection + Newman)
- rozšíření validačních pravidel (regex, délka vstupů)


## Autor

**Tomáš Čáp**  
Projekt vytvořen v rámci ENGETO Testing Akademie (2026)  
GitHub: [github.com/captomino](https://github.com/captomino) 

## Licence

Projekt je určen výhradně pro vzdělávací účely.
