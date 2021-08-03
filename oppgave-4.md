# Samples og live loop

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

Men vi vil gjerne at disse lydklippene skal spille i loop og helst vil vi kunne spille flere samtidig. Dette kan vi få til med funksjonen `live_loop`, alt vi trenger å gjøre er å gi den et navn:

```ruby
live_loop :dette_er_bass do
  sample :bd_haus, amp: 5, release: 8
  sleep 0.5
end
```

Lag din egen beat. Bruk flere live loops og ulike samples

