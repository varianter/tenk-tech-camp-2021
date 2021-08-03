# Oppgave 3: Loop og if-else

## a) Spill av lyder flere ganger
Loop, eller løkke, er en funksjon vi bruker til å omringe noe vi ønsker å spille flere ganger, eller om og om igjen.

En loop kan spilles et bestemt antall ganger eller i det uendelige. 
Men for å lage en loop må vi si til programmet hvor loopen starter og slutter, slik at den vet hvilke lyder den skal spille av om igjen. Dette gjør vi ved å omringe koden vi vil kjøre flere ganger i en `do-end`-blokk og til slutt si hva vi vil gjøre med koden i blokken. For eksempel å kjøre den flere ganger: 

```ruby
2.times do
  play :C4
  sleep 0.5
  play :D4
  sleep 0.5
  play :E4
  sleep 0.5
  play :C4, release: 3
  sleep 0.5
end
```

Nå kan du prøve å lage flere loops. Lag din egen eller prøv å fortsett på koden ovenfor. Hører du at det er sangen Fader Jakob? Klarer du å lage mer av den? 

Tips:
* Du kan ha flere loops etter hverandre. 
* Det er også lov å lage en loop inne i en annen loop. 

<details>
<summary>Løsningsforslag</summary>

```ruby
use_synth :piano
use_bpm 70

loop do
  2.times do
    play :C4
    sleep 0.5
    play :D4
    sleep 0.5
    play :E4
    sleep 0.5
    play :C4, release: 2
    sleep 0.5
  end
  
  2.times do
    play :E4
    sleep 0.5
    play :F4
    sleep 0.5
    play :G4, release: 2
    sleep 1
  end
  
  2.times do
    play :G4
    sleep 0.25
    play :A4
    sleep 0.25
    play :G4
    sleep 0.25
    play :F4
    sleep 0.25
    play :E4
    sleep 0.5
    play :C4, release: 2
    sleep 0.5
  end
  
  2.times do
    play :C4
    sleep 0.5
    play :G3
    sleep 0.5
    play :C4, release: 2
    sleep 1
  end
end
```

</details>


## b) If-else 

If-else, eller hvis-ellers er et utrykk som vil kjøre en kode i en blokk hvis et utsagn er sant. Hvis ikke den er sann, så gjør den det som er skrevet i else blokken i stedet. 

Eks. Hvis det er brus i kjøleskapet, så ta et glass brus, ellers ta et glass vann. 

Vi kan lage en slik if-else blokk i Sonic Pi ved å bruke `one_in`-funksjonen. Den trekker et tilfeldig tall mellom de tallene du gir den og hvis du får tallet 1 så er utsagnet sant.

Eks. 

```ruby
use_synth :square

if one_in(2) # Hvis jeg trekker tallet 1 av tallene 1 og 2 
  play :B5 # så spill B5
else # ellers
  play :E6 # spill E6 
  
end
```

Lag en `loop` med en if-else blokk inni der du bruker `one_in`

Tips:

* Du kan omringe koden ovenfor i en loop om du ønsker. 
* Du kan også gi `one_in`- funksjonen flere tall. 

<details>
<summary>Løsningsforslag</summary>

```ruby

use_synth :square

loop do
  if one_in(2)
    play :B5
    sleep 0.1
    play :E6
  else
    play :G4, release: 0.035
    sleep 0.035
    play :G5, release: 0.035
    sleep 0.035
    play :G6, release: 0.035
    
    sleep 0.3
    
  end
  sleep 0.5
end

```

</details>



