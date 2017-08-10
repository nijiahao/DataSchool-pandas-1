

```python
import pandas as pd
```


```python
ufo = pd.read_csv('https://raw.githubusercontent.com/justmarkham/pandas-videos/master/data/ufo.csv')
```


```python
ufo.tail()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Colors Reported</th>
      <th>Shape Reported</th>
      <th>State</th>
      <th>Time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18236</th>
      <td>Grant Park</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>IL</td>
      <td>12/31/2000 23:00</td>
    </tr>
    <tr>
      <th>18237</th>
      <td>Spirit Lake</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>IA</td>
      <td>12/31/2000 23:00</td>
    </tr>
    <tr>
      <th>18238</th>
      <td>Eagle River</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WI</td>
      <td>12/31/2000 23:45</td>
    </tr>
    <tr>
      <th>18239</th>
      <td>Eagle River</td>
      <td>RED</td>
      <td>LIGHT</td>
      <td>WI</td>
      <td>12/31/2000 23:45</td>
    </tr>
    <tr>
      <th>18240</th>
      <td>Ybor</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>FL</td>
      <td>12/31/2000 23:59</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.isnull().tail()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Colors Reported</th>
      <th>Shape Reported</th>
      <th>State</th>
      <th>Time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18236</th>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18237</th>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18238</th>
      <td>False</td>
      <td>True</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18239</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18240</th>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.isnull().sum(axis=0)
```




    City                  25
    Colors Reported    15359
    Shape Reported      2644
    State                  0
    Time                   0
    dtype: int64




```python
pd.Series([True,False,True]).sum()
```




    2




```python
ufo.City.isnull()
```




    0        False
    1        False
    2        False
    3        False
    4        False
    5        False
    6        False
    7        False
    8        False
    9        False
    10       False
    11       False
    12       False
    13       False
    14       False
    15       False
    16       False
    17       False
    18       False
    19       False
    20       False
    21        True
    22        True
    23       False
    24       False
    25       False
    26       False
    27       False
    28       False
    29       False
             ...  
    18211    False
    18212    False
    18213    False
    18214    False
    18215    False
    18216    False
    18217    False
    18218    False
    18219    False
    18220    False
    18221    False
    18222    False
    18223    False
    18224    False
    18225    False
    18226    False
    18227    False
    18228    False
    18229    False
    18230    False
    18231    False
    18232    False
    18233    False
    18234    False
    18235    False
    18236    False
    18237    False
    18238    False
    18239    False
    18240    False
    Name: City, dtype: bool




