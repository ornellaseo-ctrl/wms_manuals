# Tabelas — Billing

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **122**.

## `C_AR_INV_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | N |
| 6 | `TRANS_CNT` | Transessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 8 | `TRANS_TP` | Transessorial Tp | VARCHAR2 | 2 |  | N |
| 9 | `TRANS_AMT` | Transessorial Amt | NUMBER | 22 | 9 | N |
| 10 | `TRANS_REF_NUM` | Trans_Refessorial Num | NUMBER | 22 | 6 | N |
| 11 | `TRANS_CONF_FLAG` | Trans_Confessorial Flag | VARCHAR2 | 1 |  | N |

## `C_AR_INV_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | N |
| 6 | `INV_DATE` | Invessorial Date | DATE | 7 |  | N |
| 7 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 8 | `INV_AMT_ORG` | Inv_Amtessorial Org | NUMBER | 22 | 15 | N |
| 9 | `PMT_AMT` | Pmtessorial Amt | NUMBER | 22 | 9 | Y |
| 10 | `DISC_AMT` | Discessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `WRTOFF_AMT` | Warehouse Amt | NUMBER | 22 | 9 | Y |
| 12 | `CRT_AMT` | Crtessorial Amt | NUMBER | 22 | 9 | Y |
| 13 | `DBT_AMT` | Dbtessorial Amt | NUMBER | 22 | 9 | Y |
| 14 | `DISPT_AMT` | Disptessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `TERM_CODE` | Termessorial Code | VARCHAR2 | 4 |  | N |
| 16 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 17 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 18 | `BAT_STAT` | Batessorial Stat | VARCHAR2 | 1 |  | Y |

## `C_BAT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 38
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 5 | `BAT_DES` | Batessorial Des | VARCHAR2 | 30 |  | Y |
| 6 | `BAT_STAT` | Batessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `BAT_DATE` | Batessorial Date | DATE | 7 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 10 | `BAT_NUM_ENTRY` | Bat_Numessorial Entry | NUMBER | 22 | 9 | N |
| 11 | `BAT_LAST_AUDIT_NUM` | Bat_Last_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 12 | `BAT_CONT_TOT` | Bat_Contessorial Tot | NUMBER | 22 | 11 | Y |
| 13 | `BAT_ENTRY_TOT` | Bat_Entryessorial Tot | NUMBER | 22 | 11 | Y |
| 14 | `BAT_ACCEPT_STAT` | Bat_Acceptessorial Stat | NUMBER | 22 | 2 | Y |
| 15 | `BAT_ACCEPT_CODE` | Bat_Acceptessorial Code | VARCHAR2 | 31 |  | Y |
| 16 | `BAT_AUDIT_SPOOL` | Bat_Auditessorial Spool | VARCHAR2 | 60 |  | Y |
| 17 | `BAT_FINAL_SPOOL` | Bat_Finalessorial Spool | VARCHAR2 | 60 |  | Y |
| 18 | `BAT_REST1` | Batessorial Rest1 | VARCHAR2 | 255 |  | Y |
| 19 | `BAT_REST2` | Batessorial Rest2 | VARCHAR2 | 255 |  | Y |
| 20 | `BAT_REST3` | Batessorial Rest3 | VARCHAR2 | 255 |  | Y |
| 21 | `BAT_REST4` | Batessorial Rest4 | VARCHAR2 | 255 |  | Y |
| 22 | `BAT_REST5` | Batessorial Rest5 | VARCHAR2 | 255 |  | Y |
| 23 | `BAT_REST6` | Batessorial Rest6 | VARCHAR2 | 255 |  | Y |
| 24 | `BAT_REST7` | Batessorial Rest7 | VARCHAR2 | 255 |  | Y |
| 25 | `BAT_REST8` | Batessorial Rest8 | VARCHAR2 | 255 |  | Y |
| 26 | `BAT_REST9` | Batessorial Rest9 | VARCHAR2 | 255 |  | Y |
| 27 | `BAT_TRANS_DATE` | Bat_Transessorial Date | DATE | 7 |  | N |
| 28 | `CASH_POST_BANK_CODE` | Cash_Post_Bankessorial Code | VARCHAR2 | 12 |  | Y |
| 29 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 30 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | Y |
| 31 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 32 | `BAT_REM_TEXT` | Bat_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 33 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 34 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 35 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 36 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 37 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 38 | `BAT_REST10` | Batessorial Rest10 | VARCHAR2 | 255 |  | Y |

## `C_BAT_AUDIT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 5 | `BAT_NUM_PRT_SEQ` | Bat_Num_Prtessorial Seq | NUMBER | 22 | 4 | N |
| 6 | `BAT_AUDIT_DES` | Bat_Auditessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `FILE_NAME` | Fileessorial Name | VARCHAR2 | 255 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 10 | `PRT_DATE` | Prtessorial Date | DATE | 7 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_BAT_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 3 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 4 | `BAT_DES` | Batessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `BAT_STAT` | Batessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `BAT_DATE` | Batessorial Date | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 9 | `BAT_NUM_ENTRY` | Bat_Numessorial Entry | NUMBER | 22 | 9 | N |
| 10 | `BAT_LAST_AUDIT_NUM` | Bat_Last_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 11 | `BAT_CONT_TOT` | Bat_Contessorial Tot | NUMBER | 22 | 11 | Y |
| 12 | `BAT_ENTRY_TOT` | Bat_Entryessorial Tot | NUMBER | 22 | 11 | Y |
| 13 | `BAT_ACCEPT_STAT` | Bat_Acceptessorial Stat | NUMBER | 22 | 2 | Y |
| 14 | `BAT_ACCEPT_CODE` | Bat_Acceptessorial Code | VARCHAR2 | 11 |  | Y |
| 15 | `BANK_CODE` | Bankessorial Code | VARCHAR2 | 4 |  | Y |

## `C_BAT_SRCE_REF`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 5 | `ACCSS_SRCE_REF_FLAG` | Accss_Srce_Refessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ACCSS_SRCE_REF_NUM` | Accss_Srce_Refessorial Num | NUMBER | 22 | 9 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_BILL_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `BILL_LEV1` | Billing Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `BILL_LEV2` | Billing Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `BILL_LEV3` | Billing Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `BILL_LEV4` | Billing Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `BILL_LEV5` | Billing Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 10 | `QTY` | Qtyessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `CNVC_QTY` | Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 12 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 16 | N |
| 13 | `WGT_NET` | Wgtessorial Net | NUMBER | 22 | 16 | N |
| 14 | `CUBE` | Cubeessorial Cube | NUMBER | 22 | 16 | N |
| 15 | `RATE` | Rateessorial Rate | NUMBER | 22 | 9 | Y |
| 16 | `QUAL_QTY` | Qualessorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `QUAL_CNVC_QTY` | Qual_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 18 | `QUAL_WGT` | Qualessorial Wgt | NUMBER | 22 | 16 | Y |
| 19 | `QUAL_WGT_NET` | Qual_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 20 | `QUAL_CUBE` | Qualessorial Cube | NUMBER | 22 | 16 | Y |
| 21 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | N |
| 22 | `BAT_NUM_RENW` | Bat_Numessorial Renw | NUMBER | 22 | 9 | Y |
| 23 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_BILL_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `BILL_LEV1` | Billing Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `BILL_LEV2` | Billing Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `BILL_LEV3` | Billing Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `BILL_LEV4` | Billing Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `BILL_LEV5` | Billing Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `QTY` | Qtyessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 16 | N |
| 11 | `WGT_NET` | Wgtessorial Net | NUMBER | 22 | 16 | N |
| 12 | `SHIP_DATE` | Shipessorial Date | DATE | 7 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_BILL_ERR`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 5 | `BILL_ERR_CODE` | Bill_Erressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `BILL_ERR_TEXT` | Bill_Erressorial Text | VARCHAR2 | 2000 |  | Y |
| 7 | `BILL_ERR_DATE` | Bill_Erressorial Date | DATE | 7 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_BILL_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `BILL_LEV1` | Billing Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `BILL_LEV2` | Billing Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `BILL_LEV3` | Billing Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `BILL_LEV4` | Billing Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `BILL_LEV5` | Billing Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `PER_NUM` | Peressorial Num | NUMBER | 22 | 4 | N |
| 10 | `DATE_NXT` | Dateessorial Nxt | DATE | 7 |  | N |
| 11 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | DATE | 7 |  | N |
| 12 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | N |
| 13 | `CLS_FLAG` | Clsessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `BILL_PROF_CODE` | Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 15 | `RENW_PROS_FLAG` | Renw_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CLS_DATE` | Clsessorial Date | DATE | 7 |  | Y |
| 17 | `DATE_LAST` | Dateessorial Last | DATE | 7 |  | Y |
| 18 | `DISC_PROF_CODE` | Disc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CRS_DOCK_PROF_CODE` | Crs_Dock_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | N |
| 21 | `BAT_NUM_RENW` | Bat_Numessorial Renw | NUMBER | 22 | 9 | Y |
| 22 | `NUM_OF_FREE_DAYS` | Num_Of_Freeessorial Days | NUMBER | 22 | 4 | Y |
| 23 | `CUST_TRF_PROS_FREE_DAYS_FLAG` | Cust_Trf_Pros_Free_Daysessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `RENW_INV_DATE_NXT` | Renw_Inv_Dateessorial Nxt | DATE | 7 |  | Y |
| 25 | `RENW_INV_DATE_LAST` | Renw_Inv_Dateessorial Last | DATE | 7 |  | Y |
| 26 | `CHANGE_RENW_INV_DATE_NXT` | Change_Renw_Inv_Dateessorial Nxt | VARCHAR2 | 1 |  | Y |
| 27 | `CUST_CODE_INVT` | Cust_Codeessorial Invt | VARCHAR2 | 10 |  | Y |
| 28 | `CHG_CODE_RENW` | Chg_Codeessorial Renw | VARCHAR2 | 6 |  | Y |
| 29 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 30 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 31 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 32 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 33 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 34 | `BAT_NUM_PRE_RENW` | Bat_Num_Preessorial Renw | NUMBER | 22 | 9 | Y |

## `C_DOC_EXTRA_CHG`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 5 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | Y |
| 8 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 11 | `DOC_CONF_DATE` | Doc_Confessorial Date | DATE | 7 |  | Y |

## `C_DOC_MAN`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `DOC_MAN_CODE_TP_FLAG` | Doc_Man_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `DOC_MAN_NAME` | Doc_Manessorial Name | VARCHAR2 | 30 |  | N |
| 6 | `DOC_MAN_ADD1` | Doc_Manessorial Add1 | VARCHAR2 | 30 |  | Y |
| 7 | `DOC_MAN_ADD2` | Doc_Manessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `DOC_MAN_ADD3` | Doc_Manessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE_DOC_MAN` | Zarehouse Code Doc Man | VARCHAR2 | 10 |  | Y |
| 10 | `ZIP_CITY_DOC_MAN` | Zarehouse City Doc Man | VARCHAR2 | 30 |  | Y |
| 11 | `STATE_CODE_DOC_MAN` | State_Code_Docessorial Man | VARCHAR2 | 4 |  | Y |
| 12 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 13 | `DOC_MAN_ADD4` | Doc_Manessorial Add4 | VARCHAR2 | 30 |  | Y |
| 14 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 15 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 16 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |

