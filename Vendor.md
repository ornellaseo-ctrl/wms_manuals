# Tabelas — Vendor

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **3**.

## `M_VEND_D`

- **Tipo:** Master
- **Categoria:** Vendor
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `VEND_CODE` | Vendessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |

## `M_VEND_H`

- **Tipo:** Master
- **Categoria:** Vendor
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `VEND_CODE` | Vendessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `VEND_NAME` | Vendessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `VEND_STAT` | Vendessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `VEND_ADD1` | Vendessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `VEND_ADD2` | Vendessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `VEND_ADD3` | Vendessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `VEND_ADD4` | Vendessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `VEND_TP_CODE` | Vend_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | N |
| 14 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 15 | `EXT_REF_NUM2` | Ext_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 16 | `EXT_REF_NUM3` | Ext_Refessorial Num3 | VARCHAR2 | 20 |  | Y |
| 17 | `VEND_LAST_ACT_DATE` | Vend_Last_Actessorial Date | DATE | 7 |  | Y |
| 18 | `UCC_PROF_CODE` | Ucc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 24 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_VEND_TP`

- **Tipo:** Master
- **Categoria:** Vendor
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `VEND_TP_CODE` | Vend_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `VEND_TP_DES` | Vend_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `VEND_TP_STAT` | Vend_Tpessorial Stat | VARCHAR2 | 1 |  | N |

