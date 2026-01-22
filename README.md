Ontwerp en maak een responsive website voor een startup.

De instructies voor deze opdracht staan in: [INSTRUCTIONS.md](https://github.com/fdnd-task/the-startup-responsive-interactieve-website/blob/main/docs/INSTRUCTIONS.md)

# Titel
Voor sprint 6 heb ik de PostNL homepage nagebouwd met focus op responsive design en toegankelijkheid. Ik heb alle technieken van de afgelopen sprints toegepast: semantische HTML, mobile-first werken, CSS interacties, toegankelijkheid en goede code conventies.



## Beschrijving
<img width="1980" height="1325" alt="image" src="https://github.com/user-attachments/assets/ee774de9-ab6b-422e-843b-fc57646b0f82" />
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

### Huisstijl

Ik heb eerst de PostNL huisstijl uitgezocht voordat ik begon:

![Frame 9846](https://github.com/user-attachments/assets/93f22645-5a25-4c7e-8ccb-5b72dcc3f464)
![Image](https://github.com/user-attachments/assets/dd58ceaf-5221-4234-aaaf-4aa5113751c6)


**Kleurcontrast verbeterd:**

Tijdens een color-contrasttest kwam naar voren dat er twee verschillende oranje tinten zijn gebruikt voor de tekst "Volg je pakket". Deze voldeden allebei niet aan de WCAG-richtlijnen in combinatie met de achtergrond. Daarom is gekozen voor een andere oranje tint die wél minimaal voldoet aan het AA-niveau van de WCAG.

**Resultaten test desktop:**

<img width="1044" alt="Image" src="https://github.com/user-attachments/assets/4096f342-d69e-4e90-9577-0022242ada2f" />

**Resultaten test mobiel:**

<img width="868" alt="Image" src="https://github.com/user-attachments/assets/b64c69a4-2ce2-4868-91aa-63401581f2b7" />

**Verbeterde versie met juiste contrast:**

<img width="560" alt="Image" src="https://github.com/user-attachments/assets/8d31545b-1367-492a-8c75-16b485f06621" />  


### interactief

# Tab interactie
Met de tabs kan je makkelijk switchen tussen de verschillende services zonder de pagina te verversen. Alleen de actieve tab wordt getoond en door kleur, animaties en iconen zie je meteen welke tab actief is en wat er gebeurt bij hover of klik.
![Untitledvideo-MadewithClipchamp-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/96d12ef0-b7b8-41fc-bcfa-66eced0b9cf1)

# Popover interactie
Het menu opent als een popover met een cirkel-animatie vanaf de knop. Zo zie je duidelijk waar het menu vandaan komt. Alles werkt zonder JavaScript.  

![Bezigmetopnemen2026-01-22113920-ezgif com-video-to-gif-converter (1)](https://github.com/user-attachments/assets/5a72751a-e742-4718-8028-c0c78e336d10)




<!-- Voeg een mooie poster visual toe 📸 -->
<!-- Voeg een link toe naar Github Pages 🌐-->

## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met JS gedaan en hoe? -->

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

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).


