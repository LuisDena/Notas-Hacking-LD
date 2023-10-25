# waves over lambda
## Objetivo
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 13758`.
## Pistas
P1: Flag is not in the usual flag format

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: frequency_is_c_over_lambda_dnvtfrtayu
-------------------------------------------------------------------------
parece que es vigenere pero es sustitucion 

┌──(kali㉿kali)-[~/Downloads]
└─$ nc jupiter.challenges.picoctf.org 13758
-------------------------------------------------------------------------------
icldenpb oqeq wb rcje yxnd - yeqgjqlir_wb_i_caqe_xntzhn_hlapyepnrj
-------------------------------------------------------------------------------
kq kqeq lcp tjio tceq ponl n gjnepqe cy nl ocje cjp cy cje bows pwxx kq bnk oqe bwlf, nlh poql w jlhqebpcch yce poq ywebp pwtq konp knb tqnlp zr n bows ycjlhqewld wl poq bqn.  w tjbp niflckxqhdq w onh onehxr qrqb pc xccf js koql poq bqntql pcxh tq boq knb bwlfwld; yce yect poq tctqlp ponp poqr enpoqe sjp tq wlpc poq zcnp ponl ponp w twdop zq bnwh pc dc wl, tr oqnep knb, nb wp kqeq, hqnh kwpowl tq, snepxr kwpo yewdop, snepxr kwpo oceece cy twlh, nlh poq pocjdopb cy konp knb rqp zqyceq tq.
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ 
usando la pagina nos da lo siguiente
-------------------------------------------------------------------------------
congrats here is your flag - frequency_is_c_over_lambda_dnvtfrtayu
-------------------------------------------------------------------------------
we were not much more than a quarter of an hour out of our ship till we saw her sink, and then i understood for the first time what was meant by a ship foundering in the sea.  i must acknowledge i had hardly eyes to look up when the seamen told me she was sinking; for from the moment that they rather put me into the boat than that i might be said to go in, my heart was, as it were, dead within me, partly with fright, partly with horror of mind, and the thoughts of what was yet before me.
                                                                           

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://es.wikipedia.org/wiki/Cifrado_por_sustituci%C3%B3n
https://en.wikipedia.org/wiki/Substitution_cipher
https://www.guballa.de/substitution-solver