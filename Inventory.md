# Tabelas — Inventory

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **26**.

## `C_TONN`

- **Tipo:** Transactional
- **Categoria:** Inventory
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TONN_REC_TP` | Tonn_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `TONN_DATE` | Tonnessorial Date | DATE | 7 |  | N |
| 4 | `TONN_TP` | Tonnessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 8 | `SOME_CODE` | Someessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 10 | `UNIT` | Unitessorial Unit | NUMBER | 22 | 9 | Y |
| 11 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 11 | Y |
| 12 | `SOME_DES` | Someessorial Des | VARCHAR2 | 30 |  | Y |
| 13 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |

## `E_INVT_LOCK`

- **Tipo:** Transactional
- **Categoria:** Inventory
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
| 8 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 9 | `LOCK_DATE` | Lockessorial Date | DATE | 7 |  | N |
| 10 | `INVT_LOCK_RFRL_FLAG` | Invt_Lock_Rfrlessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `INVT_LOCK_ALLOW_ALLOC_FLAG` | Invt_Lock_Allow_Allocessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_INVT_LOC_LOCK`

- **Tipo:** Transactional
- **Categoria:** Inventory
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `E_ITEM_LOCK`

- **Tipo:** Transactional
- **Categoria:** Inventory
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `H_IMM_INV_D1`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 38
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | Y |
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

## `H_IMM_INV_D2`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | Y |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 4 | `IMM_INV_LINE_NUM` | Imm_Inv_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `IMM_INV_REM_NUM` | Imm_Inv_Remessorial Num | NUMBER | 22 | 4 | N |
| 6 | `IMM_INV_REM_TEXT` | Imm_Inv_Remessorial Text | VARCHAR2 | 45 |  | Y |

## `H_IMM_INV_H`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | Y |
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

## `H_INVT`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 50
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 11 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 12 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 13 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 14 | `INVT_CLS_FLAG` | Invt_Clsessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 16 | `UNALLOC_WGT` | Unallocessorial Wgt | NUMBER | 22 | 16 | N |
| 17 | `UNALLOC_CUBE` | Unallocessorial Cube | NUMBER | 22 | 16 | N |
| 18 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 19 | `INTRANS_WGT` | Intransessorial Wgt | NUMBER | 22 | 16 | N |
| 20 | `INTRANS_CUBE` | Intransessorial Cube | NUMBER | 22 | 16 | N |
| 21 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 22 | `ON_RCPT_WGT` | On_Rcptessorial Wgt | NUMBER | 22 | 16 | N |
| 23 | `ON_RCPT_CUBE` | On_Rcptessorial Cube | NUMBER | 22 | 16 | N |
| 24 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 25 | `ON_ORD_WGT` | On_Ordessorial Wgt | NUMBER | 22 | 16 | N |
| 26 | `ON_ORD_CUBE` | On_Ordessorial Cube | NUMBER | 22 | 16 | N |
| 27 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 28 | `ON_HAND_WGT` | On_Handessorial Wgt | NUMBER | 22 | 16 | N |
| 29 | `ON_HAND_CUBE` | On_Handessorial Cube | NUMBER | 22 | 16 | N |
| 30 | `ON_HAND_WGT_NET` | On_Hand_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 31 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 32 | `HOLD_NON_SHIP_QTY` | Hold_Non_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 33 | `HOLD_NON_SHIP_WGT` | Hold_Non_Shipessorial Wgt | NUMBER | 22 | 16 | N |
| 34 | `HOLD_NON_SHIP_CUBE` | Hold_Non_Shipessorial Cube | NUMBER | 22 | 16 | N |
| 35 | `HOLD_SHIP_QTY` | Hold_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 36 | `HOLD_SHIP_WGT` | Hold_Shipessorial Wgt | NUMBER | 22 | 16 | N |
| 37 | `HOLD_SHIP_CUBE` | Hold_Shipessorial Cube | NUMBER | 22 | 16 | N |
| 38 | `HOLD_SHIP_ON_ORD_QTY` | Hold_Ship_On_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 39 | `HOLD_SHIP_ON_ORD_WGT` | Hold_Ship_On_Ordessorial Wgt | NUMBER | 22 | 16 | N |
| 40 | `HOLD_SHIP_ON_ORD_CUBE` | Hold_Ship_On_Ordessorial Cube | NUMBER | 22 | 16 | N |
| 41 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | DATE | 7 |  | Y |
| 42 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 43 | `INVT_CL_DATE` | Invt_Clessorial Date | DATE | 7 |  | Y |
| 44 | `INVT_CLS_DATE` | Invt_Clsessorial Date | DATE | 7 |  | Y |
| 45 | `INVT_CLR_WGT_FLAG` | Invt_Clr_Wgtessorial Flag | VARCHAR2 | 1 |  | Y |
| 46 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 47 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 48 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 49 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 50 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_INVT_HOLD_STAT`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 15
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
| 13 | `MOVE_TO_HIST_DATE` | Move_To_Histessorial Date | DATE | 7 |  | N |
| 14 | `REAS_CODE_EDI` | Reas_Codeessorial Edi | VARCHAR2 | 20 |  | Y |
| 15 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `H_INVT_STAT`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 15
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
| 13 | `MOVE_TO_HIST_DATE` | Move_To_Histessorial Date | DATE | 7 |  | N |
| 14 | `EDI_REF_NUM` | Edi_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 15 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |

## `H_MVT_D`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 13
- **Campos-chave prováveis:** MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 6 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 7 | `DOC_REM_LINE_NUM` | Doc_Rem_Lineessorial Num | NUMBER | 22 | 4 | N |
| 8 | `REM_TEXT` | Remessorial Text | VARCHAR2 | 45 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_MVT_H`

