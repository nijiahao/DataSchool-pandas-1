

```python
import pandas as pd
```


```python
ufo=pd.read_csv('https://raw.githubusercontent.com/justmarkham/pandas-videos/master/data/ufo.csv')
```


```python
ufo.head()
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
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
      <td>6/1/1930 22:00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
      <td>6/30/1930 20:00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
      <td>2/15/1931 14:00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Abilene</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>KS</td>
      <td>6/1/1931 13:00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>New York Worlds Fair</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>NY</td>
      <td>4/18/1933 19:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.loc
```




    <pandas.core.indexing._LocIndexer at 0x1c711d95ac8>




```python
ufo.head(3)
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
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
      <td>6/1/1930 22:00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
      <td>6/30/1930 20:00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
      <td>2/15/1931 14:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.loc[0,:]
```




    City                       Ithaca
    Colors Reported               NaN
    Shape Reported           TRIANGLE
    State                          NY
    Time               6/1/1930 22:00
    Name: 0, dtype: object




```python
ufo.loc[[0,1,2],:]
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
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
      <td>6/1/1930 22:00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
      <td>6/30/1930 20:00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
      <td>2/15/1931 14:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.loc[0:2,:]
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
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
      <td>6/1/1930 22:00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
      <td>6/30/1930 20:00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
      <td>2/15/1931 14:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.loc[:,'City':'State']
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Abilene</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>KS</td>
    </tr>
    <tr>
      <th>4</th>
      <td>New York Worlds Fair</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>NY</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Valley City</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>ND</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Crater Lake</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Alma</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>MI</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Eklutna</td>
      <td>NaN</td>
      <td>CIGAR</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Hubbard</td>
      <td>NaN</td>
      <td>CYLINDER</td>
      <td>OR</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Fontana</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Waterloo</td>
      <td>NaN</td>
      <td>FIREBALL</td>
      <td>AL</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Belton</td>
      <td>RED</td>
      <td>SPHERE</td>
      <td>SC</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Keokuk</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>IA</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Ludington</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>MI</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Forest Home</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Los Angeles</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Hapeville</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>GA</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Oneida</td>
      <td>NaN</td>
      <td>RECTANGLE</td>
      <td>TN</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Bering Sea</td>
      <td>RED</td>
      <td>OTHER</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Nebraska</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NE</td>
    </tr>
    <tr>
      <th>21</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LA</td>
    </tr>
    <tr>
      <th>22</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>LA</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Owensboro</td>
      <td>NaN</td>
      <td>RECTANGLE</td>
      <td>KY</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Wilderness</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>WV</td>
    </tr>
    <tr>
      <th>25</th>
      <td>San Diego</td>
      <td>NaN</td>
      <td>CIGAR</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Wilderness</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>WV</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Clovis</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NM</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Los Alamos</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NM</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Ft. Duschene</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>UT</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>18211</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>DIAMOND</td>
      <td>MA</td>
    </tr>
    <tr>
      <th>18212</th>
      <td>Carson</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18213</th>
      <td>Pasadena</td>
      <td>GREEN</td>
      <td>FIREBALL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18214</th>
      <td>Austin</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18215</th>
      <td>El Campo</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18216</th>
      <td>Garden Grove</td>
      <td>ORANGE</td>
      <td>LIGHT</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18217</th>
      <td>Berthoud Pass</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CO</td>
    </tr>
    <tr>
      <th>18218</th>
      <td>Sisterdale</td>
      <td>NaN</td>
      <td>DIAMOND</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18219</th>
      <td>Garden Grove</td>
      <td>NaN</td>
      <td>CHEVRON</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18220</th>
      <td>Shasta Lake</td>
      <td>BLUE</td>
      <td>DISK</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18221</th>
      <td>Franklin</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NH</td>
    </tr>
    <tr>
      <th>18222</th>
      <td>Albrightsville</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>PA</td>
    </tr>
    <tr>
      <th>18223</th>
      <td>Greenville</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SC</td>
    </tr>
    <tr>
      <th>18224</th>
      <td>Eufaula</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>OK</td>
    </tr>
    <tr>
      <th>18225</th>
      <td>Simi Valley</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18226</th>
      <td>San Francisco</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18227</th>
      <td>San Francisco</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18228</th>
      <td>Kingsville</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18229</th>
      <td>Chicago</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>IL</td>
    </tr>
    <tr>
      <th>18230</th>
      <td>Pismo Beach</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18231</th>
      <td>Pismo Beach</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18232</th>
      <td>Lodi</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18233</th>
      <td>Anchorage</td>
      <td>RED</td>
      <td>VARIOUS</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>18234</th>
      <td>Capitola</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18235</th>
      <td>Fountain Hills</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>AZ</td>
    </tr>
    <tr>
      <th>18236</th>
      <td>Grant Park</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>IL</td>
    </tr>
    <tr>
      <th>18237</th>
      <td>Spirit Lake</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>IA</td>
    </tr>
    <tr>
      <th>18238</th>
      <td>Eagle River</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18239</th>
      <td>Eagle River</td>
      <td>RED</td>
      <td>LIGHT</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18240</th>
      <td>Ybor</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>FL</td>
    </tr>
  </tbody>
</table>
<p>18241 rows × 4 columns</p>
</div>




```python
ufo.head(3).drop('Time',axis=1)
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.loc[ufo.City=='Oakland','State']
```




    1694     CA
    2144     CA
    4686     MD
    7293     CA
    8488     CA
    8768     CA
    10816    OR
    10948    CA
    11045    CA
    12322    CA
    12941    CA
    16803    MD
    17322    CA
    Name: State, dtype: object




```python
ufo[ufo.City=='Oakland'].State
```




    1694     CA
    2144     CA
    4686     MD
    7293     CA
    8488     CA
    8768     CA
    10816    OR
    10948    CA
    11045    CA
    12322    CA
    12941    CA
    16803    MD
    17322    CA
    Name: State, dtype: object




```python
ufo.iloc[:,0:4]
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CO</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Abilene</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>KS</td>
    </tr>
    <tr>
      <th>4</th>
      <td>New York Worlds Fair</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>NY</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Valley City</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>ND</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Crater Lake</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Alma</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>MI</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Eklutna</td>
      <td>NaN</td>
      <td>CIGAR</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Hubbard</td>
      <td>NaN</td>
      <td>CYLINDER</td>
      <td>OR</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Fontana</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Waterloo</td>
      <td>NaN</td>
      <td>FIREBALL</td>
      <td>AL</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Belton</td>
      <td>RED</td>
      <td>SPHERE</td>
      <td>SC</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Keokuk</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>IA</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Ludington</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>MI</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Forest Home</td>
      <td>NaN</td>
      <td>CIRCLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Los Angeles</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Hapeville</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>GA</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Oneida</td>
      <td>NaN</td>
      <td>RECTANGLE</td>
      <td>TN</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Bering Sea</td>
      <td>RED</td>
      <td>OTHER</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Nebraska</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NE</td>
    </tr>
    <tr>
      <th>21</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LA</td>
    </tr>
    <tr>
      <th>22</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>LA</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Owensboro</td>
      <td>NaN</td>
      <td>RECTANGLE</td>
      <td>KY</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Wilderness</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>WV</td>
    </tr>
    <tr>
      <th>25</th>
      <td>San Diego</td>
      <td>NaN</td>
      <td>CIGAR</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Wilderness</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>WV</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Clovis</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NM</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Los Alamos</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NM</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Ft. Duschene</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>UT</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>18211</th>
      <td>Holyoke</td>
      <td>NaN</td>
      <td>DIAMOND</td>
      <td>MA</td>
    </tr>
    <tr>
      <th>18212</th>
      <td>Carson</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18213</th>
      <td>Pasadena</td>
      <td>GREEN</td>
      <td>FIREBALL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18214</th>
      <td>Austin</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18215</th>
      <td>El Campo</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18216</th>
      <td>Garden Grove</td>
      <td>ORANGE</td>
      <td>LIGHT</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18217</th>
      <td>Berthoud Pass</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CO</td>
    </tr>
    <tr>
      <th>18218</th>
      <td>Sisterdale</td>
      <td>NaN</td>
      <td>DIAMOND</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18219</th>
      <td>Garden Grove</td>
      <td>NaN</td>
      <td>CHEVRON</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18220</th>
      <td>Shasta Lake</td>
      <td>BLUE</td>
      <td>DISK</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18221</th>
      <td>Franklin</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>NH</td>
    </tr>
    <tr>
      <th>18222</th>
      <td>Albrightsville</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>PA</td>
    </tr>
    <tr>
      <th>18223</th>
      <td>Greenville</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SC</td>
    </tr>
    <tr>
      <th>18224</th>
      <td>Eufaula</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>OK</td>
    </tr>
    <tr>
      <th>18225</th>
      <td>Simi Valley</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18226</th>
      <td>San Francisco</td>
      <td>NaN</td>
      <td>FORMATION</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18227</th>
      <td>San Francisco</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18228</th>
      <td>Kingsville</td>
      <td>NaN</td>
      <td>LIGHT</td>
      <td>TX</td>
    </tr>
    <tr>
      <th>18229</th>
      <td>Chicago</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>IL</td>
    </tr>
    <tr>
      <th>18230</th>
      <td>Pismo Beach</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18231</th>
      <td>Pismo Beach</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18232</th>
      <td>Lodi</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18233</th>
      <td>Anchorage</td>
      <td>RED</td>
      <td>VARIOUS</td>
      <td>AK</td>
    </tr>
    <tr>
      <th>18234</th>
      <td>Capitola</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>CA</td>
    </tr>
    <tr>
      <th>18235</th>
      <td>Fountain Hills</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>AZ</td>
    </tr>
    <tr>
      <th>18236</th>
      <td>Grant Park</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>IL</td>
    </tr>
    <tr>
      <th>18237</th>
      <td>Spirit Lake</td>
      <td>NaN</td>
      <td>DISK</td>
      <td>IA</td>
    </tr>
    <tr>
      <th>18238</th>
      <td>Eagle River</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18239</th>
      <td>Eagle River</td>
      <td>RED</td>
      <td>LIGHT</td>
      <td>WI</td>
    </tr>
    <tr>
      <th>18240</th>
      <td>Ybor</td>
      <td>NaN</td>
      <td>OVAL</td>
      <td>FL</td>
    </tr>
  </tbody>