## `C_GEN_CHG_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `GEN_EXTRA_CHG_INB_OUTB_FLAG` | Gen_Extra_Chg_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `GEN_EXTRA_CHG_SEQ_NUM` | Gen_Extra_Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `GEN_EXTRA_CHG_CUST_CODE_REST` | Gen_Extra_Chg_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 10 | `GEN_EXTRA_CHG_CON_CODE_REST` | Gen_Extra_Chg_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 11 | `GEN_EXTRA_CHG_SHIP_CODE_REST` | Gen_Extra_Chg_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 12 | `GEN_EXTRA_CHG_CARR_CODE_REST` | Gen_Extra_Chg_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 13 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 6 |  | Y |
| 14 | `CHG_COMPL_FLAG` | Chg_Complessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_GEN_CHG_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `GEN_CHG_STEP_NUM` | Gen_Chg_Stepessorial Num | NUMBER | 22 | 3 | Y |
| 4 | `GEN_CHG_STEP_COMPL_FLAG` | Gen_Chg_Step_Complessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_GEN_CHG_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `GEN_CHG_DATE` | Gen_Chgessorial Date | DATE | 7 |  | N |
| 4 | `GEN_CHG_BAT_STEP_NUM` | Gen_Chg_Bat_Stepessorial Num | NUMBER | 22 | 3 | N |

## `C_GEN_EXTRA_CHG`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `GEN_EXTRA_CHG_INB_OUTB_FLAG` | Gen_Extra_Chg_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `GEN_EXTRA_CHG_SEQ_NUM` | Gen_Extra_Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `GEN_EXTRA_CHG_CUST_CODE_REST` | Gen_Extra_Chg_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 8 | `GEN_EXTRA_CHG_CON_CODE_REST` | Gen_Extra_Chg_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 9 | `GEN_EXTRA_CHG_SHIP_CODE_REST` | Gen_Extra_Chg_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 10 | `GEN_EXTRA_CHG_CARR_CODE_REST` | Gen_Extra_Chg_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 11 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |

## `C_INVT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 49
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 10 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 11 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 12 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 13 | `INVT_CLS_FLAG` | Invt_Clsessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `UNALLOC_WGT` | Unallocessorial Wgt | NUMBER | 22 | 16 | N |
| 16 | `UNALLOC_CUBE` | Unallocessorial Cube | NUMBER | 22 | 16 | N |
| 17 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 18 | `INTRANS_WGT` | Intransessorial Wgt | NUMBER | 22 | 16 | N |
| 19 | `INTRANS_CUBE` | Intransessorial Cube | NUMBER | 22 | 16 | N |
| 20 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 21 | `ON_RCPT_WGT` | On_Rcptessorial Wgt | NUMBER | 22 | 16 | N |
| 22 | `ON_RCPT_CUBE` | On_Rcptessorial Cube | NUMBER | 22 | 16 | N |
| 23 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 24 | `ON_ORD_WGT` | On_Ordessorial Wgt | NUMBER | 22 | 16 | N |
| 25 | `ON_ORD_CUBE` | On_Ordessorial Cube | NUMBER | 22 | 16 | N |
| 26 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 27 | `ON_HAND_WGT` | On_Handessorial Wgt | NUMBER | 22 | 16 | N |
| 28 | `ON_HAND_CUBE` | On_Handessorial Cube | NUMBER | 22 | 16 | N |
| 29 | `ON_HAND_WGT_NET` | On_Hand_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 30 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 31 | `HOLD_NON_SHIP_QTY` | Hold_Non_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 32 | `HOLD_NON_SHIP_WGT` | Hold_Non_Shipessorial Wgt | NUMBER | 22 | 16 | N |
| 33 | `HOLD_NON_SHIP_CUBE` | Hold_Non_Shipessorial Cube | NUMBER | 22 | 16 | N |
| 34 | `HOLD_SHIP_QTY` | Hold_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 35 | `HOLD_SHIP_WGT` | Hold_Shipessorial Wgt | NUMBER | 22 | 16 | N |
| 36 | `HOLD_SHIP_CUBE` | Hold_Shipessorial Cube | NUMBER | 22 | 16 | N |
| 37 | `HOLD_SHIP_ON_ORD_QTY` | Hold_Ship_On_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 38 | `HOLD_SHIP_ON_ORD_WGT` | Hold_Ship_On_Ordessorial Wgt | NUMBER | 22 | 16 | N |
| 39 | `HOLD_SHIP_ON_ORD_CUBE` | Hold_Ship_On_Ordessorial Cube | NUMBER | 22 | 16 | N |
| 40 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | DATE | 7 |  | Y |
| 41 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 42 | `INVT_CL_DATE` | Invt_Clessorial Date | DATE | 7 |  | Y |
| 43 | `INVT_CLS_DATE` | Invt_Clsessorial Date | DATE | 7 |  | Y |
| 44 | `INVT_CLR_WGT_FLAG` | Invt_Clr_Wgtessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 46 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 47 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 48 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 49 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INVT_ATTR`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 9 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 10 | `INVT_ATTR_VAL` | Invt_Attressorial Val | VARCHAR2 | 40 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INVT_HOLD`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 9 | `INVT_HOLD_DATE` | Invt_Holdessorial Date | DATE | 7 |  | N |
| 10 | `INVT_HOLD_REF` | Invt_Holdessorial Ref | VARCHAR2 | 20 |  | Y |

## `C_INVT_HOLD_STAT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_HOLD_STAT_SEQ_NUM` | Invt_Hold_Stat_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 10 | `HOLD_CODE_EDI_CODE` | Hold_Code_Ediessorial Code | VARCHAR2 | 20 |  | N |
| 11 | `EDI_REF_NUM` | Edi_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 12 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 13 | `REAS_CODE_EDI` | Reas_Codeessorial Edi | VARCHAR2 | 20 |  | Y |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `C_INVT_HOLD_STAT_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE, MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_HOLD_STAT_QUEUE_SEQ_NUM` | Invt_Hold_Stat_Queue_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 10 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 12 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 14 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | Y |
| 15 | `PUT_ENTITY_ON_HOLD_FLAG` | Put_Entity_On_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | Y |
| 17 | `HOLD_CODE_EDI_CODE` | Hold_Code_Ediessorial Code | VARCHAR2 | 20 |  | Y |
| 18 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 19 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |

## `C_INVT_LEV_DES`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV2_DES` | Invt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV3_DES` | Invt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV4_DES` | Invt_Lev4essorial Des | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV5_DES` | Invt_Lev5essorial Des | VARCHAR2 | 40 |  | Y |

## `C_INVT_LEV_VALUE_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV_VALUE` | Invt_Levessorial Value | NUMBER | 22 | 16 | N |
| 9 | `VALUE_INX_CODE` | Value_Inxessorial Code | VARCHAR2 | 10 |  | N |
| 10 | `VALUE_INX_DATE` | Value_Inxessorial Date | DATE | 7 |  | N |
| 11 | `VALUE_INX_VALUE` | Value_Inxessorial Value | NUMBER | 22 | 16 | N |

## `C_INVT_LEV_VALUE_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV_VALUE` | Invt_Levessorial Value | NUMBER | 22 | 16 | N |
| 9 | `INVT_LEV_VALUE_DATE` | Invt_Lev_Valueessorial Date | DATE | 7 |  | N |

## `C_INVT_MES`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 3 | `INVT_MES_RCPT_FLAG` | Invt_Mes_Rcptessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `INVT_MES_ORD_FLAG` | Invt_Mes_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INVT_MES_LOOK_FLAG` | Invt_Mes_Lookessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |

