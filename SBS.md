

```python
import random
import pandas as pd
```


```python
order = random.sample(range(100), 100)
print(order)

players = ['Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Collin', 'Collin', 'Collin', 'Collin', 'Collin', 'Jeremy', 'Jeremy', 'Jeremy', 'Jeremy', 'Jeremy', 'Cheryl', 'Cheryl', 'Cheryl', 'Cheryl', 'Cheryl']

print(len(players))

players = random.sample(players, 100)
print(players)
# print(len(players))
```

    [0, 58, 89, 85, 12, 13, 76, 59, 1, 91, 14, 82, 23, 86, 72, 81, 71, 2, 80, 96, 69, 35, 3, 47, 31, 6, 56, 57, 40, 54, 42, 51, 62, 17, 4, 97, 16, 28, 26, 52, 67, 36, 49, 11, 29, 87, 68, 84, 46, 24, 61, 73, 75, 88, 65, 94, 10, 55, 25, 39, 90, 83, 21, 9, 92, 32, 7, 41, 93, 53, 60, 63, 43, 48, 18, 98, 78, 74, 5, 44, 45, 19, 70, 8, 20, 22, 77, 27, 33, 38, 34, 15, 64, 30, 79, 95, 50, 37, 66, 99]
    100
    ['Rajiv', 'Jeremy', 'Cheryl', 'Joel', 'Rajiv', 'Rajiv', 'Richard', 'Al', 'Jake', 'Chi Shing', 'Rajiv', 'Jeremy', 'Joel', 'Richard', 'Cheryl', 'Richard', 'Jeremy', 'Jake', 'Rajiv', 'Al', 'Dai', 'Dai', 'Dai', 'Matt', 'Joel', 'Joel', 'Collin', 'Richard', 'Matt', 'Dai', 'Rajiv', 'Rajiv', 'Matt', 'Collin', 'Matt', 'Dai', 'Al', 'Chi Shing', 'Jake', 'Richard', 'Al', 'Al', 'Dai', 'Jeremy', 'Rajiv', 'Joel', 'Jeremy', 'Dai', 'Al', 'Chi Shing', 'Rajiv', 'Chi Shing', 'Cheryl', 'Matt', 'Al', 'Al', 'Joel', 'Cheryl', 'Richard', 'Matt', 'Richard', 'Matt', 'Dai', 'Joel', 'Matt', 'Rajiv', 'Jake', 'Chi Shing', 'Dai', 'Richard', 'Cheryl', 'Rajiv', 'Rajiv', 'Collin', 'Rajiv', 'Chi Shing', 'Jake', 'Richard', 'Chi Shing', 'Joel', 'Al', 'Jake', 'Chi Shing', 'Al', 'Dai', 'Matt', 'Jake', 'Chi Shing', 'Collin', 'Jake', 'Joel', 'Rajiv', 'Rajiv', 'Matt', 'Richard', 'Collin', 'Jake', 'Joel', 'Jake', 'Chi Shing']
    


```python
sbs = pd.DataFrame(index=[0, 1, 2, 3, 4, 5, 6, 7, 8, 9], columns=[0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
# sbs
```


