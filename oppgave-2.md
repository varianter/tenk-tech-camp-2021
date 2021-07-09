# Oppgave 2: Synths

Synths eller synthesiser er i hovedsak et fancy ord for elektronisk genererte lyder. I Sonic Pi har vi mange å velge mellom. 

## a) Prøv ut noen av synthene
Som standard bruker Sonic Pi `:beep`. Men du kan endre  denne ved å legge til funksjonen `use_synth` øverst i koden før første play: 
```ruby
use_synth :tb303

play 60
```

Tips: 
* Du kan se listen over alle tilgjengelige synther hvis du klikker på "Synths" nederst i hjelp-panelet. 
* Du kan endre synth flere ganger i koden. 

## b) Endre amplitude, panorering og release/fade out

`play` er en funksjon som tar inn mange ulike options/opsjoner eller alternativer. Noen av disse er `amp`, `pan`, og `release`. Disse opsjonene/alternativene gjør at vi kan endre hvordan play funksjonen spiller av lyden vår. 

- `amp` - Amplitude. Hvor sterkt eller svakt lyden skal spilles. Hvor 1 er normalt, mindre enn 1 er svakere og høyere enn 1 er sterkere. 
- `pan` -  Panorering. Styrer om lyden skal spilles på høyre eller venstre høytaler/airpod etc. 
`pan 0` vil si at det spilles likt på begge sider, `pan 1` vil si bare på høyre side, og `pan -1` vil si bare på venstre side. 
- `release` - Eller fade out, er tiden det tar for at lyden har "fadet ut". Standard er `release 1` som er ett sekund. 

Lag et ekko som går fra øre til øre, ved å bruke de tre opsjonene ovenfor. Eksempel på hvordan du kan begynne: 

```ruby
use_synth :blade

play 60, pan: -1, amp: 3, release 1
sleep 1
play 60, pan: 1, amp: 2, release 1

```

<details>
<summary>Løsningsforslag</summary>

```ruby
use_bpm 100
use_synth :blade

play 60, pan: 1, amp: 3, release: 3
sleep 1
play 60, pan: -1, amp: 2, release: 3
sleep 1
play 60, pan: 1, amp: 1, release: 3
sleep 1
play 60, pan: -1, amp: 0.5, release: 3
sleep 1
play 60, pan: 1, amp: 0.25, release: 3
sleep 1
play 60, pan: -1, amp: 0.15, release: 3
```

</details>



