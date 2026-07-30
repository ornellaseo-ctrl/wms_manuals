# Exemplos / Recortes de Campos Específicos

> Registros da terceira aba da planilha. Parece conter recortes de busca por campos específicos, como `RCPT_REF_NUM`.

| Tipo | Categoria | Tabela | # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---|---|---|---:|---|---|---|---:|---:|:---:|
| Transactional | Receipts | `C_CREATE_RCPT_H` | 11 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| Transactional | Receipts | `E_RCPT_H` | 16 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| Transactional | Receipts | `E_SAND_RCPT_H` | 14 | `SAND_RCPT_REF_NUM` | Sand_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| Historical | Receipts | `H_RCPT_H` | 17 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| Custom | Misc | `L_AP_HD_RCPT_DEL` | 4 | `HD_RCPT_REF_NUM` | Hd_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| Custom | Misc | `L_AP_HD_RCPT_H` | 4 | `HD_RCPT_REF_NUM` | Hd_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| Custom | Misc | `L_AP_RCPT_H` | 4 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| Misc | Misc | `TC_MVT_H` | 34 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| Misc | Receipts | `TE_RCPT_H` | 15 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
