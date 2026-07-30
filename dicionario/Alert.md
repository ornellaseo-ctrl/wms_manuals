# Tabelas — Alert

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **11**.

## `M_ALERT`

- **Tipo:** Master
- **Categoria:** Alert
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_DES` | Alertessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `ALERT_STAT` | Alertessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `ALERT_CLASS_CODE` | Alert_Classessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ALERT_OUTPUT_CODE` | Alert_Outputessorial Code | VARCHAR2 | 1 |  | N |
| 7 | `INIT_ALERT_FLAG` | Init_Alertessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LAST_RUN_DATE` | Last_Runessorial Date | DATE | 7 |  | Y |
| 9 | `MIN_REFRESH_TP` | Min_Refreshessorial Tp | VARCHAR2 | 1 |  | Y |
| 10 | `MIN_REFRESH_PER` | Min_Refreshessorial Per | NUMBER | 22 | 2 | Y |
| 11 | `RESTORE_SUPPRESS_REC_PER` | Restore_Suppress_Recessorial Per | NUMBER | 22 | 2 | N |
| 12 | `ALERT_REFRESH_AT_TIME` | Alert_Refresh_Atessorial Time | VARCHAR2 | 5 |  | Y |

## `M_ALERT_LINK`

- **Tipo:** Master
- **Categoria:** Alert
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `DEST_ALERT_CODE` | Dest_Alertessorial Code | VARCHAR2 | 10 |  | N |

## `M_ALERT_LINK_PARA`

- **Tipo:** Master
- **Categoria:** Alert
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COL_NAME` | Column Name | VARCHAR2 | 30 |  | N |
| 4 | `COL_TABLE_NAME` | Col_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `SRCE_ALERT_CODE` | Srce_Alertessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `SRCE_COL_NAME` | Srce_Colessorial Name | VARCHAR2 | 30 |  | N |

## `M_ALERT_PARA`

- **Tipo:** Master
- **Categoria:** Alert
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_PARA` | Alertessorial Para | VARCHAR2 | 20 |  | N |
| 4 | `ALERT_PARA_VAL` | Alert_Paraessorial Val | VARCHAR2 | 255 |  | N |

## `M_ALERT_PRT_PARA`

- **Tipo:** Master
- **Categoria:** Alert
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_PRT_PARA_SEQ_NUM` | Alert_Prt_Para_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `ALERT_PRT_PARA_CODE` | Alert_Prt_Paraessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `ALERT_PRT_PARA_VAL` | Alert_Prt_Paraessorial Val | VARCHAR2 | 80 |  | N |

## `S_ALERT`

- **Tipo:** System Setup Related
- **Categoria:** Alert
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_NUM` | Alertessorial Num | NUMBER | 22 | 3 | N |
| 2 | `ALERT_YES` | Alertessorial Yes | VARCHAR2 | 7 |  | N |
| 3 | `ALERT_NO` | Alertessorial No | VARCHAR2 | 7 |  | N |
| 4 | `ALERT_CANCEL` | Alertessorial Cancel | VARCHAR2 | 10 |  | Y |
| 5 | `ALERT_STAT` | Alertessorial Stat | VARCHAR2 | 34 |  | N |
| 6 | `ALERT_MESS` | Alertessorial Mess | VARCHAR2 | 56 |  | N |

## `S_ALERT_CLASS`

- **Tipo:** System Setup Related
- **Categoria:** Alert
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CLASS_CODE` | Alert_Classessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `ALERT_CLASS_NAME` | Alert_Classessorial Name | VARCHAR2 | 60 |  | N |
| 3 | `ALERT_MNT_CLASS_NAME` | Alert_Mnt_Classessorial Name | VARCHAR2 | 60 |  | N |

## `Z_C_ALERT_PROS`

- **Tipo:** Misc
- **Categoria:** Alert
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_ID_LIST` | Alert_Idessorial List | VARCHAR2 | 100 |  | N |
| 4 | `ALERT_ROW_STAT` | Alert_Rowessorial Stat | NUMBER | 22 | 4 | N |
| 5 | `ALERT_ROW_DATE` | Alert_Rowessorial Date | DATE | 7 |  | N |

## `Z_M_ALERT`

- **Tipo:** Misc
- **Categoria:** Alert
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_DES` | Alertessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `ALERT_STAT` | Alertessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `ALERT_CLASS_CODE` | Alert_Classessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ALERT_OUTPUT_CODE` | Alert_Outputessorial Code | VARCHAR2 | 1 |  | N |
| 7 | `INIT_ALERT_FLAG` | Init_Alertessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LAST_RUN_DATE` | Last_Runessorial Date | DATE | 7 |  | Y |
| 9 | `MIN_REFRESH_TP` | Min_Refreshessorial Tp | VARCHAR2 | 1 |  | Y |
| 10 | `MIN_REFRESH_PER` | Min_Refreshessorial Per | NUMBER | 22 | 2 | Y |
| 11 | `RESTORE_SUPPRESS_REC_PER` | Restore_Suppress_Recessorial Per | NUMBER | 22 | 2 | N |
| 12 | `ALERT_REFRESH_AT_TIME` | Alert_Refresh_Atessorial Time | VARCHAR2 | 5 |  | Y |

## `Z_M_ALERT_PARA`

- **Tipo:** Misc
- **Categoria:** Alert
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_PARA` | Alertessorial Para | VARCHAR2 | 20 |  | N |
| 4 | `ALERT_PARA_VAL` | Alert_Paraessorial Val | VARCHAR2 | 40 |  | N |

## `Z_M_ALERT_PRT_PARA`

- **Tipo:** Misc
- **Categoria:** Alert
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_PRT_PARA_SEQ_NUM` | Alert_Prt_Para_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `ALERT_PRT_PARA_CODE` | Alert_Prt_Paraessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `ALERT_PRT_PARA_VAL` | Alert_Prt_Paraessorial Val | VARCHAR2 | 80 |  | N |

