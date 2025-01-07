
## 4. Definición de Serie

Una serie matemática es __la suma__ de los términos de una sucesión. Se define como:

`
S=∑n=1∞an == Serie = sumatorio(n=1 hasta infinito) * (a sub n)
`

Donde __(a sub n)__ representa los términos de la sucesión. 
Si la suma parcial de la serie tiende a un límite finito cuando el número de términos tiende a infinito, decimos que la serie __converge__.


### Ejemplo 1: Serie aritmética

En una serie aritmética, cada término se obtiene sumando una constante dd al término anterior.

```
a = 1; % Primer término
n = 10; % Número de término
d = 2; % Diferencia común
t = a + (n-1)*d; % Último término
S_aritmetica = n * (a + t) / 2;
disp(S_aritmetica)
```

### Ejemplo 2: Serie geométrica

En una serie geométrica, cada término se obtiene multiplicando el término anterior por una constante rr.

```
r = 2; % Razón común
n = 10; % Número de términos
a = 1; % Primer término
S_geometrica = a * (1 - r^n) / (1 - r);
disp(S_geometrica)
```
