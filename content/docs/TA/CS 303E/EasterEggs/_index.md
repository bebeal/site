---
weight: 22
title: Easter Eggs
---

# Easter Eggs

---

Here's some mildly interesting things about Python. Some are actual ["Easter Eggs"](https://en.wikipedia.org/wiki/Easter_egg_(media)) other's are just things I find fun (exploits, odd outcomes, etc). 

"Why are there so many links?" - For the overly curious rabbit.


## Hello World

"In order to test the support for frozen modules, by default we define a single frozen module, __hello__.  Loading it will print some famous words..." - [Source Code](https://github.com/python/cpython/blob/8c77b8cb9188165a123f2512026e3629bf03dc9b/Python/frozen.c)



```python
>>> import __hello__
Hello world!
```


 ## The Zen of Python
 
 Introduced in [PEP 20](https://www.python.org/dev/peps/pep-0020/#id2) in 2004, and originally posted in 1999 under a thread called ["The Way of Python"](https://groups.google.com/d/msg/comp.lang.python/B_VxeTBClM0/L8W9KlsiriUJ) - Long time Pythoneer [Tim Peters](https://en.wikipedia.org/wiki/Tim_Peters_(software_engineer)) succinctly channels the [BDFL's](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life#:~:text=Benevolent%20dictator%20for%20life%20(BDFL,or%20arguments%20within%20the%20community.)) guiding principles for Python's design into 20 aphorisms, only 19 of which have been written down (one was left for [Guido van Rossum](https://en.wikipedia.org/wiki/Guido_van_Rossum), the creator of Python, to fill in). In May 2020, [Barry Warsaw](https://www.oreilly.com/library/view/python-interviews/9781788399081/ch09.html#:~:text=Barry%20Warsaw%20is%20an%20American,Python%20Foundation%20team%20at%20LinkedIn.&text=He%20was%20the%20project%20leader,manager%20and%20member%20of%20PythonLabs.) performed a [musical rendition](https://www.youtube.com/watch?v=i6G6dmVJy74&feature=youtu.be) of the aphorisms, which he blogged about [here](https://www.wefearchange.org/2020/05/zenofpython.rst.html).

 ```python
 >>> import this
 ```

{{< details title="Output" open=false >}}

```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

{{< /details >}}


### The Irony

The intentional irony behind the Zen of Python is that the `this.py` module itself violates nearly every aphorism. The module is implemented as a [ROT13](https://en.wikipedia.org/wiki/ROT13) cipher.

```python
s = """Gur Mra bs Clguba, ol Gvz Crgref
Ornhgvshy vf orggre guna htyl.
Rkcyvpvg vf orggre guna vzcyvpvg.
Fvzcyr vf orggre guna pbzcyrk.
Pbzcyrk vf orggre guna pbzcyvpngrq.
Syng vf orggre guna arfgrq.
Fcnefr vf orggre guna qrafr.
Ernqnovyvgl pbhagf.
Fcrpvny pnfrf nera'g fcrpvny rabhtu gb oernx gur ehyrf.
Nygubhtu cenpgvpnyvgl orngf chevgl.
Reebef fubhyq arire cnff fvyragyl.
Hayrff rkcyvpvgyl fvyraprq.
Va gur snpr bs nzovthvgl, ershfr gur grzcgngvba gb thrff.
Gurer fubhyq or bar-- naq cersrenoyl bayl bar --boivbhf jnl gb qb vg.
Nygubhtu gung jnl znl abg or boivbhf ng svefg hayrff lbh'er Qhgpu.
Abj vf orggre guna arire.
Nygubhtu arire vf bsgra orggre guna *evtug* abj.
Vs gur vzcyrzragngvba vf uneq gb rkcynva, vg'f n onq vqrn.
Vs gur vzcyrzragngvba vf rnfl gb rkcynva, vg znl or n tbbq vqrn.
Anzrfcnprf ner bar ubaxvat terng vqrn -- yrg'f qb zber bs gubfr!"""

d = {}
for c in (65, 97):
    for i in range(26):
        d[chr(i+c)] = chr((i+13) % 26 + c)

print("".join([d.get(c, c) for c in s]))
```

### Raymond's request

Funny enough, a Fellow of the [Python Software Foundation](https://www.python.org/psf/members/) by the name of Hye-Shik Chang attempted to apply the "Simple is better than complex." aphorism to the code on February 5th 2004:

![](/~bebeal/EE/1.png)

...but quickly changed it back on the same day per "Raymond's request" which I believe refer's to the Python guru [Raymond Hettinger](https://twitter.com/raymondh?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor)


![](/~bebeal/EE/2.png)

### A Life Lesson

A fun exploit of this

```python
>>> import this
...
>>> love = this
>>> this is love
True
>>> love is True
False
>>> love is False
False
>>> love is not True or False
True
>>> love is not True or False; love is love 
True
True
```

### The Ortographical Typo

I found it funny that a [bug report](https://bugs.python.org/issue3364) was unironically issued by a user "cheDu" in which he requests the spacing in the `There should be one-- and preferably only one --obvious way to do it.` aphorism be fixed.

## Learning How to Fly

The antigravity module, referencing the [XKCD comic](https://xkcd.com/353/) mentioning Python, was added to Python 3 by [Skip Montanaro](https://github.com/smontanaro). 

```python
>>> import antigravity
```
<img src="/~bebeal/EE/3.png" width="518" height="588" class="center" />

### Origin

The [origin](http://python-history.blogspot.com/2010/06/import-antigravity.html) story from Guido:

"But it really originated in Google App Engine! It was a last-minute addition when we launched App Engine on April 7, 2008. A few weeks before launch, when most code was already frozen, the App Engine team at Google decided we wanted an easter egg. After a great many suggestions, some too complex, some too obscure, some too risky, we chose the "antigravity" module. The App Engine version is a little more elaborate than the Python 3 version: it defines a fly() function while can randomly do one of two things: with a probability of 10%, it redirects to the XKCD comic; otherwise, it simply renders the text of the comic in HTML (with a link to the comic on the last line). To invoke it in your App Engine app, you'd have to write a little main program, like this:"

```python
import antigravity

def main():
    antigravity.fly()

if __name__ == '__main__':
    main()
```

### Geohash

Examining the implementation of the `antigravity.py` module reveals a hidden function called 'geohash' which is a reference to another [XKCD comic](https://xkcd.com/426/) about [geohashing](https://geohashing.site/geohashing/Main_Page). The function uses [Randall Munroe's](https://en.wikipedia.org/wiki/Randall_Munroe) algorithm which generates random GPS coordinates each day based on the Dow Jones Industrial Average and the current date.

```python
import webbrowser
import hashlib

webbrowser.open("https://xkcd.com/353/")

def geohash(latitude, longitude, datedow):
    '''Compute geohash() using the Munroe algorithm.
    >>> geohash(37.421542, -122.085589, b'2005-05-26-10458.68')
    37.857713 -122.544543
    '''
    # https://xkcd.com/426/
    h = hashlib.md5(datedow, usedforsecurity=False).hexdigest()
    p, q = [('%f' % float.fromhex('0.' + x)) for x in (h[:16], h[16:32])]
    print('%d%s %d%s' % (latitude, p[1:], longitude, q[1:]))
```

## Indentation > Braces

Prefer C style braces instead of indentation? [Source Code](https://github.com/python/cpython/blob/314858e2763e76e77029ea0b691d749c32939087/Python/future.c)

```python
>>> from __future__ import braces
  File "<stdin>", line 1
SyntaxError: not a chance
```

## Friendly Language Uncle For Life

An April Fool's Joke (4/01), The [PEP 401](https://www.python.org/dev/peps/pep-0401/#id13) states that Guido van Rossum is stepping down. The new title given to him would be pronounced "BDEVIL" (Benevolent Dictator Emeritus Vacationing Indefinitely from the Language) and Guido's successor will be Barry Warsaw, or as he is affectionately known, Uncle Barry. Uncle Barry's official title is "FLUFL" (Friendly Language Uncle For Life):


"Guido wrote the original implementation of Python in 1989, and after nearly 20 years of leading the community, has decided to step aside as its Benevolent Dictator For Life. His official title is now Benevolent Dictator Emeritus Vacationing Indefinitely from the Language (BDEVIL). Guido leaves Python in the good hands of its new leader and its vibrant community, in order to train for his lifelong dream of climbing Mount Everest.

After unanimous vote of the Python Steering Union (not to be confused with the Python Secret Underground, which emphatically does not exist) at the 2009 Python Conference, Guido's successor has been chosen: [Barry Warsaw](https://barry.warsaw.us/), or as he is affectionately known, Uncle Barry. Uncle Barry's official title is Friendly Language Uncle For Life (FLUFL). 

<h4> Official Acts of the FLUFL </h4>

FLUFL Uncle Barry enacts the following decisions, in order to demonstrate his intention to lead the community in the same responsible and open manner as his predecessor, whose name escapes him:

* Recognized that the selection of `Hg`(https://en.wikipedia.org/wiki/Mercurial) as the [DVCS](https://en.wikipedia.org/wiki/Distributed_version_control) of choice was clear proof of the onset of the BDEVIL's insanity, and reverting this decision to switch to `Bzr`(https://bazaar.canonical.com/en/) instead, the only true choice.
* Recognized that the `!=` inequality operator in Python 3.0 was a horrible, finger pain inducing mistake, the FLUFL reinstates the `<>` diamond operator as the sole spelling. This change is important enough to be implemented for, and released in Python 3.1. To help transition to this feature, a new future statement, `from __future__ import barry_as_FLUFL` has been added.
```python
>>> from __future__ import barry_as_FLUFL
>>> 1 <> 2
True
>>> 1 != 2
  File "<stdin>", line 1
    1 != 2
       ^
SyntaxError: invalid syntax
```

* Recognized that the print function in Python 3.0 was a horrible, pain-inducing mistake, the FLUFL reinstates the print statement. This change is important enough to be implemented for, and released in Python 3.0.2.
* Recognized that the disappointing adoption curve of Python 3.0 signals its abject failure, all work on Python 3.1 and subsequent Python 3.x versions is hereby terminated. All features in Python 3.0 shall be back ported to Python 2.7 which will be the official and sole next release. The Python 3.0 string and bytes types will be back ported to Python 2.6.2 for the convenience of developers.
* Recognized that C is a 20th-century language with almost universal rejection by programmers under the age of 30, the CPython implementation will terminate with the release of Python 2.6.2 and 3.0.2. Thereafter, the reference implementation of Python will target the [Parrot](http://www.parrot.org/) virtual machine. Alternative implementations of Python (e.g. [Jython](https://www.jython.org/), [IronPython](https://ironpython.net/), and [PyPy](https://en.wikipedia.org/wiki/PyPy)) are officially discouraged but tolerated.
* Recognized that the [Python Software Foundation](https://www.python.org/psf/) having fulfilled its mission admirably, is hereby disbanded. The [Python Steering Union](http://www.pythonlabs.com/) (not to be confused with the Python Secret Underground, which emphatically does not exist), is now the sole steward for all of Python's intellectual property. All PSF funds are hereby transferred to the PSU (not that PSU, the other PSU)."

## The Answer to Life

The hash function in Python has built-in macros so that the hash of infinity is Pi. [Source Code](https://github.com/python/cpython/blob/f453221c8b80e0570066a9375337f208d50e6406/Include/pyhash.h)

```python
>>> hash(float('inf'))
314159
>>> hash(float('-inf'))
-314159
```



