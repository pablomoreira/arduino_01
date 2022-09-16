---
marp: true
---
<!--
author: "Pablo Moreira"
theme: default
paginate: true
size: 16:9
footer: "[Link](https://github.com/pablomoreira/arduino_01/blob/main/clase01.md)"


-->

<style>
r { color: Red }
o { color: Orange }
g { color: Green }
</style> 

# **Clase 2 (Entradas Analógicas/Digitales)**
- Entradas Analógicas
- Lectura de sensor Analógicos
- Circuito con potenciómetros
- Circuito para una LDR
- Entradas Digitales
- Teclados matriciales
---
# **Analogías**

- La  *temperatura* es una magnitud física que indica la energía interna de un cuerpo, medida por un termómetro.
![bg right width:80% height:80%](https://upload.wikimedia.org/wikipedia/commons/6/6d/Translational_motion.gif)

---

# **Termómetros de Mercurio (Galio)**

![bg right width:90% height:90%](img/thermometers.jpg)
- Se mide observando la escala

---

# **Sensores Analógicos**

![bg right width:85% height:90%](https://i0.wp.com/blog.330ohms.com/wp-content/uploads/2020/06/Arduino_lm35_bb.png?resize=696%2C860&ssl=1)

- Los Sensores digitales tienen salidas que se pueden conectar a microprocesadores (Arduino)

- La analogía se hace con valores de voltage.

- Por ejemplo:  
    - 1 Volt  equivale a 10 <span>&deg;</span> Centígrados

---

#  **Potenciómetro como entrada analógica**

![bg right ](img/arduino_pote.png)

Convierte valores analógicos a digitales de 10-bit



---
<div align="center">
| int    | Volts    |
|:-:|:-:|
|0  | 0.0000 - 0.0049|
|1  | 0.0049 -  0.0098|
|2  | 0.0098 - 0.0146|
|3  | 0.0146 - 0.0195|
|1022  | 4.9902 - 4.9951|
|1023  | 4.9951 - 5.0000|

</div>

---


```cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
  Serial.println(analogRead(A1)); 
}
```