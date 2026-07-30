# Tabelas — Holiday

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `M_HOL`

- **Tipo:** Master
- **Categoria:** Holiday
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `HOL_CODE` | Holessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `HOL_DES` | Holessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `HOL_STAT` | Holessorial Stat | VARCHAR2 | 1 |  | N |

## `S_HOL`

- **Tipo:** System Setup Related
- **Categoria:** Holiday
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `HOL_CODE` | Holessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `HOL_DATE` | Holessorial Date | DATE | 7 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

