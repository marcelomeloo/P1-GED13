>### Dados Petroleo Brent

```r
  dados.brent <- quantmod::getSymbols("BZ=F", src = "yahoo", from = start, to = end, auto.assign = FALSE)
```

```
## Warning: BZ=F contains missing values. Some functions will not work if objects contain missing values in the middle of the series. Consider using na.omit(), na.approx(), na.fill(),
## etc to remove or replace them.
```

```r
  dados.brent
```

```
##            BZ=F.Open BZ=F.High BZ=F.Low BZ=F.Close BZ=F.Volume BZ=F.Adjusted
## 2022-01-03     77.94     79.28    77.04      78.98       27224         78.98
## 2022-01-04     78.95     80.55    78.60      80.00       31321         80.00
## 2022-01-05     80.08     81.49    79.55      80.80       35152         80.80
## 2022-01-06     80.15     82.84    79.63      81.99       41582         81.99
## 2022-01-07     82.06     82.99    81.44      81.75       29501         81.75
## 2022-01-10     81.79     82.27    80.49      80.87       30035         80.87
## 2022-01-11     80.96     83.97    80.88      83.72       37934         83.72
## 2022-01-12     83.69     85.20    83.51      84.67       32298         84.67
## 2022-01-13     84.78     85.09    83.79      84.47       27107         84.47
## 2022-01-14     84.13     86.50    84.03      86.06       31970         86.06
## 2022-01-18     86.50     88.55    85.55      87.51       45875         87.51
## 2022-01-19     88.45     89.17    87.63      88.44       37483         88.44
## 2022-01-20     87.73     89.51    87.03      88.38       30524         88.38
## 2022-01-21     87.35     88.22    85.71      87.89       29566         87.89
## 2022-01-24     87.65     88.88    85.02      86.27       34253         86.27
## 2022-01-25     87.17     88.36    86.19      88.20       29496         88.20
## 2022-01-26     88.02     90.48    87.80      89.96       29805         89.96
## 2022-01-27     89.78     91.04    88.98      89.34       15201         89.34
## 2022-01-28     89.89     91.69    89.41      90.03       10824         90.03
## 2022-01-31     90.80     91.30    90.75      91.21         118         91.21
## 2022-02-01     91.29     91.29    91.29      91.29       36248         91.29
## 2022-02-02     89.29     90.51    88.28      89.47       38172         89.47
## 2022-02-03     89.06     91.29    88.01      91.11       33059         91.11
## 2022-02-04     91.04     93.70    90.89      93.27       33357         93.27
## 2022-02-07     92.73     93.99    92.15      92.69       37016         92.69
## 2022-02-08     93.01     93.01    89.93      90.78       39288         90.78
## 2022-02-09     91.27     92.06    90.06      91.55       34759         91.55
## 2022-02-10     91.72     93.09    90.90      91.41       43235         91.41
## 2022-02-11     91.26     95.64    90.52      94.44       53045         94.44
## 2022-02-14     95.31     96.78    93.46      96.48       48449         96.48
## 2022-02-15     95.76     96.24    92.06      93.28       45181         93.28
## 2022-02-16     93.59     96.07    91.14      94.81       45148         94.81
## 2022-02-17     92.09     94.51    91.82      92.97       38045         92.97
## 2022-02-18     92.98     94.15    90.26      93.54       42436         93.54
## 2022-02-22     94.28     99.44    92.56      96.84       59945         96.84
## 2022-02-23     96.63     98.70    95.80      96.84       33549         96.84
## 2022-02-24     97.56    105.75    97.49      99.08       21282         99.08
## 2022-02-25     99.65    101.99    96.00      97.93        7025         97.93
## 2022-02-28    100.48    104.48    99.90     100.99         448        100.99
## 2022-03-01    100.85    100.85   100.85     100.85       56428        100.85
## 2022-03-02    107.54    115.05   106.49     112.93       59273        112.93
## 2022-03-03    114.25    119.77   109.42     110.46       37420        110.46
## 2022-03-04    110.58    118.97   109.61     118.11       34984        118.11
## 2022-03-07    121.24    137.00   119.07     123.21       29504        123.21
## 2022-03-08    124.25    133.13   121.37     127.98       38358        127.98
## 2022-03-09    129.57    131.63   108.00     111.14       42740        111.14
## 2022-03-10    112.74    118.33   108.95     109.33       30414        109.33
## 2022-03-11    109.72    113.88   107.13     112.67       18819        112.67
## 2022-03-14    112.90    113.04   103.45     106.90       19364        106.90
## 2022-03-15    106.00    106.46    97.50      99.91       26067         99.91
## 2022-03-16     99.04    103.68    96.95      98.02       18514         98.02
## 2022-03-17     98.10    107.57    97.88     106.64       15091        106.64
## 2022-03-18    107.24    109.57   105.80     107.93       10489        107.93
## 2022-03-21    107.37    116.73   107.09     115.62       11620        115.62
## 2022-03-22    116.85    119.42   112.77     115.48       14222        115.48
## 2022-03-23    114.74    122.29   114.42     121.60       14286        121.60
## 2022-03-24    121.27    123.70   116.95     119.03       12778        119.03
## 2022-03-25    118.28    120.87   115.21     120.65       14026        120.65
## 2022-03-28    120.31    120.31   109.06     112.48       15212        112.48
## 2022-03-29    109.73    114.71   104.98     110.23        7152        110.23
## 2022-03-30    111.00    114.65   110.90     113.45        4472        113.45
## 2022-03-31    108.71    109.36   107.37     107.91          31        107.91
## 2022-04-01    107.67    107.67   107.67     107.67       17144        107.67
## 2022-04-04    104.25    108.55   102.91     107.53       18406        107.53
## 2022-04-05    108.24    109.85   104.56     106.64       15613        106.64
## 2022-04-06    105.79    108.66   100.54     101.07       20212        101.07
## 2022-04-07    102.15    103.50    98.45     100.58       19577        100.58
## 2022-04-08    101.69    103.25    99.71     102.78       16735        102.78
## 2022-04-11    103.07    103.09    97.62      98.48       23852         98.48
## 2022-04-12     99.25    105.60    98.98     104.64       22697        104.64
## 2022-04-13    104.98    109.00   104.07     108.78       22260        108.78
## 2022-04-14    108.37    112.39   106.64     111.70       17418        111.70
## 2022-04-18    111.89    114.82   110.72     113.16       13187        113.16
## 2022-04-19    112.65    114.05   106.77     107.25       18972        107.25
## 2022-04-20    107.72    108.98   104.67     106.80       15985        106.80
## 2022-04-21    107.01    109.79   106.78     108.33       13203        108.33
## 2022-04-22    108.64    108.73   105.53     106.65       11040        106.65
## 2022-04-25    105.74    105.95    99.47     102.32       15464        102.32
## 2022-04-26    102.57    106.15   101.12     104.99       13279        104.99
## 2022-04-27    105.37    106.35   103.27     105.32        8064        105.32
## 2022-04-28    104.76    107.93   103.30     107.59        8567        107.59
## 2022-04-29    107.65    109.77   107.65     109.34          55        109.34
## 2022-05-02    109.36    109.36   109.36     109.36       23606        109.36
## 2022-05-03    107.37    108.30   104.62     104.97       23410        104.97
## 2022-05-04    106.10    111.00   105.50     110.14       21158        110.14
## 2022-05-05    110.14    113.99   109.23     110.90       26443        110.90
## 2022-05-06    111.15    113.52   109.88     112.39       23902        112.39
## 2022-05-09    113.05    113.22   104.95     105.94       28134        105.94
## 2022-05-10    105.56    106.91   101.70     102.46       25904        102.46
## 2022-05-11    101.70    108.26   100.93     107.51       31560        107.51
## 2022-05-12    107.56    108.69   104.69     107.45       27037        107.45
## 2022-05-13    108.00    111.69   107.81     111.55       25050        111.55
## 2022-05-16    111.41    114.78   109.04     114.24       20871        114.24
## 2022-05-17    114.29    115.66   111.12     111.93       23254        111.93
## 2022-05-18    112.89    114.13   108.35     109.11       21217        109.11
## 2022-05-19    109.30    112.27   105.70     112.04       26098        112.04
## 2022-05-20    111.50    113.22   110.54     112.55       16942        112.55
## 2022-05-23    112.74    114.36   111.86     113.42       20660        113.42
## 2022-05-24    113.36    114.63   111.72     113.56       20941        113.56
## 2022-05-25    113.92    115.32   113.04     114.03       12885        114.03
## 2022-05-26    114.45    118.00   113.84     117.40       11590        117.40
## 2022-05-27    117.54    119.73   116.68     119.43        4384        119.43
## 2022-05-30        NA        NA       NA         NA          NA            NA
## 2022-05-31    119.47    124.13   119.36     122.84        1138        122.84
## 2022-06-01    116.63    118.58   115.43     116.29       21546        116.29
## 2022-06-02    115.82    118.44   112.48     117.61       22117        117.61
## 2022-06-03    118.26    121.44   116.08     119.72       11028        119.72
## 2022-06-06    121.35    121.89   118.76     119.51       16523        119.51
## 2022-06-07    120.08    121.38   118.56     120.57       20488        120.57
## 2022-06-08    121.03    124.41   120.46     123.58       21778        123.58
## 2022-06-09    123.89    124.33   122.50     123.07       21008        123.07
## 2022-06-10    122.94    124.33   119.87     122.01       26036        122.01
## 2022-06-13    121.69    123.61   118.95     122.27       21136        122.27
## 2022-06-14    122.50    125.18   118.94     121.17       27702        121.17
## 2022-06-15    121.00    121.85   117.75     118.51       22360        118.51
## 2022-06-16    119.12    120.28   115.58     119.81       24329        119.81
## 2022-06-17    119.34    121.25   111.72     113.12       26686        113.12
## 2022-06-20    113.80    114.46   111.57     114.20       26686        114.20
## 2022-06-21    113.80    116.25   111.57     114.65       22868        114.65
## 2022-06-22    114.57    114.57   107.03     111.74       33112        111.74
## 2022-06-23    110.22    112.69   108.11     110.05       21806        110.05
## 2022-06-24    109.81    113.99   109.27     113.12       13431        113.12
## 2022-06-27    112.46    116.04   111.25     115.09       11252        115.09
## 2022-06-28    115.84    118.24   115.40     117.98        6673        117.98
## 2022-06-29    117.96    120.38   115.41     116.26        4346        116.26
## 2022-06-30    116.04    116.33   114.81     114.81       24733        114.81
## 2022-07-01    109.46    112.42   108.01     111.63       17090        111.63
## 2022-07-04        NA        NA       NA         NA          NA            NA
## 2022-07-05    111.61    114.69   101.11     102.77       43356        102.77
## 2022-07-06    104.00    105.80    98.51     100.69       28820        100.69
## 2022-07-07     99.96    106.35    98.47     104.65       22837        104.65
## 2022-07-08    104.49    107.45   103.75     107.02       20610        107.02
## 2022-07-11    106.76    107.66   103.66     107.10       17691        107.10
## 2022-07-12    106.23    106.51    98.91      99.49       22827         99.49
## 2022-07-13     99.31    101.20    97.30      99.57       22358         99.57
## 2022-07-14     99.85    100.37    94.50      99.10       27515         99.10
## 2022-07-15     99.60    102.62    98.21     101.16       19146        101.16
## 2022-07-18    100.92    106.47    99.48     106.27       20217        106.27
## 2022-07-19    105.59    107.60   103.59     107.35       21900        107.35
## 2022-07-20    107.15    107.43   105.09     106.92       23989        106.92
## 2022-07-21    106.79    106.80   101.52     103.86       26598        103.86
## 2022-07-22    104.25    105.68   101.91     103.20       17586        103.20
## 2022-07-25    103.44    105.35   101.67     105.15       14999        105.15
## 2022-07-26    104.81    107.35   103.98     104.40       20242        104.40
## 2022-07-27    104.78    107.80   103.72     106.62       11024        106.62
## 2022-07-28    107.49    108.98   105.96     107.14        6831        107.14
## 2022-07-29    108.05    110.43   108.03     110.01       24476        110.01
## 2022-08-01    103.87    104.37    99.10     100.03       25670        100.03
## 2022-08-02    100.00    102.41    98.47     100.54       17357        100.54
## 2022-08-03     99.64    102.37    96.48      96.78       22263         96.78
## 2022-08-04     97.01     97.63    93.15      94.12       21011         94.12
## 2022-08-05     93.59     96.40    92.75      94.92       16576         94.92
## 2022-08-08     94.27     96.73    92.99      96.65       17288         96.65
## 2022-08-09     96.54     98.39    94.91      96.31       20553         96.31
## 2022-08-10     96.46     97.98    93.61      97.40       29520         97.40
## 2022-08-11     97.27    100.16    96.65      99.60       20958         99.60
## 2022-08-12     99.29    100.35    96.94      98.15       20095         98.15
## 2022-08-15     97.76     98.04    92.72      95.10       20714         95.10
## 2022-08-16     93.64     95.95    91.72      92.34       22549         92.34
## 2022-08-17     92.77     94.46    91.52      93.65       21011         93.65
## 2022-08-18     93.18     97.41    93.05      96.59       21327         96.59
## 2022-08-19     96.63     97.87    94.25      96.72       22212         96.72
## 2022-08-22     95.66     97.25    92.36      96.48       26974         96.48
## 2022-08-23     96.58    100.45    96.51     100.22       22624        100.22
## 2022-08-24    100.16    102.00    99.07     101.22       24490        101.22
## 2022-08-25    101.60    102.47    99.12      99.34       20704         99.34
## 2022-08-26     99.88    101.17    98.14     100.99       14241        100.99
## 2022-08-29    100.83    105.48   100.29     105.09        6048        105.09
## 2022-08-30    105.00    105.37    97.67      99.31        7116         99.31
## 2022-08-31     99.71    100.30    95.76      96.49       24672         96.49
```

