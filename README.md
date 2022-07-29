# CapitalQuizz

[![Netlify Status](https://api.netlify.com/api/v1/badges/13ac3895-5d89-49ab-b9f2-5d917f3c03af/deploy-status)](https://app.netlify.com/sites/inspiquotes/deploys)

![alt ceci est un text alternatif](capital-quizz.gif)

[Click Here to view more](https://capital-quizz.netlify.app)

### Création d'un quizz sur les capitales du monde,

- Affichage d'un message si bonne ou mauvaise réponse

- Affichage d'un composant Card avec quelques informations sur le pays en question ( Capitale, Habitants, Monnaie ...) suite à une réponse

- Utilisation de JQuery, Ajax

- Utilisation du Framework CSS [Semantic-UI](https://semantic-ui.com/)

- Utilisation d'une API publique (pour les requêtes AJax) accessible à l'adresse [https://restcountries.com/v3.1/all](https://restcountries.com/v3.1/all), qui renvoit un fichier json contenant avec un tableau d'objets de cette forme (exemple pour le pays "FRANCE") :

```javascript
{
name: {
common: "France",
official: "French Republic",
nativeName: {
fra: {
official: "République française",
common: "France"
}
}
},
tld: [
".fr"
],
cca2: "FR",
ccn3: "250",
cca3: "FRA",
cioc: "FRA",
independent: true,
status: "officially-assigned",
unMember: true,
currencies: {
EUR: {
name: "Euro",
symbol: "€"
}
},
idd: {
root: "+3",
suffixes: [
"3"
]
},
capital: [
"Paris"
],
altSpellings: [
"FR",
"French Republic",
"République française"
],
region: "Europe",
subregion: "Western Europe",
languages: {
fra: "French"
},
translations: {
ara: {
official: "الجمهورية الفرنسية",
common: "فرنسا"
},
ces: {
official: "Francouzská republika",
common: "Francie"
},
cym: {
official: "French Republic",
common: "France"
},
deu: {
official: "Französische Republik",
common: "Frankreich"
},
est: {
official: "Prantsuse Vabariik",
common: "Prantsusmaa"
},
fin: {
official: "Ranskan tasavalta",
common: "Ranska"
},
fra: {
official: "République française",
common: "France"
},
hrv: {
official: "Francuska Republika",
common: "Francuska"
},
hun: {
official: "Francia Köztársaság",
common: "Franciaország"
},
ita: {
official: "Repubblica francese",
common: "Francia"
},
jpn: {
official: "フランス共和国",
common: "フランス"
},
kor: {
official: "프랑스 공화국",
common: "프랑스"
},
nld: {
official: "Franse Republiek",
common: "Frankrijk"
},
per: {
official: "جمهوری فرانسه",
common: "فرانسه"
},
pol: {
official: "Republika Francuska",
common: "Francja"
},
por: {
official: "República Francesa",
common: "França"
},
rus: {
official: "Французская Республика",
common: "Франция"
},
slk: {
official: "Francúzska republika",
common: "Francúzsko"
},
spa: {
official: "República francés",
common: "Francia"
},
swe: {
official: "Republiken Frankrike",
common: "Frankrike"
},
urd: {
official: "جمہوریہ فرانس",
common: "فرانس"
},
zho: {
official: "法兰西共和国",
common: "法国"
}
},
latlng: [
46,
2
],
landlocked: false,
borders: [
"AND",
"BEL",
"DEU",
"ITA",
"LUX",
"MCO",
"ESP",
"CHE"
],
area: 551695,
demonyms: {
eng: {
f: "French",
m: "French"
},
fra: {
f: "Française",
m: "Français"
}
},
flag: "🇫🇷",
maps: {
googleMaps: "https://goo.gl/maps/g7QxxSFsWyTPKuzd7",
openStreetMaps: "https://www.openstreetmap.org/relation/1403916"
},
population: 67391582,
gini: {
2018: 32.4
},
fifa: "FRA",
car: {
signs: [
"F"
],
side: "right"
},
timezones: [
"UTC-10:00",
"UTC-09:30",
"UTC-09:00",
"UTC-08:00",
"UTC-04:00",
"UTC-03:00",
"UTC+01:00",
"UTC+02:00",
"UTC+03:00",
"UTC+04:00",
"UTC+05:00",
"UTC+10:00",
"UTC+11:00",
"UTC+12:00"
],
continents: [
"Europe"
],
flags: {
png: "https://flagcdn.com/w320/fr.png",
svg: "https://flagcdn.com/fr.svg"
},
coatOfArms: {
png: "https://mainfacts.com/media/images/coats_of_arms/fr.png",
svg: "https://mainfacts.com/media/images/coats_of_arms/fr.svg"
},
startOfWeek: "monday",
capitalInfo: {
latlng: [
48.87,
2.33
]
},
postalCode: {
format: "#####",
regex: "^(\d{5})$"
}
}
```

---

Je me suis donc servi de cette API pour mes algorithmes de comparaison entre la réponse renvoyée par l'utilisateur et la vraie réponse présente dans le fichier Json, ainsi que la génération des informations du composant Card.

J'ai également du mettre en place un système de ramdom selection pour que les mauvaises réponses proposées pour chaque question ne soient pas toujours les mêmes et dans le meme ordre d'affichage.