## `C_INVT_RECON_VIRT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 8 | `CUST_CODE_VIRT` | Cust_Codeessorial Virt | VARCHAR2 | 10 |  | N |
| 9 | `INVT_LEV1_VIRT` | Invt_Lev1essorial Virt | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV2_VIRT` | Invt_Lev2essorial Virt | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV3_VIRT` | Invt_Lev3essorial Virt | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV4_VIRT` | Invt_Lev4essorial Virt | VARCHAR2 | 40 |  | N |
| 13 | `ON_HAND_QTY_VIRT` | On_Hand_Qtyessorial Virt | NUMBER | 22 | 9 | N |

## `C_INVT_STAT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_STAT_SEQ_NUM` | Invt_Stat_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 10 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `APP_CODE` | Application Code | VARCHAR2 | 30 |  | N |
| 12 | `INVT_STAT_CODE` | Invt_Statessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `EDI_REF_NUM` | Edi_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 14 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |

## `C_INV_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 7 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 8 | `INV_AMT_CUR_BASE` | Inv_Amt_Curessorial Base | NUMBER | 22 | 15 | Y |
| 9 | `INV_AMT_CUR` | Inv_Amtessorial Cur | NUMBER | 22 | 20 | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INV_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 7 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 8 | `INV_AMT_CUR_BASE` | Inv_Amt_Curessorial Base | NUMBER | 22 | 15 | Y |
| 9 | `INV_AMT_CUR` | Inv_Amtessorial Cur | NUMBER | 22 | 20 | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INV_D3`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 7 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 8 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 9 | `GL_ACC_CODE_ORG` | Gl_Acc_Codeessorial Org | VARCHAR2 | 18 |  | N |
| 10 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 11 | `INV_AMT_CUR_BASE` | Inv_Amt_Curessorial Base | NUMBER | 22 | 15 | Y |
| 12 | `INV_AMT_CUR` | Inv_Amtessorial Cur | NUMBER | 22 | 20 | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INV_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 53
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `INV_DATE` | Invessorial Date | DATE | 7 |  | N |
| 7 | `INV_REG_NUM` | Inv_Regessorial Num | NUMBER | 22 | 9 | Y |
| 8 | `INV_REG_DATE` | Inv_Regessorial Date | DATE | 7 |  | Y |
| 9 | `INV_TP` | Invessorial Tp | VARCHAR2 | 4 |  | N |
| 10 | `INV_STAT` | Invessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 12 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | Y |
| 13 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 14 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 15 | `GL_ACC_CODE_AR` | Gl_Acc_Codeessorial Ar | VARCHAR2 | 18 |  | N |
| 16 | `GL_ACC_CODE_BANK` | Gl_Acc_Codeessorial Bank | VARCHAR2 | 18 |  | N |
| 17 | `FILE_NAME` | Fileessorial Name | VARCHAR2 | 255 |  | Y |
| 18 | `INV_TAX1` | Invessorial Tax1 | NUMBER | 22 | 13 | Y |
| 19 | `INV_TAX2` | Invessorial Tax2 | NUMBER | 22 | 13 | Y |
| 20 | `COMP_CODE_ROLLUP` | Comp_Codeessorial Rollup | VARCHAR2 | 2 |  | Y |
| 21 | `INV_NUM_ROLLUP` | Inv_Numessorial Rollup | NUMBER | 22 | 9 | Y |
| 22 | `INV_PREX_ROLLUP` | Inv_Prexessorial Rollup | VARCHAR2 | 4 |  | Y |
| 23 | `INV_SUFX_ROLLUP` | Inv_Sufxessorial Rollup | VARCHAR2 | 4 |  | Y |
| 24 | `INV_EXT_INV_NUM` | Inv_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 25 | `INV_EXT_INV_PREX` | Inv_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 26 | `EDI_TRANS_DATE_LAST` | Edi_Trans_Dateessorial Last | DATE | 7 |  | Y |
| 27 | `EDI_TRANS_DATE_LAST_GMT` | Edi_Trans_Date_Lastessorial Gmt | DATE | 7 |  | Y |
| 28 | `EDI_TRANS_CNT` | Edi_Transessorial Cnt | NUMBER | 22 | 3 | Y |
| 29 | `INV_POST_BAL_STAT` | Inv_Post_Balessorial Stat | VARCHAR2 | 1 |  | Y |
| 30 | `INV_AMT_ORIG` | Inv_Amtessorial Orig | NUMBER | 22 | 13 | Y |
| 31 | `REPROS_FLAG` | Reprosessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `REPROS_DLRE_FLAG` | Repros_Dlreessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `INV_AMT_CUR_BASE` | Inv_Amt_Curessorial Base | NUMBER | 22 | 15 | Y |
| 34 | `INV_AMT_CUR` | Inv_Amtessorial Cur | NUMBER | 22 | 20 | Y |
| 35 | `INV_TAX1_CUR_BASE` | Inv_Tax1_Curessorial Base | NUMBER | 22 | 13 | Y |
| 36 | `INV_TAX1_CUR` | Inv_Tax1essorial Cur | NUMBER | 22 | 20 | Y |
| 37 | `INV_TAX2_CUR_BASE` | Inv_Tax2_Curessorial Base | NUMBER | 22 | 13 | Y |
| 38 | `INV_TAX2_CUR` | Inv_Tax2essorial Cur | NUMBER | 22 | 20 | Y |
| 39 | `CUR_CODE_BASE` | Cur_Codeessorial Base | VARCHAR2 | 4 |  | Y |
| 40 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | Y |
| 41 | `CUR_VALUE_BASE_CUR` | Cur_Value_Baseessorial Cur | NUMBER | 22 | 15 | Y |
| 42 | `MIN_INV_BAT_NUM` | Min_Inv_Batessorial Num | NUMBER | 22 | 9 | Y |
| 43 | `COST_PROS_FLAG` | Cost_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 45 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 46 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 47 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 48 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 49 | `INV_EMAIL_PROS_DATE` | Inv_Email_Prosessorial Date | DATE | 7 |  | Y |
| 50 | `INV_EMAIL_PROS_DATE_GMT` | Inv_Email_Pros_Dateessorial Gmt | DATE | 7 |  | Y |
| 51 | `INV_TO_EMAIL_ADD` | Inv_To_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 52 | `INV_CC_EMAIL_ADD` | Inv_Cc_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 53 | `CARBON_TAX_RECHG_REF` | Carbon_Tax_Rechgessorial Ref | NUMBER | 22 | 9 | Y |

## `C_INV_LOCK`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `C_INV_REF`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_DATE` | Invessorial Date | DATE | 7 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | Y |
| 7 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 8 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 9 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 15 | N |
| 10 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 11 | `REVN_GRP_CODE` | Revn_Grpessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `ACCSS_REF_DES` | Accss_Refessorial Des | VARCHAR2 | 40 |  | Y |

## `C_INV_REG_GL_ACC`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 3 | `GL_ACC_DES` | Gl_Accessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `GL_DATE` | Glessorial Date | DATE | 7 |  | N |
| 5 | `GL_AMT` | Glessorial Amt | NUMBER | 22 | 15 | N |

## `C_MAI_AR_BAL`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 7
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_FIN_INTFACE_COMP` | Comp_Fin_Intfaceessorial Comp | VARCHAR2 | 4 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `MAI_AR_BAL_INV_NUM` | Mai_Ar_Bal_Invessorial Num | VARCHAR2 | 8 |  | N |
| 4 | `MAI_AR_BAL_INV_DATE` | Mai_Ar_Bal_Invessorial Date | DATE | 7 |  | N |
| 5 | `MAI_AR_BAL_ORG_AMT` | Mai_Ar_Bal_Orgessorial Amt | NUMBER | 22 | 12 | N |
| 6 | `MAI_AR_BAL_BAL` | Mai_Ar_Balessorial Bal | NUMBER | 22 | 12 | N |
| 7 | `MAI_AR_CRT_LMT_AMT` | Mai_Ar_Crt_Lmtessorial Amt | NUMBER | 22 | 12 | N |

## `C_RENW_ORG`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 40 |  | N |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 40 |  | N |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 40 |  | N |
| 6 | `RENW_LEV4` | Renwessorial Lev4 | VARCHAR2 | 40 |  | N |
| 7 | `RENW_LEV5` | Renwessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 8 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 9 | `RENW_ORG_DATE` | Renw_Orgessorial Date | DATE | 7 |  | N |
| 10 | `RENW_ORG_RATE` | Renw_Orgessorial Rate | NUMBER | 22 | 9 | N |
| 11 | `RENW_ORG_QUAL_QTY` | Renw_Org_Qualessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `RENW_ORG_QUAL_CNVC_QTY` | Renw_Org_Qual_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 13 | `RENW_ORG_QUAL_WGT` | Renw_Org_Qualessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `RENW_ORG_QUAL_WGT_NET` | Renw_Org_Qual_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `RENW_ORG_QUAL_CUBE` | Renw_Org_Qualessorial Cube | NUMBER | 22 | 16 | N |
| 16 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `C_RENW_TRANS`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_TRANS_DATE` | Renw_Transessorial Date | DATE | 7 |  | N |
| 4 | `RENW_UPD_RENW_FLAG` | Renw_Upd_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 11 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | Y |
| 12 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 13 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 14 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 15 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 16 | `RENW_PER_NUM` | Renw_Peressorial Num | NUMBER | 22 | 4 | Y |
| 17 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 18 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | Y |
| 19 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 20 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 21 | `CUST_CODE_TRF_FROM` | Cust_Code_Trfessorial From | VARCHAR2 | 10 |  | Y |
| 22 | `RESET_RENW_DATE_FLAG` | Reset_Renw_Dateessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `INVT_ACCESS_TRF_FROM` | Invt_Access_Trfessorial From | VARCHAR2 | 5 |  | Y |
| 24 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 25 | `RENW_INV_DATE_NXT` | Renw_Inv_Dateessorial Nxt | DATE | 7 |  | Y |
| 26 | `RENW_INV_DATE_LAST` | Renw_Inv_Dateessorial Last | DATE | 7 |  | Y |

## `C_RENW_VALUE`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 40 |  | N |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 6 | `RENW_LEV4` | Renwessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 7 | `RENW_LEV5` | Renwessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 8 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 9 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 10 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 11 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 12 | `OPEN_QTY` | Openessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `OPEN_WGT` | Openessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `OPEN_WGT_NET` | Open_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `OPEN_CUBE` | Openessorial Cube | NUMBER | 22 | 16 | N |
| 16 | `OPEN_CNVC_QTY` | Open_Cnvcessorial Qty | NUMBER | 22 | 6 | N |
| 17 | `OPEN_VALUE` | Openessorial Value | NUMBER | 22 | 12 | N |
| 18 | `INB_QTY` | Inbessorial Qty | NUMBER | 22 | 9 | N |
| 19 | `INB_WGT` | Inbessorial Wgt | NUMBER | 22 | 16 | N |
| 20 | `INB_WGT_NET` | Inb_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 21 | `INB_CUBE` | Inbessorial Cube | NUMBER | 22 | 16 | N |
| 22 | `INB_CNVC_QTY` | Inb_Cnvcessorial Qty | NUMBER | 22 | 6 | N |
| 23 | `INB_VALUE` | Inbessorial Value | NUMBER | 22 | 12 | N |
| 24 | `TOT_QTY` | Totessorial Qty | NUMBER | 22 | 9 | N |
| 25 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | N |
| 26 | `TOT_WGT_NET` | Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 27 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | N |
| 28 | `TOT_CNVC_QTY` | Tot_Cnvcessorial Qty | NUMBER | 22 | 6 | N |
| 29 | `TOT_VALUE` | Totessorial Value | NUMBER | 22 | 12 | N |

