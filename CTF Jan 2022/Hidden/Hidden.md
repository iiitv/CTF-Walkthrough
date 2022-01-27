# Hidden - Forensics

## Link to the Question

[Click here](https://ililiil.herokuapp.com/)


## Answer

```
flag{s0methingIsHidd3nH3r3}
```

## Solution

The Page is pretty simple just two headings.

First Heading `I'm 󠁦󠁬󠁡󠁧󠁻󠁳󠀰󠁭󠁥󠁴󠁨󠁩󠁮󠁧󠁉󠁳󠁈󠁩󠁤󠁤󠀳󠁮󠁈󠀳󠁲󠀳󠁽Hidden󠁦󠁬󠁡󠁧󠁻󠁳󠀰󠁭󠁥󠁴󠁨󠁩󠁮󠁧󠁉󠁳󠁈󠁩󠁤󠁤󠀳󠁮󠁈󠀳󠁲󠀳󠁽`
Second Heading `:up: That's called Hide in plain sight :up:`

According to this First heading is hidden in plain sight.

Count total number of letters in First Heading.

![](./char_counter.png)

We can see that there are total of `10` letters in First Heading.

So we can conclude that there is zero width characters in First Heading.

Try searching for `zero width steganography decoder` in google.

You will find this [decoder](https://www.irongeek.com/i.php?page=security/unicode-steganography-homoglyph-encoder) in google.

Decode the First Heading.

![](./decoder.png)

So Flag is `flag{s0methingIsHidd3nH3r3}`
