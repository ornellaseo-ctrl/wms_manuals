# Tabelas — Bank

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **1**.

## `M_BANK`

- **Tipo:** Master
- **Categoria:** Bank
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BANK_CODE` | Bankessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `BANK_DES` | Bankessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `BANK_STAT` | Bankessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `BANK_ACC_NUM` | Bank_Accessorial Num | VARCHAR2 | 30 |  | N |
| 7 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 8 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

