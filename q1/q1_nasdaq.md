>### Dados NASDAQ

```r
  dados.nasdaq <- quantmod::getSymbols("^IXIC", src = "yahoo", from = start, to = end, auto.assign = FALSE)
```

```
## Registered S3 method overwritten by 'quantmod':
##   method            from
##   as.zoo.data.frame zoo
```

```
## Error in getSymbols.yahoo(Symbols = "^IXIC", env = <environment>, verbose = FALSE, : Unable to import "^IXIC".
## do not know how to convert 'x' to class "Date"
```

```r
  dados.nasdaq
```

```
## Error in eval(expr, envir, enclos): object 'dados.nasdaq' not found
```

```r
  nasdaq <- na.omit(dados.nasdaq)
```

```
## Error in na.omit(dados.nasdaq): object 'dados.nasdaq' not found
```

#### Cria o vetor de preco de fechamento

```r
  preco_fechamento <- dados.nasdaq$"IXIC.Close"
```

```
## Error in eval(expr, envir, enclos): object 'dados.nasdaq' not found
```

#### 1. Media do Preco de Fechamento 

```r
  media_pf <- mean(preco_fechamento)
```

```
## Error in mean(preco_fechamento): object 'preco_fechamento' not found
```

```r
  media_pf
```

```
## Error in eval(expr, envir, enclos): object 'media_pf' not found
```

#### 2. Moda do Preco de Fechamento 

```r
  tab_preco_fechamento <- table(preco_fechamento)
```

```
## Error in table(preco_fechamento): object 'preco_fechamento' not found
```

```r
  moda_pf <- names(tab_preco_fechamento)[which(tab_preco_fechamento==max(tab_preco_fechamento))]
```

```
## Error in eval(expr, envir, enclos): object 'tab_preco_fechamento' not found
```

```r
  moda_pf
```

```
## Error in eval(expr, envir, enclos): object 'moda_pf' not found
```

#### 3. Mediana do Preco de Fechamento 

```r
  mediana_pf <- median(preco_fechamento)
```

```
## Error in median(preco_fechamento): object 'preco_fechamento' not found
```

```r
  mediana_pf
```

```
## Error in eval(expr, envir, enclos): object 'mediana_pf' not found
```

#### 4. Variancia Nao Viesada 

```r
  variancia_pf <- var(preco_fechamento)
```

```
## Error in is.data.frame(x): object 'preco_fechamento' not found
```

```r
  variancia_pf
```

```
## Error in eval(expr, envir, enclos): object 'variancia_pf' not found
```

#### 5. Desvio-padrao 

```r
  desv_pad_pf <- sd(preco_fechamento)
```

```
## Error in is.data.frame(x): object 'preco_fechamento' not found
```

```r
  desv_pad_pf
```

```
## Error in eval(expr, envir, enclos): object 'desv_pad_pf' not found
```

#### 6. Grafico de linha do Preco de Fechamento 

```r
  ggplot(dados.dj, aes(x = index(dados.dj), y = preco_fechamento)) + geom_line() +
        labs(title="Grafico do NASDAQ", subtitle="Preco de Fechamento", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Preco (R$)") +
        theme(plot.title = element_text(hjust = 0.5), plot.subtitle = element_text(hjust = 0.5)) +
        scale_x_date(date_labels = "%b %y", date_breaks = "1 month")
```

```
## Error in ggplot(dados.dj, aes(x = index(dados.dj), y = preco_fechamento)): could not find function "ggplot"
```

#### 7. Retorno, com base no Preco de Fechamento 

```r
  retorno_pf <- (preco_fechamento - shift(preco_fechamento, 1L, type="lag"))/shift(preco_fechamento, 1L, type="lag")
```

```
## Error in eval(expr, envir, enclos): object 'preco_fechamento' not found
```

```r
  retorno_pf <- na.omit(retorno_pf)
```

```
## Error in na.omit(retorno_pf): object 'retorno_pf' not found
```

```r
  tabela_preco_retorno <- cbind(preco_fechamento, retorno_pf)
```

```
## Error in cbind(preco_fechamento, retorno_pf): object 'preco_fechamento' not found
```

```r
  head(tabela_preco_retorno)
```

```
## Error in head(tabela_preco_retorno): object 'tabela_preco_retorno' not found
```

