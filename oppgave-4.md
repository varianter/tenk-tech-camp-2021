# Samples og live loop

## a) Bruk en sample i en live_loop
Sample, eller et lydklipp, er et kort opptak av en lyd som kan benyttes til å lage musikk. Sonic Pi har mange ulike samples man kan bruke. Et eksempel er:

```ruby
sample :bd_haus
```
Eller hva med et lengre sample:
```ruby
sample :loop_amen
```

Tips: 
* Du finner en liste over alle tilgjengelige samples i hjelp-panelet nederst i venstre hjørne. 

Vi vil gjerne at disse lydklippene skal spille i loop og helst vil vi kunne spille flere samtidig. Dette kan vi få til med funksjonen `live_loop`, alt vi trenger å gjøre er å gi den et navn:

```ruby
live_loop :en_loop do
  play 54
  sleep 0.5
end
```
Prøv å lag din egen live loop med en eller flere samples.
<details>
<summary>Løsningsforslag</summary>

```ruby
live_loop :dette_er_bass do
  sample :bd_haus, amp: 5, release: 8
  sleep 0.5
end
```
</details>


## b) Lag din egen beat med flere live loops

Lag din egen beat. Bruk flere live loops og ulike samples.

<details>
<summary>Løsningsforslag</summary>

```ruby
live_loop :bass do
  sample :bd_haus, amp: 5, release: 8
  sleep 0.5
end

live_loop :snare do
  sync :bass
  sample :sn_dolf
  sleep 0.5
end

live_loop :hihat do
  sync :bass
  sleep 0.25
  sample :drum_cymbal_closed
  sleep 0.5
  sample :drum_cymbal_pedal
end


```
</details>