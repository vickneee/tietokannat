# Päivityskyselyt

### Tehtävä 1

Vesa lentää nykyiseltä sijainnilta Nottingham Airport:lle. Samalla Vesan hiilijalanjälki kasvaa 500:lla. Päivitä nämä tiedot tietokantaan.

Vihje1: Tarvitset sisäkyselyn selvittääksesi Nottingham Airportin identin.
```sql
UPDATE game
SET location = (
    SELECT id
    FROM airport
    WHERE name = "Nottingham Airport"
), co2_consumed = co2_consumed + 500
WHERE screen_name = "Vesa";
```
If you run the query above, you will get the following error message:

ERROR 1452 (23000): Cannot add or update a child row: a foreign key constraint fails (`flight_game`.`game`, CONSTRAINT `game_ibfk_1` FOREIGN KEY (`location`) REFERENCES `airport` (`ident`))

change the column name from id to ident in the subquery:

```sql
UPDATE game
SET location = (
    SELECT ident
    FROM airport
    WHERE name = "Nottingham Airport"
), co2_consumed = co2_consumed + 500
WHERE screen_name = "Vesa";
```
Game-taulun sisältä näyttää päivituksen jälkeen seuraavalta:
![Screenshot8_1](Screenshot8_1.png)

### Tehtävä 2
SELECT * FROM esimerkki WHERE kentta = 'arvo' 
![ruudunkaappaus](kuvatiedoston-nimi.png)