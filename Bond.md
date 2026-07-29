# Tabelas — Bond

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **4**.

## `C_BOND_D1`

- **Tipo:** Transactional
- **Categoria:** Bond
- **Campos:** 17
- **Campos-chave prováveis:** HOLD_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | N |
| 3 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 15 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 16 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 17 | `BOND_INVT_LEV_DES` | Bond_Invt_Levessorial Des | VARCHAR2 | 40 |  | Y |

## `C_BOND_D2`

- **Tipo:** Transactional
- **Categoria:** Bond
- **Campos:** 49
- **Campos-chave prováveis:** MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | N |
| 3 | `MVT_TRANS_DATE` | Mvt_Transessorial Date | DATE | 7 |  | N |
| 4 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 13 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 15 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 17 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 18 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 19 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 20 | `TRANS_UNIT` | Transessorial Unit | VARCHAR2 | 20 |  | N |
| 21 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 22 | `MVT_CNVC_QTY` | Mvt_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 23 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 24 | `TRANS_WGT` | Transessorial Wgt | NUMBER | 22 | 16 | N |
| 25 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |
| 26 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 27 | `MVT_WGT_NET` | Mvt_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 28 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 29 | `TRANS_CUBE` | Transessorial Cube | NUMBER | 22 | 16 | N |
| 30 | `MVT_CUBE` | Mvtessorial Cube | NUMBER | 22 | 16 | N |
| 31 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 32 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 33 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 34 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 35 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 36 | `EDI_AUDIT_NUM` | Edi_Auditessorial Num | NUMBER | 22 | 6 | N |
| 37 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 38 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 39 | `MVT_REF1` | Mvtessorial Ref1 | VARCHAR2 | 12 |  | Y |
| 40 | `MVT_REF2` | Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 41 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 42 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 43 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 44 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 45 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 46 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 47 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 48 | `MON_END_PROS_FLAG` | Mon_End_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `MVT_REP_FLAG` | Mvt_Repessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_BOND_D3`

- **Tipo:** Transactional
- **Categoria:** Bond
- **Campos:** 19
- **Campos-chave prováveis:** HOLD_CODE, LOC_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | N |
| 3 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 13 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 14 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 16 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 17 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 18 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 19 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |

## `C_BOND_H`

- **Tipo:** Transactional
- **Categoria:** Bond
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE, CUST_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | N |
| 3 | `BOND_DES` | Bondessorial Des | VARCHAR2 | 30 |  | Y |
| 4 | `BOND_DATE` | Bondessorial Date | DATE | 7 |  | N |
| 5 | `BOND_ARRV_DATE` | Bond_Arrvessorial Date | DATE | 7 |  | N |
| 6 | `BOND_RCPT_DATE` | Bond_Rcptessorial Date | DATE | 7 |  | Y |
| 7 | `BOND_DUE_DATE1` | Bond_Dueessorial Date1 | DATE | 7 |  | Y |
| 8 | `BOND_DUE_DATE2` | Bond_Dueessorial Date2 | DATE | 7 |  | Y |
| 9 | `BOND_REL_DATE` | Bond_Relessorial Date | DATE | 7 |  | Y |
| 10 | `BOND_CL_DATE` | Bond_Clessorial Date | DATE | 7 |  | Y |
| 11 | `BOND_EXPY_DATE` | Bond_Expyessorial Date | DATE | 7 |  | Y |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 13 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 14 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 15 | `BOND_PROS_STAT` | Bond_Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 16 | `BOND_STAT` | Bondessorial Stat | VARCHAR2 | 1 |  | N |
| 17 | `BOND_EXT_REF_NUM` | Bond_Ext_Refessorial Num | VARCHAR2 | 20 |  | Y |

