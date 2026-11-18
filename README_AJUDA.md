<!-- SPDX-License-Identifier: AGPL-3.0-only · Copyright (c) 2026 SBS BiM Consulting, Jordi Subirós -->
# guaitaSOL · Manual d'ús

Versió en anglès: [README_HELP.md](README_HELP.md) · Tornar al [README](README.md)

## Índex

1. Què fa
2. Carta solar
3. Càmera i sensors
4. Perfil d'horitzó
5. Hores de sol directe
6. Privadesa i seguretat
7. Límits
8. Dreceres
9. Quant a

## 1. Què fa

**guaitaSOL 1.0** calcula on és el Sol en qualsevol lloc, dia i hora, i ho mostra de quatre maneres: **carta solar**, **càmera** amb les trajectòries sobre la imatge, **perfil d'horitzó** i **hores de sol directe**. Funciona sense connexió, en un sol fitxer.

## 2. Carta solar

El diagrama mostra l'alçada i l'azimut del Sol al llarg del dia. La línia verda és el dia seleccionat; els punts són les hores oficials. En groc, blau i gris hi ha el solstici d'estiu, el d'hivern i l'equinocci. Arrossega el dit sobre la trajectòria per moure l'hora.

- **Estereogràfica**: projecció habitual en arquitectura, amb el zenit al centre i el nord amunt.
- **Equidistant**: les alçades són proporcionals a la distància al centre.
- **Cilíndrica**: azimut a l'horitzontal i alçada a la vertical.

Les línies d'hora poden ser d'**hora solar** o d'**hora oficial** (analemes, que inclouen l'horari d'estiu).

## 3. Càmera i sensors

Prem **Brúixola** per activar els sensors i **Càmera** per veure la imatge. Les trajectòries solars es dibuixen sobre l'horitzó real. Cal servir-la amb **HTTPS** (per exemple GitHub Pages); des d'un fitxer local el navegador no obre la càmera.

- **iPhone**: demana permís per als sensors; el nord ve de la brúixola d'iOS.
- **Android**: s'usa la brúixola absoluta si hi és; si no, l'orientació és relativa i cal calibrar amb el Sol.
- **Sense sensors**: el simulador d'orientació permet provar-ho a l'ordinador.

Els sensors dels mòbils tenen errors típics de 5° a 10°. Calibra amb **Calibra amb el Sol** o ajusta el rumb a mà.

## 4. Perfil d'horitzó

El perfil és la línia d'obstacles (edificis, muntanyes, arbres) vista des del teu punt. Es defineix amb punts (azimut, alçada) i s'interpola entre ells. Pots afegir-los de tres maneres:

- Apuntant la càmera a l'obstacle i prement **Punt al centre**.
- Activant **Marca** i tocant la imatge de la càmera o el gràfic d'horitzó.
- Escrivint-los a mà, o important un fitxer JSON o CSV (azimut,alçada).

El perfil es desa al dispositiu i es veu a totes les vistes.

## 5. Hores de sol directe

Calcula les hores de sol directe del dia, el total perdut per obstacles, el mapa anual (dia × hora) i la mitjana per mes. L'exportació CSV recull tot l'any. Els resultats són geomètrics: no tenen en compte els núvols.

## 6. Privadesa i seguretat

guaitaSOL no envia res enlloc. Una política de seguretat (`connect-src 'none'`) impedeix que la pàgina es connecti a cap servidor. La posició, el perfil i les fotos només viuen al dispositiu. La càmera no desa cap imatge: només la mostra.

Si la instal·les com a aplicació (PWA), el navegador només descarrega els fitxers de l'app (manifest, icones i service worker) del mateix lloc; mai dades teves ni de tercers.

Les preferències es desen al `localStorage` del navegador.

## 7. Límits

- El càlcul solar (algorisme NOAA) té un error inferior a 0,05° en alçada i 0,15° en azimut respecte d'efemèrides d'alta precisió.
- La refracció atmosfèrica es modela de manera estàndard; amb horitzons molt baixos pot variar.
- La brúixola depèn de la declinació magnètica; ajusta-la al diàleg de lloc.
- Sobre objectes metàl·lics o prop d'imants, la brúixola es desvia.

## 8. Dreceres

- `←` `→` dia anterior o següent
- `Espai` animació del dia
- `N` data i hora actuals
- `L` lloc
- `M` marcar punts
- `Z` desfer punt
- `F1` ajuda

## 9. Quant a

**guaitaSOL 1.0** · suite Guaita Apps.

Copyright (C) 2026 SBS BiM Consulting, Jordi Subirós. Llicència AGPL-3.0-only. Fonts IBM Plex (SIL OFL 1.1) incrustades.

---
SBS BIM Consulting 2026 · Copyright © 2026 Jordi Subirós · AGPL-3.0-only

Guaita Apps es distribueix «tal com és», sense cap garantia. Les eines estan pensades desde la recerca i com a suport tècnic i educatiu; la verificació dels resultats i la responsabilitat derivada del seu ús recauen únicament sobre l'usuari final.