- **Tipo:** Historical
- **Categoria:** Inventory
- **Campos:** 60
- **Campos-chave prováveis:** MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `MVT_TRANS_DATE` | Mvt_Transessorial Date | DATE | 7 |  | N |
| 5 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 13 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 14 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 15 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 16 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 18 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 19 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 20 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 21 | `TRANS_UNIT` | Transessorial Unit | VARCHAR2 | 20 |  | N |
| 22 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 23 | `MVT_CNVC_QTY` | Mvt_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 24 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 25 | `TRANS_WGT` | Transessorial Wgt | NUMBER | 22 | 16 | N |
| 26 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |
| 27 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 28 | `MVT_WGT_NET` | Mvt_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 29 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 30 | `TRANS_CUBE` | Transessorial Cube | NUMBER | 22 | 16 | N |
| 31 | `MVT_CUBE` | Mvtessorial Cube | NUMBER | 22 | 16 | N |
| 32 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 33 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 34 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 35 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 36 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 37 | `EDI_AUDIT_NUM` | Edi_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 38 | `MVT_REF1` | Mvtessorial Ref1 | VARCHAR2 | 10 |  | N |
| 39 | `MVT_REF2` | Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 40 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 41 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 42 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 43 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 44 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 45 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 46 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 47 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 48 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 49 | `MON_END_PROS_FLAG` | Mon_End_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `MVT_REP_FLAG` | Mvt_Repessorial Flag | VARCHAR2 | 1 |  | Y |
| 51 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 52 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 53 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 54 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 55 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 56 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 57 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 58 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 59 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 60 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INVT_ATTR_PROF_D`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 5 | `INVT_ATTR_DES` | Invt_Attressorial Des | VARCHAR2 | 30 |  | N |
| 6 | `INVT_ATTR_REQ_FLAG` | Invt_Attr_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `INVT_ATTR_LEV_NUM` | Invt_Attr_Levessorial Num | NUMBER | 22 | 1 | N |
| 8 | `INVT_ATTR_ALLOW_MERGE_FLAG` | Invt_Attr_Allow_Mergeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `INVT_ATTR_ALLOC_FLAG` | Invt_Attr_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `INVT_ATTR_ALLOC_SORT_SEQ_NUM` | Invt_Attr_Alloc_Sort_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 11 | `INVT_ATTR_TP_CODE` | Invt_Attr_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `INVT_ATTR_DATE_FMT` | Invt_Attr_Dateessorial Fmt | VARCHAR2 | 9 |  | Y |
| 13 | `INVT_ATTR_LEN` | Invt_Attressorial Len | NUMBER | 22 | 6 | Y |
| 14 | `INVT_ATTR_ENTRY_LEV_NUM` | Invt_Attr_Entry_Levessorial Num | NUMBER | 22 | 1 | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 20 | `INVT_ATTR_RCPT_EXCL_FLAG` | Invt_Attr_Rcpt_Exclessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `INVT_ATTR_ALLOW_OVER_NAME` | Invt_Attr_Allow_Overessorial Name | VARCHAR2 | 1 |  | Y |

## `M_INVT_ATTR_PROF_DD`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 5 | `INVT_ATTR_SEQ_NUM` | Invt_Attr_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `INVT_ATTR_VAL_REST` | Invt_Attr_Valessorial Rest | VARCHAR2 | 40 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INVT_ATTR_PROF_H`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INVT_ATTR_PROF_DES` | Invt_Attr_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INVT_ATTR_PROF_STAT` | Invt_Attr_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INVT_INQ_FMT_D`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_INQ_TP_NUM` | Invt_Inq_Tpessorial Num | NUMBER | 22 | 2 | N |
| 2 | `INVT_INQ_FMT_CODE` | Invt_Inq_Fmtessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `INVT_INQ_FMT_COL_NUM` | Invt_Inq_Fmt_Colessorial Num | NUMBER | 22 | 2 | N |
| 4 | `INVT_INQ_COL_CODE` | Invt_Inq_Colessorial Code | VARCHAR2 | 62 |  | N |
| 5 | `INVT_INQ_FMT_COL_MASK` | Invt_Inq_Fmt_Colessorial Mask | VARCHAR2 | 20 |  | Y |
| 6 | `INVT_INQ_COL_HEAD` | Invt_Inq_Colessorial Head | VARCHAR2 | 60 |  | N |
| 7 | `INVT_INQ_COL_LEN` | Invt_Inq_Colessorial Len | NUMBER | 22 | 2 | N |

