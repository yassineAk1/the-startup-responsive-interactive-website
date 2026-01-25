Ontwerp en maak een responsive website voor een startup.

De instructies voor deze opdracht staan in: [INSTRUCTIONS.md](https://github.com/fdnd-task/the-startup-responsive-interactieve-website/blob/main/docs/INSTRUCTIONS.md)

# Titel
Voor sprint 6 heb ik de PostNL homepage nagebouwd met focus op responsive design en toegankelijkheid. Ik heb alle technieken van de afgelopen sprints toegepast: semantische HTML, mobile-first werken, CSS interacties, toegankelijkheid en goede code conventies.



## Beschrijving  
![Mockup Result (7)](https://github.com/user-attachments/assets/00ca3df2-3b5a-46de-966c-49a4cc9314bf)

<!-- In de Beschrijving staat hoe je project er uit ziet, hoe het werkt en wat je er mee kan. -->

### Responsive

Ik heb gewerkt volgens mobile-first principe. Eerst mobile ontworpen, daarna uitgebreid naar desktop. De website heeft één hoofdbreakpoint op 700px.

**Schermbreedte < 400px (Mobile):**

![Free iPhone 17 Pro](https://github.com/user-attachments/assets/464c70b9-0b4f-42af-b109-2597d23e115b)
- Alles gestapeld onder elkaar
- Hamburger menu met gave cirkel-animatie
- Tabs met iconen boven de tekst
- Footer met uitklapbare accordeons



**Schermbreedte > 700px (Tablet):**  
![Mockup Result (1)](https://github.com/user-attachments/assets/56a15bf0-23b5-4c6d-b4e3-7247ebdc92c6)- Hero naast elkaar in plaats van gestapeld
- Info cards in 3 kolommen grid
- Footer altijd uitgeklapt
- Grotere fonts met `clamp()` zodat het altijd goed leesbaar blijft

**Schermbreedte > 1600px (desktop):**  
![Mockup Result (2)](https://github.com/user-attachments/assets/cb72350d-ab5f-44b5-8b0f-dfba539f91b0)

## Huisstijl PostNL

Ik heb eerst de PostNL huisstijl uitgezocht voordat ik begon:

![Frame 9846](https://github.com/user-attachments/assets/93f22645-5a25-4c7e-8ccb-5b72dcc3f464)
![Image](https://github.com/user-attachments/assets/dd58ceaf-5221-4234-aaaf-4aa5113751c6)


**Kleuren**

Ik heb de PostNL huisstijl nauwkeurig overgenomen en in CSS custom properties gezet voor consistentie door de hele website:


https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/f530920da819c79500bec59db23a6daf00aa88b7/stylesheet.css#L5-L29


**Typografie**

PostNL gebruikt twee fonts genaamd ABC Rom en hanken grotesk, ik heb deze overgenomen en responsive gemaakt met  `clamp()`:

https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/f530920da819c79500bec59db23a6daf00aa88b7/stylesheet.css#L32-L34

https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/f530920da819c79500bec59db23a6daf00aa88b7/stylesheet.css#L53-L62

https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/f530920da819c79500bec59db23a6daf00aa88b7/style.css#L216-L225



De info cards gebruiken verschillende accent kleuren uit de PostNL huisstijl:

```css
.info-card:nth-of-type(1) .card-content {
  background-color: var(--card-red-main); /* Rood accent */
}

.info-card:nth-of-type(2) .card-content {
  background-color: var(--card-blue-main); /* Blauw accent */
}

.info-card:nth-of-type(3) .card-content {
  background-color: var(--card-navy-main); /* Navy accent */
}
```

Elk card heeft ook een donkerdere variant voor de "lees meer" link, wat zorgt voor visuele hiërarchie binnen dezelfde kleurenfamilie.



### Toegankelijkheid  

Tijdens het bouwen heb ik bewust rekening gehouden met toegankelijkheid en me gehouden aan de WCAG 2.1 AA-richtlijnen. De basis bestaat uit semantische HTML, zodat de pagina logisch te gebruiken is met een screenreader of toetsenbord. Zo heb ik een skiplink toegevoegd, een duidelijke heading-structuur aangehouden en alle formulieren voorzien van zichtbare labels.

Ik heb alle kleuren getest op contrast en een oranje tint aangepast omdat deze niet voldeed aan de AA-contrastnorm. Ook heb ik duidelijke focus states toegevoegd, zodat je altijd ziet waar je bent als je met het toetsenbord navigeert. Het hamburger menu is volledig met toetsenbord te bedienen en sluit automatisch met de Escape-toets.

**Reduced Motion**

Sommige mensen krijgen duizeligheid of misselijkheid van bewegende animaties. Daarom heb ik `prefers-reduced-motion` toegevoegd aan specifieke animaties.
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/901b0e138a09ce34c09c6a8a6c9a1b34b3d284b9/style.css#L385-L436

**Wat dit doet:**
- Als iemand in hun OS "Reduce motion" aan heeft staan, worden animaties beperkt of uitgeschakeld
- Icon bounce speelt maar 1x af in plaats van infinite loop
- Spin animatie wordt helemaal uitgeschakeld


Dit is belangrijk voor mensen met:
- Epilepsie
- ADHD
- Migraine gevoeligheid

**Kleurcontrast verbeterd:**

Tijdens een color-contrasttest kwam naar voren dat er twee verschillende oranje tinten zijn gebruikt voor de tekst "Volg je pakket". Deze voldeden allebei niet aan de WCAG-richtlijnen in combinatie met de achtergrond. Daarom is gekozen voor een andere oranje tint die wél minimaal voldoet aan het AA-niveau van de WCAG.

**Resultaten test desktop:**

<img width="1044" alt="Image" src="https://github.com/user-attachments/assets/4096f342-d69e-4e90-9577-0022242ada2f" />

**Resultaten test mobiel:**

<img width="868" alt="Image" src="https://github.com/user-attachments/assets/b64c69a4-2ce2-4868-91aa-63401581f2b7" />

**Verbeterde versie met juiste contrast:**

<img width="560" alt="Image" src="https://github.com/user-attachments/assets/8d31545b-1367-492a-8c75-16b485f06621" />  

### Ontwerpkeuzes

De grootste ontwerpkeuze was om het tab-systeem te maken zonder JavaScript. 
Normaal zou ik hier JavaScript voor gebruiken, maar ik wilde het proberen met alleen CSS omdat ik hoorde dat dit mogelijk was.



**Waarom geen JavaScript?**
- **Performance:** Geen JavaScript die geladen moeten worden
- **Toegankelijkheid:** Werkt altijd, zelfs als JavaScript is uitgeschakeld
- **Progressive Enhancement:** De functionaliteit werkt in alle browsers
  
# Interactief  

## Tab interactie
Met de tabs kan je makkelijk switchen tussen de verschillende services zonder de pagina te verversen. Alleen de actieve tab wordt getoond en door kleur, animaties en iconen zie je meteen welke tab actief is en wat er gebeurt bij hover of klik.
![Untitledvideo-MadewithClipchamp-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/96d12ef0-b7b8-41fc-bcfa-66eced0b9cf1)

## Popover interactie
Het menu opent als een popover met een cirkel-animatie vanaf de knop. Zo zie je duidelijk waar het menu vandaan komt. Alles werkt zonder JavaScript.  

![Bezigmetopnemen2026-01-22113920-ezgif com-video-to-gif-converter (1)](https://github.com/user-attachments/assets/5a72751a-e742-4718-8028-c0c78e336d10)




<!-- Voeg een mooie poster visual toe 📸 -->
<!-- Voeg een link toe naar Github Pages 🌐-->

## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met JS gedaan en hoe? -->
### Belangrijke features

**1. Tab-systeem**

Het tab systeem is de belangrijkste feature. Gebruikers kunnen makkelijk switchen tussen "Volg je pakket", "Versturen", "PostNL-punten" en "Postcodes". Normaal zou ik hier JavaScript voor gebruiken, maar ik heb het opgelost met de `:target` pseudo-class van CSS.

**Hoe werkt het:**
Elke tab is een link met een hash (bijvoorbeeld `#volg`). Als je erop klikt, komt die hash in de URL en kan CSS daar op reageren met `:target`. Het bijbehorende formulier wordt dan getoond terwijl de anderen verborgen blijven.

**Feedback voor de gebruiker:**
- Actieve tab krijgt grijze achtergrond
- Icon verandert van blauw naar groen (met `filter: hue-rotate()`)
- scrollt naar de tab content
- Box shadow

**Feedforward (wat kan ik verwachten?):**
- Bij hover bounced het icoontje omhoog en omlaag
- Tab wordt iets donkerder
- Schaduw wordt groter
- Cursor wordt pointer
  
```css
.tab-content {
  display: none; /* Standaard verstopt */
}

.tab-content:target {
  display: block; /* Alleen zichtbaar als de hash matcht */
  background-color: var(--bg-accent-gray);
}

/* Eerste tab standaard zichtbaar als er geen hash is */
.tabs-section:not(:has(:target)) #volg {
  display: block;
}
```
### disney principes - anticipation, squash & stretch 
Voor de animaties heb ik Disney principes toegepast. Bij hover bounced het icon (Anticipation), bij klikken schaalt de tab (Squash & Stretch) en draait het icon.   

volledige code:
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/103b86b0087f1f6211bd64126186d67559a74bd5/style.css#L285-L445

**2. Hamburger Menu**

Het hamburger menu was een uitdaging vanwege de open en sluit animatie die specifieke features nodig hebben om goe te werken, zoals display: allow discrete en overlay: allow discrete. 

**Waarom een cirkel-animatie?**  
### Disney principes - Exaggeration en Appeal:  
Ik wilde dat het duidelijk is waar het menu vandaan komt. Door de animatie te starten bij de button 90% horizontaal, 10% verticaal.
De cirkel-animatie is bewust overdreven (Exaggeration) in plaats van een simpele slide groeit de cirkel uit tot 150% van het scherm. Dit trekt de aandacht van de gebruiker naar deze belangrijke actie.
```css
.menu-popover {
  clip-path: circle(0% at 90% 10%); /* Start klein rechtsboven */
  transition: all 0.6s ease-in;
}

.menu-popover:popover-open {
  clip-path: circle(150% at 90% 10%); /* Breidt uit tot 150% */
}

/* Starting-style zorgt voor smooth opening */
@starting-style {
  .menu-popover:popover-open {
    clip-path: circle(0% at 90% 10%);
  }
}
```

volledige code:
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/103b86b0087f1f6211bd64126186d67559a74bd5/style.css#L285-L445  

## Naamgeving
### code conventies:  

#### class namen in het engels
al mijn class namen zijn in het engels om de code beter leesbaar te maken voor iedereen, paar voorbeelden hieronder
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/index.html#L17
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/index.html#L51
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/index.html#L56
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/index.html#L102

#### Ademruimte HTML
witregel tussen structuur elementen
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/aaa4a6988de409c96f04def93229f3ab4b912090/index.html#L295-L387

#### nesten van media queries
media queries worden genest voor betere leesbaarheid, hieronder enekele voorbeelden
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/style.css#L38-L41
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/style.css#L164-L176
https://github.com/yassineAk1/the-startup-responsive-interactive-website/blob/66991924fc05681033bda7155661a5c754a92a92/style.css#L404-L414



## Bronnen
https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/:target#:~:text=This%20feature%20is%20well%20established,back()%20%2C%20history.
https://stackoverflow.com/questions/77042256/css-transition-animation-not-working-for-popover-attribute
https://css-tricks.com/css-target/#:~:text=We'll%20touch%20on%20all,down%20further%20on%20a%20page.
https://developer.mozilla.org/en-US/docs/Web/API/Popover_API/Using#:~:text=Transitioning%20a%20popover,are%20not%20by%20default%20animatable.
https://www.smashingmagazine.com/2025/01/transitioning-top-layer-entries-display-property-css/
## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).


