
## 4. Definición de Serie

Una serie matemática es __la suma__ de los términos de una sucesión. Se define como:


$`S = \sum_{n=1}^{\infty} a_n`$

Donde __(a sub n)__ representa los términos de la sucesión. 
Si la suma parcial de la serie tiende a un límite finito cuando el número de términos tiende a infinito, decimos que la serie __converge__.


### Ejemplo 1: Serie aritmética

En una serie aritmética, cada término se obtiene sumando una constante dd al término anterior.

```matlab
a = 1; % Primer término
n = 10; % Número de término
d = 2; % Diferencia común
t = a + (n-1)*d; % Último término
S_aritmetica = n * (a + t) / 2;
disp(S_aritmetica)
```

### Ejemplo 2: Serie geométrica

En una serie geométrica, cada término se obtiene multiplicando el término anterior por una constante rr.

```matlab
r = 2; % Razón común
n = 10; % Número de términos
a = 1; % Primer término
S_geometrica = a * (1 - r^n) / (1 - r);
disp(S_geometrica)
```


Claro, aquí tienes las dos secciones separadas y detalladas.
4. Definición de Serie

Una serie matemática es la suma de los términos de una sucesión. Se define como:
S=∑n=1∞an
S=n=1∑∞​an​

Donde anan​ representa los términos de la sucesión. Si la suma parcial de la serie tiende a un límite finito cuando el número de términos tiende a infinito, decimos que la serie converge.
Ejemplo 1: Serie aritmética

En una serie aritmética, cada término se obtiene sumando una constante dd al término anterior.

a = 1; % Primer término
n = 10; % Número de términos
d = 2; % Diferencia común
t = a + (n-1)*d; % Último término
S_aritmetica = n * (a + t) / 2;
disp(S_aritmetica)

Ejemplo 2: Serie geométrica

En una serie geométrica, cada término se obtiene multiplicando el término anterior por una constante rr.

r = 2; % Razón común
n = 10; % Número de términos
a = 1; % Primer término
S_geometrica = a * (1 - r^n) / (1 - r);
disp(S_geometrica)

## 5. Tipos de series

Existen varios tipos de series, entre las más comunes se encuentran:

Serie aritmética: Suma de términos con una diferencia constante.

$`S = a + (a + d) + (a + 2d) + …`$

Serie geométrica: Suma de términos con una razón constante.

$`S = a+ar+ar2+…`$

Serie armónica: Suma de los inversos de los números naturales.

$`S = \sum_{n = 1}^{\infty} \frac{1}{n}`$
    
Serie de potencias: Expresión de una función como suma infinita de potencias.

$`S = \sum_{n = 0}^{\infty} c_n(x - a)^n`$

### Ejemplo: Serie armónica

```matlab
n = 10; % Número total de términos a sumar
harmonic_terms = 1 ./ (1:n); % Generar los términos de la serie armónica
S_armonica = sum(harmonic_terms); % Sumar los términos de la serie armónica
S_armonica; % Mostrar resultado
```

### Ejemplo: Serie de potencias

```matlab
syms x n % Declaramos los simbolos que utilizaremos
c = 1; % Coeficiente constante en cada término de la serie
a = 0; % Centro de la expansión (valor de x donde converge la serie)
serie_potencias = symsum(c * (x - a)^n, n, 0, 5); % Suma de los primeros 5 términos de la serie de potencias
serie_potencias; % Mostrar resultado
```

#### Gráfica comparativa

```matlab
% Gráfica de diferentes tipos de series
n_vals = 1:10; % Valores de "n" para los términos de la serie
serie_aritmetica = cumsum(1:10); % Cálculo de suma parcial para la serie aritmética
serie_geometrica = cumsum(1 * 2.^(0:9)); % Cálculo de suma parcial para la serie geométrica
serie_armonica = cumsum(1 ./ n_vals); % Cálculo de suma parcial para la serie armónica

figure; % Crear una nueva figura
plot(n_vals, serie_aritmetica, '-o', 'DisplayName', 'Serie Aritmética'); % Graficar la serie aritmética
hold on; % Permitir agregar más gráficas
plot(n_vals, serie_geometrica, '-s', 'DisplayName', 'Serie Geométrica'); % Graficar la serie geométrica
plot(n_vals, serie_armonica, '-x', 'DisplayName', 'Serie Armónica'); % Graficar la serie armónica
legend; % Agregar leyenda
xlabel('Número de términos'); % Etiqueta del eje x
ylabel('Suma parcial'); % Etiqueta del eje y
title('Comparación de Tipos de Series'); % Título de la gráfica

```
