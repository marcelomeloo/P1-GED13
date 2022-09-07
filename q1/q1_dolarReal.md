>### Dados Dolar Real

```r
  dados.dolar.real <- quantmod::getSymbols("BRL=X", src = "yahoo", from = start, to = end, auto.assign = FALSE)
  dados.dolar.real
```

```
##            BRL=X.Open BRL=X.High BRL=X.Low BRL=X.Close BRL=X.Volume BRL=X.Adjusted
## 2022-01-03   5.460600   5.670700  5.460600    5.569300            0       5.569300
## 2022-01-04   5.680900   5.707600  5.638900    5.681200            0       5.681200
## 2022-01-05   5.676000   5.691600  5.641800    5.676200            0       5.676200
## 2022-01-06   5.707700   5.721800  5.682800    5.705635            0       5.705635
## 2022-01-07   5.680289   5.706900  5.619900    5.682400            0       5.682400
## 2022-01-10   5.632000   5.689500  5.624600    5.632200            0       5.632200
## 2022-01-11   5.662100   5.673000  5.581573    5.662200            0       5.662200
## 2022-01-12   5.568400   5.598800  5.545577    5.567300            0       5.567300
## 2022-01-13   5.533100   5.558000  5.497654    5.533200            0       5.533200
## 2022-01-14   5.527500   5.550500  5.523507    5.526700            0       5.526700
## 2022-01-17   5.531900   5.534100  5.493700    5.533300            0       5.533300
## 2022-01-18   5.515800   5.546500  5.504800    5.515800            0       5.515800
## 2022-01-19   5.565500   5.566300  5.459912    5.565700            0       5.565700
## 2022-01-20   5.437200   5.456800  5.399700    5.437200            0       5.437200
## 2022-01-21   5.415809   5.473500  5.404100    5.418100            0       5.418100
## 2022-01-24   5.455800   5.517100  5.448961    5.457100            0       5.457100
## 2022-01-25   5.486100   5.517700  5.465400    5.486100            0       5.486100
## 2022-01-26   5.440295   5.454000  5.412000    5.440704            0       5.440704
## 2022-01-27   5.429167   5.432100  5.352800    5.429167            0       5.429167
## 2022-01-28   5.403456   5.424200  5.375200    5.403485            0       5.403485
## 2022-01-31   5.365500   5.395800  5.282676    5.362600            0       5.362600
## 2022-02-01   5.303100   5.313705  5.271400    5.303100            0       5.303100
## 2022-02-02   5.264700   5.311900  5.255267    5.264500            0       5.264500
## 2022-02-03   5.261500   5.319600  5.258240    5.260900            0       5.260900
## 2022-02-04   5.282800   5.348600  5.277500    5.282900            0       5.282900
## 2022-02-07   5.326200   5.343000  5.276800    5.326900            0       5.326900
## 2022-02-08   5.262800   5.284900  5.251000    5.262600            0       5.262600
## 2022-02-09   5.256489   5.288000  5.232774    5.258400            0       5.258400
## 2022-02-10   5.231429   5.244600  5.170000    5.234500            0       5.234500
## 2022-02-11   5.248600   5.251200  5.182800    5.248700            0       5.248700
## 2022-02-14   5.250500   5.263300  5.195300    5.249956            0       5.249956
## 2022-02-15   5.213700   5.219900  5.166288    5.214000            0       5.214000
## 2022-02-16   5.158000   5.184725  5.143800    5.157900            0       5.157900
## 2022-02-17   5.133567   5.180000  5.121471    5.135800            0       5.135800
## 2022-02-18   5.168756   5.175100  5.116900    5.170600            0       5.170600
## 2022-02-21   5.136400   5.149900  5.074800    5.137500            0       5.137500
## 2022-02-22   5.102300   5.106600  5.046696    5.102700            0       5.102700
## 2022-02-23   5.057200   5.060600  4.996500    5.057100            0       5.057100
## 2022-02-24   5.006725   5.146600  5.000000    5.008700            0       5.008700
## 2022-02-25   5.120520   5.166200  5.076349    5.122200            0       5.122200
## 2022-02-28   5.166000   5.166500  5.151300    5.159400            0       5.159400
## 2022-03-01   5.158900   5.159900  5.154538    5.158400            0       5.158400
## 2022-03-02   5.159900   5.212400  5.146400    5.159000            0       5.159000
## 2022-03-03   5.098700   5.107600  5.018600    5.096503            0       5.096503
## 2022-03-04   5.031000   5.097900  5.026275    5.030900            0       5.030900
## 2022-03-07   5.058900   5.088916  5.026200    5.060560            0       5.060560
## 2022-03-08   5.110100   5.111830  5.060375    5.110500            0       5.110500
## 2022-03-09   5.059000   5.060000  4.983800    5.058800            0       5.058800
## 2022-03-10   5.011100   5.073300  5.000905    5.011500            0       5.011500
## 2022-03-11   5.010200   5.053000  4.983300    5.009700            0       5.009700
## 2022-03-14   5.073100   5.083800  5.037000    5.073500            0       5.073500
## 2022-03-15   5.121700   5.149500  5.089902    5.121400            0       5.121400
## 2022-03-16   5.163200   5.163700  5.095000    5.163200            0       5.163200
## 2022-03-17   5.076000   5.104300  5.040100    5.073875            0       5.073875
## 2022-03-18   5.036666   5.071900  5.008420    5.039400            0       5.039400
## 2022-03-21   5.017800   5.025100  4.928282    5.017800            0       5.017800
## 2022-03-22   4.933000   4.948900  4.903000    4.935200            0       4.935200
## 2022-03-23   4.910000   4.912000  4.843000    4.910000            0       4.910000
## 2022-03-24   4.824200   4.837570  4.763647    4.824200            0       4.824200
## 2022-03-25   4.826100   4.828500  4.746200    4.826300            0       4.826300
## 2022-03-28   4.736900   4.815800  4.730483    4.736900            0       4.736900
## 2022-03-29   4.764100   4.771100  4.714928    4.764100            0       4.764100
## 2022-03-30   4.756200   4.786300  4.726700    4.756200            0       4.756200
## 2022-03-31   4.769700   4.790800  4.723229    4.769700            0       4.769700
## 2022-04-01   4.737800   4.739600  4.689045    4.737800            0       4.737800
## 2022-04-04   4.657200   4.670100  4.604057    4.657200            0       4.657200
## 2022-04-05   4.593800   4.669100  4.575500    4.593800            0       4.593800
## 2022-04-06   4.650700   4.712600  4.647900    4.650700            0       4.650700
## 2022-04-07   4.715200   4.769900  4.690400    4.715200            0       4.715200
## 2022-04-08   4.752100   4.791300  4.707518    4.752100            0       4.752100
## 2022-04-11   4.698000   4.732600  4.684016    4.698100            0       4.698100
## 2022-04-12   4.693600   4.697100  4.621500    4.693600            0       4.693600
## 2022-04-13   4.673100   4.702300  4.653200    4.673100            0       4.673100
## 2022-04-14   4.690200   4.738100  4.669788    4.690200            0       4.690200
## 2022-04-15   4.701000   4.710000  4.696500    4.701000            0       4.701000
## 2022-04-18   4.700600   4.704900  4.659300    4.700600            0       4.700600
## 2022-04-19   4.652000   4.683800  4.637000    4.652000            0       4.652000
## 2022-04-20   4.665000   4.676700  4.609000    4.665000            0       4.665000
## 2022-04-21   4.620800   4.621600  4.606555    4.620800            0       4.620800
## 2022-04-22   4.620800   4.770700  4.617611    4.620800            0       4.620800
## 2022-04-25   4.795200   4.943000  4.790587    4.795200            0       4.795200
## 2022-04-26   4.876200   4.995800  4.873625    4.876200            0       4.876200
## 2022-04-27   4.997800   5.036400  4.977440    4.997800            0       4.997800
## 2022-04-28   4.963600   5.040900  4.960196    4.963600            0       4.963600
## 2022-04-29   4.937800   4.954800  4.858228    4.937800            0       4.937800
## 2022-05-02   4.971300   5.040200  4.967100    4.971300            0       4.971300
## 2022-05-03   5.084700   5.085800  4.992600    5.084700            0       5.084700
## 2022-05-04   4.958100   5.028500  4.954729    4.958100            0       4.958100
## 2022-05-05   4.918800   5.052800  4.903801    4.918800            0       4.918800
## 2022-05-06   5.028000   5.111400  5.009100    5.028000            0       5.028000
## 2022-05-09   5.080400   5.148389  5.074281    5.080400            0       5.080400
## 2022-05-10   5.160900   5.162200  5.111000    5.160900            0       5.160900
## 2022-05-11   5.131300   5.165100  5.091936    5.131300            0       5.131300
## 2022-05-12   5.134252   5.207500  5.106800    5.134252            0       5.134252
## 2022-05-13   5.133400   5.145900  5.068500    5.133400            0       5.133400
## 2022-05-16   5.058300   5.101700  5.031900    5.058300            0       5.058300
## 2022-05-17   5.059700   5.060600  4.949100    5.059700            0       5.059700
## 2022-05-18   4.938100   4.978100  4.915875    4.938100            0       4.938100
## 2022-05-19   4.967500   4.970300  4.893300    4.967500            0       4.967500
## 2022-05-20   4.930000   4.931200  4.852000    4.930000            0       4.930000
## 2022-05-23   4.880200   4.880200  4.789300    4.880200            0       4.880200
## 2022-05-24   4.813500   4.851000  4.774023    4.813500            0       4.813500
## 2022-05-25   4.817800   4.858800  4.814712    4.817800            0       4.817800
## 2022-05-26   4.822800   4.840900  4.776500    4.822800            0       4.822800
## 2022-05-27   4.768200   4.777900  4.713917    4.768200            0       4.768200
## 2022-05-30   4.729600   4.741600  4.690600    4.729600            0       4.729600
## 2022-05-31   4.752400   4.774024  4.696900    4.752400            0       4.752400
## 2022-06-01   4.730400   4.806800  4.721500    4.730400            0       4.730400
## 2022-06-02   4.815500   4.816600  4.773600    4.815500            0       4.815500
## 2022-06-03   4.795700   4.828400  4.765131    4.795700            0       4.795700
## 2022-06-06   4.775000   4.802700  4.745628    4.775000            0       4.775000
## 2022-06-07   4.794200   4.926400  4.789800    4.794200            0       4.794200
## 2022-06-08   4.867526   4.904300  4.842500    4.867526            0       4.867526
## 2022-06-09   4.898100   4.915600  4.865091    4.898100            0       4.898100
## 2022-06-10   4.903300   5.008600  4.883527    4.903300            0       4.903300
## 2022-06-13   4.984000   5.134800  4.983900    4.984000            0       4.984000
## 2022-06-14   5.113400   5.134300  5.083500    5.113400            0       5.113400
## 2022-06-15   5.116100   5.131100  5.082382    5.116100            0       5.116100
## 2022-06-16   5.052000   5.053900  5.046274    5.052000            0       5.052000
## 2022-06-17   5.052200   5.146500  5.049120    5.052200            0       5.052200
## 2022-06-20   5.152100   5.186600  5.135865    5.152100            0       5.152100
## 2022-06-21   5.187200   5.189000  5.117500    5.187200            0       5.187200
## 2022-06-22   5.122800   5.178600  5.120937    5.122800            0       5.122800
## 2022-06-23   5.193600   5.212000  5.165558    5.193600            0       5.193600
## 2022-06-24   5.238000   5.273400  5.202000    5.238000            0       5.238000
## 2022-06-27   5.241400   5.273200  5.200900    5.241400            0       5.241400
## 2022-06-28   5.236800   5.260100  5.186483    5.236800            0       5.236800
## 2022-06-29   5.266600   5.272400  5.208400    5.266600            0       5.266600
## 2022-06-30   5.180900   5.268800  5.177619    5.180900            0       5.180900
## 2022-07-01   5.252000   5.335400  5.249412    5.252000            0       5.252000
## 2022-07-04   5.331000   5.331400  5.287100    5.331000            0       5.331000
## 2022-07-05   5.328300   5.401300  5.304464    5.328300            0       5.328300
## 2022-07-06   5.385200   5.459700  5.381861    5.385200            0       5.385200
## 2022-07-07   5.428000   5.429500  5.329027    5.428000            0       5.428000
## 2022-07-08   5.338200   5.363200  5.277800    5.338200            0       5.338200
## 2022-07-11   5.254000   5.359000  5.250876    5.254000            0       5.254000
## 2022-07-12   5.377200   5.427000  5.371500    5.377200            0       5.377200
## 2022-07-13   5.436500   5.462500  5.362110    5.436500            0       5.436500
## 2022-07-14   5.390900   5.486600  5.388757    5.390900            0       5.390900
## 2022-07-15   5.422800   5.446100  5.375200    5.422800            0       5.422800
## 2022-07-18   5.410100   5.410600  5.350735    5.410100            0       5.410100
## 2022-07-19   5.436800   5.438500  5.371300    5.436800            0       5.436800
## 2022-07-20   5.413100   5.448000  5.384050    5.413100            0       5.413100
## 2022-07-21   5.470200   5.502300  5.431200    5.470200            0       5.470200
## 2022-07-22   5.497800   5.501500  5.435300    5.497800            0       5.497800
## 2022-07-25   5.496700   5.499600  5.399200    5.496700            0       5.496700
## 2022-07-26   5.356300   5.389700  5.331600    5.356300            0       5.356300
## 2022-07-27   5.350100   5.351000  5.291000    5.350100            0       5.350100
## 2022-07-28   5.243000   5.269000  5.174200    5.243000            0       5.243000
## 2022-07-29   5.182700   5.218888  5.148400    5.182700            0       5.182700
## 2022-08-01   5.171200   5.192600  5.127050    5.171200            0       5.171200
## 2022-08-02   5.184000   5.244200  5.157262    5.184000            0       5.184000
## 2022-08-03   5.277700   5.313000  5.246200    5.277700            0       5.277700
## 2022-08-04   5.282700   5.292000  5.211857    5.282700            0       5.282700
## 2022-08-05   5.211100   5.270994  5.181602    5.211100            0       5.211100
## 2022-08-08   5.164600   5.166300  5.102100    5.164600            0       5.164600
## 2022-08-09   5.110100   5.146700  5.093100    5.110100            0       5.110100
## 2022-08-10   5.123700   5.127700  5.035500    5.123700            0       5.123700
## 2022-08-11   5.093700   5.155400  5.056500    5.093700            0       5.093700
## 2022-08-12   5.157000   5.160900  5.082800    5.157000            0       5.157000
## 2022-08-15   5.074900   5.136300  5.067652    5.074900            0       5.074900
## 2022-08-16   5.095600   5.149100  5.075443    5.095600            0       5.095600
## 2022-08-17   5.141739   5.211300  5.141095    5.141739            0       5.141739
## 2022-08-18   5.165000   5.197000  5.129600    5.165000            0       5.165000
## 2022-08-19   5.167000   5.217000  5.164235    5.167000            0       5.167000
## 2022-08-22   5.168400   5.202100  5.161800    5.168400            0       5.168400
## 2022-08-23   5.156100   5.157100  5.071300    5.156100            0       5.156100
## 2022-08-24   5.103500   5.120300  5.077318    5.103500            0       5.103500
## 2022-08-25   5.110100   5.139700  5.081051    5.110100            0       5.110100
## 2022-08-26   5.108700   5.113700  5.064000    5.108700            0       5.108700
## 2022-08-29   5.062500   5.077800  5.024100    5.062500            0       5.062500
## 2022-08-30   5.027200   5.076500  4.998009    5.027200            0       5.027200
## 2022-08-31   5.121900   5.196800  5.093873    5.121900            0       5.121900
## 2022-09-01   5.181700   5.232300  5.144000    5.181700            0       5.181700
```

```r
  dolar.real <- na.omit(dados.dolar.real)
```

#### Cria o vetor de preco de fechamento

```r
  preco_fechamento <- dados.dj$"BRL=X.Close"
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
        labs(title="Grafico do Dolar Real", subtitle="Preco de Fechamento", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Preco (R$)") +
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
        labs(title="Grafico do Dolar Real", subtitle="Retorno", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Retorno (%)") +
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
  knit("./q1/q1_dolarReal.rmd", output = "./q1/q1_dolarReal.md")
```

```
## Warning in file(con, "r"): cannot open file './q1/q1_dolarReal.rmd': No such file or directory
```

```
## Error in file(con, "r"): cannot open the connection
```

