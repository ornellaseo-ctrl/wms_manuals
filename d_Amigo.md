# Tabelas — d'Amigo

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **5**.

## `DAMIGO_CHILD`

- **Tipo:** Misc
- **Categoria:** d'Amigo
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_CHILD_ID` | Drms_Childessorial Id | NUMBER | 22 | 6 | N |
| 3 | `DRMS_ROLE_ID` | Drms_Roleessorial Id | NUMBER | 22 | 6 | N |
| 4 | `DRMS_CHILD_SHORT` | Drms_Childessorial Short | VARCHAR2 | 20 |  | N |
| 5 | `DRMS_CHILD_DES` | Drms_Childessorial Des | VARCHAR2 | 40 |  | Y |
| 6 | `DRMS_SEL` | Drmsessorial Sel | VARCHAR2 | 2000 |  | Y |
| 7 | `DRMS_WHERE` | Drmsessorial Where | VARCHAR2 | 2000 |  | Y |
| 8 | `DRMS_ORD` | Drmsessorial Ord | VARCHAR2 | 2000 |  | Y |
| 9 | `DRMS_GRP_BY_FLAG` | Drms_Grp_Byessorial Flag | VARCHAR2 | 1 |  | Y |

## `DAMIGO_D1`

- **Tipo:** Misc
- **Categoria:** d'Amigo
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_SKEL` | Drmsessorial Skel | VARCHAR2 | 2000 |  | Y |
| 3 | `DRMS_PROP_STR` | Drms_Propessorial Str | LONG | 0 |  | Y |

## `DAMIGO_D2`

- **Tipo:** Misc
- **Categoria:** d'Amigo
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_SEQ_NUM` | Drms_Seqessorial Num | NUMBER | 22 | 1 | N |
| 3 | `DRMS_TABLE_NAME` | Drms_Tableessorial Name | VARCHAR2 | 30 |  | N |

## `DAMIGO_D3`

- **Tipo:** Misc
- **Categoria:** d'Amigo
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_FIELD_NAME` | Drms_Fieldessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `DRMS_PROP_CODE` | Drms_Propessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DRMS_PROP_VALUE` | Drms_Propessorial Value | VARCHAR2 | 100 |  | Y |
| 5 | `DRMS_PROP_USER_INP_FLAG` | Drms_Prop_User_Inpessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `LAST_UPD_OP_CODE` | Last_Upd_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `LAST_UPD_DATE` | Last_Updessorial Date | DATE | 7 |  | Y |

## `DAMIGO_H`

- **Tipo:** Misc
- **Categoria:** d'Amigo
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_PARENT_SHORT` | Drms_Parentessorial Short | VARCHAR2 | 20 |  | N |
| 3 | `DRMS_PARENT_DES` | Drms_Parentessorial Des | VARCHAR2 | 40 |  | Y |
| 4 | `DRMS_PARENT_ID_MENU` | Drms_Parent_Idessorial Menu | NUMBER | 22 | 6 | Y |

