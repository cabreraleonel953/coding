---
marp: true
theme: default
footer: "Uso de markdown"
header: "Uso de marp"
author: "Leonel Cabrera"
---

# Proyecto Aplicativo 
## Victor Leonel Cabrera Garduño
### 00603018

---

## Álgebra Vectorial y Matricial 
  
---

## Codigo
### Figura propuesta

```
import numpy as np
import matplotlib.pyplot as plt

def pixel(x, y):
   return np.array([
       [x, y],
       [x+1, y],
       [x+1, y+1],
       [x, y+1]
   ])
```
---

``` python
W, H = 30, 32
fig, ax = plt.subplots(figsize=(7,9))

color_map = {
   'b': 'white',     
   'n': 'black',
   'c': '#f2c6a0',
   'v': 'green',
   'ac': '#4cc9f0',
   'af': '#1d4ed8'
}
```

---

``` python
def expand_row(row):
   result = []
   for item in row.split():
       if item.endswith('ac') or item.endswith('af'):
           num = int(item[:-2])
           col = item[-2:]
       else:
           num = int(item[:-1])
           col = item[-1]
       result += [col] * num
   return result

rows = [
   "4b 4n 14b 4n 4b",
   "4b 4n 14b 4n 4b",
   "2b 2n 4b 14n 4b 2n 2b",
   "2b 2n 4b 14n 4b 2n 2b",
   "2b 2n 22b 2n 2b",
   "2b 2n 22b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 2b 18c 2b 2n 2b",
   "2b 2n 2b 18c 2b 2n 2b",
   "2b 2n 2b 2c 2n 10c 2n 2c 2b 2n 2b",
   "2b 2n 2b 2c 2n 10c 2n 2c 2b 2n 2b",
   "2b 2n 2b 6c 6n 6c 2b 2n 2b",
   "2b 2n 2b 6c 6n 6c 2b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2n 4v 18b 4v 2n",
   "2n 4v 18b 4v 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 22ac 2c 2n",
   "2n 2c 22ac 2c 2n",
   "2b 2n 22ac 2n 2b",
   "2b 2n 22ac 2n 2b",
   "2b 2n 22af 2n 2b",
   "2b 2n 22af 2n 2b",
   "2b 2n 6af 10n 6af 2n 2b",
   "2b 2n 6af 10n 6af 2n 2b",
   "4b 6n 10b 6n 4b",
   "4b 6n 10b 6n 4b"
]

grid = []
for r in rows:
   fila = expand_row(r)
   grid.append(fila)

while len(grid) < H:
   grid.insert(0, ['b'] * W)

for y in range(H):
   for x in range(W):
       color = grid[H-1-y][x]
       if color != 'b':
           ax.fill(*pixel(x, y).T, color=color_map[color])

ax.set_xlim(-1, W+1)
ax.set_ylim(0, H)
ax.set_aspect('equal')
ax.grid(True, linestyle='--', alpha=0.3)
plt.title("Finn")
plt.show()
```

---

``` python
rows = [
   "4b 4n 14b 4n 4b",
   "4b 4n 14b 4n 4b",
   "2b 2n 4b 14n 4b 2n 2b",
   "2b 2n 4b 14n 4b 2n 2b",
   "2b 2n 22b 2n 2b",
   "2b 2n 22b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 2b 18c 2b 2n 2b",
   "2b 2n 2b 18c 2b 2n 2b",
   "2b 2n 2b 2c 2n 10c 2n 2c 2b 2n 2b",
   "2b 2n 2b 2c 2n 10c 2n 2c 2b 2n 2b",
   "2b 2n 2b 6c 6n 6c 2b 2n 2b",
   "2b 2n 2b 6c 6n 6c 2b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2b 2n 4b 14c 4b 2n 2b",
   "2n 4v 18b 4v 2n",
   "2n 4v 18b 4v 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 2v 18ac 2v 2c 2n",
   "2n 2c 22ac 2c 2n",
   "2n 2c 22ac 2c 2n",
   "2b 2n 22ac 2n 2b",
   "2b 2n 22ac 2n 2b",
   "2b 2n 22af 2n 2b",
   "2b 2n 22af 2n 2b",
   "2b 2n 6af 10n 6af 2n 2b",
   "2b 2n 6af 10n 6af 2n 2b",
   "4b 6n 10b 6n 4b",
   "4b 6n 10b 6n 4b"
]

grid = []
for r in rows:
   fila = expand_row(r)
   grid.append(fila)

while len(grid) < H:
   grid.insert(0, ['b'] * W)

for y in range(H):
   for x in range(W):
       color = grid[H-1-y][x]
       if color != 'b':
           ax.fill(*pixel(x, y).T, color=color_map[color])

ax.set_xlim(-1, W+1)
ax.set_ylim(0, H)
ax.set_aspect('equal')
ax.grid(True, linestyle='--', alpha=0.3)
plt.title("Finn")
plt.show()
```

 ---

 ## Formula 
 
 Derivate of $f(x) = x^2$

Average:

 $$
 \overline{x} = \frac{\sum_{i = 1}^{n} x_i}{n}
 $$

---

# Investigación de la Rotación y Translación en $\mathbb{R}^2$

---

## Rotación

  Supongamos que tenemos un vector en $\mathbb{R}^2$ tal que $v = (x, y)^T$ y queremos rotarlo en un ángulo θ (medido en grados o radianes) en sentido contrario de las manecillas del reloj. Llamemos a este nuevo vector rotado $v' = (x', y')^T$ . Entonces como se ve en la figura 5.3, si r denota la longitud de v (que no cambia por rotación) (Grossman, 1996, p.469).
Donde r se puede entender como la norma del vector definida por $\|v\| = \sqrt{x^2 + y^2}$.

---

Y nuestras componentes sean:

$x = r \cos(\alpha), \; y = r \sin(\alpha)$

$x' = r \cos(\theta + \alpha), \; y' = r \sin(\theta + \alpha)$

 <img src="https://res.cloudinary.com/dm5i1yoqe/image/upload/q_auto/f_auto/v1777055912/Captura_de_pantalla_2026-04-24_a_la_s_12.38.11_p.m._pa6kfk.png" width="380">

---

 Pero:$r \cos(\theta + \alpha) = r\cos(\theta)\cos(\alpha) - r \sin(\theta)\sin(\alpha)$
  de manera que:

$$
x' = x \cos(\theta) - y \sin(\theta)
$$

De manera similar: $r \sin(\theta +\alpha) = r \sin(\theta)\cos(\alpha) + r \cos(\theta)\sin(\alpha)
$
o sea:

$$
y' = x \sin(\theta) + y \cos(\theta)
$$

Siendo así, su matriz de transformación:


<div>
<img src="https://res.cloudinary.com/dm5i1yoqe/image/upload/q_auto/f_auto/v1777058949/Captura_de_pantalla_2026-04-24_a_la_s_1.29.01_p.m._opdaxz.png" width="200">
<br>
<em>Nota. Figura de matriz, por Grossman, 1996, p.470</em>
</div>