## `M_INVT_INQ_FMT_H`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_INQ_TP_NUM` | Invt_Inq_Tpessorial Num | NUMBER | 22 | 2 | N |
| 2 | `INVT_INQ_FMT_CODE` | Invt_Inq_Fmtessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `INVT_INQ_FMT_DES` | Invt_Inq_Fmtessorial Des | VARCHAR2 | 60 |  | N |
| 4 | `INVT_INQ_COL_OFFS` | Invt_Inq_Colessorial Offs | NUMBER | 22 | 1 | N |

## `M_INVT_TERMGY`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INVT_TERMGY_CODE` | Invt_Termgyessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INVT_TERMGY_DES` | Invt_Termgyessorial Des | VARCHAR2 | 20 |  | N |
| 5 | `INVT_TERMGY_STAT` | Invt_Termgyessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `INVT_TERMGY_RF` | Invt_Termgyessorial Rf | VARCHAR2 | 2 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_VELOCITY_ITEM_LOC_PROF`

- **Tipo:** Master
- **Categoria:** Inventory
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_VELOCITY_CODE` | Item_Velocityessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_INVT_ACCESS`

- **Tipo:** System Setup Related
- **Categoria:** Inventory
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `INVT_ACCESS_LAST_DATE` | Invt_Access_Lastessorial Date | DATE | 7 |  | Y |

## `S_INVT_INQ_COL`

- **Tipo:** System Setup Related
- **Categoria:** Inventory
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_INQ_TP_NUM` | Invt_Inq_Tpessorial Num | NUMBER | 22 | 2 | N |
| 2 | `INVT_INQ_COL_CODE` | Invt_Inq_Colessorial Code | VARCHAR2 | 62 |  | N |
| 3 | `INVT_INQ_COL_DES` | Invt_Inq_Colessorial Des | VARCHAR2 | 60 |  | N |
| 4 | `INVT_INQ_COL_MASK` | Invt_Inq_Colessorial Mask | VARCHAR2 | 20 |  | Y |
| 5 | `INVT_INQ_COL_LEN` | Invt_Inq_Colessorial Len | NUMBER | 22 | 2 | N |

