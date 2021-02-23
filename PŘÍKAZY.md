# Základní příkazy
* [Více rozepsaný seznam příkazů a jejch užití zde:](https://cs.wikibooks.org/wiki/Linux:P%C5%99ehled_z%C3%A1kladn%C3%ADch_p%C5%99%C3%ADkaz%C5%AF)
## Práce se soubory a adresářy
* mkdir 
  * mkdir slouží na vytváření adresářů: 
    * `mkdir ovoce`
   * dá se vytvářet i více adresářů najednou: 
    * mkdir ovoce zelenina
  * s přepínačem -p se dají dělat i podadresáře:
    * `mkdir ovoce/hrušky zelenina/okurky`
* cd
  * cd slouží pro přepínání pracovního adresáře
    * `cd / (přepne do kořenového adresáře)`
    * `cd ovoce`
    * `cd ovoce/hrušky`
* pwd
  * pwd vypíše cestu ve které se nacházíme
* rmdir
  * rmdir pro mazání prázdných adresářů
    * `rmdir ovoce zelenina`
* ls
  * ls vypíše všechny soubory
* touch
  * touch vytváří prázdné soubory
* mv
  * mv přesouvá 
* cp
  * cp slouží pro kopírování souborů
  * `cp -r` zkopíruje celé adresáře
* ln
  * ln vytváří propojení mezi soubory, jeden soubor může odkazovat na jiný
* rm
  * rm se používá na mazání souborů 
  * `rm -rf` smaže adresář i soubory v něm
## Práva
* Formát práv: typ souboru - vlastník - skupina - kdokoliv jiný 
* Typ souboru: (- normální soubor), (d - adresář), (l - odkaz)
* chmod
  * chmod slouží pro změnu práv
  * chmod si bere jako první argument jeden ze 4 přepínačů a - Pro všechny u - Pro uživatele g - Pro skupinu o - Pro ostatní
  * Pro přidání oprávnění se používá + a pro odebrání -
    * `chmod a+r jménosouboru #Nyní budou všichni moct číst soubor`
    * `chmod ug+rw jménosouboru # Nyní může uživatel i skupina číst a zapisovat do souboru`
* chown
  * chown mění vlastníka souboru
    * `chown uživatelskéjméno jménosouboru`
* chgrp
  * chgrp změní skupinu pro soubor
    * `chown jménoskupiny jménosouboru`
## Obsah souborů
* | slouží pro slučování příkazů
* cat
  * používá se hlavně s | aby načetl obsah do dalšího příkazů
  * pomocí cat můžeme slučovat obsah více souborů do jednoho
    * `cat jmenosouboru1.txt jemnosouboru2.txt > sloučenésoubory.txt #Sloučí a uloží do nového souboru`
    * `cat jmenosouboru1.txt jemnosouboru2.txt | sort > sloučenésoubory.txt #Užitečný příkaz jenž je seřadí a potom uloží do nového souboru`
* less
  * slouží k vypsání obsahu souboru
    * `less jménosouboru`
* tail
  * vypíše poslední řádek/y
  * `tail -n 10 jmenosouboru #Vypíše posledních 10 řádků`
  * `tail -n +10 jmenosouboru #Vypíše vše nad posledními desíti řádky`
* head
  * vypíše první řádek/y
  * `head -n 10 jmenosouboru #Vypíše prvních 10 řádků`
* find
  * slouží pro hledání souborů nebo adresářů
    * je komplikovaný na zadání zpaměti!
    * `find . -name '*.js' #vyhledá všechny soubory s koncovkou js v aktuálním adresáři `
* wc
  * wc vypíše kolik slov obsahuje soubor
    * `wc soubor`
    * `wc soubor1 soubor2 soubor3`
    
## [Kompletní seznam příkazů ANGLICKY](https://en.wikipedia.org/wiki/List_of_Unix_commands)
## [Kompletní seznam příkazů ČESKY](https://cs.qaz.wiki/wiki/List_of_Unix_commands)
* Při práci s textem hledejte příkazy v kategorii Text processing	(head,tail,wc,...)
* Při práci v systému hledejte příkazy v kategorii Filesystem (cd,mkdir,...)
