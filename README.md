# Databáze pro vstupenky na fotbalové zápasy
## Popis projektu

Tento projekt představuje návrh a implementaci relační databáze pro správu vstupenek na fotbalové zápasy. Databáze umožňuje evidovat týmy, zápasy, zákazníky a zakoupené vstupenky.

Cílem projektu je ukázat principy návrhu databází, práci s relacemi mezi tabulkami a využití cizích klíčů.

## Použité technologie
MySQL
MySQL Workbench (ER diagram)
SQL (DDL skripty)
Git + GitHub (verzování projektu)

## Struktura databáze

Databáze obsahuje 4 hlavní tabulky:

## Team
id_team – primární klíč
name – název týmu

## Match
id_match – primární klíč
match_date – datum zápasu
home_team_id – domácí tým (FK)
away_team_id – hostující tým (FK)

vztah:

1 tým → může hrát více zápasů (1)

## Customer
id_customer – primární klíč
name – jméno zákazníka
email – email

## Ticket
id_ticket – primární klíč
seat – místo
price – cena
id_customer – zákazník (FK)
id_match – zápas (FK)

vztahy:

1 zákazník → více vstupenek (1)
1 zápas → více vstupenek (1)

## Vztahy mezi tabulkami
Team ↔ Match → 1
Customer ↔ Ticket → 1
Match ↔ Ticket → 1

## Principy návrhu
Použit relační model databází (RMD)
Využití primárních a cizích klíčů
Dodržení základních normálních forem (1NF, 2NF, 3NF)
Eliminace duplicitních dat

## ER diagram

ER diagram byl vytvořen v MySQL Workbench a znázorňuje vztahy mezi jednotlivými entitami.

(sem můžeš vložit obrázek diagramu)

## Spuštění projektu

Otevřít MySQL Workbench nebo phpMyAdmin
Vytvořit databázi (např. mydb)
Spustit SQL skript (CREATE TABLE ...)
Databáze je připravena k použití

## Účel projektu

Projekt slouží jako ukázka:

návrhu databáze
práce s SQL
pochopení vztahů mezi entitami
## Autor

Student – Miroslav Urban V2I projekt do předmětu databázové systémy (DBS)