```r
  brent <- na.omit(dados.brent)
```

#### Cria o vetor de preco de fechamento

```r
  preco_fechamento <- dados.dj$"BZ=F.Close"
```

#### 1. Media do Preco de Fechamento ----

```r
  media_pf <- mean(preco_fechamento)
```

```
## Warning in mean.default(preco_fechamento): argument is not numeric or logical: returning NA
```

```r
  media_pf
```

```
## [1] NA
```

#### 2. Moda do Preco de Fechamento ----

```r
  tab_preco_fechamento <- table(preco_fechamento)
  moda_pf <- names(tab_preco_fechamento)[which(tab_preco_fechamento==max(tab_preco_fechamento))]
```

```
## Warning in max(tab_preco_fechamento): no non-missing arguments to max; returning -Inf
```

```r
  moda_pf
```

```
## NULL
```

#### 3. Mediana do Preco de Fechamento ----

```r
  mediana_pf <- median(preco_fechamento)
  mediana_pf
```

```
## NULL
```

#### 4. Variancia Nao Viesada ----

```r
  variancia_pf <- var(preco_fechamento)
```

```
## Error in var(preco_fechamento): 'x' is NULL
```

```r
  variancia_pf
```

```
##           DJI.Close
## DJI.Close   2520219
```

#### 5. Desvio-padrao ----