## `S_INVT_INQ_D`

- **Tipo:** System Setup Related
- **Categoria:** Inventory
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_INQ_TP_NUM` | Invt_Inq_Tpessorial Num | NUMBER | 22 | 2 | N |
| 2 | `INVT_INQ_COL_DES1` | Invt_Inq_Colessorial Des1 | VARCHAR2 | 17 |  | N |
| 3 | `INVT_INQ_COL_DES2` | Invt_Inq_Colessorial Des2 | VARCHAR2 | 17 |  | Y |
| 4 | `INVT_INQ_COL_DES3` | Invt_Inq_Colessorial Des3 | VARCHAR2 | 17 |  | Y |
| 5 | `INVT_INQ_COL_DES4` | Invt_Inq_Colessorial Des4 | VARCHAR2 | 17 |  | Y |
| 6 | `INVT_INQ_COL_DES5` | Invt_Inq_Colessorial Des5 | VARCHAR2 | 17 |  | Y |
| 7 | `INVT_INQ_COL_DES6` | Invt_Inq_Colessorial Des6 | VARCHAR2 | 17 |  | Y |
| 8 | `INVT_INQ_COL_DES7` | Invt_Inq_Colessorial Des7 | VARCHAR2 | 17 |  | Y |
| 9 | `INVT_INQ_COL_DES8` | Invt_Inq_Colessorial Des8 | VARCHAR2 | 17 |  | Y |
| 10 | `INVT_INQ_COL_DES9` | Invt_Inq_Colessorial Des9 | VARCHAR2 | 17 |  | Y |
| 11 | `INVT_INQ_COL_DES10` | Invt_Inq_Colessorial Des10 | VARCHAR2 | 17 |  | Y |
| 12 | `INVT_INQ_COL_DES11` | Invt_Inq_Colessorial Des11 | VARCHAR2 | 17 |  | Y |
| 13 | `INVT_INQ_COL_DES12` | Invt_Inq_Colessorial Des12 | VARCHAR2 | 17 |  | Y |

## `S_INVT_INQ_H`

- **Tipo:** System Setup Related
- **Categoria:** Inventory
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_INQ_TP_NUM` | Invt_Inq_Tpessorial Num | NUMBER | 22 | 2 | N |
| 2 | `INVT_INQ_TP_DES` | Invt_Inq_Tpessorial Des | VARCHAR2 | 30 |  | N |

## `S_ITEM_WGT_TP`

- **Tipo:** System Setup Related
- **Categoria:** Inventory
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ITEM_WGT_TP_CODE` | Item_Wgt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ITEM_WGT_TP_DES` | Item_Wgt_Tpessorial Des | VARCHAR2 | 70 |  | N |
| 4 | `ITEM_WGT_TP_STAT` | Item_Wgt_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `T_C_INVT`

- **Tipo:** Temporary
- **Categoria:** Inventory
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 5 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 6 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |

## `T_OPEN_CLOSE_BAL`

