# Tabelas — Message

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **4**.

## `M_MES`

- **Tipo:** Master
- **Categoria:** Message
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MES_CODE` | Message Code | VARCHAR2 | 30 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `VERT_CODE` | Vertessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 5 | `MES_SEQ_NUM` | Mes_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 80 |  | N |

## `M_MES_D`

- **Tipo:** Master
- **Categoria:** Message
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 4 | `MES_LINE_NUM` | Mes_Lineessorial Num | NUMBER | 22 | 5 | N |
| 5 | `MES_LINE_ROOT_FLAG` | Mes_Line_Rootessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `MES_LINE_CONN_NUM` | Mes_Line_Connessorial Num | NUMBER | 22 | 5 | N |
| 7 | `MES_LINE_TEXT` | Mes_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_MES_H`

- **Tipo:** Master
- **Categoria:** Message
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 4 | `MES_DES` | Mesessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MES_STAT` | Mesessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 2000 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_MES`

- **Tipo:** System Setup Related
- **Categoria:** Message
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MES_CODE` | Message Code | VARCHAR2 | 30 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `VERT_CODE` | Vertessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 5 | `MES_SEQ_NUM` | Mes_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 80 |  | N |

