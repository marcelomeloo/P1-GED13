>### Dados Bovespa

```r
  dados.bovespa <- quantmod::getSymbols("^BVSP", src = "yahoo", from = start, to = end, auto.assign = FALSE)
  dados.bovespa
```

```
##            BVSP.Open BVSP.High BVSP.Low BVSP.Close BVSP.Volume BVSP.Adjusted
## 2022-01-03    104823    106125   103413     103922    11128500        103922
## 2022-01-04    103922    104276   103096     103514    11491600        103514
## 2022-01-05    103514    103514   100850     101006           0        101006
## 2022-01-06    101006    102235   101000     101561    11749200        101561
## 2022-01-07    101561    102719   101104     102719    11733200        102719
## 2022-01-10    102719    102719   101038     101945    10264700        101945
## 2022-01-11    101946    103780   101918     103779    12421500        103779
## 2022-01-12    103779    105869   103771     105686    13026500        105686
## 2022-01-13    105686    106251   104974     105530    11712300        105530
## 2022-01-14    105530    107062   105028     106928    11457100        106928
## 2022-01-17    106927    106928   106097     106692     6924200        106692
## 2022-01-18    106369    107013   105786     106522    11221900        106522
## 2022-01-19    106670    108602   106669     108013    12595600        108013
## 2022-01-20    108015    109873   108015     109102    13630500        109102
## 2022-01-21    109097    109786   108368     108942    13408400        108942
## 2022-01-24    108941    108948   106624     107752    12700800        107752
## 2022-01-25    107935    110115   107185     109845    13713900        109845
## 2022-01-26    110207    112695   110204     111573    15513800        111573
## 2022-01-27    111303    113057   111303     112315    14812000        112315
## 2022-01-28    112611    112969   111407     111478    13520100        111478
## 2022-01-31    111910    112495   111195     112388    12190800        112388
## 2022-02-01    112143    113302   112135     113147    11133300        113147
## 2022-02-02    113228    113666   111645     112161    11751200        112161
## 2022-02-03    111897    112502   111225     111696    11039700        111696
## 2022-02-04    111696    112415   110321     112245           0        112245
## 2022-02-07    112247    112517   111490     111996    10672800        111996
## 2022-02-08    111995    112251   110943     112234    10157500        112234
## 2022-02-09    112233    113163   111710     112461    13794500        112461
## 2022-02-10    112462    113812   112163     113359    13267900        113359
## 2022-02-11    113368    114899   113128     113572    18602800        113572
## 2022-02-14    113643    114167   113358     113807    10757600        113807
## 2022-02-15    113905    114819   113882     114660    11649600        114660
## 2022-02-16    114830    115734   114816     115181    12052100        115181
## 2022-02-17    115181    115214   113389     113528    10807500        113528
## 2022-02-18    113534    114213   112701     112768    11300700        112768
## 2022-02-21    112880    113405   111608     111725     7864900        111725
## 2022-02-22    111727    113315   111727     112892    12707000        112892
## 2022-02-23    112892    113721   111748     112008    12120600        112008
## 2022-02-24    112001    112001   109125     111592    16794700        111592
## 2022-02-25    111591    113142   110673     113142    17555700        113142
## 2022-03-02    113143    115429   113143     115174           0        115174
## 2022-03-03    115173    115948   115010     115166    12123000        115166
## 2022-03-04    115166    115166   113389     114474    10715700        114474
## 2022-03-07    114469    114529   111140     111593    14057700        111593
## 2022-03-08    111594    112390   110969     111203    15698500        111203
## 2022-03-09    111210    114051   111207     113900    14705400        113900
## 2022-03-10    113900    113939   111889     113663    12984000        113663
## 2022-03-11    113664    114627   111332     111713    12475800        111713
## 2022-03-14    111716    112299   109717     109928    10480900        109928
## 2022-03-15    109925    109925   107781     108959    13653800        108959
## 2022-03-16    108958    111183   108958     111112    13205200        111112
## 2022-03-17    111113    113088   111070     113076    14407500        113076
## 2022-03-18    113076    115311   112475     115311    19552500        115311
## 2022-03-21    115307    116360   115208     116155    10378700        116155
## 2022-03-22    116157    117541   116157     117272    11382700        117272
## 2022-03-23    117270    118270   117036     117457    11083700        117457
## 2022-03-24    117460    119256   117151     119053    13474400        119053
## 2022-03-25    119062    119729   118548     119081    13814500        119081
## 2022-03-28    119082    119444   118061     118738     9167700        118738
## 2022-03-29    118740    120900   118740     120014    12931900        120014
## 2022-03-30    120013    120531   119775     120260    10893300        120260
## 2022-03-31    120261    120880   119999     119999    11202100        119999
## 2022-04-01    120001    121579   120001     121570    13780900        121570
## 2022-04-04    121569    121570   120754     121280     8812500        121280
## 2022-04-05    121279    121628   118794     118885    11788300        118885
## 2022-04-06    118885    118885   116791     118228    13410800        118228
## 2022-04-07    118226    119247   117509     118862    11520100        118862
## 2022-04-08    118861    118868   117487     118322    11225800        118322
## 2022-04-11    118320    118320   116953     116953     9558400        116953
## 2022-04-12    116963    118615   116054     116147    11406800        116147
## 2022-04-13    116150    117329   116150     116782    12070500        116782
## 2022-04-14    116781    116781   115624     116182    10365400        116182
## 2022-04-18    116182    116191   115177     115687     8404900        115687
## 2022-04-19    115687    115687   114277     115057           0        115057
## 2022-04-20    115057    115057   113945     114344    10747700        114344
## 2022-04-22    114343    114343   110591     111078    10877300        111078
## 2022-04-25    111077    111155   109222     110685    11098300        110685
## 2022-04-26    110684    110685   107978     108213    11747500        108213
## 2022-04-27    108214    110107   108214     109349    11515700        109349
## 2022-04-28    109349    110702   108905     109919    11129900        109919
## 2022-04-29    109922    111819   107876     107876    13662200        107876
## 2022-05-02    107876    107884   105218     106639    11935100        106639
## 2022-05-03    106640    107127   106033     106528     9935500        106528
## 2022-05-04    106529    108382   104933     108344    14558600        108344
## 2022-05-05    108337    108337   103923     105304    13826200        105304
## 2022-05-06    105303    106268   103984     105135    14137700        105135
## 2022-05-09    105109    105109   102768     103250    13196700        103250
## 2022-05-10    103251    104286   102386     103110    13507400        103110
## 2022-05-11    103110    105374   103008     104397    13425100        104397
## 2022-05-12    104395    105708   103579     105688    13995600        105688
## 2022-05-13    105691    107773   105691     106924    12369300        106924
## 2022-05-16    108685    108685   108199     108233    10596900        108233
## 2022-05-17    108246    109774   108245     108789    16503400        108789
## 2022-05-18    107903    108096   106038     106247    14752800        106247
## 2022-05-19    106249    107420   105760     107005    11426400        107005
## 2022-05-20    108520    108795   107351     108488    12866400        108488
## 2022-05-23    108500    110680   108500     110346    10682700        110346
## 2022-05-24    110340    110635   108399     110581    11724400        110581
## 2022-05-25    110085    111006   109699     110580    10737700        110580
## 2022-05-26    110577    112102   110388     111890    13077400        111890
## 2022-05-27    111890    112441   111558     111942     9979300        111942
## 2022-05-30    111944    112690   110655     111032     7284500        111032
## 2022-05-31    111036    111903   110685     111351    15809400        111351
## 2022-06-01    111351    111931   110822     111360     9790200        111360
## 2022-06-02    111363    112709   111218     112393    10051100        112393
## 2022-06-03    112392    112392   110935     111102     8757500        111102
## 2022-06-06    111102    111935   110015     110186     8212400        110186
## 2022-06-07    110185    110435   109394     110070     9466200        110070
## 2022-06-08    110067    110142   108045     108368    10379900        108368
## 2022-06-09    108367    108510   107068     107094    11955500        107094
## 2022-06-10    107091    107092   104648     105481    12840500        105481
## 2022-06-13    105476    105478   101700     102598    13837900        102598
## 2022-06-14    102598    103328   101325     102063    11563200        102063
## 2022-06-15    102068    103952   102046     102807    16023500        102807
## 2022-06-17    102800    102801    98402      99825    18927300         99825
## 2022-06-20     99824    100481    98409      99853    10900800         99853
## 2022-06-21     99854    101069    99167      99685    11072300         99685
## 2022-06-22     99678    100374    98050      99522    11675100         99522
## 2022-06-23     99523    100232    97775      98080    12397700         98080
## 2022-06-24     98081     99313    98031      98672    10345200         98672
## 2022-06-27     98673    101106    98672     100764     9895900        100764
## 2022-06-28    100766    102237    99956     100591    10493900        100591
## 2022-06-29    100592    101313    99218      99622    10448100         99622
## 2022-06-30     99619     99619    97758      98542    14588800         98542
## 2022-07-01     98542     99340    97231      98954    11609800         98954
## 2022-07-04     98952     99353    98264      98609     6279300         98609
## 2022-07-05     98608     98608    96499      98295    13358800         98295
## 2022-07-06     98294     99141    97423      98719    13348200         98719
## 2022-07-07     98722    101420    98722     100730    12696300        100730
## 2022-07-08    100732    101577    99958     100289     9730400        100289
## 2022-07-11    100282    100282    97854      98212     8893400         98212
## 2022-07-12     98212     98737    97253      98271    12566300         98271
## 2022-07-13     98258     98928    97403      97881    12208100         97881
## 2022-07-14     97879     97879    95431      96121    12579000         96121
## 2022-07-15     96119     96971    95267      96551    11347600         96551
## 2022-07-18     96553     98291    96553      96916    10738200         96916
## 2022-07-19     96920     98346    96917      98245    10295900         98245
## 2022-07-20     98244     98366    97277      98287    12941700         98287
## 2022-07-21     98286     99057    97088      99033    10060000         99033
## 2022-07-22     99034     99724    98321      98925    10033500         98925
## 2022-07-25     98926    100508    98925     100270     8621800        100270
## 2022-07-26    100270    100753    99365      99772     9136600         99772
## 2022-07-27     99773    101471    99772     101438    10263100        101438
## 2022-07-28    101437    102686   101045     102597    11130000        102597
## 2022-07-29    102597    103989   102514     103165    12934200        103165
## 2022-08-01    103165    103317   101764     102225    11626700        102225
## 2022-08-02    102225    103660   101694     103362    10124500        103362
## 2022-08-03    103362    103878   102822     103775    12379600        103775
## 2022-08-04    103777    106162   103777     105892    15499000        105892
## 2022-08-05    105893    107176   105518     106472    12947500        106472
## 2022-08-08    106473    108489   106473     108402    12674600        108402
## 2022-08-09    108403    109331   107842     108651    12147900        108651
## 2022-08-10    108658    110362   108657     110236    13376200        110236
## 2022-08-11    110236    111310   109604     109718    14944800        109718
## 2022-08-12    109718    112764   109718     112764    18704900        112764
## 2022-08-15    112767    113214   111067     113032    15552900        113032
## 2022-08-16    113034    113626   112690     113512    12986400        113512
## 2022-08-17    113508    114146   112483     113708    14652800        113708
## 2022-08-18    113708    114375   113304     113813    10644200        113813
## 2022-08-19    113807    113807   111146     111496    12678600        111496
## 2022-08-22    111487    111487   109858     110501    11010900        110501
## 2022-08-23    110504    112965   110503     112857    11892000        112857
## 2022-08-24    112856    113888   112632     112898    13758600        112898
## 2022-08-25    112898    114156   112768     113532    11838500        113532
## 2022-08-26    113533    114091   111978     112299    11159700        112299
## 2022-08-29    112296    113222   111689     112323     9795800        112323
## 2022-08-30    112323    112869   110103     110431    11937900        110431
## 2022-08-31    110431    111364   109523     109523    14791100        109523
```

```r
  bovespa <- na.omit(dados.bovespa)
```

#### Cria o vetor de preco de fechamento

```r
  preco_fechamento <- dados.dj$"BVSP.Close"
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
        labs(title="Grafico do Bovespa", subtitle="Preco de Fechamento", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Preco (R$)") +
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
        labs(title="Grafico do Bovespa", subtitle="Retorno", caption="Fonte: https://finance.yahoo.com/", x = "Data ", y="Retorno (%)") +
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
  knit("./q1/q1_bovespa.rmd", output = "./q1/q1_bovespa.md")
```

```
## Warning in file(con, "r"): cannot open file './q1/q1_bovespa.rmd': No such file or directory
```

```
## Error in file(con, "r"): cannot open the connection
```
