

```python
import pandas as pd
```


```python
drinks = pd.read_csv('https://raw.githubusercontent.com/justmarkham/pandas-videos/master/data/drinks.csv')
```


```python
drinks.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>beer_servings</th>
      <th>spirit_servings</th>
      <th>wine_servings</th>
      <th>total_litres_of_pure_alcohol</th>
      <th>continent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.0</td>
      <td>Asia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Albania</td>
      <td>89</td>
      <td>132</td>
      <td>54</td>
      <td>4.9</td>
      <td>Europe</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Algeria</td>
      <td>25</td>
      <td>0</td>
      <td>14</td>
      <td>0.7</td>
      <td>Africa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Andorra</td>
      <td>245</td>
      <td>138</td>
      <td>312</td>
      <td>12.4</td>
      <td>Europe</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
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
drinks.dtypes
```




    country                          object
    beer_servings                     int64
    spirit_servings                   int64
    wine_servings                     int64
    total_litres_of_pure_alcohol    float64
    continent                        object
    dtype: object




```python
drinks.dtypes
```




    country                          object
    beer_servings                     int64
    spirit_servings                   int64
    wine_servings                     int64
    total_litres_of_pure_alcohol    float64
    continent                        object
    dtype: object




```python
drinks['beer_servings']=drinks.beer_servings.astype(float)
```


```python
drinks.dtypes
```




    country                          object
    beer_servings                   float64
    spirit_servings                   int64
    wine_servings                     int64
    total_litres_of_pure_alcohol    float64
    continent                        object
    dtype: object




```python

```


```python

```