## `C_REP_LINK_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_LINK_TABLE_NAME` | Rep_Link_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 2 | `REP_LINK_TABLE_FROM` | Rep_Link_Tableessorial From | VARCHAR2 | 30 |  | N |
| 3 | `REP_LINK_LINE_NUM` | Rep_Link_Lineessorial Num | NUMBER | 22 | 2 | N |
| 4 | `REP_LINK_COL_CODE` | Rep_Link_Colessorial Code | VARCHAR2 | 30 |  | N |
| 5 | `REP_LINK_COL_FROM_TABLE` | Rep_Link_Col_Fromessorial Table | VARCHAR2 | 30 |  | Y |
| 6 | `REP_LINK_COL_FROM_CODE` | Rep_Link_Col_Fromessorial Code | VARCHAR2 | 30 |  | N |

## `C_REP_LINK_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_LINK_TABLE_NAME` | Rep_Link_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 2 | `REP_LINK_TABLE_FROM` | Rep_Link_Tableessorial From | VARCHAR2 | 30 |  | N |
| 3 | `REP_LINK_LINE_NUM` | Rep_Link_Lineessorial Num | NUMBER | 22 | 2 | N |
| 4 | `REP_LINK_DES` | Rep_Linkessorial Des | VARCHAR2 | 60 |  | Y |
| 5 | `REP_LINK_SINGLE_ROW_FLAG` | Rep_Link_Single_Rowessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_REP_RUN_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_ID` | Repessorial Id | NUMBER | 22 | 9 | N |
| 2 | `REP_PROMPT_PROF_CODE` | Rep_Prompt_Professorial Code | VARCHAR2 | 20 |  | N |
| 3 | `REP_PROMPT_VAL` | Rep_Promptessorial Val | VARCHAR2 | 1000 |  | N |

## `C_REP_RUN_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_ID` | Repessorial Id | NUMBER | 22 | 9 | N |
| 2 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `SCH_PROF_CODE` | Sch_Professorial Code | VARCHAR2 | 20 |  | N |
| 6 | `REP_DATE` | Repessorial Date | DATE | 7 |  | Y |

## `C_REVN_ANAL`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 4 | `REVN_DATE` | Revnessorial Date | DATE | 7 |  | N |
| 5 | `REVN_AMT` | Revnessorial Amt | NUMBER | 22 | 13 | N |
| 6 | `REVN_CONV_AMT` | Revn_Convessorial Amt | NUMBER | 22 | 13 | Y |
| 7 | `REVN_AMT_CUR_BASE` | Revn_Amt_Curessorial Base | NUMBER | 22 | 16 | Y |
| 8 | `REVN_CONV_AMT_CUR_BASE` | Revn_Conv_Amt_Curessorial Base | NUMBER | 22 | 16 | Y |

## `C_SOLOMON_AR`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 5
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 2 | `SOLOMON_AR_TRANS_NUM` | Solomon_Ar_Transessorial Num | VARCHAR2 | 10 |  | N |
| 3 | `SOLOMON_AR_TRANS_TP` | Solomon_Ar_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 4 | `SOLOMON_AR_TRANS_DATE` | Solomon_Ar_Transessorial Date | DATE | 7 |  | N |
| 5 | `SOLOMON_AR_TRANS_AMT` | Solomon_Ar_Transessorial Amt | NUMBER | 22 | 12 | Y |

## `E_ACCSS_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 7 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 8 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 9 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 10 | `ACCSS_QTY` | Access Quantity | NUMBER | 22 | 9 | N |
| 11 | `ACCSS_RATE` | Access Rate | NUMBER | 22 | 9 | N |
| 12 | `ACCSS_AMT` | Accssessorial Amt | NUMBER | 22 | 10 | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ACCSS_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `ACCSS_REM_NUM` | Accss_Remessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ACCSS_REM_TEXT` | Accss_Remessorial Text | VARCHAR2 | 45 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ACCSS_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 90
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `ACCSS_STAT` | Accssessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ACCSS_DATE` | Access Date | DATE | 7 |  | N |
| 7 | `ACCSS_REM_FLAG` | Accss_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `BAT_NUM_ACCSS` | Bat_Numessorial Accss | NUMBER | 22 | 9 | N |
| 10 | `BAT_NUM_RENW` | Bat_Numessorial Renw | NUMBER | 22 | 9 | N |
| 11 | `ACCSS_SRCE_REF_FLAG` | Accss_Srce_Refessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `ACCSS_SRCE_REF_CHG_TP_FLAG` | Accss_Srce_Ref_Chg_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `ACCSS_SRCE_REF_NUM` | Accss_Srce_Refessorial Num | NUMBER | 22 | 9 | N |
| 14 | `ACCSS_SRCE_REF_LINE_NUM` | Accss_Srce_Ref_Lineessorial Num | NUMBER | 22 | 4 | N |
| 15 | `ACCSS_SRCE_REF_CONF_FLAG` | Accss_Srce_Ref_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CHG_SEQ_NUM` | Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 17 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 18 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 19 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 20 | `INV_TP_CODE` | Inv_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 21 | `CHG_PRT_FLAG` | Chg_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 23 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 24 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 25 | `QUAL_QTY` | Qualessorial Qty | NUMBER | 22 | 16 | N |
| 26 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | N |
| 27 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 28 | `CHG_FLAT_RATE_FLAG` | Chg_Flat_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `CHG_RATE_ORG` | Chg_Rateessorial Org | NUMBER | 22 | 15 | N |
| 30 | `CHG_RATE_CRNT` | Chg_Rateessorial Crnt | NUMBER | 22 | 15 | N |
| 31 | `CHG_TOT` | Charge Total | NUMBER | 22 | 16 | N |
| 32 | `CHG_MIN_FLAG` | Chg_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `CHG_MAX_FLAG` | Chg_Maxessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `ACCSS_AUDIT_FLAG` | Accss_Auditessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `GL_MODY_SUB_MODY` | Gl_Mody_Subessorial Mody | VARCHAR2 | 10 |  | Y |
| 36 | `ACCSS_REF_DES` | Accss_Refessorial Des | VARCHAR2 | 40 |  | Y |
| 37 | `ACCSS_REF_NUM` | Accss_Refessorial Num | VARCHAR2 | 40 |  | Y |
| 38 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | Y |
| 39 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | Y |
| 40 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 41 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 42 | `CHG_TAX1` | Chgessorial Tax1 | NUMBER | 22 | 13 | Y |
| 43 | `CHG_TAX2` | Chgessorial Tax2 | NUMBER | 22 | 13 | Y |
| 44 | `CUST_CODE_INVT` | Cust_Codeessorial Invt | VARCHAR2 | 10 |  | Y |
| 45 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 46 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 47 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 48 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 49 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 50 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 51 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | Y |
| 52 | `ENT_QTY` | Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 53 | `QTY` | Qtyessorial Qty | NUMBER | 22 | 9 | Y |
| 54 | `CNVC_QTY` | Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 55 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 56 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 16 | Y |
| 57 | `WGT_NET` | Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 58 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 59 | `CUBE` | Cubeessorial Cube | NUMBER | 22 | 16 | Y |
| 60 | `OP_CODE_AUDIT` | Op_Codeessorial Audit | VARCHAR2 | 20 |  | Y |
| 61 | `ACCSS_AUDIT_DATE` | Accss_Auditessorial Date | DATE | 7 |  | Y |
| 62 | `ACCSS_AUDIT_PRT_CNT` | Accss_Audit_Prtessorial Cnt | NUMBER | 22 | 2 | Y |
| 63 | `COMP_CODE_ROLLUP` | Comp_Codeessorial Rollup | VARCHAR2 | 2 |  | Y |
| 64 | `INV_NUM_ROLLUP` | Inv_Numessorial Rollup | NUMBER | 22 | 9 | Y |
| 65 | `INV_PREX_ROLLUP` | Inv_Prexessorial Rollup | VARCHAR2 | 4 |  | Y |
| 66 | `INV_SUFX_ROLLUP` | Inv_Sufxessorial Rollup | VARCHAR2 | 4 |  | Y |
| 67 | `BAT_NUM_ACCSS_ROLLUP` | Bat_Num_Accssessorial Rollup | NUMBER | 22 | 9 | Y |
| 68 | `BAT_NUM_RENW_ROLLUP` | Bat_Num_Renwessorial Rollup | NUMBER | 22 | 9 | Y |
| 69 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 70 | `BAT_NUM_EXCH` | Bat_Numessorial Exch | NUMBER | 22 | 9 | Y |
| 71 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 72 | `ACCSS_AUDIT_NUM` | Accss_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 73 | `SURCHG_INCL_FLAG` | Surchg_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 74 | `CRT_FLAG` | Crtessorial Flag | VARCHAR2 | 1 |  | Y |
| 75 | `REPROS_DLRE_FLAG` | Repros_Dlreessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `NUM_OF_FREE_DAYS` | Num_Of_Freeessorial Days | NUMBER | 22 | 4 | Y |
| 77 | `CHG_TOT_CUR_BASE` | Chg_Tot_Curessorial Base | NUMBER | 22 | 16 | Y |
| 78 | `CHG_TOT_CUR` | Chg_Totessorial Cur | NUMBER | 22 | 20 | Y |
| 79 | `BAT_NUM_INV_MIN` | Bat_Num_Invessorial Min | NUMBER | 22 | 9 | Y |
| 80 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 81 | `DEPT_CODE` | Deptessorial Code | VARCHAR2 | 10 |  | Y |
| 82 | `BAT_NUM_PRO_FORMA` | Bat_Num_Proessorial Forma | NUMBER | 22 | 9 | Y |
| 83 | `BAT_NUM_PRE_RENW` | Bat_Num_Preessorial Renw | NUMBER | 22 | 9 | Y |
| 84 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 85 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | Y |
| 86 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 87 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 88 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 89 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 90 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_AR_CASH_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_SEQ_NUM` | Check_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `CHECK_INV_LINE_NUM` | Check_Inv_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 7 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 8 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 9 | `CHECK_INV_LINE_AMT` | Check_Inv_Lineessorial Amt | NUMBER | 22 | 13 | N |
| 10 | `CHECK_INV_LINE_REM` | Check_Inv_Lineessorial Rem | VARCHAR2 | 1000 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_AR_CASH_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_SEQ_NUM` | Check_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `CHECK_REF_NUM` | Check_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CHECK_ENTRY_DATE` | Check_Entryessorial Date | DATE | 7 |  | N |
| 7 | `CHECK_DATE` | Checkessorial Date | DATE | 7 |  | N |
| 8 | `CHECK_AMT` | Checkessorial Amt | NUMBER | 22 | 13 | N |
| 9 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 10 | `CHECK_STAT` | Checkessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `CHECK_BAT_FLAG` | Check_Batessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `CHECK_REM` | Checkessorial Rem | VARCHAR2 | 1000 |  | Y |
| 14 | `CASH_POST_BAT_NUM` | Cash_Post_Batessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `CASH_POST_TO_ACCT_AMT` | Cash_Post_To_Acctessorial Amt | NUMBER | 22 | 13 | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_BAT_ACTN`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_SPC_CODE` | Bat_Spcessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `BAT_ACTN_FLAG` | Bat_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 6 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 7 | `BAT_PRT_TRANS_FLAG` | Bat_Prt_Transessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_CART_CNT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CART_CNT_NUM` | Cart_Cntessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CART_CNT_START_DATE` | Cart_Cnt_Startessorial Date | DATE | 7 |  | N |
| 4 | `CART_CNT_MOD_DATE` | Cart_Cnt_Modessorial Date | DATE | 7 |  | Y |
| 5 | `CART_CNT_NEW_FLAG` | Cart_Cnt_Newessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 8 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 11 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `CART_CNT_QTY` | Cart_Cntessorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `CART_CNT_ENT_QTY` | Cart_Cnt_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 19 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 20 | `CART_CNT_STAT` | Cart_Cntessorial Stat | VARCHAR2 | 1 |  | N |

