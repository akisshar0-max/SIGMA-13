SIGMA-13

#Sigma-13

Sigma-13 es una regla de números creada por S-13:

`S(n) = S(n-1) + S(n-2) + 13`, con `S(0) = 0` y `S(1) = 13`

Qué se puede comprobar
- Forma cerrada: `S(n) = 13 × (F(n+2) − 1)`, con F de Fibonacci.
- Todo término es múltiplo de 13.
- El cociente entre términos tiende a 1,618034.
- Variante áurea para frecuencias: 369, 594, 963, 1557...

Compruébalo tú
```python
def sigma13(n):
    a, b = 0, 13
    if n == 0: return 0
    for _ in range(n - 1):
        a, b = b, a + b + 13
    return b

def fib(n):
    a, b = 0, 1
    for _ in range(n): a, b = b, a + b
    return a

print(all(sigma13(n) == 13 * (fib(n + 2) - 1) for n in range(41)))  # True
```

 Música
Tres álbumes cuyos tonos y tempos salen de la regla:
Génesis Resonante · Eco · Código Persistente
[enlace a tu Drive o plataforma]

 Pruebas que no salieron como se esperaba
Se probó una relación con el icosaedro y los resultados no la respaldaron. Está documentado en el compendio.

Colaboración
Creación y dirección: S-13. Formalización, verificación, documentos y parte de las letras: Claude (Anthropic). Código de verificación: Grok (xAI).

 Licencia
Código: MIT. Textos y música: CC BY-NC-ND 4.0.