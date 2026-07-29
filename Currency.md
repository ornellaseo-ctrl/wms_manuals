# Tabelas — Currency

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `M_CUR`

- **Tipo:** Master
- **Categoria:** Currency
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 4 | `CUR_DES` | Curessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUR_STAT` | Curessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUR_VALUE_BASE_CUR` | Cur_Value_Baseessorial Cur | NUMBER | 22 | 15 | N |
| 7 | `GL_ACC_CODE_RLIZE_EXCHNG` | Gl_Acc_Code_Rlizeessorial Exchng | VARCHAR2 | 12 |  | Y |
| 8 | `GL_ACC_CODE_AR_TRD` | Gl_Acc_Code_Aressorial Trd | VARCHAR2 | 12 |  | Y |
| 9 | `GL_ACC_CODE_AR_DISC` | Gl_Acc_Code_Aressorial Disc | VARCHAR2 | 12 |  | Y |
| 10 | `GL_ACC_CODE_AR_INT` | Gl_Acc_Code_Aressorial Int | VARCHAR2 | 12 |  | Y |
| 11 | `GL_ACC_CODE_AP_TRD` | Gl_Acc_Code_Apessorial Trd | VARCHAR2 | 12 |  | Y |
| 12 | `GL_ACC_CODE_AP_DISC` | Gl_Acc_Code_Apessorial Disc | VARCHAR2 | 12 |  | Y |
| 13 | `GL_ACC_CODE_AP_INT` | Gl_Acc_Code_Apessorial Int | VARCHAR2 | 12 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUR_EXCHNG_DATE`

- **Tipo:** Master
- **Categoria:** Currency
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 4 | `CUR_EXCHNG_DATE` | Cur_Exchngessorial Date | DATE | 7 |  | N |
| 5 | `CUR_VALUE_BASE_CUR` | Cur_Value_Baseessorial Cur | NUMBER | 22 | 15 | N |
| 6 | `CUR_EXCHNG_EFF_DATE` | Cur_Exchng_Effessorial Date | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 13 | `CUR_EXCHNG_AUTO_RATE_FLAG` | Cur_Exchng_Auto_Rateessorial Flag | VARCHAR2 | 1 |  | Y |

