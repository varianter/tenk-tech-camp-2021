# Oppgave 1: Play og sleep

## a) Lag din første melodi
Kopier inn koden i Sonic Pi og trykk på "Run"-knappen (spill av) øverst i høyre hjørne

```ruby
play 60
play 63
play 68
```

Prøv så å lage din første melodi ved å legge til sleep mellom play-linjene. `sleep` forteller programmet at den må vente litt før den kan spille av neste lyd. 
<details>
<summary>Løsningsforslag</summary>

```ruby
play 60
sleep 1
play 63
sleep 1
play 68
```

</details>



## b) Nå kan du prøve å lage din egen melodi! 
Legg til dine egne `play` og `sleep`, og endre, lytt og endre igjen!

Tips: 
* Velg mellom verdier mellom 0 - 127 for `play`, der 0 er veldig mørkt og 127 er veldig lyst. 
* Legg til både korte og lange `sleep`. Eks. `sleep 0.5` eller `sleep 2`
* Du kan også bruke vanlige noter for `play` eks. `play :C` = `play 60`
* Desimalverdier er også lov! Eks. `play 60.25` og `sleep 0.2`  
* Du kan også endre takten ved å bruke funksjonen `use_bpm {takt}` i starten før første `play`-linje. Eks. `use_bpm 80` (standard er 60)


<details>
<summary>Løsningsforslag</summary>

```ruby

use_bpm 120

play 70
sleep 0.25
play 72
sleep 0.5
play 79
sleep 0.5
play 82
sleep 0.25
play 72
sleep 0.25
play 84
sleep 0.5
play 72
sleep 0.25
play 67
sleep 0.25
play 84
play 79

# Eller hva med AHA - Take on me:  

use_bpm 80

play :Fs4
sleep 0.25
play :Fs4
sleep 0.25
play :Fs4
sleep 0.25
play :D4
sleep 0.5
play :B3
sleep 0.5
play :E4
sleep 0.5
play :E4
sleep 0.5
play :E4
sleep 0.25
play :Gs4
sleep 0.25
play :Gs4
sleep 0.25
play :A4
sleep 0.25
play :B4
sleep 0.25
play :A4
sleep 0.25
play :A4
sleep 0.25
play :A4
sleep 0.25
play :E4
sleep 0.5
play :D4
sleep 0.5
play :Fs4
sleep 0.5
play :Fs4

```

</details>