```r
  desv_pad_pf <- sd(preco_fechamento)
  desv_pad_pf
```

```
## [1] NA
```

#### 6. Grafico de linha do Preco de Fechamento ----

```r
  ggplot(dados.dj, aes(x = index(dados.dj), y = preco_fechamento)) + geom_line() +
        labs(title="Grafico do Petroleo Brent", subtitle="Preco de Fechamento", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Preco (R$)") +
        theme(plot.title = element_text(hjust = 0.5), plot.subtitle = element_text(hjust = 0.5)) +
        scale_x_date(date_labels = "%b %y", date_breaks = "1 month")
```

```
## Error in `check_required_aesthetics()`:
## ! geom_line requires the following missing aesthetics: y
```

#### 7. Retorno, com base no Preco de Fechamento ----

```r
  retorno_pf <- (preco_fechamento - shift(preco_fechamento, 1L, type="lag"))/shift(preco_fechamento, 1L, type="lag")
  retorno_pf <- na.omit(retorno_pf)
  tabela_preco_retorno <- cbind(preco_fechamento, retorno_pf)
  head(tabela_preco_retorno)
```

```
##      preco_fechamento retorno_pf
```

#### 8. Grafico de linha do Retorno ----

```r
  ggplot(retorno_pf, aes(x = index(retorno_pf), y = 100*retorno_pf)) + geom_line() +
        labs(title="Grafico do Petroleo Brent", subtitle="Retorno", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Retorno (%)") +
        theme(plot.title = element_text(hjust = 0.5), plot.subtitle = element_text(hjust = 0.5)) +
        scale_x_date(date_labels = "%b %y", date_breaks = "1 month")
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

#### 9. Box plot para dados originais (Preco de Fechamento e Retorno) e padronizados ----

```r
  boxplot_pf <- ggplot(data = preco_fechamento, aes(x = "", y = preco_fechamento))+
                      geom_violin(trim = FALSE, color="blue") +
                      geom_boxplot(width=0.4, color="blue", alpha = 1, outlier.size = 1) +
                      labs(x = "Preco", y = "") +
                      scale_y_continuous(breaks = seq(16, 23, by = 1))

  z_preco_fechamento <- (preco_fechamento - mean(preco_fechamento)) / sd(preco_fechamento)