- **Tipo:** Temporary
- **Categoria:** Inventory
- **Campos:** 39
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `OPEN_CLOSE_BAL_DATE` | Open_Close_Balessorial Date | DATE | 7 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `OPEN_UNIT` | Openessorial Unit | NUMBER | 22 | 16 | Y |
| 7 | `OPEN_WGT` | Openessorial Wgt | NUMBER | 22 | 20 | Y |
| 8 | `OPEN_WGT_NET` | Open_Wgtessorial Net | NUMBER | 22 | 20 | Y |
| 9 | `OPEN_CUBE` | Openessorial Cube | NUMBER | 22 | 20 | Y |
| 10 | `OPEN_CNVC` | Openessorial Cnvc | NUMBER | 22 | 9 | Y |
| 11 | `OPEN_PLT` | Openessorial Plt | NUMBER | 22 | 16 | Y |
| 12 | `INB_UNIT` | Inbessorial Unit | NUMBER | 22 | 16 | Y |
| 13 | `INB_WGT` | Inbessorial Wgt | NUMBER | 22 | 20 | Y |
| 14 | `INB_WGT_NET` | Inb_Wgtessorial Net | NUMBER | 22 | 20 | Y |
| 15 | `INB_CUBE` | Inbessorial Cube | NUMBER | 22 | 20 | Y |
| 16 | `INB_CNVC` | Inbessorial Cnvc | NUMBER | 22 | 9 | Y |
| 17 | `INB_PLT` | Inbessorial Plt | NUMBER | 22 | 16 | Y |
| 18 | `OUTB_UNIT` | Outbessorial Unit | NUMBER | 22 | 16 | Y |
| 19 | `OUTB_WGT` | Outbessorial Wgt | NUMBER | 22 | 20 | Y |
| 20 | `OUTB_WGT_NET` | Outb_Wgtessorial Net | NUMBER | 22 | 20 | Y |
| 21 | `OUTB_CUBE` | Outbessorial Cube | NUMBER | 22 | 20 | Y |
| 22 | `OUTB_CNVC` | Outbessorial Cnvc | NUMBER | 22 | 9 | Y |
| 23 | `OUTB_PLT` | Outbessorial Plt | NUMBER | 22 | 16 | Y |
| 24 | `ADJ_UNIT` | Adjessorial Unit | NUMBER | 22 | 16 | Y |
| 25 | `ADJ_WGT` | Adjessorial Wgt | NUMBER | 22 | 20 | Y |
| 26 | `ADJ_WGT_NET` | Adj_Wgtessorial Net | NUMBER | 22 | 20 | Y |
| 27 | `ADJ_CUBE` | Adjessorial Cube | NUMBER | 22 | 20 | Y |
| 28 | `ADJ_CNVC` | Adjessorial Cnvc | NUMBER | 22 | 9 | Y |
| 29 | `ADJ_PLT` | Adjessorial Plt | NUMBER | 22 | 16 | Y |
| 30 | `CLOSE_UNIT` | Closeessorial Unit | NUMBER | 22 | 16 | Y |
| 31 | `CLOSE_WGT` | Closeessorial Wgt | NUMBER | 22 | 20 | Y |
| 32 | `CLOSE_WGT_NET` | Close_Wgtessorial Net | NUMBER | 22 | 20 | Y |
| 33 | `CLOSE_CUBE` | Closeessorial Cube | NUMBER | 22 | 20 | Y |
| 34 | `CLOSE_CNVC` | Closeessorial Cnvc | NUMBER | 22 | 9 | Y |
| 35 | `CLOSE_PLT` | Closeessorial Plt | NUMBER | 22 | 16 | Y |
| 36 | `WHSE_LOC_BILL_TP_FLAG` | Warehouse Loc Bill Tp Flag | VARCHAR2 | 1 |  | Y |
| 37 | `WHSE_LOC_BILL_CODE` | Warehouse Loc Bill Code | VARCHAR2 | 4 |  | Y |
| 38 | `REVN_AMT` | Revnessorial Amt | NUMBER | 22 | 16 | Y |
| 39 | `UNBILL_AMT` | Unbillessorial Amt | NUMBER | 22 | 16 | Y |

