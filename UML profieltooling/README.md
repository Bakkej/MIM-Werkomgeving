# HANDLEIDING MIM-PROFIEL, -TOOLBOX, -MDG GENEREREN

## GITHUB: DOCUMENTEN EN BESTANDEN
 - GitHub: MIM-werkomgeving
 - Folder UML profile tooling
 - We werken nu in "werkversie 1.1.1"

## WELKE PACKAGES ALS PROFIEL PUBLISEREN
 1. `«profile» Keuzeattribuut`
 1. `«profile» Keuzebasis`
 1. `«profile» Keuzedatatype`
 1. `«profile» Keuzerelatie`
 1. `«profile» MIM`
 1. `«profile toolbox» MIM`

## NOG ONDERBRENGEN
 - Met al die profielen maak je een MDG MIM toolbox v1.1.1.xml
 - MTS is een configuratieprofiel
 - Dit is vooral handig als je meerdere keren het profiel moet genereren
 - En dat gebeurt
 - Voor MIM 1.1.1 bestaat dit bestand al
 - Voor profielen: zie afbeelding
 - Rood en groen

 > **Opm: Een diagram moet je als als diagram publishen!** `Publish Diagram as UML Profile`

## STAP 1: PUBLICEER "PACKAGE" ALS UML PROFIEL
 - Kies package MIM-UML profiel
 - Je kiest per profiel
 - Ga naar: "Specialize" 
 - Kies: "Publish Technologie"
 - Kies: "Publish Pack As UML profile"
 - Typ: profile name: "MIM"
 - Kies: `<path>`
 - typ: version: `<versienummer>` (bijv.:1.1.1)

Let op er zijn twee belangrijke voorwaarden
 > **opm.**: [**CONTROLEREN**]De profile name moet overeenkomenm met de naam van het package
Verder lijkt het erop of «profile»MIM en «toolbox profile»MIM niet alleen overeen moeten komen met de naam van het package, maar eveneens onderling ... 

1. De vier keuze-packages moeten een unieke naam hebben bij profile name (bijv. "MIM_Keuzeattribuut")
2. Het basisprofiel <naam> (iets van «profile» MIM), moet bij profile name dezelfde naam hebben als «toolbox profile» MIM

 > **opm**: ~zorg dat profile name en version overal exact hetzelfde zijn, anders werkt het profiel niet~. Dit kan eventueel met een XML-editor gerepareerd worden, maar voorkomen is beter dan genezen.

In MIM-toolbox diagram kun je aan de prefixen zien, wat de profile names moeten zijn
Als je diagram rtoevoegd moet je drie stappen doorlopen bij het selecteren van profielen

 - Klik: "Save"
 - Herhaal dit proces voor alle bovengenoemde onderdelen (dus ook voor toolbox profile)

 >**Let op**: de toolbox moet samengesteld worden uit verschillende profielen (lijst). Het 'basisprofiel' is ... en dat moet dezelfde naam hebb

## STAP 2: GENEREER MDG TECHNOLOGIE
 - Selecteer vervolgens het package waaronder alle subpackages vallen
 - Ga weer naar "Specialize"
 - Kies: "Publish Package"
 - Kies: "Generate MDG Technology"
 - Kies Volgende
 - Kies 'Open an existing MTS file'
 - Negeer de melding
 
 > **Opm**: De MTS file vult een aantal standaard configuraties vooraf in, maar je kunt deze tijdens het proces nog aanpassen.

 - Vanuit MTS file wordt het volgende venster al ingevuld
 - Technology: MIM
 - Filename: ingevuld, maar kun je zelf kiezen
 - ID: MIM
 - Version: 1.1.1

 > **Opm**: deze twee moeten dus kloppen met stap x in packages publiceren

 - Icon en logo blijven vooralsnog leeg
 - URL: link naar corresponderende MIM-documentatie op GitHub/ReSpec
 - Support, link naar website geonovum
 - Notes: Vul in het notes veld kort release notes in: wat is er nieuw/aangepast
 - Klik volgende
 - Laat de instellingen in venster onaangepast

 > **Opm**: In het metaprofiel zitten profiles en toolboxes

 - Alle configuraties kun je laden vanuit de MTF file
 - Voor de eerste keer kun je ook een MTS-file genereren
 - Select:  "Files To Be Included As Profiles"
 - Kies hier alle xml bestanden, behalve de toolboxprofile
 - In de volgende stap doe je precies het omgekeerde
 - Klik volgende
 - Check de box Save to MTS en klik op voltooien

 - Indien je wijzigingen in de configuratie hebt aangebracht:
 - Kies checkbox  "Save To Mts"
 - Klik: "Voltooien"

## STAP 3: TEST DE TOOLBOX
 - Laad het MIM-profiel via "Resources"
 - maar er is een EAP-testf file
 - Verschillende manieren om de nieuwe toolbox te testen
 - Een model bouwen met alle MIM-mogelijkheden erin
 - Of: een nieuwe toolbox laden en update van het bestaande model uitvoeren
 - En dat kan door MIM metaklassen te slepen
 - Of door gebruik te maken va "Sync Tagged Values And Constraints"
 - Deze laatste optie vind je terug in het "Resources" menu

## SCREENSHOTS (NOG PLAATSEN)
> **Opm.**: voor diagram nog één afbeelding wijzigen (MDG tech wizard - contents), kruis diagram ... aan en afbeelding diagram selection toevoegen

![tekst](media/MIM_01_profile_benodigde_profielen.jpg)
![tekst](media/MIM_02_profile_publish_as_uml_settings.jpg)
![tekst](media/MIM_03_publish_as_UML_or_MDG.jpg)
![tekst](media/MIM_04_mdg_tech.jpg)
![tekst](media/MIM_05_mdg_tech.jpg)
![tekst](media/MIM_06_mdg_tech.jpg)
![tekst](media/MIM_07_mdg_tech.jpg)
![tekst](media/MIM_08_mdg_tech.jpg)

<!-- ## OPMERKINGEN
 - MIM willen we zien welke versie het is 
 - Bij test blijken een aantal stereotypen niet te werken
 - Paul laat zien hoe dat zit
 - Dat MIMprofile blijkt niet te werken
 - Bij versie staat ergens default 1.0, moet 1.1.1 worden
 - Paul moest in het XML iets veranderen
 - Lukt even niet... -->

## MIM_MDG
 - profile helpers, model wizard: https://sparxsystems.com/enterprise_architect_user_guide/15.2/modeling/using_the_profile_helpers.html
 - Create Diagram Profiles using the Profile Helpers:https://sparxsystems.com/enterprise_architect_user_guide/15.2/modeling/create_diagram_profiles_using_.html
 - Morgen weer verder!

## Aandachtspunt
 - Tekstveld voor teolichting, niet initial value, maar notes veld als datatype
 - Uitgebreide toelichting wordt afgekapt vanwege maximale lengte.
 - Profiel niet elke keer opnieuw moeten laden door het kopppelen aan een (std.) diagram
 - MIM 1.1 build 1
 - Vorige versie had ook zo'n naam, dit kun je op website of github terugvinden. gaat om de naam van de het XML