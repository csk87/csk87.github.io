---
layout: post
title: "Mina tankar om CSS Pre-Processors"
img: /images/css.jpg
excerpt: Detta blogginlägg handlar om mina tankar kring CSS Pre-Processors som SASS etc.
---

**Vad tycker jag om att pre-compilera min CSS?**
**Jämfört med vanlig CSS**

Då det är första gången jag jobbar med SASS och "pre-compiled CSS" så är det som med all annan programmering och webbutveckling en inlärninskurva och vanesak. 
Eftersom vi samtidigt skulle lära oss (som i mitt fall) Cloud 9 eller Docker som även det är nya mjukvaror för mig så har det varit lite klurigt att förstå och få till allt. 

**Vilken teknik använde jag?**

Då kraven för uppgiften var att använda Pre-processorn SASS så har jag använt den. Självklart tillsammans med lite vanlig CSS kod (dvs inte alltid skrivit nya variabler)


**Fördelar, nackdelar?**

Fördelarna med SASS, LESS och andra Pre-processors för CSS är självklart att man följer DRY principen. Det är smidigt att kunna använda redan definerade variablar i sin kod och kunna ändra på ett specifikt ställe för att göra större justeringar.
(ex byta font eller huvudfärg på webbplatsen.)

Nackdelarna som jag ser det är att man måste lära sig ännu ett "språk" (som om man inte behöver kunna nog många redan..).
Samt den största nackdelen som jag märkt: Man kan inte göra uppdateringar och testa sin kod utan att kompilera filen till CSS först vilket gör realtidsuppdateringar omöjligt (men jag har kanske fel om detta?)

**Vad tycker jag om statiska site generatorer?**

För utvecklare som ska sköta allt på en webbplats känns det som ett rätt val att köra en statisk site generator då sidorna både blir snabba och säkra då det inte finns någon databas. 
dock kommer problemen då ex en klient/kund vill kunna uppdatera innehållet själv då dom måste ha viss programmeringskunskap. 

Då jag själv jobbar med wordpress så har jag nu sett många fördelar med i detta fallet jekyll som jag ska försöka anväda på mindre projekt i mitt företag. 
Det ser ut att finnas en stor potential om det kan utnyttjas tillsammans med något bra CMS system. 



**Till vilka typer av projekt passar det att använda Static site generators?** 

Min personliga åsikt är att mindre projekt där det ändå krävs en viss mån av "dynamiskt innehåll" likt blogginlägg och liknande är den rätta typen av projekt för SSG. 
Är det hela Webbplatser är det förmodligen bättre med ett större CMS likt drupal eller Wordpress då användaren kan anväda en WYSIWYG - Editor för att ändra i texten och inte behöver kunna ex Markdown för att göra nya sidor och inlägg. 

**vad är robots.txt och hur har jag konfigruerat den för min website?**

robots.txt är en textfil som placeras i root mappen och styr vilka delar på din website som robotar får besöka. 
ett exempel på när en robot används är när google indexerar webbplatser. Detta gära av en robot. 
Jag har valt att inte tillåta robotar alls på min sida då jag använder min företagslogga på bloggen och inte vill att den skall indexeras. 

**vad är humans.txt och hur har jag konfigruerat den för min website?**

Humans.txt är en textfil som beskriver viss information om personerna bakom en webbplats.
Jag har valt att lägga med information om: 
  * Projektet
  * Författaren (jag) 
  * Sociala medier
  * Lite Meta information

**Hur implementerade jag kommentarer till min website?**

Kommentarerna implementerade jag till varje enskild post genom att använda universalcode från disqus då dem inte hade specifik implementering för just jekyll. 
Detta är bara javascriptkod som använder en specifik identiferare för varje enskild "post".

**Vad är Open Graph och hur har jag utnyttjat det??**

Open graph är metataggar som används för att specificera vissa element från den websida du länkar och på så sätt kunna uppvisa den information du vill med delningen (länkningen). 
du kan ex bestämma vilken bild och information som skall visas upp när du postar en länk till din site på facebook eller twitter. 

Jag har försökt använda "conditionals" med if satser som skall kolla om ex en viss titel finns angedd på den urlen man vill posta. Om det inte finns så skall en "generell" titel användas. 
innehållet (content) hämtas med hjälp av variabler ex: 
```text
site.title
page.title
```
mm.  

Har dock haft lite problem med att få ändringarna att ske på cloud9 så vet inte om dett fungerar exakt som jag vill.

