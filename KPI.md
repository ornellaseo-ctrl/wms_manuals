# Tabelas — KPI

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `C_KPI_DOC_D1`

- **Tipo:** Transactional
- **Categoria:** KPI
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `KPI_SEQ_NUM` | Kpi_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `KPI_DOC_EXPT_ARR_DATE` | Kpi_Doc_Expt_Arressorial Date | DATE | 7 |  | Y |
| 3 | `KPI_DOC_RAD_DATE` | Kpi_Doc_Radessorial Date | DATE | 7 |  | Y |
| 4 | `KPI_DOC_RAD_REAS_CODE` | Kpi_Doc_Rad_Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 5 | `KPI_DOC_RAD_COMPLNCE_LATE` | Kpi_Doc_Rad_Complnceessorial Late | NUMBER | 22 | 16 | Y |
| 6 | `KPI_DOC_DELV_DATE` | Kpi_Doc_Delvessorial Date | DATE | 7 |  | Y |
| 7 | `KPI_DOC_DELV_REAS_CODE` | Kpi_Doc_Delv_Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `KPI_DOC_DELV_COMPLNCE_LATE` | Kpi_Doc_Delv_Complnceessorial Late | NUMBER | 22 | 16 | Y |
| 9 | `KPI_DOC_TRANS_DATE` | Kpi_Doc_Transessorial Date | DATE | 7 |  | N |

## `C_KPI_DOC_H`

- **Tipo:** Transactional
- **Categoria:** KPI
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `KPI_SEQ_NUM` | Kpi_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `KPI_ENTRY_DATE` | Kpi_Entryessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `DOC_INB_OUTB_FLAG` | Doc_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `KPI_ACC_CODE` | Kpi_Accessorial Code | VARCHAR2 | 10 |  | N |
| 10 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 11 | `KPI_DOC_DATE` | Kpi_Docessorial Date | DATE | 7 |  | N |
| 12 | `KPI_DOC_CONF_DATE` | Kpi_Doc_Confessorial Date | DATE | 7 |  | N |
| 13 | `KPI_DOC_TOT_UNIT` | Kpi_Doc_Totessorial Unit | NUMBER | 22 | 16 | Y |
| 14 | `KPI_DOC_TOT_LADING_QTY` | Kpi_Doc_Tot_Ladingessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `KPI_DOC_TOT_WGT` | Kpi_Doc_Totessorial Wgt | NUMBER | 22 | 16 | Y |

