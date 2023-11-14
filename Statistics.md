# Microbiome

## Alfa-diversity

> p-value < 0.05 (0.01) --> rechaza nula

> p-value > 0.05 (0.99) --> rechaza alternativa


### Shapiro

Test de normalidad

- Hipótesi nula: la población se distribuye de manera **normal** 

- Hipótesi alternativa: la población se distribuye de manera **no normal** 

> p-value < 0.05 (0.01) --> **no normal** --> *test no paramétrico* --> kruskal (>2 grupos) / wilcox (2 grupos)

> p-value > 0.05 (0.99) --> **normal** --> *test paramétrico* --> t-test

### Levene

Test de igualdad de varianzas (homocedasticidad)

- Hipótesi nula: la población se distribuye con varianzas **no distintas** 

- Hipótesi alternativa: la población se distribuye con varianzas **distintas** 

> p-value < 0.05 (0.01) --> **distintas** --> *test no paramétrico* --> kruskal (>2 grupos) / wilcox (2 grupos)

> p-value > 0.05 (0.99) --> **no distintas** --> *test paramétrico* --> t-test




