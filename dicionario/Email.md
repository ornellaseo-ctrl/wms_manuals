# Tabelas — Email

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **1**.

## `M_AUTO_EMAIL_CONFIG`

- **Tipo:** Master
- **Categoria:** Email
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `AUTO_EMAIL_DIR` | Auto_Emailessorial Dir | VARCHAR2 | 60 |  | Y |
| 5 | `AUTO_EMAIL_SUBJECT_LINE` | Auto_Email_Subjectessorial Line | VARCHAR2 | 200 |  | Y |
| 6 | `AUTO_EMAIL_VERBIAGE` | Auto_Emailessorial Verbiage | VARCHAR2 | 250 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

