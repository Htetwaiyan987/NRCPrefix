NRCPrefix
=========

Prefixer for Myanmar National Registration Card's Format

## Match Formats

`[State Number]\[District]([NAING/N])[Register No]`

- `12/MYG(N)164516`
- `12/MYG(N)164516`
- `12/MYG(NAING)164516`

Prefer formats
- `12/MYG(N)164516`
- `12/MYG(NAING)164516`
- `၁၂/မရက(နိုင်)၁၆၄၅၁၆`

*NOTE*

Three english characters in district are not complete format and will not support some function.
So you should be use six english characters for district.

## Usage
### Get format

```js
var nrc = MMNRC("12/MYG (NAING) 164516");

nrc.getFormat() // 12/MYG(N)164516
nrc.getFormat("mm") // ၁၂/မရက(နိုင်)၁၆၄၅၁၆
```

### Test Equal

```js
var nrc = MMNRC("12/MYG (N) 164516");

nrc.isEqual('၁၂/မရက(နိုင်)၁၆၄၅၁၆') // return true;
```

### Get State name from nrc card

```js
var nrc = MMNRC("12/MYG(N)164516");

nrc.getState("mm") //ရန်ကုန်တိုင်းဒေသကြီး
nrc.getState() // Yangon
```