#### 8. Grafico de linha do Retorno 

```r
  ggplot(retorno_pf, aes(x = index(retorno_pf), y = 100*retorno_pf)) + geom_line() +
        labs(title="Grafico do NASDAQ", subtitle="Retorno", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Retorno (%)") +
        theme(plot.title = element_text(hjust = 0.5), plot.subtitle = element_text(hjust = 0.5)) +
        scale_x_date(date_labels = "%b %y", date_breaks = "1 month")
```

```
## Error in ggplot(retorno_pf, aes(x = index(retorno_pf), y = 100 * retorno_pf)): could not find function "ggplot"
```

#### 9. Box plot para dados originais (Preco de Fechamento e Retorno) e padronizados 

```r
  boxplot_pf <- ggplot(data = preco_fechamento, aes(x = "", y = preco_fechamento))+
                      geom_violin(trim = FALSE, color="blue") +
                      geom_boxplot(width=0.4, color="blue", alpha = 1, outlier.size = 1) +
                      labs(x = "Preco", y = "") +
                      scale_y_continuous(breaks = seq(16, 23, by = 1))
```

```
## Error in ggplot(data = preco_fechamento, aes(x = "", y = preco_fechamento)): could not find function "ggplot"
```

```r
  z_preco_fechamento <- (preco_fechamento - mean(preco_fechamento)) / sd(preco_fechamento)
```

```
## Error in eval(expr, envir, enclos): object 'preco_fechamento' not found
```

```r
  boxplot_z_pf <- ggplot(data = z_preco_fechamento, aes(x = "", y = z_preco_fechamento)) +
                        geom_violin(trim = FALSE, color="goldenrod3") +
                        geom_boxplot(width=0.4, color="red", alpha = 1, outlier.size = 1)+
                        labs(x = "Preco Padronizado", y = "") +
                        scale_y_continuous(breaks = seq(-5, 23, by = 1))
```

```
## Error in ggplot(data = z_preco_fechamento, aes(x = "", y = z_preco_fechamento)): could not find function "ggplot"
```

```r
  boxplots_pf <- ggarrange(boxplot_pf, boxplot_z_pf,ncol = 2, nrow = 1)
```

```
## Error in ggarrange(boxplot_pf, boxplot_z_pf, ncol = 2, nrow = 1): could not find function "ggarrange"
```

```r
  annotate_figure(boxplots_pf, top = text_grob("Boxplot/Vioplot do Preco de Fechamento\ne Preco de Fechamento Padronizado", color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/", color = "black", hjust = 1.02, x = 1,size = 10))
```

```
## Error in annotate_figure(boxplots_pf, top = text_grob("Boxplot/Vioplot do Preco de Fechamento\ne Preco de Fechamento Padronizado", : could not find function "annotate_figure"
```

```r
  boxplot_retorno <- ggplot(data = retorno_pf, aes(x = "", y = 100*retorno_pf)) +
                            geom_violin(trim = FALSE, color="blue") +
                            geom_boxplot(width=0.4, color="blue", alpha = 1, outlier.size = 1) +
                            labs(x = "Retorno (%)", y = "") +
                            scale_y_continuous(breaks = seq(-7, 6, by = 2))
```

```
## Error in ggplot(data = retorno_pf, aes(x = "", y = 100 * retorno_pf)): could not find function "ggplot"
```

```r
  z_retorno_pf <- (retorno_pf - mean(retorno_pf))/(sd(retorno_pf))
```

```
## Error in eval(expr, envir, enclos): object 'retorno_pf' not found
```

```r
  boxplot_z_retorno_pf <- ggplot(data = z_retorno_pf, aes(x = "", y = z_retorno_pf)) +
                            geom_violin(trim = FALSE, color="red") +
                            geom_boxplot(width=0.4, color="red", alpha = 1, outlier.size = 1) +
                            labs(x = "Retorno Padronizado", y = "") +
                            scale_y_continuous(breaks = seq(-3, 11, by = 2))
```

```
## Error in ggplot(data = z_retorno_pf, aes(x = "", y = z_retorno_pf)): could not find function "ggplot"
```

```r
  boxplots_retorno <- ggarrange(boxplot_retorno, boxplot_z_retorno_pf,ncol = 2, nrow = 1)
```