## `E_CHECK_LIST_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_DOC_NUM` | Check_List_Docessorial Num | NUMBER | 22 | 9 | N |
| 4 | `CHECK_LIST_SEQ_NUM` | Check_List_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHECK_LIST_QUEST` | Check_Listessorial Quest | VARCHAR2 | 250 |  | N |
| 6 | `CHECK_LIST_ANSW` | Check_Listessorial Answ | VARCHAR2 | 250 |  | Y |
| 7 | `CHECK_LIST_ANSW_FAIL_FLAG` | Check_List_Answ_Failessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_CHECK_LIST_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_DOC_NUM` | Check_List_Docessorial Num | NUMBER | 22 | 9 | N |
| 4 | `CHECK_LIST_CODE` | Check_Listessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `CHECK_LIST_START_DATE` | Check_List_Startessorial Date | DATE | 7 |  | N |
| 9 | `CHECK_LIST_END_DATE` | Check_List_Endessorial Date | DATE | 7 |  | Y |
| 10 | `CHECK_LIST_ENTRY_COMPL_FLAG` | Check_List_Entry_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CHECK_LIST_ENTRY_FAIL_FLAG` | Check_List_Entry_Failessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |

## `E_COST_ALLOC_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PER_PROF_FIS_YEAR` | Per_Prof_Fisessorial Year | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `COST_CAT_CODE` | Cost_Catessorial Code | VARCHAR2 | 12 |  | N |
| 5 | `PER_SEQ_NUM` | Per_Seqessorial Num | NUMBER | 22 | 3 | N |
| 6 | `PER_PROF_CODE` | Per_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `COST_CAT_CALC_METHOD` | Cost_Cat_Calcessorial Method | VARCHAR2 | 4 |  | Y |
| 8 | `COST_CAT_AMOUNT1` | Cost_Catessorial Amount1 | NUMBER | 22 | 7 | N |
| 9 | `COST_CAT_AMOUNT2` | Cost_Catessorial Amount2 | NUMBER | 22 | 7 | N |
| 10 | `COST_CAT_AMOUNT3` | Cost_Catessorial Amount3 | NUMBER | 22 | 7 | N |
| 11 | `COST_ALLOC_AMOUNT1` | Cost_Allocessorial Amount1 | NUMBER | 22 | 7 | N |
| 12 | `COST_ALLOC_AMOUNT2` | Cost_Allocessorial Amount2 | NUMBER | 22 | 7 | N |
| 13 | `COST_ALLOC_AMOUNT3` | Cost_Allocessorial Amount3 | NUMBER | 22 | 7 | N |

## `E_COST_ALLOC_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PER_PROF_FIS_YEAR` | Per_Prof_Fisessorial Year | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `COST_CAT_CODE` | Cost_Catessorial Code | VARCHAR2 | 12 |  | N |
| 5 | `PER_PROF_CODE` | Per_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `COST_CAT_CALC_METHOD` | Cost_Cat_Calcessorial Method | VARCHAR2 | 4 |  | N |
| 7 | `COST_CAT_AMOUNT1_TOTAL` | Cost_Cat_Amount1essorial Total | NUMBER | 22 | 12 | N |
| 8 | `COST_CAT_AMOUNT2_TOTAL` | Cost_Cat_Amount2essorial Total | NUMBER | 22 | 12 | N |
| 9 | `COST_CAT_AMOUNT3_TOTAL` | Cost_Cat_Amount3essorial Total | NUMBER | 22 | 12 | N |
| 10 | `COST_ALLOC_AMOUNT1_TOTAL` | Cost_Alloc_Amount1essorial Total | NUMBER | 22 | 12 | N |
| 11 | `COST_ALLOC_AMOUNT2_TOTAL` | Cost_Alloc_Amount2essorial Total | NUMBER | 22 | 12 | N |
| 12 | `COST_ALLOC_AMOUNT3_TOTAL` | Cost_Alloc_Amount3essorial Total | NUMBER | 22 | 12 | N |
| 13 | `E_COST_ALLOC_STAT` | E_Cost_Allocessorial Stat | VARCHAR2 | 1 |  | N |

## `E_DOC_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `DOC_QUEUE_TRANS_DATE` | Doc_Queue_Transessorial Date | DATE | 7 |  | N |
| 4 | `REC_TP_CODE` | Rec_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 7 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | N |
| 8 | `DOC_PRTY_NUM` | Doc_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 9 | `DOC_QUEUE_ACT_TO_TAKE_FLAG` | Doc_Queue_Act_To_Takeessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 11 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |

## `E_FRT_BILL_GRP_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `BILL_GRP_UNIT` | Bill_Grpessorial Unit | NUMBER | 22 | 9 | Y |
| 6 | `BILL_GRP_WGT` | Bill_Grpessorial Wgt | NUMBER | 22 | 11 | Y |
| 7 | `BILL_GRP_CUBE` | Bill_Grpessorial Cube | NUMBER | 22 | 12 | Y |
| 8 | `BILL_GRP_ASWGT` | Bill_Grpessorial Aswgt | NUMBER | 22 | 11 | Y |
| 9 | `BILL_GRP_RATE` | Bill_Grpessorial Rate | NUMBER | 22 | 9 | Y |
| 10 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 11 | `BILL_GRP_AMT` | Bill_Grpessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `BILL_GRP_DISC_PCENT` | Bill_Grp_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 13 | `BILL_GRP_FLAG` | Bill_Grpessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_BILL_GRP_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | N |
| 4 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 8 | `BILL_GRP_CHG_DES` | Bill_Grp_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `BILL_GRP_CHG_QTY` | Bill_Grp_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `BILL_GRP_CHG_RATE` | Bill_Grp_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 11 | `BILL_GRP_CHG_AMT` | Bill_Grp_Chgessorial Amt | NUMBER | 22 | 10 | N |

## `E_FRT_BILL_GRP_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | N |
| 4 | `BILL_GRP_DES` | Bill_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `BILL_GRP_DEST_CODE_ORIGIN` | Bill_Grp_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 7 | `BILL_GRP_DEST_CODE` | Bill_Grp_Destessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `BILL_GRP_ENTRY_DATE` | Bill_Grp_Entryessorial Date | DATE | 7 |  | Y |
| 9 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 10 | `BILL_GRP_TOT_AMT` | Bill_Grp_Totessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `BILL_GRP_TOT_ADDI_AMT` | Bill_Grp_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 13 | `BILL_GRP_INTRA_FLAG` | Bill_Grp_Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `BILL_GRP_DISC_PCENT` | Bill_Grp_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 15 | `BILL_GRP_ASWGT` | Bill_Grpessorial Aswgt | NUMBER | 22 | 11 | Y |
| 16 | `BILL_GRP_RATE_LEV` | Bill_Grp_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 17 | `BILL_GRP_RATE_BY_FLAG` | Bill_Grp_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `BILL_GRP_DELV_FLAG` | Bill_Grp_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 20 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |

## `E_FRT_CARR_PAY_D`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_INV_NUM` | Carr_Invessorial Num | NUMBER | 22 | 10 | N |
| 5 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 6 | `LOAD_NUM` | Load Number | NUMBER | 22 | 10 | N |
| 7 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 8 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 9 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 10 |  | N |
| 10 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `E_FRT_CARR_PAY_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_INV_NUM` | Carr_Invessorial Num | NUMBER | 22 | 10 | N |
| 5 | `CARR_INV_DATE` | Carr_Invessorial Date | DATE | 7 |  | N |
| 6 | `CARR_INV_AMT` | Carr_Invessorial Amt | NUMBER | 22 | 9 | Y |
| 7 | `CARR_INV_TAX_AMT1` | Carr_Inv_Taxessorial Amt1 | NUMBER | 22 | 9 | Y |
| 8 | `CARR_INV_TAX_AMT2` | Carr_Inv_Taxessorial Amt2 | NUMBER | 22 | 9 | Y |

