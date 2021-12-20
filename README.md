

# OV_Rotterdam

* [Classes](#classes)
	* [PlayerModel](#playermodel)
	* [PlayersModel](#playersmodel)
* [User Interface Classes](#user-interface-classes)
    * [Button](#button)
    * [SquareButton](#squarebutton)
    * [Label](#label)
    * [Panel](#panel)
    * [InputField](#inputfield)
    * [ListBox](#listbox)
    * [Image](#image)
* [User Interface Functies](#user-interface-functies)
    * [setScreen()](#setscreen)
    * [buttonPress()](#buttonpress)
    * [squareButtonPress()](#squarebuttonpress)
    * [pressedImage()](#pressedimage)
    * [overButton()](#overbutton)
    * [overSquareButton()](#oversquarebutton)
    * [overImage()](#overImage)

## <a id='classes'>Classes</a>

### <a id='playermodel'>PlayerModel</a>

Een PlayerModel is een object waar speler gegevens in opgeslagen kunnen worden

Eigenschap | Beschrijving | Type
--- | --- | ---
name | De naam van de speler | `string`
points | Aantal punten | `int`
buses | Aantal aangelegde buspionnen (max. 20) | `int`
metros | Aantal aangelegde metropionnen (max. 20) | `int`
redcards | Aantal rode kaarten | `int`
greencards | Aantal groene kaarten | `int`
bluecards | Aantal blauwe kaarten | `int`
yellowcards | Aantal gele kaarten | `int`
wildcards | Aantal Wildcards | `int`

### <a id='playersmodel'>PlayersModel</a>

Een PlayerModel is een object waar meerdere spelers in opgeslagen kan worden

Eigenschap | Beschrijving | Type
--- | --- | ---
names | Een dictionary van alle spelers, met de naam als string als index en de PlayerModel object als value | `dict<string, PlayerModel>`
turn | De speler die momenteel aan de beurt is | `string`




## <a id='user-interface-classes'>User Interface Classes</a>

### <a id='button'>Button<a/>
Een Button object is een knop waar je met je muis op kunt klikken, alle knoppen hebben een hoogte van 50 pixels.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de button | `string`
t | De tekst dat op de button komt de staan| `string`
x | De x-positie | `int`
y | De y-positie | `int`
w | De breedte van de button | `int`
visible | Of de button zichtbaar is | `boolean`
enabled | Of er op de button geklikt kan worden | `boolean` | `True`
bgcolor | `''` voor grijs, `'red'` voor rood en `'green'` voor groen | `string` | `''`
screen | Op welke scherm(en) de button staat | `string` of `list<string>` | `''`
img | De bestandsnaam voor een plaatje | `string` | `''`
alignment | De tekstpositie: `LEFT`, `CENTER` of `RIGHT` | | `CENTER`

**Voorbeeld**: `Buttons['hello'] = Button('hello', 'Hello world!', 10, 10, 300, True, True, '')`  
Deze code voegt een nieuwe regel toe aan de dictionary, met als key de string `'hello'` en value een Button class object.  
Het is de bedoeling dat je deze code in je `setup()` functie zet, zodat deze code alleen eenmalig wordt uitgevoerd bij het opstarten van je programma.



### <a id='squarebutton'>SquareButton</a>
Een SquareButton is een knop waar je met je muis op kunt klikken, een squarebutton heeft altijd een vierkante vorm.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de button | `string`
t | De tekst dat op de button komt de staan| `string`
x | De x-positie | `int`
y | De y-positie | `int`
s | De lengte en breedte van de button | `int`
visible | Of de button zichtbaar is | `boolean` | `True`
enabled | Of er op de button geklikt kan worden | `boolean` | `True`
bgcolor | `''` voor grijs, `'red'` voor rood en `'green'` voor groen | `string` | `''`
screen | Op welke scherm(en) de button staat | `string` of `list<string>` | `''`
img | De bestandsnaam voor een plaatje | `string` | `''`
alignment | De tekstpositie: `LEFT`, `CENTER` of `RIGHT` | | `CENTER`

**Voorbeeld**: `SquareButtons['hello'] = SquareButton('hello', 'Hello world!', 20, 60, 250, True, True, '')`



###  <a id='label'>Label</a>
Een Label is een stuk tekst.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de label | `string`
t | De tekst voor de label | `string` | 
x | De x-positie | `int`
y | De y-positie | `int`
bold | Of de tekst groot en dikgedrukt is | `boolean`
alignment | De uitlijning: `LEFT`, `CENTER` of `RIGHT` |
visible | Of de label zichtbaar is | `boolean` | `True`
screen | Op welke scherm(en) de label staat | `string` of `list<string>` | `''`

**Voorbeeld**: `Labels['hello'] = Label('hello', 'Hello world!', 5, 320, False, LEFT, True)`



###  <a id='panel'>Panel</a>
Een panel is een rechthoekig vak.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de panel | `string`
x | De x-positie | `int`
y | De y-positie | `int`
w | De breedte | `int`
h | De hoogte | `int`
mode | Hoe de panel eruit ziet (zie tabel hieronder) | `string`
visible | Of de panel zichtbaar is | `boolean` | `True`
screen | Op welke scherm(en) de panel staat | `string` of `list<string>` | `''`

Mode | Beschrijving
--- | ---
`''` | standaard (grijs)
`'highlight'` | gemarkeerd (lichtgrijs)
`'alpha'` | doorzichtig (grijs)
`'red'` | rood
`'green'` | groen
`'blue'` | blauw
`'yellow'` | geel

**Voorbeeld:** `Panels['hello'] = Panel('hello', 20, 350, 100, 50, '', True)`



### <a id='inputfield'>InputField</a>
Een InputField is een veld waarin getypt kan worden door de gebruiker.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de input field| `string`
placeholder | De placeholder tekst dat binnen de input field komt te staan als het leeg is| `string`
x | De x-positie | `int`
y | De y-positie | `int`
w | De breedte | `int`
visible | Of de input field zichtbaar is | `boolean` | `True`
enabled | Of de input field ingeschakeld is | `boolean` | `True`
startWithCapitalLetter | Of de input field altijd met een hoofdletter moet beginnen | `boolean` | `False`
screen | Op welke scherm(en) de input field staat | `string` of `list<string>` | `''`

**Voorbeeld:** `InputFields['hello'] = InputField('hello', 'voer tekst in', 10, 10, 300)`



### <a id='listbox'>ListBox</a>
Een ListBox is een lijst waar items toegevoegd en verwijderd kunnen worden.

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de ListBox | `string`
listItems | Een lijst van de items die in de ListBox staan | `list`
x | De x-positie | `int`
y | De y-positie | `int`
w | De breedte | `int`
h | De hoogte | `int`
visible | Of de ListBox zichtbaar is | `boolean` | `True`
screen | Op welke scherm(en) de ListBox staat | `string` of `list<string>` | `''`

**Voorbeeld:** `ListBoxes['hello'] = ListBox('hello', ['a', 'b', 'c'], 10, 10, 300, 200)`



### <a id='image'>Image</a>
Een Image is een afbeelding. Het kan eventueel als een Button gebruikt kan worden

Eigenschap | Beschrijving | Type | Standaard
--- | --- | --- | ---
name | De unieke naam voor de ListBox | `string`
x | De x-positie | `int`
y | De y-positie | `int`
w | De breedte (zet op `-1` voor originele grootte) | `int`
h | De hoogte (zet op `-1` voor originele grootte) | `int`
img | De bestandsnaam van de afbeelding | `string`
scaling | Schaling van de afbeelding (`1.0` staat voor 100%, `0.5` voor 50%, `2.0` voor 200% etc.) | `float` | `1`
a | Alpha: De zichtbaarheid van de afbeelding (`255` staat voor 100%) | `float` | `255`
isButton | Of de Image een Button is | `boolean` | `False`
visible | Of de ListBox zichtbaar is | `boolean` | `True`
screen | Op welke scherm(en) de ListBox staat | `string` of `list<string>` | `''`

**Voorbeeld:** `Images['hello'] = Image('hello', 10, 10, -1, -1, 'hello.png', CORNER)`


## <a id='user-interface-functies'>User Interface Functies</a>



### <a id='setscreen'>setScreen(*`screen`*)</a>

Verandert het scherm waar de gebruiker op staat

Argument | Beschrijving | Type
--- | --- | ---
screen | De naam van het scherm | `string`

**Voorbeeld:** `setScreen('hello')`



### <a id='buttonpress'>buttonPress(*`button`*)</a>

Controleert of er op een Button is geklikt, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
button | De unieke naam van de Button | `string`

**Voorbeeld code**:

```python
if buttonPress('test'):
    Buttons['test'].enabled = False
    Buttons['test'].t = "Clicked!"
```



### <a id='squarebuttonpress'>squareButtonPress(*`button`*)</a>

Controleert of er op een SquareButton is geklikt, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
button | De unieke naam van de SquareButton | `string`


### <a id='imagePress'>imagePress(*`image`*)</a>

Controleert of er op een Image is geklikt, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
image | De unieke naam van de Image | `string`



### <a id='overbutton'>overButton(*`button`*)</a>

Controleert of de muis boven een Button staat, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
button | De unieke naam van de Button | `string`



### <a id='oversquarebutton'>overSquareButton(*`button`*)</a>

Controleert of de muis boven een SquareButton staat, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
button | De unieke naam van de SquareButton | `string`


### <a id='overimage'>overImage(*`image`*)</a>

Controleert of de muis boven een Image staat, zo ja return `True`, anders `False`

Argument | Beschrijving | Type
--- | --- | ---
image | De unieke naam van de Image | `string`
