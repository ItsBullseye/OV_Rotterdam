# OV_Rotterdam

* [User Interface Classes](#user-interface-classes)
    * [Button](#button)
    * [SquareButton](#squarebutton)
    * [Label](#label)
    * [Panel](#panel)
    * [InputField](#inputfield)
    * [ListBox](#listbox)
* [User Interface Functies](#user-interface-functies)
    * [setScreen()](#setscreen)
    * [buttonPress()](#buttonpress)
    * [squareButtonPress()](#squarebuttonpress)
    * [overButton()](#overbutton)
    * [overSquareButton()](#oversquarebutton)

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
screen | Op welke scherm(en) de button staat | `string` of `list (string)` | `''`
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
visible | Of de button zichtbaar is | `boolean`
enabled | Of er op de button geklikt kan worden | `boolean` | `True`
bgcolor | `''` voor grijs, `'red'` voor rood en `'green'` voor groen | `string` | `''`
screen | Op welke scherm(en) de button staat | `string` of `list (string)` | `''`
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
visible | Of de label zichtbaar is | `boolean`
screen | Op welke scherm(en) de label staat | `string` of `list (string)` | `''`

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
visible | Of de panel zichtbaar is | `boolean`
screen | Op welke scherm(en) de panel staat | `string` of `list (string)` | `''`

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



### <a id='listbox'>ListBox</a>
Een ListBox is een lijst waar items toegevoegd en verwijderd kunnen worden.



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
