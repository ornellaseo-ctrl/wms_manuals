# Tabelas — Audit

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **3**.

## `C_ONLINE_AUDIT`

- **Tipo:** Transactional
- **Categoria:** Audit
- **Campos:** 74

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ONLINE_AUDIT_NUM` | Online_Auditessorial Num | NUMBER | 22 | 12 | N |
| 2 | `ONLINE_AUDIT_DATE` | Online_Auditessorial Date | DATE | 7 |  | N |
| 3 | `PA_FUNCTION` | Paessorial Function | VARCHAR2 | 10 |  | N |
| 4 | `PA_INVT_ACCESS` | Pa_Invtessorial Access | VARCHAR2 | 5 |  | Y |
| 5 | `PA_MVT_TRANS_TP` | Pa_Mvt_Transessorial Tp | VARCHAR2 | 2 |  | Y |
| 6 | `PA_COMP_CODE` | Pa_Compessorial Code | VARCHAR2 | 2 |  | Y |
| 7 | `PA_GLOBAL_COMP` | Pa_Globalessorial Comp | VARCHAR2 | 2 |  | Y |
| 8 | `PA_CUST_CODE` | Pa_Custessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `PA_INVT_LEV1` | Pa_Invtessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 10 | `PA_INVT_LEV2` | Pa_Invtessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 11 | `PA_INVT_LEV3` | Pa_Invtessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 12 | `PA_INVT_LEV4` | Pa_Invtessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 13 | `PA_INVT_LEV5` | Pa_Invtessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 14 | `PA_INVT_LEV2_DES` | Pa_Invt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 15 | `PA_INVT_LEV3_DES` | Pa_Invt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 16 | `PA_INVT_LEV4_DES` | Pa_Invt_Lev4essorial Des | VARCHAR2 | 40 |  | Y |
| 17 | `PA_INVT_LEV5_DES` | Pa_Invt_Lev5essorial Des | VARCHAR2 | 40 |  | Y |
| 18 | `PA_SKU_CODE_FACT` | Pa_Sku_Codeessorial Fact | VARCHAR2 | 20 |  | Y |
| 19 | `PA_INVT_QTY_BKD_FACT` | Pa_Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 20 | `PA_HOLD_CODE` | Pa_Holdessorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `PA_HOLD_SHIP_FLAG` | Pa_Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `PA_HOLD_RENW_FLAG` | Pa_Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `PA_WHSE_CODE` | Pa_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `PA_LOC_CODE` | Pa_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 25 | `PA_LOC_BILL_CODE` | Pa_Loc_Billessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `PA_LOC_RECD_DATE` | Pa_Loc_Recdessorial Date | DATE | 7 |  | Y |
| 27 | `PA_MVT_EFF_TRANS_DATE` | Pa_Mvt_Eff_Transessorial Date | DATE | 7 |  | Y |
| 28 | `PA_QTY_BKD_PROF_CODE` | Pa_Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `PA_INVT_EXPY_DATE` | Pa_Invt_Expyessorial Date | DATE | 7 |  | Y |
| 30 | `PA_TRANS_UNIT` | Pa_Transessorial Unit | VARCHAR2 | 20 |  | Y |
| 31 | `PA_MVT_UNIT` | Pa_Mvtessorial Unit | NUMBER | 22 | 9 | Y |
| 32 | `PA_CNVC_QTY` | Pa_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 33 | `PA_WGT_MEAS_CODE` | Pa_Wgt_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 34 | `PA_TRANS_WGT` | Pa_Transessorial Wgt | NUMBER | 22 | 16 | Y |
| 35 | `PA_TRANS_WGT_NET` | Pa_Trans_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 36 | `PA_LINEAR_MEAS_CODE` | Pa_Linear_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 37 | `PA_TRANS_CUBE` | Pa_Transessorial Cube | NUMBER | 22 | 16 | Y |
| 38 | `PA_CARR_CODE` | Pa_Carressorial Code | VARCHAR2 | 10 |  | Y |
| 39 | `PA_LOAD_TP_CODE` | Pa_Load_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `PA_MVT_REF1` | Pa_Mvtessorial Ref1 | VARCHAR2 | 10 |  | Y |
| 41 | `PA_MVT_REF2` | Pa_Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 42 | `PA_DOC_PREX` | Pa_Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 43 | `PA_DOC_SUFX` | Pa_Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 44 | `PA_DOC_NUM` | Pa_Docessorial Num | NUMBER | 22 | 9 | Y |
| 45 | `PA_DOC_LINE_NUM` | Pa_Doc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 46 | `PA_DOC_LOC_LINE_NUM` | Pa_Doc_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 47 | `PA_DOC_TP` | Pa_Docessorial Tp | VARCHAR2 | 10 |  | Y |
| 48 | `PA_DOC_REF1` | Pa_Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 49 | `PA_DOC_REF2` | Pa_Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 50 | `PA_DOC_REF3` | Pa_Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 51 | `PA_DOC_REF4` | Pa_Docessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 52 | `PA_OP_CODE` | Pa_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 53 | `PA_ORG_HOLD_CODE` | Pa_Org_Holdessorial Code | VARCHAR2 | 4 |  | Y |
| 54 | `PA_ORG_HOLD_SHIP_FLAG` | Pa_Org_Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 55 | `PA_ORG_WHSE_CODE` | Pa_Org_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 56 | `PA_ORG_LOC_CODE` | Pa_Org_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 57 | `PA_ORG_MVT_UNIT` | Pa_Org_Mvtessorial Unit | NUMBER | 22 | 9 | Y |
| 58 | `PA_ORG_WGT_MEAS_CODE` | Pa_Org_Wgt_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 59 | `PA_ORG_TRANS_WGT` | Pa_Org_Transessorial Wgt | NUMBER | 22 | 16 | Y |
| 60 | `PA_ORG_TRANS_WGT_NET` | Pa_Org_Trans_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 61 | `PA_ORG_LINEAR_MEAS_CODE` | Pa_Org_Linear_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 62 | `PA_ORG_TRANS_CUBE` | Pa_Org_Transessorial Cube | NUMBER | 22 | 16 | Y |
| 63 | `PA_INVT_CLS_DATE` | Pa_Invt_Clsessorial Date | DATE | 7 |  | Y |
| 64 | `PA_ORG_CNVC_QTY` | Pa_Org_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 65 | `PA_ADD_FIELD1` | Pa_Addessorial Field1 | VARCHAR2 | 20 |  | Y |
| 66 | `PA_ADD_FIELD2` | Pa_Addessorial Field2 | VARCHAR2 | 20 |  | Y |
| 67 | `PA_ADD_FIELD3` | Pa_Addessorial Field3 | VARCHAR2 | 20 |  | Y |
| 68 | `PA_ADD_FIELD4` | Pa_Addessorial Field4 | VARCHAR2 | 20 |  | Y |
| 69 | `PA_ADD_FIELD5` | Pa_Addessorial Field5 | VARCHAR2 | 20 |  | Y |
| 70 | `PA_ADD_FIELD6` | Pa_Addessorial Field6 | VARCHAR2 | 20 |  | Y |
| 71 | `PA_WHSE_CODE_STATIC` | Pa_Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 72 | `PA_LOC_CODE_STATIC` | Pa_Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 73 | `PA_WHSE_CODE_MOVE` | Pa_Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 74 | `PA_LOC_CODE_MOVE` | Pa_Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |

## `C_TER_AUD_LOG`

- **Tipo:** Transactional
- **Categoria:** Audit
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `AUD_LOG_MES_REF` | Aud_Log_Mesessorial Ref | VARCHAR2 | 20 |  | N |
| 4 | `TER_AUD_LOG_MES` | Ter_Aud_Logessorial Mes | VARCHAR2 | 2000 |  | Y |
| 5 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | Y |
| 7 | `EXE_CLASS_NAME` | Exe_Classessorial Name | VARCHAR2 | 2000 |  | Y |
| 8 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 9 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 10 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 11 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 18 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 19 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 20 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 21 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 23 | `LOCK_DATE` | Lockessorial Date | DATE | 7 |  | Y |

## `C_TRF_AUDIT`

- **Tipo:** Transactional
- **Categoria:** Audit
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_NUM_TEMP` | Rcpt_Numessorial Temp | NUMBER | 22 | 9 | Y |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 6 | Y |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 5 | Y |
| 7 | `TRF_PROS_FLAG` | Trf_Prosessorial Flag | NUMBER | 22 | 2 | Y |
| 8 | `INVT_COMP_FLAG` | Invt_Compessorial Flag | NUMBER | 22 | 2 | Y |

