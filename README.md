<h1 align="center">Welcome to farbprinter</h1> 


> Let's bring a little bit of color in our grey ~~life~~ terminal!
>
> [Github](https://github.com/hansalemaos/Farbprinter/) 
>
> [PyPi](https://pypi.org/project/farbprinter/)

## Prerequisites

**requirements**

- Pillow

- python-box

- addict

- pyfiglet

- ansi

  ***tested on Python 3.8 and Windows 10***

## Install

```sh
pip install farbprinter
```

## Author

**Johannes Fischer aka Hans Alemão**

* Website: https://www.queroestudaralemao.com.br/
* Github: [@hansalemaos](https://github.com/hansalemaos)

<h2>How to use</h2>





## 1st - import



Let's import **Farbprinter** and create an instance which we creatively call **drucker** *(google it if you want to find out what it means! :-)* ) 

```python
from farbprinter.farbprinter import Farbprinter
drucker = Farbprinter()
```



### 2nd - overview - functions (methods) / attributes

Let's start with an overview of all important functions (methods) and attributes of the class **Farbprinter**

```python
#Functions
drucker.p_ascii_font_2_colors()
drucker.p_ascii_font_on_flag()
drucker.p_ascii_front_on_flag_with_border()
drucker.p_pandas_list_dict()
drucker.p_picture_to_ascii_art()
drucker.p_show_all_color_combinations()

#Attributes 
drucker.p #-> p for "print" (very creative, right?)
drucker.f # -> f for "format" 
```

As you can see, all functions that matter start with the prefix **p_** I think it is pretty clear what they can be used for *(at least for me, hahaha)*. Scroll down if you want to see detailed examples for each one of them. **The names of the attributes "p" and "f" are anything but self-explaining. Since they are the "heart" of the class, let's talk about them first!**

### <br>2nd - Farbprinter.p  and Farbprinter.f 

By using the attribute "**f**", you can access the *lambda functions* in the "**format-dict**" which allow you to format strings and use them anywhere you want. If you are impatient and want to print them right away, use the "**p**" attribute to access the lambda functions in the "**print-dict**"!

```python
drucker.f.red.black.italic('Wie geht es dir?')
'\x1b[3m\x1b[41m\x1b[30mWie geht es dir?\x1b[3m\x1b[0m'  #formated string

drucker.p.red.black.italic('Wie geht es dir?')
drucker.p.yellow.blue.bold('Ich bleibe hier')
```



![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme01.png?raw=true)



And now the best part… Since **Farbprinter** was made for lazy people by someone lazy, it supports **auto-completion** in **PyCharm** and other IDEs.

![](https://github.com/hansalemaos/Farbprinter/blob/main/pic_for_readme14.png?raw=true)



Well, once you press the "**magic dot key for lazy people**" on your keyboard, you will find out that there are many color combinations (what a surprise, right?) If you want to spend the whole weekend choosing the right one(s) for you, you can use 

```
drucker.p_show_all_color_combinations() 
```

to… guess what ... **to see all colo(u)r combinations** 

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme02.png?raw=true)



### 3rd - Is it a pirate's parrot or a pandas DataFrame? 

Since [pandas](https://github.com/pandas-dev/pandas) is one of the greatest things mankind has ever invented, I had to honor it somehow.I thought that making a pirate's parrot out of a DataFrame would be a great start! :-) Just use

```python
drucker.p_pandas_list_dict(df)
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme04.png?raw=true)



If the data in DataFrame's cells is so big, that you could wrap it 10 times around your belly even after a 16 X 16 at In-N-Out-Burger, you can crop it (the DataFrame, not your belly). Just use:

```python
drucker.p_pandas_list_dict(df, linebreak=10)
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme05.png?raw=true)

### <br>4th - Lists and dictionaries from San Francisco - 1968

If a pandas DataFrame could easily be confused with the album's cover of Jimi Hendrix' "Axis: Bold as Love", it should also be possible for lists and dictionaries, right?

```python
#Let's create a list containing German vocabulary
liste = ['(amtliches) Schreiben {n}', '(an jdn./etw.) glauben', '(aus etw.) bestehen', '(automatischer) Ausschalter {m}', '(automatischer) Schaltmechanismus {m}', '(bei etw.) ein Auge zudrücken', '(Chinesische) Samtpappel {f}', '(Chinesische) Samtpappel {f}', '(dicke) Jacke {f}', '(die) Schuld haben', '(die) Schuld haben', '(eine Tätigkeit) aufnehmen', '(Es) ist okay! {n} [ugs.]', '(etw. [Akk.]) essen', '(Europäischer) Feldhase {m}', '(ganz) im Gegenteil', '(gellender) Schrei {m}', '(hohes) Alter {n}', '(in) die Hand beißen, die einen füttert', '(in der) Schlange stehen', '(in die Luft) sprengen', '(in die Luft) sprengen', '(jdn.) um Hilfe bitten', '(Kalifornischer) Eselhase {m}', '(Kalifornischer) Eselhase {m}', '(kleine) Bucht {f}', '(miteinander) verflechten', '(mit jdm.) verwandt sein', '(Nasen-) Nebenhöhlenentzündung {f}', '(nicht) von Belang sein', '(nicht) von Belang sein', '(noch) ein Ass im Ärmel haben [fig.]', '(Schwarzer) Degenfisch {m}', '(sehr) fleißig', '(sehr) wenig', '(sich) ablösen', '(sich) beugen', '(sich) kauern', '(sich) reimend', '(sich) versehen mit']

#and now...
drucker.p_pandas_list_dict(liste)


```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme06.png?raw=true)



Nested lists? No problem! Let's show Jupyter who we are! 

```python
liste_deutsch_portugiesisch = [['(amtliches) Schreiben {n}', '(an jdn./etw.) glauben', '(aus etw.) bestehen', '(automatischer) Ausschalter {m}', '(automatischer) Schaltmechanismus {m}', '(bei etw.) ein Auge zudrücken', '(Chinesische) Samtpappel {f}', '(Chinesische) Samtpappel {f}', '(dicke) Jacke {f}', '(die) Schuld haben'], ['ofício {m}', 'crer (em alguém/algo)', 'consistir (em / de algo)', 'disjuntor {m}', 'disjuntor {m}', 'fazer vista grossa (para algo)', 'juta {f} da China [Abutilon theophrasti, syn.: A. avicennae, Sida abutilon]', 'juta {f} de Tien-Tsin [Abutilon theophrasti, syn.: A. avicennae, Sida abutilon]', 'japona {f}', 'ser culpado']]

#go and get a partner!
drucker.p_pandas_list_dict(liste_deutsch_portugiesisch)


```



![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme07.png?raw=true)



If you don't like all those beautiful, paired up German / Portuguese words on top of each other, then [keep them separated](https://www.youtube.com/watch?v=8FWdQVNeTlI) with:

```python
drucker.p_pandas_list_dict(liste_deutsch_portugiesisch, listtranspose=True)
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme08.png?raw=true)

Are you still nagging? And what if I offered you … some beautiful yellow headers? For your nested list! I am serious! All free of charge! 

```python
drucker.p_pandas_list_dict(liste_deutsch_portugiesisch, listtranspose=True, header=['de', 'pt'])
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme09.png?raw=true)



Dictionaries are like divas - beautiful, elegant, but need an exceptional treatment, if you prefer not to have thrown exceptions in your face every time you ask the diva for a favor. The good news is, you can print those divas as well, the bad: they don’t look great when they are nested! But hey, at least you can transpose them (and even pass a tiny little cute header for the key/value pair.)

```python
pt_de_dict = {}
pt_de_dict['das Wort'] = 'a palavra'
pt_de_dict['das Haus'] = 'a casa'
pt_de_dict['die Frau'] = 'a mulher'
print(pt_de_dict)
drucker.p_pandas_list_dict(pt_de_dict, listtranspose=False)
drucker.p_pandas_list_dict(pt_de_dict, listtranspose=True)
drucker.p_pandas_list_dict(pt_de_dict, listtranspose=False, header=['de', 'pt'])
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme10.png?raw=true)



### <br>5th - Picture to ASCII/ANSI/whatever art

If you want to surprise your eight-year-old daughter, take a picture of her and turn it/her into a letter soup using: 

```python
drucker.p_picture_to_ascii_art(picture_path=r"dukotztmichan.png",
letter_for_ascii_art='QUEROESTUDARALEMAO.COM.BR-',
contrast=1,
desired_width=60,
savetopath=None,
printpicture=True,
black_and_white=False,
black_and_white_thresh=50,
rgb8_16_256=256)
```

This transforms any picture into ASCII Art (Is that what it is called??) There are some arguments you can pass, all kind of self explaining (at least for me :-) ).Play around with them. I haven't written neither doc strings nor type hints yet, but will do soon! (Shame on me) ***If you go to the source code,don't be surprised if you encounter variables with strange names, mixing up English with German (and Portuguese sometimes, [to make it worse hahaha]).***

| ![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme13.png?raw=true) | ![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme03.png?raw=true) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |



### <br>6th - Text to ASCII/ANSI/whatever art 

Let's impress our kids a little more by showing them how the world was when we were kids, and would get into trouble playing Commander Keen during word-processing class in school!

Let's print some ASCII/ANSI/font (I never know how it is actually called)

```python
drucker.p_ascii_font_2_colors(text='Hallo, Welt, alles fit?', colorfunction=drucker.f.black.yellow.bold, font='puffy',width = 1000, offset_from_left_side=25, offset_from_text=5)

```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme11.png?raw=true)



If you really want to get this "Back to the Future feeling" and see a list of all available fonts, just pass "None" as font:

```python
drucker.p_ascii_font_2_colors(text='Hallo, Welt, alles fit?', colorfunction=drucker.f.black.yellow.bold, font=None,width = 1000, offset_from_left_side=25, offset_from_text=5)
```



![](https://github.com/hansalemaos/Farbprinter/blob/main/pic_for_readme15.png?raw=true)



Or do you want to have some kind of flag with multiple colors as background? Since I am not a programmer, but a German teacher, let's use the German flag

```python
colorfunctions = [drucker.f.black.brightyellow.normal, drucker.f.brightred.black.normal,                 drucker.f.brightyellow.black.normal]

drucker.p_ascii_font_on_flag(text='Lern Deutsch mit mir!', colorfunctions=colorfunctions, font='doom', width=1000, offset_from_left_side=25,offset_from_text=5)
```

![](https://github.com/hansalemaos/Farbprinter/blob/becb9e516fade66de729a300186f3da5123b0da7/pic_for_readme12.png?raw=true)

Since the German flag is not one of the most creative flags on the planet, let's reinvent it and give add a border and some new colors/colours.

```python
colorfunctions = [drucker.f.black.red.normal, drucker.f.black.white.normal]
drucker.p_ascii_front_on_flag_with_border(text='Lern Deutsch mit mir!',colorfunctions=colorfunctions, bordercolorfunction=drucker.f.brightmagenta.brightcyan.negative, font='xtimes',width = 1000, offset_from_left_side=5, offset_from_text=15)
```



![](https://github.com/hansalemaos/Farbprinter/blob/main/pic_for_readme16.png?raw=true)

Beautiful new German flag! [Adenauer](https://en.wikipedia.org/wiki/Konrad_Adenauer) would turn in his grave. 

That's it! Have fun! :-) 

## Thanks to:

the creators of the packages I used: 

[ansi]: https://github.com/tehmaze/ansi/
[pyfiglet]: https://github.com/pwaller/pyfiglet
[addict]: https://github.com/mewwts/addict
[python-box]: https://github.com/cdgriffith/Box
[Pillow]: https://pypi.org/project/Pillow/



## Contributing

Like I mentioned above, I am not a professional programmer, but a German teacher. This year I had to spend 3 months in hospital due to a bone infection. I started learning Python there to kill time. 
My main intention is creating tools that will help others expanding their German knowledge. I published Farbprinter because I will be using it in almost all those tools and I think it might be useful for others because it combines all important features for a real "Back to the Future feeling" hahaha.

**Contributions, issues, and feature requests are welcome!**

About 20 to 25 years ago, I learned some QBasic, C, Java, JavaScript, PHP, and MySQL, but never got further than a simple calculator. Back then, it was so hard getting good information. It is amazing to see how things have changed! Nowadays it is possible to create something really useful in a short period of time! Awesome!

Give a star if this project helped you!

## License

Copyright © 2021 [Johannes Fischer aka Hans Alemão](https://queroestudaralemao.com.br).<br />
This project is MIT licensed.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

***
_This README was generated by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
