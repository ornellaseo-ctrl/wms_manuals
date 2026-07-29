# Tabelas — CRM

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **4**.

## `C_CRM_D1`

- **Tipo:** Transactional
- **Categoria:** CRM
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CRM_NUM` | Crmessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CRM_TP_CODE` | Crm_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CRM_LINE_DATE` | Crm_Lineessorial Date | DATE | 7 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `CRM_LINE_DES` | Crm_Lineessorial Des | VARCHAR2 | 2000 |  | N |
| 7 | `CRM_ELAPSE_HOUR` | Crm_Elapseessorial Hour | NUMBER | 22 | 2 | Y |
| 8 | `CRM_ELAPSE_MIN` | Crm_Elapseessorial Min | NUMBER | 22 | 2 | Y |
| 9 | `CRM_ELAPSE_TOT_MIN` | Crm_Elapse_Totessorial Min | NUMBER | 22 | 6 | Y |
| 10 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `OP_CODE_CRM` | Op_Codeessorial Crm | VARCHAR2 | 20 |  | Y |

## `C_CRM_D2`

- **Tipo:** Transactional
- **Categoria:** CRM
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CRM_NUM` | Crmessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CRM_STAT_CODE` | Crm_Statessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CRM_STAT_DATE` | Crm_Statessorial Date | DATE | 7 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `CRM_INFO_DES` | Crm_Infoessorial Des | VARCHAR2 | 30 |  | Y |

## `C_CRM_H`

- **Tipo:** Transactional
- **Categoria:** CRM
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CRM_NUM` | Crmessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CRM_RQST_NAME` | Crm_Rqstessorial Name | VARCHAR2 | 30 |  | Y |
| 5 | `CRM_TEL_NUM` | Crm_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `CRM_TEL_NUM_EXT` | Crm_Tel_Numessorial Ext | VARCHAR2 | 4 |  | Y |
| 7 | `CRM_REF_NUM` | Crm_Refessorial Num | VARCHAR2 | 100 |  | Y |
| 8 | `CRM_DES` | Crmessorial Des | VARCHAR2 | 2000 |  | Y |
| 9 | `OP_CODE_PRM` | Op_Codeessorial Prm | VARCHAR2 | 20 |  | Y |
| 10 | `OP_CODE_ASS` | Op_Codeessorial Ass | VARCHAR2 | 20 |  | Y |
| 11 | `CRM_STAT_CODE` | Crm_Statessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `CRM_STAT_DATE` | Crm_Statessorial Date | DATE | 7 |  | N |
| 13 | `CRM_ACCSS_CHG_FLAG` | Crm_Accss_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CRM_CODE` | Crmessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CRM_SRCE_FLAG` | Crm_Srceessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CRM_SRCE_REF_FLAG` | Crm_Srce_Refessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `CRM_SRCE_REF_NUM` | Crm_Srce_Refessorial Num | NUMBER | 22 | 9 | Y |
| 18 | `CRM_EST_TOT_MIN` | Crm_Est_Totessorial Min | NUMBER | 22 | 6 | Y |
| 19 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 20 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 21 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 23 | `CRM_LAB_HOUR_RATE` | Crm_Lab_Houressorial Rate | NUMBER | 22 | 6 | Y |

## `M_CRM`

- **Tipo:** Master
- **Categoria:** CRM
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CRM_CODE` | Crmessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CRM_DES` | Crmessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CRM_STAT` | Crmessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