## `E_IMM_INV_D1`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 43
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `IMM_INV_LINE_NUM` | Imm_Inv_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 7 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `IMM_INV_LINE_REF_DES` | Imm_Inv_Line_Refessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 10 | `GL_MODY_SUB_MODY` | Gl_Mody_Subessorial Mody | VARCHAR2 | 10 |  | Y |
| 11 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 12 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 13 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 14 | `QUAL_QTY` | Qualessorial Qty | NUMBER | 22 | 16 | N |
| 15 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | N |
| 16 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 17 | `CHG_FLAT_RATE_FLAG` | Chg_Flat_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 15 | N |
| 19 | `CHG_TOT` | Charge Total | NUMBER | 22 | 16 | N |
| 20 | `CHG_TAX1` | Chgessorial Tax1 | NUMBER | 22 | 13 | Y |
| 21 | `CHG_TAX2` | Chgessorial Tax2 | NUMBER | 22 | 13 | Y |
| 22 | `CHG_LINE_REM_FLAG` | Chg_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `CHG_MIN_FLAG` | Chg_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `CHG_MAX_FLAG` | Chg_Maxessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `CHG_SEQ_NUM` | Chg_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 27 | `CRT_FLAG` | Crtessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `REPROS_DLRE_FLAG` | Repros_Dlreessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `CHG_TOT_CUR_BASE` | Chg_Tot_Curessorial Base | NUMBER | 22 | 16 | Y |
| 30 | `CHG_TOT_CUR` | Chg_Totessorial Cur | NUMBER | 22 | 20 | Y |
| 31 | `CHG_TAX1_CUR_BASE` | Chg_Tax1_Curessorial Base | NUMBER | 22 | 13 | Y |
| 32 | `CHG_TAX1_CUR` | Chg_Tax1essorial Cur | NUMBER | 22 | 20 | Y |
| 33 | `CHG_TAX2_CUR_BASE` | Chg_Tax2_Curessorial Base | NUMBER | 22 | 13 | Y |
| 34 | `CHG_TAX2_CUR` | Chg_Tax2essorial Cur | NUMBER | 22 | 20 | Y |
| 35 | `CUR_CODE_BASE` | Cur_Codeessorial Base | VARCHAR2 | 4 |  | Y |
| 36 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | Y |
| 37 | `CUR_VALUE_BASE_CUR` | Cur_Value_Baseessorial Cur | NUMBER | 22 | 15 | Y |
| 38 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 39 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 40 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 41 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 42 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 43 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_IMM_INV_D2`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `IMM_INV_LINE_NUM` | Imm_Inv_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `IMM_INV_REM_NUM` | Imm_Inv_Remessorial Num | NUMBER | 22 | 4 | N |
| 6 | `IMM_INV_REM_TEXT` | Imm_Inv_Remessorial Text | VARCHAR2 | 45 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_IMM_INV_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 5 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `IMM_INV_DATE` | Imm_Invessorial Date | DATE | 7 |  | N |
| 8 | `IMM_INV_REF_DES` | Imm_Inv_Refessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `IMM_INV_REM_FLAG` | Imm_Inv_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 11 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 12 | `BAT_STAT` | Batessorial Stat | VARCHAR2 | 1 |  | Y |
| 13 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_INV_COST_H`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 5 | `COST_LINE_NUM` | Cost_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 8 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 10 | `GL_MODY_SUB_MODY` | Gl_Mody_Subessorial Mody | VARCHAR2 | 10 |  | Y |
| 11 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 12 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 13 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 14 | `QUAL_QTY` | Qualessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | N |
| 16 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 17 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 15 | N |
| 18 | `CHG_TOT` | Charge Total | NUMBER | 22 | 16 | N |
| 19 | `CHG_TAX1` | Chgessorial Tax1 | NUMBER | 22 | 13 | Y |
| 20 | `CHG_TAX2` | Chgessorial Tax2 | NUMBER | 22 | 13 | Y |
| 21 | `CHG_LINE_REM_FLAG` | Chg_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CHG_MIN_FLAG` | Chg_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `CHG_MAX_FLAG` | Chg_Maxessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `CHG_TOT_CUR_BASE` | Chg_Tot_Curessorial Base | NUMBER | 22 | 16 | Y |
| 25 | `CHG_TOT_CUR` | Chg_Totessorial Cur | NUMBER | 22 | 20 | Y |
| 26 | `CHG_TAX1_CUR_BASE` | Chg_Tax1_Curessorial Base | NUMBER | 22 | 13 | Y |
| 27 | `CHG_TAX1_CUR` | Chg_Tax1essorial Cur | NUMBER | 22 | 20 | Y |
| 28 | `CHG_TAX2_CUR_BASE` | Chg_Tax2_Curessorial Base | NUMBER | 22 | 13 | Y |
| 29 | `CHG_TAX2_CUR` | Chg_Tax2essorial Cur | NUMBER | 22 | 20 | Y |
| 30 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | Y |
| 31 | `CUR_VALUE_BASE_CUR` | Cur_Value_Baseessorial Cur | NUMBER | 22 | 15 | Y |
| 32 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |

## `E_PROS_BAT`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 4 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 5 | `BAT_PROS_FLAG` | Bat_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RENW_LOCK`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 6 | `RENW_LEV4` | Renwessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 7 | `RENW_LEV5` | Renwessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 8 | `RENW_PER_NUM` | Renw_Peressorial Num | NUMBER | 22 | 4 | Y |
| 9 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 10 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | Y |
| 11 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 12 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `E_RENW_TRANS`

- **Tipo:** Transactional
- **Categoria:** Billing
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 6 | `RENW_LEV4` | Renwessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 7 | `RENW_LEV5` | Renwessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 8 | `RENW_PER_NUM` | Renw_Peressorial Num | NUMBER | 22 | 4 | Y |
| 9 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 10 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | Y |
| 11 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 12 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 13 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 14 | `RENW_PROS_DATE` | Renw_Prosessorial Date | DATE | 7 |  | Y |
| 15 | `RENW_INV_DATE_NXT` | Renw_Inv_Dateessorial Nxt | DATE | 7 |  | Y |
| 16 | `RENW_INV_DATE_LAST` | Renw_Inv_Dateessorial Last | DATE | 7 |  | Y |

## `L_RY_INVT_LEV`

- **Tipo:** Custom
- **Categoria:** Billing
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LEV_NUM` | Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `INVT_LEV` | Invtessorial Lev | VARCHAR2 | 40 |  | N |

## `M_ALT_INVT_REP_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `ALT_INVT_REP_DES` | Alt_Invt_Repessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `ALT_INVT_REP_STAT` | Alt_Invt_Repessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `ITEM_BILL_PROF_CODE` | Item_Bill_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `ALT_INVT_REP_EXT_REF` | Alt_Invt_Rep_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ALT_INVT_REP_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ALT_INVT_REP_TP_DES` | Alt_Invt_Rep_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ALT_INVT_REP_TP_STAT` | Alt_Invt_Rep_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ALT_TP`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ALT_TP_CODE` | Alt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ALT_TP_DES` | Alt_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ALT_TP_STAT` | Alt_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_APPO_A1SCH_INTFACE_CONFIG`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `APPO_A1SCH_STAT` | Appo_A1Schessorial Stat | VARCHAR2 | 100 |  | N |
| 5 | `APPO_3PL_STAT` | Appo_3Plessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `APPO_DOC_ADV_FLOW_FLAG` | Appo_Doc_Adv_Flowessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `INB_FLOW_PROS_CODE` | Inb_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `OUTB_FLOW_PROS_CODE` | Outb_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_APPR_LEV`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `APPR_LEV_CODE` | Appr_Levessorial Code | VARCHAR2 | 1 |  | N |
| 3 | `APPR_LEV_DES` | Appr_Levessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `APPR_LEV_STAT` | Appr_Levessorial Stat | VARCHAR2 | 1 |  | N |

## `M_AUD_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 2 | `COL_NAME` | Column Name | VARCHAR2 | 40 |  | N |
| 3 | `COL_DES` | Colessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `AUD_COL_FLAG` | Aud_Colessorial Flag | VARCHAR2 | 1 |  | N |

## `M_AUD_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 2 | `TAB_DES` | Tabessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `TAB_GRP_TP` | Tab_Grpessorial Tp | VARCHAR2 | 20 |  | Y |
| 4 | `TAB_TRG_PRC` | Tab_Trgessorial Prc | VARCHAR2 | 1000 |  | Y |

