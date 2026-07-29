# Tabelas — Fax

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **5**.

## `M_FAX_COVER`

- **Tipo:** Master
- **Categoria:** Fax
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FAX_COVER_DES` | Fax_Coveressorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FAX_COVER_STAT` | Fax_Coveressorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FAX_MES`

- **Tipo:** Master
- **Categoria:** Fax
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FAX_CODE` | Faxessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `FAX_TP` | Faxessorial Tp | VARCHAR2 | 4 |  | N |
| 4 | `FAX_MES_LINE_NUM` | Fax_Mes_Lineessorial Num | NUMBER | 22 | 5 | N |
| 5 | `FAX_MES_LINE_ROOT_FLAG` | Fax_Mes_Line_Rootessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `FAX_MES_LINE_CONN_NUM` | Fax_Mes_Line_Connessorial Num | NUMBER | 22 | 5 | N |
| 7 | `FAX_MES_LINE_TEXT` | Fax_Mes_Lineessorial Text | VARCHAR2 | 65 |  | Y |

## `M_FAX_OVRL`

- **Tipo:** Master
- **Categoria:** Fax
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FAX_OVRL_CODE` | Fax_Ovrlessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FAX_OVRL_DES` | Fax_Ovrlessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FAX_OVRL_STAT` | Fax_Ovrlessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `FAX_OVRL_ARCH_ID` | Fax_Ovrl_Archessorial Id | VARCHAR2 | 60 |  | Y |
| 7 | `FAX_OVRL_SIDE_FLAG` | Fax_Ovrl_Sideessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_FAX_LOG`

- **Tipo:** System Setup Related
- **Categoria:** Fax
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FAX_ID` | Faxessorial Id | NUMBER | 22 | 6 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | N |
| 4 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | N |
| 6 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | N |
| 7 | `FAX_COMMENT` | Faxessorial Comment | VARCHAR2 | 60 |  | Y |
| 8 | `FAX_FILE_NAME` | Fax_Fileessorial Name | VARCHAR2 | 60 |  | N |
| 9 | `FAX_STAT` | Faxessorial Stat | VARCHAR2 | 20 |  | Y |
| 10 | `FAX_CNT` | Faxessorial Cnt | NUMBER | 22 | 2 | Y |
| 11 | `FAX_DATE` | Faxessorial Date | DATE | 7 |  | Y |
| 12 | `FAX_TIME` | Faxessorial Time | NUMBER | 22 | 4 | Y |
| 13 | `FAX_PAGE_CNT` | Fax_Pageessorial Cnt | VARCHAR2 | 10 |  | Y |

## `S_FILTER_COL`

- **Tipo:** System Setup Related
- **Categoria:** Fax
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `FILTER_COL_NAME` | Filter_Colessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `FILTER_COL_DES` | Filter_Colessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FILTER_COL_TP` | Filter_Colessorial Tp | VARCHAR2 | 1 |  | Y |
| 5 | `FILTER_COL_TABLE_NAME` | Filter_Col_Tableessorial Name | VARCHAR2 | 30 |  | Y |

