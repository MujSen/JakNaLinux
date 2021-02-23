## Základ
1. musíme vždy označit na začátku soubor jako spustitelný pomocí chmod +x
2. Každý soubor musí mít označení, že má být spuštěn přes bash
* #!/bin/bash 
* 
## Proměnné
* Ukládání do proměnných
* Aritmetické operace
  * Píší se vždy v  $((  ))
  * Aritmetické znaménka máme: +; -; /; *; **; % (** - znamená na druhou, na třetí)
  * Příklad:
    ```bash
      $(( 10 + 3 )), výsledek=13
      $(( 10 - 3 )), výsledek=7
      $(( 10 * 3 )), výsledek=30
      $(( 10 / 3 )), výsledek=3
      $((  10 ** 3 )), výsledek=1000
      $(( 10 % 3 )), výsledek=1
    ```
  * Slovíčko let nám dovoluje zapsat aritmetické operace i takto:
    ```bash	
      x=10
      let "x += 3" || let "x -= 3" || let "x *= 3" || let "10 /= 3" || let "10 %= 3"  #|| je zde použito jen na ukázání možností
      echo $x
      výsledek=13  ||     7        || 30            ||        3             ||    1
    ```
   * Ukládání do proměnných
    ```bash	
      proměnná=3
    ```
    * !Nikdy nedávejte mezeru před nebo za!
    * Když uděláte 
    ```bash	
      proměnná= 3
      //Error 3 není příkaz
    ```
    ```bash	
      proměnná =3
      //Error proměnná není příkaz
    ```
    ```bash	
      proměnná=3
      //Když bude před proměnnou mezera tak se nic nestane
    ```
## If (jestli)
    ```bash	
      if [ výraz ];
      then  
      příkazy  
      fi  
    ```
 * Nejtypičtější výrazy: -eq -gt -lt -d -e -r -s -w -x -n -z ! == !=
 * Můžeme použít operátory || nebo && a
    ```bash	
      if [ výraz ] || [ výraz ];
      then  
      příkazy  
      fi  
    ``` 
 * Když chceme více výrazů než dva
    ```bash	
      if [ výraz && výraz || výraz ]; 
      then  
      příkazy  
      fi  
    ```
 * Použití else if a else
    ```bash	
      if [ výraz ];  
      then  
      příkazy 
      elif [ výraz ];  
      then  
      příkazy
      else  
      příkazy
      fi  
    ```
  *
## Smyčky
  * for (pro)
    ```bash	
      for letadlo in $letadla
      do  
      echo $letadlo  
      done  
    ```
    ```bash	
      for ((i=1; i<=10; i++))  
      do  
      echo "$i"  
      done  
    ```
    ```bash	
      for num in {1..10}  
      do  
      echo $num  
      done   
    ```
  * while (pokud)
    ```bash	
      while [ výraz ];  #Stejné jako u if
      do  
      příkazy   
      done     
    ```
  * until (dokud) Je stejný jako while 😊
    ```bash	
      until [ výraz ];  
      do  
      příkazy  
      done     
    ```
  * 