```python
for n in range(len(order)):
    sq = str(order[n]).zfill(2)
    player = players[n]
    t1 = int(sq[0])
    t2 = int(sq[1])
    print(sq, player)
    sbs.at[t1, t2] = player
final_sbs = sbs
final_sbs = final_sbs.rename(index={0: 'KC0', 1: 'KC1', 2: 'KC2', 3: 'KC3', 4: 'KC4', 5: 'KC5', 6: 'KC6', 7: 'KC7', 8: 'KC8', 9:'KC9'})
final_sbs = final_sbs.rename(columns={0: 'TB0', 1: 'TB1', 2: 'TB2', 3: 'TB3', 4: 'TB4', 5: 'TB5', 6: 'TB6', 7: 'TB7', 8: 'TB8', 9:'TB9'})
final_sbs
    
    
```

    00 Rajiv
    58 Jeremy
    89 Cheryl
    85 Joel
    12 Rajiv
    13 Rajiv
    76 Richard
    59 Al
    01 Jake
    91 Chi Shing
    14 Rajiv
    82 Jeremy
    23 Joel
    86 Richard
    72 Cheryl
    81 Richard
    71 Jeremy
    02 Jake
    80 Rajiv
    96 Al
    69 Dai
    35 Dai
    03 Dai
    47 Matt
    31 Joel
    06 Joel
    56 Collin
    57 Richard
    40 Matt
    54 Dai
    42 Rajiv
    51 Rajiv
    62 Matt
    17 Collin
    04 Matt
    97 Dai
    16 Al
    28 Chi Shing
    26 Jake
    52 Richard
    67 Al
    36 Al
    49 Dai
    11 Jeremy
    29 Rajiv
    87 Joel
    68 Jeremy
    84 Dai
    46 Al
    24 Chi Shing
    61 Rajiv
    73 Chi Shing
    75 Cheryl
    88 Matt
    65 Al
    94 Al
    10 Joel
    55 Cheryl
    25 Richard
    39 Matt
    90 Richard
    83 Matt
    21 Dai
    09 Joel
    92 Matt
    32 Rajiv
    07 Jake
    41 Chi Shing
    93 Dai
    53 Richard
    60 Cheryl
    63 Rajiv
    43 Rajiv
    48 Collin
    18 Rajiv
    98 Chi Shing
    78 Jake
    74 Richard
    05 Chi Shing
    44 Joel
    45 Al
    19 Jake
    70 Chi Shing
    08 Al
    20 Dai
    22 Matt
    77 Jake
    27 Chi Shing
    33 Collin
    38 Jake
    34 Joel
    15 Rajiv
    64 Rajiv
    30 Matt
    79 Richard
    95 Collin
    50 Jake
    37 Joel
    66 Jake
    99 Chi Shing
    




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>TB0</th>
      <th>TB1</th>
      <th>TB2</th>
      <th>TB3</th>
      <th>TB4</th>
      <th>TB5</th>
      <th>TB6</th>
      <th>TB7</th>
      <th>TB8</th>
      <th>TB9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>KC0</th>
      <td>Rajiv</td>
      <td>Jake</td>
      <td>Jake</td>
      <td>Dai</td>
      <td>Matt</td>
      <td>Chi Shing</td>
      <td>Joel</td>
      <td>Jake</td>
      <td>Al</td>
      <td>Joel</td>
    </tr>
    <tr>
      <th>KC1</th>
      <td>Joel</td>
      <td>Jeremy</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Al</td>
      <td>Collin</td>
      <td>Rajiv</td>
      <td>Jake</td>
    </tr>
    <tr>
      <th>KC2</th>
      <td>Dai</td>
      <td>Dai</td>
      <td>Matt</td>
      <td>Joel</td>
      <td>Chi Shing</td>
      <td>Richard</td>
      <td>Jake</td>
      <td>Chi Shing</td>
      <td>Chi Shing</td>
      <td>Rajiv</td>
    </tr>
    <tr>
      <th>KC3</th>
      <td>Matt</td>
      <td>Joel</td>
      <td>Rajiv</td>
      <td>Collin</td>
      <td>Joel</td>
      <td>Dai</td>
      <td>Al</td>
      <td>Joel</td>
      <td>Jake</td>
      <td>Matt</td>
    </tr>
    <tr>
      <th>KC4</th>
      <td>Matt</td>
      <td>Chi Shing</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Joel</td>
      <td>Al</td>
      <td>Al</td>
      <td>Matt</td>
      <td>Collin</td>
      <td>Dai</td>
    </tr>
    <tr>
      <th>KC5</th>
      <td>Jake</td>
      <td>Rajiv</td>
      <td>Richard</td>
      <td>Richard</td>
      <td>Dai</td>
      <td>Cheryl</td>
      <td>Collin</td>
      <td>Richard</td>
      <td>Jeremy</td>
      <td>Al</td>
    </tr>
    <tr>
      <th>KC6</th>
      <td>Cheryl</td>
      <td>Rajiv</td>
      <td>Matt</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Al</td>
      <td>Jake</td>
      <td>Al</td>
      <td>Jeremy</td>
      <td>Dai</td>
    </tr>
    <tr>
      <th>KC7</th>
      <td>Chi Shing</td>
      <td>Jeremy</td>
      <td>Cheryl</td>
      <td>Chi Shing</td>
      <td>Richard</td>
      <td>Cheryl</td>
      <td>Richard</td>
      <td>Jake</td>
      <td>Jake</td>
      <td>Richard</td>
    </tr>
    <tr>
      <th>KC8</th>
      <td>Rajiv</td>
      <td>Richard</td>
      <td>Jeremy</td>
      <td>Matt</td>
      <td>Dai</td>
      <td>Joel</td>
      <td>Richard</td>
      <td>Joel</td>
      <td>Matt</td>
      <td>Cheryl</td>
    </tr>
    <tr>
      <th>KC9</th>
      <td>Richard</td>
      <td>Chi Shing</td>
      <td>Matt</td>
      <td>Dai</td>
      <td>Al</td>
      <td>Collin</td>
      <td>Al</td>
      <td>Dai</td>
      <td>Chi Shing</td>
      <td>Chi Shing</td>
    </tr>
  </tbody>
</table>
</div>




```python
final_sbs.to_csv("L:\Marketing\Digital_Marketing\MY_Drop_Files\SBS.csv")
```


```python

```