```

```
## Warning in mean.default(preco_fechamento): argument is not numeric or logical: returning NA
```

```r
  boxplot_z_pf <- ggplot(data = z_preco_fechamento, aes(x = "", y = z_preco_fechamento)) +
                        geom_violin(trim = FALSE, color="goldenrod3") +
                        geom_boxplot(width=0.4, color="red", alpha = 1, outlier.size = 1)+
                        labs(x = "Preco Padronizado", y = "") +
                        scale_y_continuous(breaks = seq(-5, 23, by = 1))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  boxplots_pf <- ggarrange(boxplot_pf, boxplot_z_pf,ncol = 2, nrow = 1)
```

```
## Error in `check_required_aesthetics()`:
## ! stat_ydensity requires the following missing aesthetics: y
```

```r
  annotate_figure(boxplots_pf, top = text_grob("Boxplot/Vioplot do Preco de Fechamento\ne Preco de Fechamento Padronizado", color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/", color = "black", hjust = 1.02, x = 1,size = 10))
```

![plot of chunk unnamed-chunk-11](figure/unnamed-chunk-11-1.png)

```r
  boxplot_retorno <- ggplot(data = retorno_pf, aes(x = "", y = 100*retorno_pf)) +
                            geom_violin(trim = FALSE, color="blue") +
                            geom_boxplot(width=0.4, color="blue", alpha = 1, outlier.size = 1) +
                            labs(x = "Retorno (%)", y = "") +
                            scale_y_continuous(breaks = seq(-7, 6, by = 2))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  z_retorno_pf <- (retorno_pf - mean(retorno_pf))/(sd(retorno_pf))

  boxplot_z_retorno_pf <- ggplot(data = z_retorno_pf, aes(x = "", y = z_retorno_pf)) +
                            geom_violin(trim = FALSE, color="red") +
                            geom_boxplot(width=0.4, color="red", alpha = 1, outlier.size = 1) +
                            labs(x = "Retorno Padronizado", y = "") +
                            scale_y_continuous(breaks = seq(-3, 11, by = 2))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  boxplots_retorno <- ggarrange(boxplot_retorno, boxplot_z_retorno_pf,ncol = 2, nrow = 1)
```

```
## Error in `check_aesthetics()`:
## ! Aesthetics must be either length 1 or the same as the data (166): y
```

```r
  annotate_figure(boxplots_retorno, top = text_grob("Boxplot/Vioplot do Retorno\ne Retorno Padronizado",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

![plot of chunk unnamed-chunk-11](figure/unnamed-chunk-11-2.png)


#### 10. Histograma para dados originais (Preco de Fechamento e Retorno) e padronizados ----

```r
  histograma_pf <- ggplot(data = preco_fechamento,aes(x = preco_fechamento)) +
                          geom_histogram(color="blue", fill = "white", bins = 30) +
                          labs(y = "Quantidade", x = "Preco") +
                          scale_x_continuous(breaks = seq(17, 22, by = 0.5)) +
                          scale_y_continuous(breaks = seq(0, 30, by = 5)) +
                          theme(plot.title = element_text(hjust = 0.5))

  histograma_z_pf <- ggplot(data = z_preco_fechamento,aes(x = z_preco_fechamento)) +
                            geom_histogram(color="red", fill = "white", bins = 30) +
                            labs(y = "Quantidade", x = "Preco Padronizado") +
                            scale_x_continuous(breaks = seq(-2, 3.5, by = 0.5)) +
                            scale_y_continuous(breaks = seq(0, 50, by = 5)) +
                            theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  histogramas_pf <- ggarrange(histograma_pf, histograma_z_pf,ncol = 1, nrow = 2)
```

```
## Error in `check_aesthetics()`:
## ! Aesthetics must be either length 1 or the same as the data (167): x
```

```r
  annotate_figure(histogramas_pf, top = text_grob("Histograma do Preco de Fechamento",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

![plot of chunk unnamed-chunk-12](figure/unnamed-chunk-12-1.png)

```r
  histograma_retorno <- ggplot(data = retorno_pf,aes(x = 100*retorno_pf)) + 
                                geom_histogram(color="blue", fill = "white", bins = 25) + 
                                labs(y = "Quantidade", x = "Retorno (%)") + 
                                scale_x_continuous(breaks = seq(-6, 6, by = 1)) + 
                                scale_y_continuous(breaks = seq(0, 40, by = 5)) + 
                                theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  histograma_z_retorno <- ggplot(data = z_retorno_pf ,aes(x = z_retorno_pf)) + 
                                geom_histogram(color="red", fill = "white", bins = 25) + 
                                labs(y = "Quantidade", x = "Retorno Padronizado") + 
                                scale_x_continuous(breaks = seq(-6, 6, by = 1)) + 
                                scale_y_continuous(breaks = seq(0, 35, by = 5)) + 
                                theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  histogramas_retorno <- ggarrange(histograma_retorno, histograma_z_retorno,ncol = 1, nrow = 2)
```

```
## Error in `check_aesthetics()`:
## ! Aesthetics must be either length 1 or the same as the data (166): x
```

```r
  annotate_figure(histogramas_retorno, top = text_grob("Histograma do Retorno",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

![plot of chunk unnamed-chunk-12](figure/unnamed-chunk-12-2.png)

#### 11. QQPlot do retorno.  ----

```r
  qqplot_retorno <- ggplot(data = retorno_pf, aes(sample = 100*as.vector(retorno_pf))) +
                          stat_qq(size = 0.6) +labs(x = "Quantis Teoricos", y = "Quantis Amostrais",
                          title = "QQPlot do Retorno (%)") + theme(plot.title = element_text(hjust = 0.5)) +
                          scale_y_continuous(breaks = seq(-6, 4.5, by = 1.5))
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

#### 12. QQLine do retorno (fazer junto com o QQPlot).  ----

```r
  histograma_retorno_qqplot <- ggplot(data = retorno_pf,aes(x = 100*retorno_pf)) +
                                      geom_histogram(aes(y=..density..),color="blue", fill = "white", bins = 25) +
                                      stat_function(fun = dnorm, args = list(mean = mean(100*retorno_pf), sd = sd(100*retorno_pf)),
                                      col="red",lwd=1)+ theme(axis.text.x = element_blank(), axis.text.y = element_blank()) +
                                      labs(y = "", x = "") 
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  qqplot_linha_retorno <- ggplot(data = retorno_pf, aes(sample = 100*as.vector(retorno_pf))) +
                                stat_qq(size = 0.6) + labs(x = "Quantis Teoricos", y = "Quantis Amostrais", title = "QQPlot do Retorno (%)") +
                                theme(plot.title = element_text(hjust = 0.5)) +scale_y_continuous(breaks = seq(-6, 4.5, by = 1.5)) +
                                stat_qq_line(col = 2,lwd=1,lty=1) 
```

```
## Error in `fortify()`:
## ! `data` must be a data frame, or other object coercible by `fortify()`, not a numeric vector.
```

```r
  plot_principal <- qqplot_linha_retorno

  plot_para_inserir <- histograma_retorno_qqplot

  plot.com.insercao <- ggdraw() + draw_plot(plot_principal) + draw_plot(plot_para_inserir, x = 0.07, y = 0.6, width = .3, height = .3)
```

```
## Error in `check_aesthetics()`:
## ! Aesthetics must be either length 1 or the same as the data (166): sample
```

```r
  plot.com.insercao
```

![plot of chunk unnamed-chunk-14](figure/unnamed-chunk-14-1.png)

#### 13. Assimetria amostral nao viesada do retorno.   ----

```r
  n <- length(retorno_pf)
  somatorio <- c()
  for(i in 1:n){
    somatorio[i] <- ((retorno_pf[i] - mean(retorno_pf))/ sd(retorno_pf))^3
  }
  p1_s3 <- n/((n -1)*(n-2))
  p2_s3 <- sum(somatorio)
  s3 <- p1_s3*p2_s3
  s3
```

```
## [1] NA
```

#### 14. Curtose amostral nao viesada do retorno.   ----

```r
  n <- length(retorno_pf)
  somatorio <- c()
  for(i in 1:n){
    somatorio[i] <- ((retorno_pf[i] - mean(retorno_pf))/ sd(retorno_pf))^4
  }
  p1_s4 <- (n*(n +1))/((n -1)*(n-2)*(n-3))
  p2_s4 <- (sum(somatorio))
  p3_s4 <- (3*((n-1)^2))/((n-2)*(n-3))
  s4 <- p1_s4 * p2_s4 - p3_s4
  s4
```

```
## [1] NA
```


```r
  library("knitr")
  knit("./q1/q1_brent.rmd", output = "./q1/q1_brent.md")
```

```
## Warning in file(con, "r"): cannot open file './q1/q1_brent.rmd': No such file or directory
```

```
## Error in file(con, "r"): cannot open the connection
```