</table>
<p>18241 rows × 4 columns</p>
</div>




```python
list(range(0,4))
```




    [0, 1, 2, 3]




```python
ufo.iloc[0:3,:]
```


```python
ufo.loc(['City','State'])
```




    <pandas.core.indexing._LocIndexer at 0x1c711361eb8>




```python
ufo[0:2]
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
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
      <td>TRIANGLE</td>
      <td>NY</td>
      <td>6/1/1930 22:00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NJ</td>
      <td>6/30/1930 20:00</td>
    </tr>
  </tbody>
</table>
</div>




```python
drinks=pd.read_csv('https://raw.githubusercontent.com/justmarkham/pandas-videos/master/data/drinks.csv',index_col='country')
```


```python
drinks.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>beer_servings</th>
      <th>spirit_servings</th>
      <th>wine_servings</th>
      <th>total_litres_of_pure_alcohol</th>
      <th>continent</th>
    </tr>
    <tr>
      <th>country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Afghanistan</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.0</td>
      <td>Asia</td>
    </tr>
    <tr>
      <th>Albania</th>
      <td>89</td>
      <td>132</td>
      <td>54</td>
      <td>4.9</td>
      <td>Europe</td>
    </tr>
    <tr>
      <th>Algeria</th>
      <td>25</td>
      <td>0</td>
      <td>14</td>
      <td>0.7</td>
      <td>Africa</td>
    </tr>
    <tr>
      <th>Andorra</th>
      <td>245</td>
      <td>138</td>
      <td>312</td>
      <td>12.4</td>
      <td>Europe</td>
    </tr>
    <tr>
      <th>Angola</th>
      <td>217</td>
      <td>57</td>
      <td>45</td>
      <td>5.9</td>
      <td>Africa</td>
    </tr>
  </tbody>
</table>
</div>




```python
drinks.ix['Algeria',0]
```




    25




```python
drinks.ix[1,'beer_servings']
```




    89




```python
drinks.ix['Albania':'Andorra',0:2]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>beer_servings</th>
      <th>spirit_servings</th>
    </tr>
    <tr>
      <th>country</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Albania</th>
      <td>89</td>
      <td>132</td>
    </tr>
    <tr>
      <th>Algeria</th>
      <td>25</td>
      <td>0</td>
    </tr>
    <tr>
      <th>Andorra</th>
      <td>245</td>
      <td>138</td>
    </tr>
  </tbody>
</table>
</div>




```python
ufo.ix[0:2,0:2]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Colors Reported</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ithaca</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Willingboro</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Holyoke</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
主要索引方式为 loc和iloc，ix索引推荐只在同时需要行和列一起筛选时使用
```
