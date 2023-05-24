## Description

Write a function, which takes a non-negative integer (seconds) as input and returns the time in a human-readable format (HH:MM:SS)

``` HH ``` = hours, padded to 2 digits, range: 00 - 99

``` MM ``` = minutes, padded to 2 digits, range: 00 - 59

``` SS ``` = seconds, padded to 2 digits, range: 00 - 59
The maximum time never exceeds 359999 (99:59:59)

You can find some examples in the test fixtures.


**First:**
```javascript
function humanReadable(seconds) {
  let horas = "00";
  let minutos = "00";
  let segundos = "00";

  horas = String(parseInt(seconds / 3600));
  minutos = String(parseInt((seconds - horas * 3600) / 60));
  segundos = String(parseInt(seconds - (horas * 3600 + minutos * 60)));

  horas = horas.length < 2 ? `0${horas}` : horas;
  minutos = minutos.length < 2 ? `0${minutos}` : minutos;
  segundos = segundos.length < 2 ? `0${segundos}` : segundos;

  return `${horas}:${minutos}:${segundos}`;
}
```

