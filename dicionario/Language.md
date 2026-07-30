# Tabelas — Language

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **1**.

## `M_LANG`

- **Tipo:** Master
- **Categoria:** Language
- **Campos:** 14

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `LANG_DES` | Langessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `LANG_STAT` | Langessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `MENU_SEL_CODE_FIRST` | Menu_Sel_Codeessorial First | VARCHAR2 | 10 |  | Y |
| 6 | `RF_MENU_SEL_CODE_FIRST` | Rf_Menu_Sel_Codeessorial First | VARCHAR2 | 10 |  | Y |
| 7 | `PARENT_LANG_CODE` | Parent_Langessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `ISO_LANG_CODE` | Iso_Langessorial Code | VARCHAR2 | 5 |  | Y |
| 9 | `NLS_LANG_CODE` | Nls_Langessorial Code | VARCHAR2 | 50 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