## `M_BAT_TP_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 6 | `BAT_TP_AUD_CONF_FLAG` | Bat_Tp_Aud_Confessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BAT_TP_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 4 | `BAT_TP_DES` | Bat_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `BAT_TP_STAT` | Bat_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `BAT_TP_CRNT_NUM` | Bat_Tp_Crntessorial Num | NUMBER | 22 | 6 | N |
| 7 | `BAT_TP_GEN_CREATE_FLAG` | Bat_Tp_Gen_Createessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `BAT_TP_REAUD_FLAG` | Bat_Tp_Reaudessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `BAT_TP_CONT_FLAG` | Bat_Tp_Contessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `BAT_TP_BAL_FLAG` | Bat_Tp_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHG`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 4 | `CHG_DES` | Chgessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CHG_STAT` | Chgessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CHG_BKD_FLAG` | Chg_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | Y |
| 9 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | Y |
| 10 | `INV_TP_CODE` | Inv_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | Y |
| 12 | `SKU_CODE_CHG_RND_FLAG` | Sku_Code_Chg_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | Y |
| 14 | `SKU_CODE_QUAL_RND_FLAG` | Sku_Code_Qual_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `CHG_CODE_RATE` | Chg_Codeessorial Rate | VARCHAR2 | 6 |  | Y |
| 16 | `CHG_FORUL` | Chgessorial Forul | VARCHAR2 | 40 |  | Y |
| 17 | `CHG_REF` | Chgessorial Ref | VARCHAR2 | 30 |  | Y |
| 18 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 19 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 20 | `TAX_FORCE_FLAG` | Tax_Forceessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHG_DATE_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 6 | `CHG_DATE_BK_NUM` | Chg_Date_Bkessorial Num | NUMBER | 22 | 2 | N |
| 7 | `CHG_DATE_BK_QTY` | Chg_Date_Bkessorial Qty | NUMBER | 22 | 12 | Y |
| 8 | `CHG_DATE_BK_AMT` | Chg_Date_Bkessorial Amt | NUMBER | 22 | 15 | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHG_DATE_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 6 | `CHG_DATE_PCENT` | Chg_Dateessorial Pcent | NUMBER | 22 | 7 | Y |
| 7 | `CHG_DATE_FLAT_AMT` | Chg_Date_Flatessorial Amt | NUMBER | 22 | 12 | Y |
| 8 | `CHG_DATE_FLAT_BK_TOT` | Chg_Date_Flat_Bkessorial Tot | NUMBER | 22 | 2 | Y |
| 9 | `CHG_DATE_BK_TOT` | Chg_Date_Bkessorial Tot | NUMBER | 22 | 2 | Y |
| 10 | `CHG_DATE_MIN_AMT` | Chg_Date_Minessorial Amt | NUMBER | 22 | 12 | Y |
| 11 | `CHG_DATE_MAX_AMT` | Chg_Date_Maxessorial Amt | NUMBER | 22 | 12 | Y |
| 12 | `CHG_SUPPRESS_SURCHG_FLAG` | Chg_Suppress_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | Y |
| 14 | `SKU_CODE_CHG_RND_FLAG` | Sku_Code_Chg_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | Y |
| 16 | `SKU_CODE_QUAL_RND_FLAG` | Sku_Code_Qual_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 22 | `CHG_SUPPRESS_RCPT_SURCHG_FLAG` | Chg_Suppress_Rcpt_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `CHG_SUPPRESS_RENW_SURCHG_FLAG` | Chg_Suppress_Renw_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `CHG_SUPPRESS_ACCS_SURCHG_FLAG` | Chg_Suppress_Accs_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `CHG_SUPPRESS_IINV_SURCHG_FLAG` | Chg_Suppress_Iinv_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `CHG_ID` | Chgessorial Id | RAW | 32 |  | N |

## `M_CHG_GRP_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHG_GRP_CODE` | Chg_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHG_GRP_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHG_GRP_CODE` | Chg_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHG_GRP_DES` | Chg_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CHG_GRP_STAT` | Chg_Grpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CHG_CODE_MIN_MAX` | Chg_Code_Minessorial Max | VARCHAR2 | 6 |  | N |
| 7 | `CHG_GRP_TP_CODE` | Chg_Grp_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHG_MULT_FACT`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 4 | `CHG_CODE_MULT_FACT` | Chg_Code_Multessorial Fact | NUMBER | 22 | 10 | N |

## `M_DENS_CHG`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHG_CODE_DENS` | Chg_Codeessorial Dens | VARCHAR2 | 6 |  | N |
| 4 | `DENS_CHG_BK_VALUE` | Dens_Chg_Bkessorial Value | NUMBER | 22 | 12 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |

## `M_EXTRA_CHG_PROF_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 36
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EXTRA_CHG_PROF_INB_OUTB_FLAG` | Extra_Chg_Prof_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `EXTRA_CHG_PROF_SEQ_NUM` | Extra_Chg_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `EXTRA_CHG_PROF_ACTN_FLAG` | Extra_Chg_Prof_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EXTRA_CHG_PROF_ENTRY_TP_FLAG` | Extra_Chg_Prof_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `EXTRA_CHG_PROF_OVRR_QTY_FLAG` | Extra_Chg_Prof_Ovrr_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EXTRA_CHG_PROF_TREAT_FLAG` | Extra_Chg_Prof_Treatessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `EXTRA_CHG_PROF_CUST_CODE_REST` | Extra_Chg_Prof_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 14 | `EXTRA_CHG_PROF_CON_CODE_REST` | Extra_Chg_Prof_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 15 | `EXTRA_CHG_PROF_SHIP_CODE_REST` | Extra_Chg_Prof_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 16 | `EXTRA_CHG_PROF_CARR_CODE_REST` | Extra_Chg_Prof_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 17 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |
| 18 | `EXTRA_CHG_PROF_HOLD_CODE_REST` | Extra_Chg_Prof_Hold_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 19 | `EXTRA_CHG_PROF_DATE_BAT_DOC_TP` | Extra_Chg_Prof_Date_Bat_Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 20 | `EXTRA_CHG_PROF_LOAD_TP_REST` | Extra_Chg_Prof_Load_Tpessorial Rest | VARCHAR2 | 250 |  | Y |
| 21 | `EXTRA_CHG_PROF_RF_FLAG` | Extra_Chg_Prof_Rfessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 23 | `EXTRA_CHG_PROF_RF_OVRR_FLAG` | Extra_Chg_Prof_Rf_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `EXTRA_CHG_PROF_PALL_CODE_REST` | Extra_Chg_Prof_Pall_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 25 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | Y |
| 28 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | Y |
| 30 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 31 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 32 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 33 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 34 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 35 | `EXTRA_CHG_PROF_LOC_TP_REST` | Extra_Chg_Prof_Loc_Tpessorial Rest | VARCHAR2 | 250 |  | Y |
| 36 | `EXTRA_CHG_PROF_LOAD_FLAG` | Extra_Chg_Prof_Loadessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_EXTRA_CHG_PROF_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EXTRA_CHG_PROF_DES` | Extra_Chg_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `EXTRA_CHG_PROF_STAT` | Extra_Chg_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_GEN_EXTRA_CHG`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `GEN_EXTRA_CHG_INB_OUTB_FLAG` | Gen_Extra_Chg_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `GEN_EXTRA_CHG_SEQ_NUM` | Gen_Extra_Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `GEN_EXTRA_CHG_CUST_CODE_REST` | Gen_Extra_Chg_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 8 | `GEN_EXTRA_CHG_CON_CODE_REST` | Gen_Extra_Chg_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 9 | `GEN_EXTRA_CHG_SHIP_CODE_REST` | Gen_Extra_Chg_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 10 | `GEN_EXTRA_CHG_CARR_CODE_REST` | Gen_Extra_Chg_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 11 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_GL_ACC`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 4 | `GL_ACC_DES` | Gl_Accessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `GL_ACC_STAT` | Gl_Accessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `GL_REF_NUM` | Gl_Refessorial Num | VARCHAR2 | 10 |  | Y |
| 7 | `GL_REF_NUM2` | Gl_Refessorial Num2 | VARCHAR2 | 10 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_GL_MODY`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `GL_MODY_DES` | Gl_Modyessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `GL_MODY_SUB_MODY` | Gl_Mody_Subessorial Mody | VARCHAR2 | 10 |  | Y |
| 6 | `GL_MODY_STAT` | Gl_Modyessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `ACC_REF_NUM1` | Acc_Refessorial Num1 | VARCHAR2 | 10 |  | Y |
| 8 | `ACC_REF_NUM2` | Acc_Refessorial Num2 | VARCHAR2 | 10 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INV_REG_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_REG_BKD_NUM` | Inv_Reg_Bkdessorial Num | NUMBER | 22 | 1 | N |
| 4 | `INV_REG_BKD_COL_NUM` | Inv_Reg_Bkd_Colessorial Num | NUMBER | 22 | 1 | N |
| 5 | `INV_REG_BKD_COL_DES1` | Inv_Reg_Bkd_Colessorial Des1 | VARCHAR2 | 10 |  | N |
| 6 | `INV_REG_BKD_COL_DES2` | Inv_Reg_Bkd_Colessorial Des2 | VARCHAR2 | 10 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INV_REG_DD`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_REG_BKD_NUM` | Inv_Reg_Bkdessorial Num | NUMBER | 22 | 1 | N |
| 4 | `INV_REG_BKD_COL_NUM` | Inv_Reg_Bkd_Colessorial Num | NUMBER | 22 | 1 | N |
| 5 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INV_REG_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_REG_BKD_NUM` | Inv_Reg_Bkdessorial Num | NUMBER | 22 | 1 | N |
| 4 | `INV_REG_BKD_DES` | Inv_Reg_Bkdessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INV_BKD_CODE` | Inv_Bkdessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INV_TP`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_TP_CODE` | Inv_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INV_TP_DES` | Inv_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INV_TP_STAT` | Inv_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROGR_BILL_PROF_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PROF_BILL_PROF_CODE` | Prof_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PROG_BILL_PROF_SEQ_NUM` | Prog_Bill_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `PROG_BILL_PROF_DAY_MODY` | Prog_Bill_Prof_Dayessorial Mody | NUMBER | 22 | 2 | N |
| 6 | `PROG_BILL_PROF_THOLD_PCENT_HOU` | Prog_Bill_Prof_Thold_Pcentessorial Hou | NUMBER | 22 | 5 | N |
| 7 | `PROG_BILL_PROF_AMT_TO_BILL` | Prog_Bill_Prof_Amt_Toessorial Bill | NUMBER | 22 | 10 | N |

