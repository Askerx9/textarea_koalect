# textarea — Koalect
I use Vue-cli

[result](https://vigilant-wilson-97b24f.netlify.com)
## Project setup
```
npm install
```
## docs

DATA:
 - value: text I type in the textearea
 - charMax: maxlength for textarea and to calculator how many characters left

COMPUTED:
 - charLeft: calcul to display how many characters left with maxlength - value.length

COLOR: I check if charLeft is 0 (false) if this condition is true then I apply class "text--alert"
