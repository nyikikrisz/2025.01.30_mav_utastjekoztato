# ez a máv utastájékoztato tanulóverziója

## index.html
```html
<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>máv utastájékotató</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <table>
        <thead>
            <tr style="background-color: gray; color: green;">
                <th>8:43</th>
                <th></th>
                <th></th>
                <th></th>
                <th></th>
                <th><img src="BSicon_MAV.svg" alt="logo" height="40" title="Máv logo"></th>
            </tr>
            <tr style="background-color: green">
                <th>Tervezett érkezés</th>
                <th>Érkezés</th>
                <th>Vonat</th>
                <th>Honnan</th>
                <th>Hova</th>
                <th>Vágány</th>
            </tr>
        </thead>

        <tbody>
            <tr style="background-color: rgb(0, 184, 0);">
                <td class="elsooszlop">8:30</td>
                <td id="keses">8:42</td>
                <td>IC</td>
                <td>Seged</td>
                <td>Szatymaz-Kistelek</td>
                <td>5</td>
            </tr>  

```
## induló vonatok
```html
<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MÁV Induló Játatok</title>
    <link rel="stylesheet" href="indulovonatok.css">
</head>
<body>
    <table>
        <thead>
            <tr id="elso">
                <th>
                    <body onload="startTime()">
                    <div id="txt"></div>
                    
                    <script>
                    function startTime() {
                      const today = new Date();
                      let h = today.getHours();
                      let m = today.getMinutes();
                      let s = today.getSeconds();
                      m = checkTime(m);
                      s = checkTime(s);
                      document.getElementById('txt').innerHTML =  h + ":" + m + ":" + s;
                      setTimeout(startTime, 1000);
                    }
                    
                    function checkTime(i) {
                      if (i < 10) {i = "0" + i};  // add zero in front of numbers < 10
                      return i;
                    }
                    </script>
                </th>
                <th>Indulás</th>
                <th colspan="2">Induló járatok</th>
                <th colspan="2">Érkező Járatok</th>
                <th rowspan="2" style="background-color:rgb(0, 150, 12);"><img src="BSicon_MAV.svg" alt="logo" height="40" title="Máv logo"></th>
            </tr>
            <tr >
                <th>Tervezett indulás</th>
                <th>Valós indulás</th>
                <th>Vonat</th>
                <th>Honnan</th>
                <th>Hova</th>
                <th>Vágány</th>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>08:31</td>
                <td id="keso_indulo_vonat">08:43</td>
                <td>717</td>
                <td>Budapest-Nyugati</td>
                <td>Kecskemét-cegléd</td>
                <td colspan="2">5</td>
            </tr>
```
## css🎨
```css
table, th, td {  
    /* betűszín */
    color: rgb(0, 0, 0);
    font-family: 'Times New Roman', Times, serif;
    width: auto;
    height: 5px;
  }
  th{
    background-color:rgb(92, 92, 92);
    color: white;
  }
  #keses{
    background-color: red;
  }
   td {
  border-collapse: collapse, 5px, solid, black;
  }
  .elsooszlop {
    background-color: rgb(0, 105, 105);
  }
  ```
## Használat 
Nyisd meg a linket és ott van 👁️👄👁️ </p>
[link: index](https://nyikikrisz.github.io/2025.01.30_mav_utastjekoztato/indulo_vonatok.html)</p>
[link: induló vonatok](https://nyikikrisz.github.io/2025.01.30_mav_utastjekoztato/index.html)

## Funkciók 🚀
Csináltam egy órát ami a valós időt mutatja 🕑</p>
```html
 <body onload="startTime()">
    <div id="txt"></div>
                    
<script>
    function startTime() {
    const today = new Date();
    let h = today.getHours();
    let m = today.getMinutes();
    let s = today.getSeconds();
    m = checkTime(m);
    s = checkTime(s);
    document.getElementById('txt').innerHTML =  h + ":" + m + ":" +s;
    setTimeout(startTime, 1000);
    }
                    
    function checkTime(i) {
    if (i < 10) {i = "0" + i};  // add zero in front of numbers < 10
    return i;
    }
</script>
```
Jó lehet nem én csináltam de azért komoly

## fejlesztési lehetőségek
- [x] Nagyon komoly óra
- [ ] Érteni az óra műkködik a nagyon komoly óra
- [ ] Nagyon sok pént keresni