## `M_PROGR_BILL_PROF_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PROG_BILL_PROF_CODE` | Prog_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PROG_BILL_PROF_DES` | Prog_Bill_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FLOW_PROS_CODE_APPR` | Flow_Pros_Codeessorial Appr | VARCHAR2 | 4 |  | Y |
| 5 | `FLOW_PROS_CODE_CLOSE` | Flow_Pros_Codeessorial Close | VARCHAR2 | 4 |  | Y |
| 6 | `PROG_BILL_PROF_STAT` | Prog_Bill_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_RATE_DES`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `RATE_DES` | Rateessorial Des | VARCHAR2 | 60 |  | N |
| 6 | `RATE_EXT_GRP` | Rate_Extessorial Grp | VARCHAR2 | 6 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RENW_SCH_PROF_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RENW_SCH_PROF_CODE` | Renw_Sch_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RENW_SCH_PROF_SEQ_NUM` | Renw_Sch_Prof_Seqessorial Num | NUMBER | 22 | 3 | N |
| 4 | `RENW_SCH_PROF_DATE_BASE_FLAG` | Renw_Sch_Prof_Date_Baseessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `RENW_SCH_PROF_INC_DAY` | Renw_Sch_Prof_Incessorial Day | NUMBER | 22 | 2 | Y |
| 6 | `RENW_SCH_PROF_REPT_FLAG` | Renw_Sch_Prof_Reptessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `RENW_SCH_PROF_CODE_EXTRA` | Renw_Sch_Prof_Codeessorial Extra | VARCHAR2 | 4 |  | Y |

## `M_RENW_SCH_PROF_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RENW_SCH_PROF_CODE` | Renw_Sch_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RENW_SCH_PROF_DES` | Renw_Sch_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `RENW_SCH_PROF_STAT` | Renw_Sch_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_RENW_STOR_PROF_D`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RENW_STOR_PROF_CODE` | Renw_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `RENW_STOR_PROF_PER_NUM` | Renw_Stor_Prof_Peressorial Num | NUMBER | 22 | 2 | N |
| 5 | `RENW_STOR_PROF_FRQ_CODE` | Renw_Stor_Prof_Frqessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `RENW_STOR_PROF_FRQ_NUM` | Renw_Stor_Prof_Frqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `RENW_STOR_PROF_RESET_DATE_FLAG` | Renw_Stor_Prof_Reset_Dateessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RENW_STOR_PROF_DD`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RENW_STOR_PROF_CODE` | Renw_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `RENW_STOR_PROF_PER_NUM` | Renw_Stor_Prof_Peressorial Num | NUMBER | 22 | 2 | N |
| 5 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RENW_STOR_PROF_DDD`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RENW_STOR_PROF_CODE` | Renw_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `RENW_STOR_PROF_PER_NUM` | Renw_Stor_Prof_Peressorial Num | NUMBER | 22 | 2 | N |
| 5 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 6 | `VALUE_INX_CODE` | Value_Inxessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RENW_STOR_PROF_H`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RENW_STOR_PROF_CODE` | Renw_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `RENW_STOR_PROF_DES` | Renw_Stor_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `RENW_STOR_PROF_STAT` | Renw_Stor_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_REVN_ANAL`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 4 | `REVN_ANAL_DES` | Revn_Analessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `REVN_ANAL_STAT` | Revn_Analessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `REVN_ANAL_REVN_FLAG` | Revn_Anal_Revnessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `REVN_GRP_CODE` | Revn_Grpessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_REVN_GRP`

- **Tipo:** Master
- **Categoria:** Billing
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `REVN_GRP_CODE` | Revn_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `REVN_GRP_DES` | Revn_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `REVN_GRP_STAT` | Revn_Grpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `OLD_C_RENW_D`

- **Tipo:** Misc
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 20 |  | N |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 20 |  | N |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 20 |  | N |
| 6 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 7 | `RENW_QTY` | Renwessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `RENW_WGT` | Renwessorial Wgt | NUMBER | 22 | 16 | N |
| 9 | `RENW_WGT_NET` | Renw_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 10 | `RENW_CUBE` | Renwessorial Cube | NUMBER | 22 | 16 | N |
| 11 | `RENW_RATE` | Renwessorial Rate | NUMBER | 22 | 9 | Y |
| 12 | `RENW_QUAL_QTY` | Renw_Qualessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `RENW_QUAL_WGT` | Renw_Qualessorial Wgt | NUMBER | 22 | 16 | Y |
| 14 | `RENW_QUAL_WGT_NET` | Renw_Qual_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 15 | `RENW_QUAL_CUBE` | Renw_Qualessorial Cube | NUMBER | 22 | 16 | Y |

## `OLD_C_RENW_H`

- **Tipo:** Misc
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `RENW_LEV1` | Renwessorial Lev1 | VARCHAR2 | 20 |  | N |
| 4 | `RENW_LEV2` | Renwessorial Lev2 | VARCHAR2 | 20 |  | N |
| 5 | `RENW_LEV3` | Renwessorial Lev3 | VARCHAR2 | 20 |  | N |
| 6 | `RENW_PER_NUM` | Renw_Peressorial Num | NUMBER | 22 | 4 | N |
| 7 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | N |
| 8 | `RENW_DATE_LAST` | Renw_Dateessorial Last | DATE | 7 |  | Y |
| 9 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | DATE | 7 |  | N |

## `S_BAT_AUTO`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | N |
| 2 | `BAT_AUTO_FLAG` | Bat_Autoessorial Flag | VARCHAR2 | 9 |  | N |

## `S_GEN_CHG_D1`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `GEN_EXTRA_CHG_INB_OUTB_FLAG` | Gen_Extra_Chg_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `GEN_EXTRA_CHG_SEQ_NUM` | Gen_Extra_Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `GEN_EXTRA_CHG_CUST_CODE_REST` | Gen_Extra_Chg_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 9 | `GEN_EXTRA_CHG_CON_CODE_REST` | Gen_Extra_Chg_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 10 | `GEN_EXTRA_CHG_SHIP_CODE_REST` | Gen_Extra_Chg_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 11 | `GEN_EXTRA_CHG_CARR_CODE_REST` | Gen_Extra_Chg_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 12 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 6 |  | Y |
| 13 | `CHG_COMPL_FLAG` | Chg_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `BAT_NUM` | Batch Number | NUMBER | 22 | 6 | Y |

## `S_GEN_CHG_D2`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STAT_NUM` | Statessorial Num | NUMBER | 22 | 3 | Y |
| 2 | `STAT_COMPL_FLAG` | Stat_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 6 | Y |

## `S_GEN_CHG_H`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `RUN_DATE` | Runessorial Date | DATE | 7 |  | Y |
| 3 | `RUN_STAT` | Runessorial Stat | NUMBER | 22 | 3 | Y |
| 4 | `BAT_NUM` | Batch Number | NUMBER | 22 | 6 | Y |

## `S_INV_PRT_PROF`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INV_PRT_PROF_CODE` | Inv_Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `INV_PRT_PROF_DES` | Inv_Prt_Professorial Des | VARCHAR2 | 40 |  | N |
| 4 | `INV_PRT_PROF_STAT` | Inv_Prt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `INV_PRT_PROF_NUM_INV` | Inv_Prt_Prof_Numessorial Inv | NUMBER | 22 | 1 | N |
| 6 | `INV_PRT_PROF_INV1_DES` | Inv_Prt_Prof_Inv1essorial Des | VARCHAR2 | 40 |  | N |
| 7 | `INV_PRT_PROF_INV2_DES` | Inv_Prt_Prof_Inv2essorial Des | VARCHAR2 | 40 |  | Y |
| 8 | `INV_PRT_PROF_INV3_DES` | Inv_Prt_Prof_Inv3essorial Des | VARCHAR2 | 40 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_INV_REG`

- **Tipo:** System Setup Related
- **Categoria:** Billing
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_REG_NUM` | Inv_Regessorial Num | NUMBER | 22 | 9 | N |
| 3 | `INV_REG_STAT` | Inv_Regessorial Stat | VARCHAR2 | 2 |  | N |
| 4 | `INV_REG_STAT_PREX` | Inv_Reg_Statessorial Prex | VARCHAR2 | 4 |  | Y |
| 5 | `INV_REG_STAT_NUM` | Inv_Reg_Statessorial Num | NUMBER | 22 | 6 | N |
| 6 | `INV_REG_STAT_CODE` | Inv_Reg_Statessorial Code | VARCHAR2 | 30 |  | Y |

## `T_CHG_TOT`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 15 | N |
| 3 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 4 | `CHG_TOT` | Charge Total | NUMBER | 22 | 16 | N |
| 5 | `CHG_MIN_FLAG` | Chg_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CHG_MAX_FLAG` | Chg_Maxessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CHG_FLAT_RATE_FLAG` | Chg_Flat_Rateessorial Flag | VARCHAR2 | 1 |  | N |

## `T_GEN_CHG_DOC`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 4 | `STAT_COMPL_FLAG` | Stat_Complessorial Flag | VARCHAR2 | 1 |  | Y |

## `T_GEN_EXTRA_CHG`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 6 | Y |
| 3 | `GEN_EXTRA_CHG_INB_OUTB_FLAG` | Gen_Extra_Chg_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `GEN_EXTRA_CHG_SEQ_NUM` | Gen_Extra_Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `GEN_EXTRA_CHG_CUST_CODE_REST` | Gen_Extra_Chg_Cust_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 8 | `GEN_EXTRA_CHG_CON_CODE_REST` | Gen_Extra_Chg_Con_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 9 | `GEN_EXTRA_CHG_SHIP_CODE_REST` | Gen_Extra_Chg_Ship_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 10 | `GEN_EXTRA_CHG_CARR_CODE_REST` | Gen_Extra_Chg_Carr_Codeessorial Rest | VARCHAR2 | 250 |  | Y |
| 11 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `VAL_INTERP_CODE` | Val_Interpessorial Code | VARCHAR2 | 4 |  | N |

## `T_INVT_ACCESS`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |

## `T_INV_D1`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 5 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 6 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |

## `T_INV_D2`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 5 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 6 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |

## `T_INV_D3`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 5 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 6 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 18 |  | N |
| 7 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 8 | `GL_ACC_CODE_ORG` | Gl_Acc_Codeessorial Org | VARCHAR2 | 18 |  | N |
| 9 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |

## `T_INV_H`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 4 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 5 | `INV_DATE` | Invessorial Date | DATE | 7 |  | N |
| 6 | `INV_REG_NUM` | Inv_Regessorial Num | NUMBER | 22 | 9 | Y |
| 7 | `INV_REG_DATE` | Inv_Regessorial Date | DATE | 7 |  | Y |
| 8 | `INV_TP` | Invessorial Tp | VARCHAR2 | 4 |  | N |
| 9 | `INV_STAT` | Invessorial Stat | VARCHAR2 | 1 |  | N |
| 10 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 11 | `BAT_TP_CODE` | Batch Type Code | VARCHAR2 | 4 |  | Y |
| 12 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 13 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 14 | `GL_ACC_CODE_AR` | Gl_Acc_Codeessorial Ar | VARCHAR2 | 18 |  | N |
| 15 | `GL_ACC_CODE_BANK` | Gl_Acc_Codeessorial Bank | VARCHAR2 | 18 |  | N |

## `T_REVN_ANAL`

- **Tipo:** Temporary
- **Categoria:** Billing
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_NAME` | Compessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | N |
| 5 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 6 | `REVN_ANAL_DES` | Revn_Analessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `REVN_DATE` | Revnessorial Date | DATE | 7 |  | N |
| 8 | `REVN_AMT` | Revnessorial Amt | NUMBER | 22 | 13 | N |
| 9 | `REVN_CONV_AMT` | Revn_Convessorial Amt | NUMBER | 22 | 13 | Y |

