# Tabelas — ISOL

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `M_ISOL_D`

- **Tipo:** Master
- **Categoria:** ISOL
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 4 | `ISOL_OVFL_NUM` | Isol_Ovflessorial Num | NUMBER | 22 | 2 | N |
| 5 | `ISOL_CODE_OVFL` | Isol_Codeessorial Ovfl | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ISOL_H`

- **Tipo:** Master
- **Categoria:** ISOL
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 4 | `ISOL_DES` | Isolessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ISOL_STAT` | Isolessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

