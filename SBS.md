

```python
import random
import pandas as pd
```


```python
order = random.sample(range(100), 100)
print(order)

players = ['Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Rajiv', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Matt', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Chi Shing', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Dai', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Jake', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Joel', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Al', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Richard', 'Collin', 'Collin', 'Collin', 'Collin', 'Collin', 'Jeremy', 'Jeremy', 'Jeremy', 'Jeremy', 'Jeremy', 'Aurelio', 'Aurelio', 'Aurelio', 'Aurelio', 'Aurelio']

print(len(players))

players = random.sample(players, 100)
print(players)
# print(len(players))
```

    [44, 77, 27, 17, 14, 39, 19, 51, 70, 82, 30, 43, 91, 84, 28, 50, 90, 33, 64, 23, 78, 6, 7, 16, 61, 38, 35, 96, 66, 80, 15, 41, 71, 3, 97, 59, 88, 75, 37, 13, 58, 31, 99, 57, 12, 93, 47, 49, 9, 83, 32, 29, 42, 86, 79, 76, 62, 55, 25, 18, 54, 65, 22, 26, 98, 73, 95, 81, 20, 69, 56, 48, 40, 92, 8, 5, 94, 24, 85, 11, 1, 60, 0, 36, 63, 67, 53, 89, 68, 72, 2, 74, 52, 34, 46, 87, 10, 4, 45, 21]
    100
    ['Al', 'Jeremy', 'Collin', 'Dai', 'Richard', 'Joel', 'Rajiv', 'Al', 'Jeremy', 'Chi Shing', 'Aurelio', 'Richard', 'Joel', 'Al', 'Joel', 'Jake', 'Jake', 'Chi Shing', 'Dai', 'Matt', 'Dai', 'Richard', 'Joel', 'Richard', 'Dai', 'Jeremy', 'Rajiv', 'Joel', 'Dai', 'Jeremy', 'Richard', 'Joel', 'Al', 'Matt', 'Al', 'Aurelio', 'Chi Shing', 'Jake', 'Rajiv', 'Al', 'Rajiv', 'Aurelio', 'Al', 'Dai', 'Matt', 'Matt', 'Chi Shing', 'Dai', 'Joel', 'Rajiv', 'Aurelio', 'Matt', 'Matt', 'Rajiv', 'Rajiv', 'Joel', 'Jake', 'Matt', 'Richard', 'Rajiv', 'Chi Shing', 'Rajiv', 'Jake', 'Rajiv', 'Collin', 'Al', 'Rajiv', 'Joel', 'Chi Shing', 'Matt', 'Jeremy', 'Chi Shing', 'Matt', 'Rajiv', 'Al', 'Chi Shing', 'Rajiv', 'Jake', 'Richard', 'Richard', 'Jake', 'Rajiv', 'Aurelio', 'Collin', 'Dai', 'Dai', 'Jake', 'Joel', 'Jake', 'Matt', 'Collin', 'Rajiv', 'Al', 'Chi Shing', 'Richard', 'Jake', 'Dai', 'Chi Shing', 'Richard', 'Collin']
    


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

    44 Al
    77 Jeremy
    27 Collin
    17 Dai
    14 Richard
    39 Joel
    19 Rajiv
    51 Al
    70 Jeremy
    82 Chi Shing
    30 Aurelio
    43 Richard
    91 Joel
    84 Al
    28 Joel
    50 Jake
    90 Jake
    33 Chi Shing
    64 Dai
    23 Matt
    78 Dai
    06 Richard
    07 Joel
    16 Richard
    61 Dai
    38 Jeremy
    35 Rajiv
    96 Joel
    66 Dai
    80 Jeremy
    15 Richard
    41 Joel
    71 Al
    03 Matt
    97 Al
    59 Aurelio
    88 Chi Shing
    75 Jake
    37 Rajiv
    13 Al
    58 Rajiv
    31 Aurelio
    99 Al
    57 Dai
    12 Matt
    93 Matt
    47 Chi Shing
    49 Dai
    09 Joel
    83 Rajiv
    32 Aurelio
    29 Matt
    42 Matt
    86 Rajiv
    79 Rajiv
    76 Joel
    62 Jake
    55 Matt
    25 Richard
    18 Rajiv
    54 Chi Shing
    65 Rajiv
    22 Jake
    26 Rajiv
    98 Collin
    73 Al
    95 Rajiv
    81 Joel
    20 Chi Shing
    69 Matt
    56 Jeremy
    48 Chi Shing
    40 Matt
    92 Rajiv
    08 Al
    05 Chi Shing
    94 Rajiv
    24 Jake
    85 Richard
    11 Richard
    01 Jake
    60 Rajiv
    00 Aurelio
    36 Collin
    63 Dai
    67 Dai
    53 Jake
    89 Joel
    68 Jake
    72 Matt
    02 Collin
    74 Rajiv
    52 Al
    34 Chi Shing
    46 Richard
    87 Jake
    10 Dai
    04 Chi Shing
    45 Richard
    21 Collin
    




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
      <td>Aurelio</td>
      <td>Jake</td>
      <td>Collin</td>
      <td>Matt</td>
      <td>Chi Shing</td>
      <td>Chi Shing</td>
      <td>Richard</td>
      <td>Joel</td>
      <td>Al</td>
      <td>Joel</td>
    </tr>
    <tr>
      <th>KC1</th>
      <td>Dai</td>
      <td>Richard</td>
      <td>Matt</td>
      <td>Al</td>
      <td>Richard</td>
      <td>Richard</td>
      <td>Richard</td>
      <td>Dai</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
    </tr>
    <tr>
      <th>KC2</th>
      <td>Chi Shing</td>
      <td>Collin</td>
      <td>Jake</td>
      <td>Matt</td>
      <td>Jake</td>
      <td>Richard</td>
      <td>Rajiv</td>
      <td>Collin</td>
      <td>Joel</td>
      <td>Matt</td>
    </tr>
    <tr>
      <th>KC3</th>
      <td>Aurelio</td>
      <td>Aurelio</td>
      <td>Aurelio</td>
      <td>Chi Shing</td>
      <td>Chi Shing</td>
      <td>Rajiv</td>
      <td>Collin</td>
      <td>Rajiv</td>
      <td>Jeremy</td>
      <td>Joel</td>
    </tr>
    <tr>
      <th>KC4</th>
      <td>Matt</td>
      <td>Joel</td>
      <td>Matt</td>
      <td>Richard</td>
      <td>Al</td>
      <td>Richard</td>
      <td>Richard</td>
      <td>Chi Shing</td>
      <td>Chi Shing</td>
      <td>Dai</td>
    </tr>
    <tr>
      <th>KC5</th>
      <td>Jake</td>
      <td>Al</td>
      <td>Al</td>
      <td>Jake</td>
      <td>Chi Shing</td>
      <td>Matt</td>
      <td>Jeremy</td>
      <td>Dai</td>
      <td>Rajiv</td>
      <td>Aurelio</td>
    </tr>
    <tr>
      <th>KC6</th>
      <td>Rajiv</td>
      <td>Dai</td>
      <td>Jake</td>
      <td>Dai</td>
      <td>Dai</td>
      <td>Rajiv</td>
      <td>Dai</td>
      <td>Dai</td>
      <td>Jake</td>
      <td>Matt</td>
    </tr>
    <tr>
      <th>KC7</th>
      <td>Jeremy</td>
      <td>Al</td>
      <td>Matt</td>
      <td>Al</td>
      <td>Rajiv</td>
      <td>Jake</td>
      <td>Joel</td>
      <td>Jeremy</td>
      <td>Dai</td>
      <td>Rajiv</td>
    </tr>
    <tr>
      <th>KC8</th>
      <td>Jeremy</td>
      <td>Joel</td>
      <td>Chi Shing</td>
      <td>Rajiv</td>
      <td>Al</td>
      <td>Richard</td>
      <td>Rajiv</td>
      <td>Jake</td>
      <td>Chi Shing</td>
      <td>Joel</td>
    </tr>
    <tr>
      <th>KC9</th>
      <td>Jake</td>
      <td>Joel</td>
      <td>Rajiv</td>
      <td>Matt</td>
      <td>Rajiv</td>
      <td>Rajiv</td>
      <td>Joel</td>
      <td>Al</td>
      <td>Collin</td>
      <td>Al</td>
    </tr>
  </tbody>
</table>
</div>




```python
final_sbs.to_csv("L:\Marketing\Digital_Marketing\MY_Drop_Files\SBS.csv")
```


```python

```