```python
ufo[ufo.City.isnull()]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Colors Reported</th>
      <th>Shape Reported</th>
      <th>State</th>
      <th>Time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>21</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LA</td>
      <td>8/15/1943 0:00</td>
    </tr>
    <tr>
      <th>22</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>LA</td>
      <td>8/15/1943 0:00</td>
    </tr>
    <tr>
      <th>204</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>CA</td>
      <td>7/15/1952 12:30</td>
    </tr>
    <tr>
      <th>241</th>
      <td>NaN</td>
      <td>BLUE</td>
      <td>DISK</td>
      <td>MT</td>
      <td>7/4/1953 14:00</td>
    </tr>
    <tr>
      <th>613</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NV</td>
      <td>7/1/1960 12:00</td>
    </tr>
    <tr>
      <th>1877</th>
      <td>NaN</td>
      <td>YELLOW</td>
      <td>CIRCLE</td>
      <td>AZ</td>
      <td>8/15/1969 1:00</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NH</td>
      <td>8/1/1970 9:30</td>
    </tr>
    <tr>
      <th>2546</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>FIREBALL</td>
      <td>OH</td>
      <td>10/25/1973 23:30</td>
    </tr>
    <tr>
      <th>3123</th>
      <td>NaN</td>
      <td>RED</td>
      <td>TRIANGLE</td>
      <td>WV</td>
      <td>11/25/1975 23:00</td>
    </tr>
    <tr>
      <th>4736</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>SPHERE</td>
      <td>CA</td>
      <td>6/23/1982 23:00</td>
    </tr>
    <tr>
      <th>5269</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>AZ</td>
      <td>6/30/1985 21:30</td>
    </tr>
    <tr>
      <th>6735</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>TX</td>
      <td>4/1/1992 2:00</td>
    </tr>
    <tr>
      <th>7208</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>MI</td>
      <td>10/4/1993 17:30</td>
    </tr>
    <tr>
      <th>8828</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>WA</td>
      <td>10/30/1995 21:30</td>
    </tr>
    <tr>
      <th>8967</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>VARIOUS</td>
      <td>CA</td>
      <td>12/8/1995 18:00</td>
    </tr>
    <tr>
      <th>9273</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>OH</td>
      <td>5/1/1996 3:00</td>
    </tr>
    <tr>
      <th>9388</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CA</td>
      <td>6/12/1996 12:00</td>
    </tr>
    <tr>
      <th>9587</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>EGG</td>
      <td>FL</td>
      <td>8/24/1996 15:00</td>
    </tr>
    <tr>
      <th>10399</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>IL</td>
      <td>6/15/1997 23:00</td>
    </tr>
    <tr>
      <th>11625</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>TX</td>
      <td>6/7/1998 7:00</td>
    </tr>
    <tr>
      <th>12441</th>
      <td>NaN</td>
      <td>RED</td>
      <td>FIREBALL</td>
      <td>WA</td>
      <td>10/26/1998 17:58</td>
    </tr>
    <tr>
      <th>15767</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>RECTANGLE</td>
      <td>NV</td>
      <td>1/21/2000 11:30</td>
    </tr>
    <tr>
      <th>15812</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>NV</td>
      <td>2/2/2000 3:00</td>
    </tr>
    <tr>
      <th>16054</th>
      <td>NaN</td>
      <td>GREEN</td>
      <td>NaN</td>
      <td>FL</td>
      <td>3/11/2000 3:30</td>
    </tr>
    <tr>
      <th>16608</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>SPHERE</td>
      <td>NY</td>
      <td>6/15/2000 15:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.shape
```




    (18241, 5)




```python
ufo.dropna(how='any').shape
```




    (2486, 5)




```python
ufo.dropna(how='all').shape
```




    (18241, 5)




```python
ufo.dropna(subset=['City','Shape Reported'],how='any').shape
```




    (15576, 5)




```python
ufo['Shape Reported'].value_counts()
```




    LIGHT        2803
    DISK         2122
    TRIANGLE     1889
    OTHER        1402
    CIRCLE       1365
    SPHERE       1054
    FIREBALL     1039
    OVAL          845
    CIGAR         617
    FORMATION     434
    VARIOUS       333
    RECTANGLE     303
    CYLINDER      294
    CHEVRON       248
    DIAMOND       234
    EGG           197
    FLASH         188
    TEARDROP      119
    CONE           60
    CROSS          36
    DELTA           7
    CRESCENT        2
    ROUND           2
    HEXAGON         1
    FLARE           1
    PYRAMID         1
    DOME            1
    Name: Shape Reported, dtype: int64




```python
ufo['Shape Reported'].fillna(value='VARIOUS',inplace=True)
```


```python
ufo['Shape Reported'].value_counts()
```




    VARIOUS      2977
    LIGHT        2803
    DISK         2122
    TRIANGLE     1889
    OTHER        1402
    CIRCLE       1365
    SPHERE       1054
    FIREBALL     1039
    OVAL          845
    CIGAR         617
    FORMATION     434
    RECTANGLE     303
    CYLINDER      294
    CHEVRON       248
    DIAMOND       234
    EGG           197
    FLASH         188
    TEARDROP      119
    CONE           60
    CROSS          36
    DELTA           7
    ROUND           2
    CRESCENT        2
    FLARE           1
    HEXAGON         1
    PYRAMID         1
    DOME            1
    Name: Shape Reported, dtype: int64




```python

```