```
## Error in ggarrange(boxplot_retorno, boxplot_z_retorno_pf, ncol = 2, nrow = 1): could not find function "ggarrange"
```

```r
  annotate_figure(boxplots_retorno, top = text_grob("Boxplot/Vioplot do Retorno\ne Retorno Padronizado",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

```
## Error in annotate_figure(boxplots_retorno, top = text_grob("Boxplot/Vioplot do Retorno\ne Retorno Padronizado", : could not find function "annotate_figure"
```


#### 10. Histograma para dados originais (Preco de Fechamento e Retorno) e padronizados 

```r
  histograma_pf <- ggplot(data = preco_fechamento,aes(x = preco_fechamento)) +
                          geom_histogram(color="blue", fill = "white", bins = 30) +
                          labs(y = "Quantidade", x = "Preco") +
                          scale_x_continuous(breaks = seq(17, 22, by = 0.5)) +
                          scale_y_continuous(breaks = seq(0, 30, by = 5)) +
                          theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in ggplot(data = preco_fechamento, aes(x = preco_fechamento)): could not find function "ggplot"
```

```r
  histograma_z_pf <- ggplot(data = z_preco_fechamento,aes(x = z_preco_fechamento)) +
                            geom_histogram(color="red", fill = "white", bins = 30) +
                            labs(y = "Quantidade", x = "Preco Padronizado") +
                            scale_x_continuous(breaks = seq(-2, 3.5, by = 0.5)) +
                            scale_y_continuous(breaks = seq(0, 50, by = 5)) +
                            theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in ggplot(data = z_preco_fechamento, aes(x = z_preco_fechamento)): could not find function "ggplot"
```

```r
  histogramas_pf <- ggarrange(histograma_pf, histograma_z_pf,ncol = 1, nrow = 2)
