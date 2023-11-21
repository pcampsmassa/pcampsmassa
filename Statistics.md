# Microbiome

## Alfa-diversity

> p-value < 0.05 (0.01) --> rechaza nula

> p-value > 0.05 (0.99) --> rechaza alternativa


### Shapiro

Test de normalidad
```
res1 <- lm(chao1 ~ Sample_type, data=alphaDH_RPre)
summary(res1)
shapiro.test(res1$residuals)
```
- Hipótesi nula: la población se distribuye de manera **normal** 

- Hipótesi alternativa: la población se distribuye de manera **no normal** 

> p-value < 0.05 (0.01) --> **no normal** --> *test no paramétrico* --> kruskal (>2 grupos) / wilcox (2 grupos)

> p-value > 0.05 (0.99) --> **normal** --> *test paramétrico* --> t-test

### Levene

Test de igualdad de varianzas (homocedasticidad)

```
leveneTest(y = alphaQ1$variable1, group = alphaQ1$variable2, center = "median")
```

- Hipótesi nula: la población se distribuye con **igualdad** de varianzas

- Hipótesi alternativa: la población se distribuye con varianzas **distintas** 

> p-value < 0.05 (0.01) --> **distintas** --> *test no paramétrico* --> kruskal (>2 grupos) / wilcox (2 grupos)

> p-value > 0.05 (0.99) --> **igualdad** --> *test paramétrico* --> t-test

### T-test

```
t.test(alphaQ1$chao1)
```
### Kruskal-Wallis test

```
kruskal.test(alphaQ1$variable1, alphaQ1$variable2)
```
### Mann-Whitney-Wilcoxon test
```
wilcox.test(diversity_shannon ~ Contacto_pacientes, data=alphaQ1)
```










