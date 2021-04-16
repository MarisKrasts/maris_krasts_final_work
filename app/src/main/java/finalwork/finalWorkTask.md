# Produktu grāmatvedības sistēma

Aplikācijā jābūt produkta pievienošana / noņemšana / saņemšana (CRUD operations).

### Minimālās prasības (iespējamie izvēlnes elementi):

- Produkta pievienošana
- Produkta saņemšana pēc id
- Visu produktu saraksta saņemšana
- produkta dzēšana pēc id

Vismaz jābūt 1 interfeisam vai abstraktajai klasei. Lietot tikai pēc nepieciešamības.

Vismaz 1 kolekcija (jebkura no List, Map, Set)

Nosaukumiem jāatbilst aplikācijas loģikai. (Clean Code palīdzēs)
Nevajadzētu būt komentāriem - kodam ir jābūt skaidram bez komentāriem.

Galvenā vienība ir Product.

#### Galvenie laukumi (mandatory fields):

- Nosaukums (name) - datu tips String (piemērs: Apple)
- Identifikācijas numurs (id) - datu tips Long (piemērs: 123)
- Cena (price) - datu tips BigDecimal (piemērs: 0.14)
- Kategorija (category) - enum (piemērs: FRUIT)

#### papildus laukumi (optional fields):

- Atlaide (discount) - datu tips BigDecimal (piemērs: 0,05) (5%)
- Apraksts (description) - datu tips String (piemērs: Tasty apples from Latvia)

Ja galvenais laukums nebija ievadīts - neierakstīt produktu, bet informēt lietotāju, ka laukums nav ievadīts vai
ievadīts nepareizi.

Pievienojot produktu, lietotājs nenorāda id. Id piešķiras kodā.

Piemēram: kad pirmo reizi pievienojat produktu id būs 0, kad pievienojat nākamo produktu, nākošajam produktam jau id būs
1, utt.

Ja produktam ir atlaide, tad, parādot informāciju konsolē, ir jābūt skaidrs, ka ir atlaide.

### Piemēram:

#### Product information:

- Id: 123
- Name: Apple
- Regular price: 0.14
- Discount: 50%
- Actual price: 0.07

InMemoryDatabase jūs varat izmantot jebkuru kolekciju .

### Papildus prasības:

- Nepieciešams lai būtu iespēja viegli ievadīt jaunas funkcijas (features) un viegli tās noņemt.

- Funkcionālu ir jāsadala tādā veidā, lai UI konsole / biznesa loģika (service) un datu bāze (Database) būtu sadalītas
  līmeņos (sadalīšanai izmantojiet packages).

- UI-console līmenī tikai saziņa ar lietotāju (menu, izvēlne)

- service līmenī visa lietojumprogrammas biznesa loģika (arī validācija)

- Datubāzes līmenī tikai datu bāze (kolekcija)

#### Funkcionālās prasības:

- Pievienot iegūšans iespēju konkrētas kategorijas saraksta .
- Pievienot iespēju mainīt produkta informāciju. Piemēram, mainīt cenu vai pievienot / noņemt atlaidi.
- Pievienot iespēju noteikt atlaidi visiem produktiem noteiktās kategorijas.
- Programmai jābūt notestētai, izmantojot jUnit. (drīkst arī uzrakstīt savus testus)

* Menu netestēt

### Testa pārklājums (code coverage)> 70%

### Papildus prasības #2:

- Iepazīstieties ar build tool gradle rīku un izmanto to projektā

- Pārliecināties ka komandas clean un install darbojas.

- Augšupielādēt projektu uz github