```

```
## Error in ggarrange(histograma_pf, histograma_z_pf, ncol = 1, nrow = 2): could not find function "ggarrange"
```

```r
  annotate_figure(histogramas_pf, top = text_grob("Histograma do Preco de Fechamento",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

```
## Error in annotate_figure(histogramas_pf, top = text_grob("Histograma do Preco de Fechamento", : could not find function "annotate_figure"
```

```r
  histograma_retorno <- ggplot(data = retorno_pf,aes(x = 100*retorno_pf)) + 
                                geom_histogram(color="blue", fill = "white", bins = 25) + 
                                labs(y = "Quantidade", x = "Retorno (%)") + 
                                scale_x_continuous(breaks = seq(-6, 6, by = 1)) + 
                                scale_y_continuous(breaks = seq(0, 40, by = 5)) + 
                                theme(plot.title = element_text(hjust = 0.5))
```

```
## Error in ggplot(data = retorno_pf, aes(x = 100 * retorno_pf)): could not find function "ggplot"
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
## Error in ggplot(data = z_retorno_pf, aes(x = z_retorno_pf)): could not find function "ggplot"
```

```r
  histogramas_retorno <- ggarrange(histograma_retorno, histograma_z_retorno,ncol = 1, nrow = 2)
```

```
## Error in ggarrange(histograma_retorno, histograma_z_retorno, ncol = 1, : could not find function "ggarrange"
```

```r
  annotate_figure(histogramas_retorno, top = text_grob("Histograma do Retorno",
                  color = "Black", face = "bold", size = 14),
                  bottom = text_grob("Fonte: https://finance.yahoo.com/",
                  color = "black", hjust = 1.02, x = 1, size = 10))
```

```
## Error in annotate_figure(histogramas_retorno, top = text_grob("Histograma do Retorno", : could not find function "annotate_figure"
```

#### 11. QQPlot do retorno.  

```r
  qqplot_retorno <- ggplot(data = retorno_pf, aes(sample = 100*as.vector(retorno_pf))) +
                          stat_qq(size = 0.6) +labs(x = "Quantis Teoricos", y = "Quantis Amostrais",
                          title = "QQPlot do Retorno (%)") + theme(plot.title = element_text(hjust = 0.5)) +
                          scale_y_continuous(breaks = seq(-6, 4.5, by = 1.5))
```

```
## Error in ggplot(data = retorno_pf, aes(sample = 100 * as.vector(retorno_pf))): could not find function "ggplot"
```

#### 12. QQLine do retorno (fazer junto com o QQPlot).  

```r
  histograma_retorno_qqplot <- ggplot(data = retorno_pf,aes(x = 100*retorno_pf)) +
                                      geom_histogram(aes(y=..density..),color="blue", fill = "white", bins = 25) +
                                      stat_function(fun = dnorm, args = list(mean = mean(100*retorno_pf), sd = sd(100*retorno_pf)),
                                      col="red",lwd=1)+ theme(axis.text.x = element_blank(), axis.text.y = element_blank()) +
                                      labs(y = "", x = "") 
```

```
## Error in ggplot(data = retorno_pf, aes(x = 100 * retorno_pf)): could not find function "ggplot"
```

```r
  qqplot_linha_retorno <- ggplot(data = retorno_pf, aes(sample = 100*as.vector(retorno_pf))) +
                                stat_qq(size = 0.6) + labs(x = "Quantis Teoricos", y = "Quantis Amostrais", title = "QQPlot do Retorno (%)") +
                                theme(plot.title = element_text(hjust = 0.5)) +scale_y_continuous(breaks = seq(-6, 4.5, by = 1.5)) +
                                stat_qq_line(col = 2,lwd=1,lty=1) 
```

```
## Error in ggplot(data = retorno_pf, aes(sample = 100 * as.vector(retorno_pf))): could not find function "ggplot"
```

```r
  plot_principal <- qqplot_linha_retorno
```

```
## Error in eval(expr, envir, enclos): object 'qqplot_linha_retorno' not found
```

```r
  plot_para_inserir <- histograma_retorno_qqplot
```

```
## Error in eval(expr, envir, enclos): object 'histograma_retorno_qqplot' not found
```

```r
  plot.com.insercao <- ggdraw() + draw_plot(plot_principal) + draw_plot(plot_para_inserir, x = 0.07, y = 0.6, width = .3, height = .3)
```

```
## Error in ggdraw(): could not find function "ggdraw"
```

```r
  plot.com.insercao
```

```
## Error in eval(expr, envir, enclos): object 'plot.com.insercao' not found
```

#### 13. Assimetria amostral nao viesada do retorno.   

```r
  n <- length(retorno_pf)
```

```
## Error in eval(expr, envir, enclos): object 'retorno_pf' not found
```

```r
  somatorio <- c()
  for(i in 1:n){
    somatorio[i] <- ((retorno_pf[i] - mean(retorno_pf))/ sd(retorno_pf))^3
  }
```

```
## Error in eval(expr, envir, enclos): object 'n' not found
```

```r
  p1_s3 <- n/((n -1)*(n-2))
```

```
## Error in eval(expr, envir, enclos): object 'n' not found
```

```r
  p2_s3 <- sum(somatorio)
  s3 <- p1_s3*p2_s3
```

```
## Error in eval(expr, envir, enclos): object 'p1_s3' not found
```

```r
  s3
```

```
## Error in eval(expr, envir, enclos): object 's3' not found
```

#### 14. Curtose amostral nao viesada do retorno.   

```r
  n <- length(retorno_pf)
```

```
## Error in eval(expr, envir, enclos): object 'retorno_pf' not found
```

```r
  somatorio <- c()
  for(i in 1:n){
    somatorio[i] <- ((retorno_pf[i] - mean(retorno_pf))/ sd(retorno_pf))^4
  }
```

```
## Error in eval(expr, envir, enclos): object 'n' not found
```

```r
  p1_s4 <- (n*(n +1))/((n -1)*(n-2)*(n-3))
```

```
## Error in eval(expr, envir, enclos): object 'n' not found
```

```r
  p2_s4 <- (sum(somatorio))
  p3_s4 <- (3*((n-1)^2))/((n-2)*(n-3))
```

```
## Error in eval(expr, envir, enclos): object 'n' not found
```

```r
  s4 <- p1_s4 * p2_s4 - p3_s4
```

```
## Error in eval(expr, envir, enclos): object 'p1_s4' not found
```

```r
  s4
```

```
## Error in eval(expr, envir, enclos): object 's4' not found
```


```r
  library("knitr")
  knit("./q1/q1_nasdaq.rmd", output = "./q1/q1_nasdaq.md")
```

```
## Warning in file(con, "r"): cannot open file './q1/q1_nasdaq.rmd': No such file or directory
```

```
## Error in file(con, "r"): cannot open the connection
```
