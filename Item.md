# Tabelas — Item

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **48**.

## `C_ITEM_CHANGE_D`

- **Tipo:** Transactional
- **Categoria:** Item
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_QTY_BKD_LEV_NUM` | Item_Qty_Bkd_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `ITEM_QTY_BKD_QTY` | Item_Qty_Bkdessorial Qty | NUMBER | 22 | 4 | Y |
| 6 | `ITEM_QTY_BKD_MIN_QTY` | Item_Qty_Bkd_Minessorial Qty | NUMBER | 22 | 4 | Y |
| 7 | `ITEM_QTY_BKD_BASE_FLAG` | Item_Qty_Bkd_Baseessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ITEM_QTY_BKD_WHOLE_FLAG` | Item_Qty_Bkd_Wholeessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 10 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 11 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 12 | `ITEM_QTY_BKD_OVRR_CONFIG_FLAG` | Item_Qty_Bkd_Ovrr_Configessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 14 | `ITEM_QTY_BKD_HGT` | Item_Qty_Bkdessorial Hgt | NUMBER | 22 | 7 | Y |
| 15 | `ITEM_QTY_BKD_WID` | Item_Qty_Bkdessorial Wid | NUMBER | 22 | 7 | Y |
| 16 | `ITEM_QTY_BKD_LEN` | Item_Qty_Bkdessorial Len | NUMBER | 22 | 7 | Y |
| 17 | `ITEM_QTY_BKD_CUBE` | Item_Qty_Bkdessorial Cube | NUMBER | 22 | 9 | Y |
| 18 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 19 | `ITEM_QTY_BKD_WGT_GROSS` | Item_Qty_Bkd_Wgtessorial Gross | NUMBER | 22 | 14 | Y |
| 20 | `ITEM_QTY_BKD_WGT_NET` | Item_Qty_Bkd_Wgtessorial Net | NUMBER | 22 | 14 | Y |
| 21 | `ITEM_QTY_BKD_WGT_TARE` | Item_Qty_Bkd_Wgtessorial Tare | NUMBER | 22 | 14 | Y |
| 22 | `ITEM_QTY_BKD_WGT_TLR_PCENT` | Item_Qty_Bkd_Wgt_Tlressorial Pcent | NUMBER | 22 | 2 | Y |
| 23 | `VOL_MEAS_CODE` | Vol_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `ITEM_QTY_BKD_VOL` | Item_Qty_Bkdessorial Vol | NUMBER | 22 | 14 | Y |

## `C_ITEM_CHANGE_H`

- **Tipo:** Transactional
- **Categoria:** Item
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_CHANGE_ENTRY_DATE` | Item_Change_Entryessorial Date | DATE | 7 |  | N |
| 6 | `ITEM_CHANGE_PROS_FLAG` | Item_Change_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `ITEM_CHANGE_PROS_DATE` | Item_Change_Prosessorial Date | DATE | 7 |  | Y |
| 8 | `ERR_CODE` | Error Code | VARCHAR2 | 60 |  | Y |
| 9 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |

## `Column ID`

- **Tipo:** Misc
- **Categoria:** Item
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACC_ITEM_ACC_CODE` | Acc_Item_Accessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `ACC_ITEM_ACC_TP` | Acc_Item_Accessorial Tp | VARCHAR2 | 4 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 8 | `ALT_TP_CODE` | Alt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `ACC_ITEM_CODE` | Accessorial Item Code | VARCHAR2 | 20 |  | N |
| 10 | `ACC_ITEM_UPC` | Acc_Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 11 | `ACC_ITEM_DES1` | Acc_Itemessorial Des1 | VARCHAR2 | 40 |  | Y |
| 12 | `ACC_ITEM_DES2` | Acc_Itemessorial Des2 | VARCHAR2 | 60 |  | Y |
| 13 | `ACC_ITEM_QTY` | Acc_Itemessorial Qty | NUMBER | 22 | 6 | Y |
| 14 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_PROS_ITEM_CHANGE`

- **Tipo:** Transactional
- **Categoria:** Item
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `E_PROS_ITEM_ITSH_CHANGE`

- **Tipo:** Transactional
- **Categoria:** Item
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | N |

## `E_PROS_ITSH_EXPY_CHANGE`

- **Tipo:** Transactional
- **Categoria:** Item
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | Y |

## `M_ITEM_BILL_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_BILL_PROF_CODE` | Item_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_BILL_PROF_DES` | Item_Bill_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_BILL_PROF_STAT` | Item_Bill_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `INIT_STOR_PROF_CODE` | Init_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `RENW_STOR_PROF_CODE` | Renw_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 8 | `HAND_PROF_CODE` | Hand_Professorial Code | VARCHAR2 | 4 |  | N |
| 9 | `DATE_PROF_CODE` | Date_Professorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CHG_CODE_BILL_ENTI` | Chg_Code_Billessorial Enti | VARCHAR2 | 6 |  | Y |
| 11 | `CHG_CODE_RENW` | Chg_Codeessorial Renw | VARCHAR2 | 6 |  | Y |
| 12 | `CHG_CODE_STOR` | Chg_Codeessorial Stor | VARCHAR2 | 6 |  | Y |
| 13 | `CHG_CODE_HAND` | Chg_Codeessorial Hand | VARCHAR2 | 6 |  | Y |
| 14 | `ITEM_BILL_PROF_ORG_RATE_FLAG` | Item_Bill_Prof_Org_Rateessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `ITEM_BILL_PROF_RATE_QUAL_FLAG` | Item_Bill_Prof_Rate_Qualessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `ANNIV_NXT_INV_NUM_DAYS` | Anniv_Nxt_Inv_Numessorial Days | NUMBER | 22 | 3 | Y |
| 17 | `CREATE_RENW_INV_ZERO_INVT` | Create_Renw_Inv_Zeroessorial Invt | VARCHAR2 | 1 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 23 | `ITEM_BILL_PROF_INV_TP_CODE` | Item_Bill_Prof_Inv_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `ITEM_BILL_RENW_SUMM_CODE` | Item_Bill_Renw_Summessorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `ITEM_BILL_RENW_RES_QTY` | Item_Bill_Renw_Resessorial Qty | NUMBER | 22 | 16 | Y |
| 26 | `ITEM_BILL_INV_REP_CODE_FLAG` | Item_Bill_Inv_Rep_Codeessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 28 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 29 | `ITEM_BILL_PROF_IGN_LODE_FLAG` | Item_Bill_Prof_Ign_Lodeessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_ITEM_CARTZN_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_CARTZN_PROF_CODE` | Item_Cartzn_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_CARTZN_PROF_DES` | Item_Cartzn_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_CARTZN_PROF_STAT` | Item_Cartzn_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ITEM_CARTZN_PROF_TP` | Item_Cartzn_Professorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `ITEM_CARTZN_PROF_LEN_FACTOR` | Item_Cartzn_Prof_Lenessorial Factor | NUMBER | 22 | 4 | Y |
| 8 | `ITEM_CARTZN_PROF_WID_FACTOR` | Item_Cartzn_Prof_Widessorial Factor | NUMBER | 22 | 4 | Y |
| 9 | `ITEM_CARTZN_PROF_HGT_FACTOR` | Item_Cartzn_Prof_Hgtessorial Factor | NUMBER | 22 | 4 | Y |
| 10 | `ITEM_CARTZN_PROF_CUBE_FACTOR` | Item_Cartzn_Prof_Cubeessorial Factor | NUMBER | 22 | 4 | Y |
| 11 | `ITEM_CARTZN_PROF_WGT_FACTOR` | Item_Cartzn_Prof_Wgtessorial Factor | NUMBER | 22 | 4 | Y |
| 12 | `CASE_PICK_METH_INCL_FLAG` | Case_Pick_Meth_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_D1`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_QTY_BKD_LEV_NUM` | Item_Qty_Bkd_Levessorial Num | NUMBER | 22 | 1 | N |
| 6 | `ITEM_QTY_BKD_QTY` | Item_Qty_Bkdessorial Qty | NUMBER | 22 | 4 | Y |
| 7 | `ITEM_QTY_BKD_MIN_QTY` | Item_Qty_Bkd_Minessorial Qty | NUMBER | 22 | 4 | Y |
| 8 | `ITEM_QTY_BKD_BASE_FLAG` | Item_Qty_Bkd_Baseessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ITEM_QTY_BKD_WHOLE_FLAG` | Item_Qty_Bkd_Wholeessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 11 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 12 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 13 | `ITEM_QTY_BKD_OVRR_CONFIG_FLAG` | Item_Qty_Bkd_Ovrr_Configessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 15 | `ITEM_QTY_BKD_HGT` | Item_Qty_Bkdessorial Hgt | NUMBER | 22 | 7 | Y |
| 16 | `ITEM_QTY_BKD_WID` | Item_Qty_Bkdessorial Wid | NUMBER | 22 | 7 | Y |
| 17 | `ITEM_QTY_BKD_LEN` | Item_Qty_Bkdessorial Len | NUMBER | 22 | 7 | Y |
| 18 | `ITEM_QTY_BKD_CUBE` | Item_Qty_Bkdessorial Cube | NUMBER | 22 | 9 | Y |
| 19 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 20 | `ITEM_QTY_BKD_WGT_GROSS` | Item_Qty_Bkd_Wgtessorial Gross | NUMBER | 22 | 14 | Y |
| 21 | `ITEM_QTY_BKD_WGT_NET` | Item_Qty_Bkd_Wgtessorial Net | NUMBER | 22 | 14 | Y |
| 22 | `ITEM_QTY_BKD_WGT_TARE` | Item_Qty_Bkd_Wgtessorial Tare | NUMBER | 22 | 14 | Y |
| 23 | `ITEM_QTY_BKD_WGT_TLR_PCENT` | Item_Qty_Bkd_Wgt_Tlressorial Pcent | NUMBER | 22 | 2 | Y |
| 24 | `VOL_MEAS_CODE` | Vol_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `ITEM_QTY_BKD_VOL` | Item_Qty_Bkdessorial Vol | NUMBER | 22 | 14 | Y |
| 26 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 27 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 29 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 30 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 31 | `UNIT_QTY_CUBE` | Unit_Qtyessorial Cube | NUMBER | 22 | 10 | Y |

## `M_ITEM_D2`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_SUB_SEQ_NUM` | Item_Sub_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | N |
| 7 | `ITEM_SUB_TP_FLAG` | Item_Sub_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ITEM_SUB_CHAIN_FLAG` | Item_Sub_Chainessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_D3`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_D4`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE_COMPN` | Item_Codeessorial Compn | VARCHAR2 | 20 |  | N |
| 7 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | NUMBER | 22 | 16 | Y |
| 8 | `ITEM_COMPN_ENT_QTY` | Item_Compn_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 9 | `ITEM_COMPN_SEQ_NUM` | Item_Compn_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 10 | `ITEM_COMPN_WGT` | Item_Compnessorial Wgt | NUMBER | 22 | 16 | Y |
| 11 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 12 | `ITEM_COMPN_PER_KIT_ENT_QTY` | Item_Compn_Per_Kit_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 13 | `ITEM_COMPN_PER_KIT_QTY` | Item_Compn_Per_Kitessorial Qty | NUMBER | 22 | 9 | Y |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 83
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_CODE_SEQ` | Item_Codeessorial Seq | VARCHAR2 | 41 |  | Y |
| 6 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | N |
| 7 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 8 | `ITEM_STAT` | Itemessorial Stat | VARCHAR2 | 1 |  | N |
| 9 | `GENR_INFO_PROF_CODE` | Genr_Info_Professorial Code | VARCHAR2 | 4 |  | N |
| 10 | `ITEM_BILL_PROF_CODE1` | Item_Bill_Professorial Code1 | VARCHAR2 | 4 |  | N |
| 11 | `ITEM_BILL_PROF_CODE2` | Item_Bill_Professorial Code2 | VARCHAR2 | 4 |  | Y |
| 12 | `ITEM_BILL_PROF_CODE3` | Item_Bill_Professorial Code3 | VARCHAR2 | 4 |  | Y |
| 13 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | N |
| 14 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | N |
| 15 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 17 | `ITEM_HOLD_PROF_CODE` | Item_Hold_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_WGT_TP_CODE` | Item_Wgt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 19 | `ITEM_VALUE` | Itemessorial Value | NUMBER | 22 | 12 | Y |
| 20 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 6 |  | Y |
| 21 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 22 | `ITEM_CRS_DOCK_FLAG` | Item_Crs_Dockessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `ITEM_VAR_QTY_BKD_FLAG` | Item_Var_Qty_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `ITEM_TARE_PROF_CODE` | Item_Tare_Professorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | N |
| 27 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | N |
| 28 | `ITEM_OPEN_ENTI_NUM_DAY` | Item_Open_Enti_Numessorial Day | NUMBER | 22 | 2 | N |
| 29 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | N |
| 30 | `ITEM_UPC` | Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 31 | `ITEM_DISC_FLAG` | Item_Discessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `ITEM_DISC_PROF_CODE` | Item_Disc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 33 | `SCAN_PARAM_CODE` | Scan_Paramessorial Code | VARCHAR2 | 4 |  | Y |
| 34 | `ITEM_KIT_FLAG` | Item_Kitessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `ITEM_KIT_TP_FLAG` | Item_Kit_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `ITEM_ALLOW_ENTRY_LEV_NUM` | Item_Allow_Entry_Levessorial Num | NUMBER | 22 | 1 | N |
| 37 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 38 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 39 | `WGT_TLR_PROF_CODE` | Wgt_Tlr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 41 | `ITEM_LAB_STD_MODY_NUM` | Item_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 42 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 43 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 44 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 45 | `PUT_PROF_CODE` | Put_Professorial Code | VARCHAR2 | 4 |  | Y |
| 46 | `ITEM_VAL_PROF_CODE` | Item_Val_Professorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `ITEM_CODE_MAST` | Item_Codeessorial Mast | VARCHAR2 | 20 |  | Y |
| 48 | `ITEM_CODE_MAST_FLAG` | Item_Code_Mastessorial Flag | VARCHAR2 | 1 |  | N |
| 49 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 50 | `ITEM_VAR_QTY_BKD_RENW_FLAG` | Item_Var_Qty_Bkd_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 51 | `ITEM_ALLOW_MIX_PLT_FLAG` | Item_Allow_Mix_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 52 | `ITEM_HAZ_FLAG` | Item_Hazessorial Flag | VARCHAR2 | 1 |  | N |
| 53 | `ITEM_ALLOW_BAND_FLAG` | Item_Allow_Bandessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `ITEM_BAND_SKU_CLASS_NUM` | Item_Band_Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 55 | `ITEM_BAND_MAX_QTY` | Item_Band_Maxessorial Qty | NUMBER | 22 | 9 | Y |
| 56 | `ITEM_PLT_BUILD_REST_CODE` | Item_Plt_Build_Restessorial Code | VARCHAR2 | 4 |  | Y |
| 57 | `ITEM_RF_PROF_CODE` | Item_Rf_Professorial Code | VARCHAR2 | 4 |  | Y |
| 58 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 59 | `ITEM_MOD_DATE` | Item_Modessorial Date | DATE | 7 |  | Y |
| 60 | `ITEM_CARTZN_PROF_CODE` | Item_Cartzn_Professorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `ITEM_DES_EXTN` | Item_Desessorial Extn | VARCHAR2 | 250 |  | Y |
| 62 | `ITEM_OVPI_IGNORE_CON_FLAG` | Item_Ovpi_Ignore_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 64 | `ITEM_OVERSIZE_FLAG` | Item_Oversizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 65 | `RFCH_SCAN_PROF_CODE` | Rfch_Scan_Professorial Code | VARCHAR2 | 4 |  | Y |
| 66 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 67 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 68 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 69 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 70 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 71 | `ITEM_STACK_TP_CODE` | Item_Stack_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 72 | `ITEM_STACK_STOR_QTY` | Item_Stack_Storessorial Qty | NUMBER | 22 | 4 | Y |
| 73 | `ITEM_REPI_MERGE_LOC_FLAG` | Item_Repi_Merge_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 74 | `ITEM_ALLOC_PLT_BY_ENTITY_FLAG` | Item_Alloc_Plt_By_Entityessorial Flag | VARCHAR2 | 1 |  | Y |
| 75 | `MIN_MAX_DATE_SUPERVISOR_OVER` | Min_Max_Date_Supervisoressorial Over | VARCHAR2 | 1 |  | Y |
| 76 | `ITEM_MIN_EXPY_DAY` | Item_Min_Expyessorial Day | NUMBER | 22 | 4 | Y |
| 77 | `ITEM_MAX_EXPY_DAY` | Item_Max_Expyessorial Day | NUMBER | 22 | 4 | Y |
| 78 | `ITEM_MAX_PROD_DAY` | Item_Max_Prodessorial Day | NUMBER | 22 | 4 | Y |
| 79 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 80 | `ITEM_PALL_TP_HGT` | Item_Pall_Tpessorial Hgt | NUMBER | 22 | 7 | Y |
| 81 | `ITEM_SPACER_HGT` | Item_Spaceressorial Hgt | NUMBER | 22 | 7 | Y |
| 82 | `ITEM_VELOCITY_CODE` | Item_Velocityessorial Code | VARCHAR2 | 4 |  | Y |
| 83 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |

## `M_ITEM_HAZ_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 72
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `TRSPT_MODE_TP` | Trspt_Modeessorial Tp | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_HAZ_INNER_PACK_TP_CODE` | Item_Haz_Inner_Pack_Tpessorial Code | VARCHAR2 | 5 |  | Y |
| 8 | `ITEM_HAZ_INNER_PACK_TP_DES` | Item_Haz_Inner_Pack_Tpessorial Des | VARCHAR2 | 255 |  | Y |
| 9 | `ITEM_HAZ_INNER_PACK_QTY` | Item_Haz_Inner_Packessorial Qty | NUMBER | 22 | 5 | Y |
| 10 | `ITEM_HAZ_SHIP_NAME` | Item_Haz_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 11 | `ITEM_HAZ_NOS` | Item_Hazessorial Nos | VARCHAR2 | 4 |  | Y |
| 12 | `ITEM_HAZ_TECH_NAME` | Item_Haz_Techessorial Name | VARCHAR2 | 255 |  | Y |
| 13 | `ITEM_HAZ_MULTIPLIER` | Item_Hazessorial Multiplier | NUMBER | 22 | 5 | Y |
| 14 | `ITEM_HAZ_WGT_NET` | Item_Haz_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 15 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `ITEM_HAZ_QTY` | Item_Hazessorial Qty | NUMBER | 22 | 16 | Y |
| 17 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_HAZ_FLASHPOINT` | Item_Hazessorial Flashpoint | VARCHAR2 | 6 |  | Y |
| 19 | `ITEM_HAZ_ADR_UN_ID` | Item_Haz_Adr_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 20 | `ITEM_HAZ_ADR_PRIMARY_CLASS` | Item_Haz_Adr_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 21 | `ITEM_HAZ_ADR_VALUE` | Item_Haz_Adressorial Value | VARCHAR2 | 3 |  | Y |
| 22 | `ITEM_HAZ_ADR_SUB_RISK_CLASS` | Item_Haz_Adr_Sub_Riskessorial Class | VARCHAR2 | 3 |  | Y |
| 23 | `ITEM_HAZ_ADR_PRIMARY_LABEL` | Item_Haz_Adr_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 24 | `ITEM_HAZ_ADR_SECD_LABEL` | Item_Haz_Adr_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 25 | `ITEM_HAZ_ADR_TERTIARY_LABEL` | Item_Haz_Adr_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 26 | `ITEM_HAZ_ADR_PACK_GRP_CODE` | Item_Haz_Adr_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 27 | `ITEM_HAZ_ADR_SPC_REQ_CODE` | Item_Haz_Adr_Spc_Reqessorial Code | VARCHAR2 | 5 |  | Y |
| 28 | `ITEM_HAZ_IMO_UN_ID` | Item_Haz_Imo_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 29 | `ITEM_HAZ_IMO_PACK_GRP_CODE` | Item_Haz_Imo_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 30 | `ITEM_HAZ_IMO_PRIMARY_CLASS` | Item_Haz_Imo_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 31 | `ITEM_HAZ_IMO_SECD_CLASS` | Item_Haz_Imo_Secdessorial Class | VARCHAR2 | 3 |  | Y |
| 32 | `ITEM_HAZ_IMO_SHIP_NAME` | Item_Haz_Imo_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 33 | `ITEM_HAZ_IMDG_LIMIT_QTY_FLAG` | Item_Haz_Imdg_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `ITEM_HAZ_IMDG_PRIMARY_LABEL` | Item_Haz_Imdg_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 35 | `ITEM_HAZ_IMDG_SECD_LABEL` | Item_Haz_Imdg_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 36 | `ITEM_HAZ_IMDG_TERTIARY_LABEL` | Item_Haz_Imdg_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 37 | `ITEM_HAZ_MARINE_POLLUT_FLAG` | Item_Haz_Marine_Pollutessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `ITEM_HAZ_IMDG_CERTIFICATE` | Item_Haz_Imdgessorial Certificate | VARCHAR2 | 20 |  | Y |
| 39 | `ITEM_HAZ_IATA_UN_ID` | Item_Haz_Iata_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 40 | `ITEM_HAZ_IATA_PRIMARY_CLASS` | Item_Haz_Iata_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 41 | `ITEM_HAZ_IATA_PACK_GRP_CODE` | Item_Haz_Iata_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 42 | `ITEM_HAZ_IATA_SUB_RISK_CLASS` | Item_Haz_Iata_Sub_Riskessorial Class | VARCHAR2 | 3 |  | Y |
| 43 | `ITEM_HAZ_AIR_SHIP_NAME_1` | Item_Haz_Air_Ship_Nameessorial 1 | VARCHAR2 | 60 |  | Y |
| 44 | `ITEM_HAZ_AIR_SHIP_NAME_2` | Item_Haz_Air_Ship_Nameessorial 2 | VARCHAR2 | 60 |  | Y |
| 45 | `ITEM_HAZ_IATA_PRIMARY_LABEL` | Item_Haz_Iata_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 46 | `ITEM_HAZ_IATA_SECD_LABEL` | Item_Haz_Iata_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 47 | `ITEM_HAZ_IATA_TERTIARY_LABEL` | Item_Haz_Iata_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 48 | `ITEM_HAZ_IMOD_EMS` | Item_Haz_Imodessorial Ems | VARCHAR2 | 6 |  | Y |
| 49 | `ITEM_HAZ_EXT_REF_CODE` | Item_Haz_Ext_Refessorial Code | VARCHAR2 | 20 |  | Y |
| 50 | `ITEM_HAZ_OFC_CODE` | Item_Haz_Ofcessorial Code | VARCHAR2 | 5 |  | Y |
| 51 | `ITEM_HAZ_MAT_WORKCENTER_FLAG` | Item_Haz_Mat_Workcenteressorial Flag | VARCHAR2 | 1 |  | Y |
| 52 | `ITEM_HAZ_DOT_UN_ID` | Item_Haz_Dot_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 53 | `ITEM_HAZ_DOT_ID` | Item_Haz_Dotessorial Id | VARCHAR2 | 6 |  | Y |
| 54 | `ITEM_HAZ_DOT_PRIMARY_CLASS` | Item_Haz_Dot_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 55 | `ITEM_HAZ_DOT_SECD_CLASS` | Item_Haz_Dot_Secdessorial Class | VARCHAR2 | 3 |  | Y |
| 56 | `ITEM_HAZ_DOT_TERTIARY_CLASS` | Item_Haz_Dot_Tertiaryessorial Class | VARCHAR2 | 3 |  | Y |
| 57 | `ITEM_HAZ_DOT_PRIMARY_LABEL` | Item_Haz_Dot_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 58 | `ITEM_HAZ_DOT_SECD_LABEL` | Item_Haz_Dot_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 59 | `ITEM_HAZ_DOT_TERTIARY_LABEL` | Item_Haz_Dot_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 60 | `ITEM_HAZ_DOT_SHIP_NAME` | Item_Haz_Dot_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 61 | `ITEM_HAZ_DOT_PACK_GRP_CODE` | Item_Haz_Dot_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 62 | `ITEM_HAZ_DOT_LIMIT_QTY_FLAG` | Item_Haz_Dot_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `ITEM_HAZ_DOT_EXEMPTION_ID` | Item_Haz_Dot_Exemptionessorial Id | VARCHAR2 | 5 |  | Y |
| 64 | `ITEM_HAZ_MARINE_POLLUT_LABEL` | Item_Haz_Marine_Pollutessorial Label | VARCHAR2 | 2 |  | Y |
| 65 | `ITEM_HAZ_IMDG_SEGREG_GRP` | Item_Haz_Imdg_Segregessorial Grp | VARCHAR2 | 4 |  | Y |
| 66 | `ITEM_HAZ_IMDG_SEGREG_GRP_DES` | Item_Haz_Imdg_Segreg_Grpessorial Des | VARCHAR2 | 40 |  | Y |
| 67 | `ITEM_HAZ_IMDG_PHASES_ACID` | Item_Haz_Imdg_Phasesessorial Acid | VARCHAR2 | 2 |  | Y |
| 68 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 69 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 70 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 71 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 72 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_HAZ_DD`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_HAZ_ADR_SHIP_NAME` | Item_Haz_Adr_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 8 | `ITEM_HAZ_TEXT_1` | Item_Haz_Textessorial 1 | VARCHAR2 | 255 |  | Y |
| 9 | `ITEM_HAZ_TEXT_2` | Item_Haz_Textessorial 2 | VARCHAR2 | 255 |  | Y |
| 10 | `ITEM_HAZ_TEXT_3` | Item_Haz_Textessorial 3 | VARCHAR2 | 255 |  | Y |
| 11 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_HAZ_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_HAZ_MULTIPART_FLAG` | Item_Haz_Multipartessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `ITEM_HAZ_PACK_TP_CODE` | Item_Haz_Pack_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `ITEM_HAZ_PACK_TP_DES` | Item_Haz_Pack_Tpessorial Des | VARCHAR2 | 255 |  | Y |
| 8 | `ITEM_HAZ_IMO_EMS_NUM` | Item_Haz_Imo_Emsessorial Num | VARCHAR2 | 6 |  | Y |
| 9 | `ITEM_HAZ_IMO_MFAG_NUM` | Item_Haz_Imo_Mfagessorial Num | NUMBER | 22 | 3 | Y |
| 10 | `ITEM_HAZ_FLASHPOINT` | Item_Hazessorial Flashpoint | VARCHAR2 | 6 |  | Y |
| 11 | `ITEM_HAZ_ADR_LIMIT_QTY_FLAG` | Item_Haz_Adr_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `ITEM_HAZ_DOT_LIMIT_QTY_FLAG` | Item_Haz_Dot_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `ITEM_HAZ_RQ_LIMIT_QTY_FLAG` | Item_Haz_Rq_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `ITEM_HAZ_IATA_PACK_INS` | Item_Haz_Iata_Packessorial Ins | VARCHAR2 | 5 |  | Y |
| 15 | `ITEM_HAZ_LABEL_CODE_1` | Item_Haz_Label_Codeessorial 1 | VARCHAR2 | 2 |  | Y |
| 16 | `ITEM_HAZ_LABEL_CODE_2` | Item_Haz_Label_Codeessorial 2 | VARCHAR2 | 2 |  | Y |
| 17 | `ITEM_HAZ_ACID_FLAG` | Item_Haz_Acidessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `ITEM_HAZ_AIR_STAT_CODE` | Item_Haz_Air_Statessorial Code | VARCHAR2 | 1 |  | Y |
| 19 | `ITEM_HAZ_OVER_LABEL_CODE` | Item_Haz_Over_Labelessorial Code | VARCHAR2 | 1 |  | Y |
| 20 | `ITEM_HAZ_TREM_CARD_NUM` | Item_Haz_Trem_Cardessorial Num | NUMBER | 22 | 9 | Y |
| 21 | `ITEM_HAZ_ACCESSIBLE_FLAG` | Item_Haz_Accessibleessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 27 | `ITEM_HAZ_CPG_FLAG` | Item_Haz_Cpgessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `ITEM_HAZ_PHYS_MATTER_TP` | Item_Haz_Phys_Matteressorial Tp | VARCHAR2 | 4 |  | Y |

## `M_ITEM_HAZ_REST_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_HAZ_CLASS` | Item_Hazessorial Class | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_HAZ_REST_LINE_NUM` | Item_Haz_Rest_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ITEM_HAZ_CLASS_REST` | Item_Haz_Classessorial Rest | VARCHAR2 | 4 |  | N |
| 6 | `TRSPT_MODE_TP` | Trspt_Modeessorial Tp | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_HAZ_REST_TP` | Item_Haz_Restessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_HAZ_REST_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_HAZ_CLASS` | Item_Hazessorial Class | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_HAZ_TEXT` | Item_Hazessorial Text | VARCHAR2 | 30 |  | Y |
| 5 | `ITEM_HAZ_STAT` | Item_Hazessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_HIER_PROF_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ITEM_HIER_PROF_CODE` | Item_Hier_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ITEM_HIER_PROF_LEV_NUM` | Item_Hier_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 4 | `ITEM_HIER_PROF_LEV_DES` | Item_Hier_Prof_Levessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_HIER_PROF_LEV_SHORT_DES` | Item_Hier_Prof_Lev_Shortessorial Des | VARCHAR2 | 4 |  | N |
| 6 | `ITEM_HIER_PROF_LEV_LEN` | Item_Hier_Prof_Levessorial Len | NUMBER | 22 | 2 | N |
| 7 | `ITEM_HIER_PROF_LEV_VAL_CHAR` | Item_Hier_Prof_Lev_Valessorial Char | VARCHAR2 | 50 |  | Y |

## `M_ITEM_HIER_PROF_DD`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ITEM_HIER_PROF_CODE` | Item_Hier_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ITEM_HIER_PROF_LEV_NUM` | Item_Hier_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 4 | `ITEM_HIER_PROF_CHAR_POS` | Item_Hier_Prof_Charessorial Pos | NUMBER | 22 | 2 | N |
| 5 | `ITEM_HIER_PROF_POS_VAL_CHAR` | Item_Hier_Prof_Pos_Valessorial Char | VARCHAR2 | 50 |  | N |

## `M_ITEM_HIER_PROF_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ITEM_HIER_PROF_CODE` | Item_Hier_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ITEM_HIER_PROF_DES` | Item_Hier_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `ITEM_HIER_PROF_STAT` | Item_Hier_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `ITEM_HIER_PROF_MAX_LEV` | Item_Hier_Prof_Maxessorial Lev | NUMBER | 22 | 1 | N |
| 6 | `ITEM_HIER_PROF_SEP_VAL` | Item_Hier_Prof_Sepessorial Val | VARCHAR2 | 1 |  | Y |

## `M_ITEM_HIER_VAL`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ITEM_HIER_VAL_SEQ_NUM` | Item_Hier_Val_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_HIER_PROF_CODE` | Item_Hier_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_HIER_PROF_LEV_NUM` | Item_Hier_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 6 | `ITEM_HIER_VAL_CODE_LEV1` | Item_Hier_Val_Codeessorial Lev1 | VARCHAR2 | 40 |  | N |
| 7 | `ITEM_HIER_VAL_CODE_LEV2` | Item_Hier_Val_Codeessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 8 | `ITEM_HIER_VAL_CODE_LEV3` | Item_Hier_Val_Codeessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 9 | `ITEM_HIER_VAL_CODE_LEV4` | Item_Hier_Val_Codeessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 10 | `ITEM_HIER_VAL_CODE_LEV5` | Item_Hier_Val_Codeessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 11 | `ITEM_HIER_VAL_CODE_LEV6` | Item_Hier_Val_Codeessorial Lev6 | VARCHAR2 | 40 |  | Y |
| 12 | `ITEM_HIER_VAL_CODE_LEV7` | Item_Hier_Val_Codeessorial Lev7 | VARCHAR2 | 40 |  | Y |
| 13 | `ITEM_HIER_VAL_CODE_LEV8` | Item_Hier_Val_Codeessorial Lev8 | VARCHAR2 | 40 |  | Y |
| 14 | `ITEM_HIER_VAL_CODE_LEV9` | Item_Hier_Val_Codeessorial Lev9 | VARCHAR2 | 40 |  | Y |
| 15 | `ITEM_HIER_VAL_DES` | Item_Hier_Valessorial Des | VARCHAR2 | 30 |  | N |
| 16 | `ITEM_HIER_VAL_STAT` | Item_Hier_Valessorial Stat | VARCHAR2 | 1 |  | N |

## `M_ITEM_HOLD_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_HOLD_PROF_CODE` | Item_Hold_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_HOLD_PROF_DES` | Item_Hold_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_HOLD_PROF_STAT` | Item_Hold_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `HOLD_CODE_INB` | Hold_Codeessorial Inb | VARCHAR2 | 4 |  | Y |
| 7 | `HOLD_CODE_OUTB` | Hold_Codeessorial Outb | VARCHAR2 | 4 |  | Y |
| 8 | `HOLD_SHIP_SEQ_PROF_CODE` | Hold_Ship_Seq_Professorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `ALLOW_CORE_RF_HOLD_OVRR_FLAG` | Allow_Core_Rf_Hold_Ovrressorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 15 | `TRANS_RCPT_HOLD_EXCLUDE_FLAG` | Trans_Rcpt_Hold_Excludeessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_ITEM_HOLD_PROF_LOC_TP`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_HOLD_PROF_CODE` | Item_Hold_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_CODE_INB` | Hold_Codeessorial Inb | VARCHAR2 | 4 |  | N |
| 5 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_INCUB_HOLD`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_INCUB_HOLD_CODE` | Item_Incub_Holdessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ITEM_INCUB_HOLD_NUM_DAYS` | Item_Incub_Hold_Numessorial Days | NUMBER | 22 | 6 | N |
| 7 | `ITEM_INCUB_HOLD_DATE_FORUL` | Item_Incub_Hold_Dateessorial Forul | VARCHAR2 | 255 |  | N |
| 8 | `ITEM_INCUB_HOLD_DATE_FORUL_FMT` | Item_Incub_Hold_Date_Forulessorial Fmt | VARCHAR2 | 20 |  | N |
| 9 | `ITEM_INCUB_HOLD_STAT` | Item_Incub_Holdessorial Stat | VARCHAR2 | 1 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 15 | `INCUB_HOLD_PROF_CODE` | Incub_Hold_Professorial Code | VARCHAR2 | 4 |  | Y |

## `M_ITEM_ISOL_ZONE_OVRR`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 6 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_LANG`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `LANG_ITEM_DES1` | Lang_Itemessorial Des1 | VARCHAR2 | 40 |  | N |
| 6 | `LANG_ITEM_DES2` | Lang_Itemessorial Des2 | VARCHAR2 | 60 |  | Y |

## `M_ITEM_LOC_PROF_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INB_OUTB_CODE` | Inb_Outbessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_LOC_PROF_SEQ_NUM` | Item_Loc_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `ITEM_LOC_PROF_SEQ_DES` | Item_Loc_Prof_Seqessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 80 |  | Y |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 80 |  | Y |
| 9 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 15 | `ITEM_LOC_PROF_HGT_GAP` | Item_Loc_Prof_Hgtessorial Gap | NUMBER | 22 | 7 | Y |
| 16 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 17 | `ITEM_LOC_PROF_RANGE_QTY` | Item_Loc_Prof_Rangeessorial Qty | NUMBER | 22 | 4 | Y |

## `M_ITEM_LOC_PROF_DD`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INB_OUTB_CODE` | Inb_Outbessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_LOC_PROF_SEQ_NUM` | Item_Loc_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `INB_OUTB_PARA_NUM` | Inb_Outb_Paraessorial Num | NUMBER | 22 | 2 | N |
| 7 | `INB_OUTB_PARA_OPT_NUM` | Inb_Outb_Para_Optessorial Num | NUMBER | 22 | 2 | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_LOC_PROF_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_LOC_PROF_DES` | Item_Loc_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_LOC_PROF_STAT` | Item_Loc_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_MIN_SHIP_LEV_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 4 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_MIN_SHIP_VAL` | Item_Min_Shipessorial Val | VARCHAR2 | 40 |  | N |
| 6 | `ITEM_MIN_SHIP_EXCPT_VAL` | Item_Min_Ship_Excptessorial Val | VARCHAR2 | 255 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_MIN_SHIP_LEV_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 4 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_MIN_SHIP_START_CHAR_NUM` | Item_Min_Ship_Start_Charessorial Num | NUMBER | 22 | 2 | N |
| 6 | `ITEM_MIN_SHIP_LEN_NUM` | Item_Min_Ship_Lenessorial Num | NUMBER | 22 | 2 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_NEW_PROS`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |

## `M_ITEM_PLT_BUILD_REST_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_PLT_BUILD_REST_CODE` | Item_Plt_Build_Restessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_PLT_BUILD_REST_CODE_REST` | Item_Plt_Build_Rest_Codeessorial Rest | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_PLT_BUILD_ALLOW_TOP_FLAG` | Item_Plt_Build_Allow_Topessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_PLT_BUILD_REST_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_PLT_BUILD_REST_CODE` | Item_Plt_Build_Restessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_PLT_BUILD_REST_DES` | Item_Plt_Build_Restessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_PLT_BUILD_REST_STAT` | Item_Plt_Build_Restessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_RCPT_HOLD_PROF_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_RCPT_HOLD_PROF_CODE` | Item_Rcpt_Hold_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_RCPT_HOLD_PROF_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_RCPT_HOLD_PROF_CODE` | Item_Rcpt_Hold_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_RCPT_HOLD_PROF_DES` | Item_Rcpt_Hold_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_RCPT_HOLD_PROF_STAT` | Item_Rcpt_Hold_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_RF_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_RF_PROF_CODE` | Item_Rf_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_RF_PROF_DES` | Item_Rf_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_RF_PROF_STAT` | Item_Rf_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ITEM_RF_ALLOW_SUSP_HOLD_RFPIC` | Item_Rf_Allow_Susp_Holdessorial Rfpic | VARCHAR2 | 1 |  | Y |
| 7 | `ITEM_RF_SHOW_ITEM_DESC_RFCH` | Item_Rf_Show_Item_Descessorial Rfch | VARCHAR2 | 1 |  | Y |
| 8 | `ITEM_RF_SHOW_ITEM_DESC_RFPIC` | Item_Rf_Show_Item_Descessorial Rfpic | VARCHAR2 | 1 |  | Y |
| 9 | `ITEM_RF_ACTIVE_CYCLE_RFPIC` | Item_Rf_Active_Cycleessorial Rfpic | VARCHAR2 | 4 |  | Y |
| 10 | `ITEM_RF_INVT_CNT_ACTIVE_TP` | Item_Rf_Invt_Cnt_Activeessorial Tp | VARCHAR2 | 1 |  | Y |
| 11 | `ITEM_RF_INVT_CNT_VAL_TP` | Item_Rf_Invt_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `RF_PROF_INVT_CNT_THRESH_QTY` | Rf_Prof_Invt_Cnt_Threshessorial Qty | NUMBER | 22 | 6 | Y |
| 18 | `RF_PROF_MISC_CNT_PGM` | Rf_Prof_Misc_Cntessorial Pgm | VARCHAR2 | 1 |  | Y |
| 19 | `RF_PROF_MISC_CNT_ACTIVE_TP` | Rf_Prof_Misc_Cnt_Activeessorial Tp | VARCHAR2 | 1 |  | Y |
| 20 | `RF_PROF_MISC_CNT_VAL_TP` | Rf_Prof_Misc_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | Y |
| 21 | `RF_PROF_MISC_CNT_THRESH_QTY` | Rf_Prof_Misc_Cnt_Threshessorial Qty | NUMBER | 22 | 6 | Y |
| 22 | `RF_PROF_INVT_CNT_BASE_TP` | Rf_Prof_Invt_Cnt_Baseessorial Tp | VARCHAR2 | 1 |  | Y |

## `M_ITEM_SELL_BKD_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `SELL_BKD_PROF_CODE` | Sell_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_SELL_BKD_DATE` | Item_Sell_Bkdessorial Date | DATE | 7 |  | N |
| 6 | `ITEM_SELL_BKD_LEV_NUM` | Item_Sell_Bkd_Levessorial Num | NUMBER | 22 | 1 | N |
| 7 | `ITEM_SELL_UPC` | Item_Sellessorial Upc | VARCHAR2 | 20 |  | Y |
| 8 | `ITEM_SELL_BKD_QTY` | Item_Sell_Bkdessorial Qty | NUMBER | 22 | 4 | Y |
| 9 | `ITEM_SELL_BKD_NUM_LAY` | Item_Sell_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 10 | `ITEM_SELL_BKD_QTY_PER_LAY` | Item_Sell_Bkd_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 11 | `ITEM_SELL_BKD_QTY_ODD_LAY` | Item_Sell_Bkd_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 12 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `ITEM_SELL_BKD_HGT` | Item_Sell_Bkdessorial Hgt | NUMBER | 22 | 7 | Y |
| 14 | `ITEM_SELL_BKD_WID` | Item_Sell_Bkdessorial Wid | NUMBER | 22 | 7 | Y |
| 15 | `ITEM_SELL_BKD_LEN` | Item_Sell_Bkdessorial Len | NUMBER | 22 | 7 | Y |
| 16 | `ITEM_SELL_BKD_CUBE` | Item_Sell_Bkdessorial Cube | NUMBER | 22 | 9 | Y |
| 17 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_SELL_BKD_WGT_GROSS` | Item_Sell_Bkd_Wgtessorial Gross | NUMBER | 22 | 14 | Y |
| 19 | `ITEM_SELL_BKD_WGT_NET` | Item_Sell_Bkd_Wgtessorial Net | NUMBER | 22 | 14 | Y |
| 20 | `ITEM_SELL_BKD_WGT_TARE` | Item_Sell_Bkd_Wgtessorial Tare | NUMBER | 22 | 14 | Y |

## `M_ITEM_SELL_BKD_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `SELL_BKD_PROF_CODE` | Sell_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ITEM_SELL_BKD_DATE` | Item_Sell_Bkdessorial Date | DATE | 7 |  | N |

## `M_ITEM_SHIP_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_SHIP_PROF_DES` | Item_Ship_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_SHIP_PROF_STAT` | Item_Ship_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ITEM_SHIP_PROF_BORD_LEV_NUM` | Item_Ship_Prof_Bord_Levessorial Num | NUMBER | 22 | 1 | Y |
| 7 | `ITEM_SHIP_PROF_FORD_FLAG` | Item_Ship_Prof_Fordessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ITEM_SHIP_PROF_EXPY_DATE_FLAG` | Item_Ship_Prof_Expy_Dateessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ITEM_SHIP_PROF_EXPY_CODE` | Item_Ship_Prof_Expyessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `ITEM_SHIP_PROF_EXPY_FORUL` | Item_Ship_Prof_Expyessorial Forul | VARCHAR2 | 500 |  | Y |
| 11 | `ITEM_SHIP_PROF_EXPY_SHELF_PER` | Item_Ship_Prof_Expy_Shelfessorial Per | NUMBER | 22 | 4 | Y |
| 12 | `ITEM_SHIP_PROF_EXPY_SHELF_FRQ` | Item_Ship_Prof_Expy_Shelfessorial Frq | VARCHAR2 | 1 |  | Y |
| 13 | `ITEM_SHIP_PROF_ITEM_SUB_FLAG` | Item_Ship_Prof_Item_Subessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `ITEM_SHIP_PROF_WGT_SHIP_FLAG` | Item_Ship_Prof_Wgt_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `ITEM_SHIP_PROF_EXPY_FORUL_FMT` | Item_Ship_Prof_Expy_Forulessorial Fmt | VARCHAR2 | 20 |  | Y |
| 16 | `ITEM_SHIP_DYN_RECAL_EXPY_DT_TP` | Item_Ship_Dyn_Recal_Expy_Dtessorial Tp | VARCHAR2 | 1 |  | Y |
| 17 | `ITEM_SHIP_PROF_WGT_RND_METH` | Item_Ship_Prof_Wgt_Rndessorial Meth | VARCHAR2 | 1 |  | Y |
| 18 | `EXPY_INVT_AUTO_HOLD_CODE` | Expy_Invt_Auto_Holdessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 24 | `ITEM_SHIP_PROF_STALE_PER` | Item_Ship_Prof_Staleessorial Per | NUMBER | 22 | 4 | Y |
| 25 | `STALE_INVT_AUTO_HOLD_CODE` | Stale_Invt_Auto_Holdessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `ITEM_SHIP_PROF_MIN_MAX_DATE_TP` | Item_Ship_Prof_Min_Max_Dateessorial Tp | VARCHAR2 | 1 |  | Y |
| 27 | `ITEM_SHIP_PROF_LEV_EXPY_SHELF` | Item_Ship_Prof_Lev_Expyessorial Shelf | VARCHAR2 | 4 |  | Y |
| 28 | `MIN_MAX_DATE_SUPERVISOR_OVER` | Min_Max_Date_Supervisoressorial Over | VARCHAR2 | 1 |  | Y |
| 29 | `ITEM_SHIP_PROF_MIN_EXPY_DAY` | Item_Ship_Prof_Min_Expyessorial Day | NUMBER | 22 | 4 | Y |
| 30 | `ITEM_SHIP_PROF_MAX_EXPY_DAY` | Item_Ship_Prof_Max_Expyessorial Day | NUMBER | 22 | 4 | Y |
| 31 | `ITEM_SHIP_PROF_MAX_PROD_DAY` | Item_Ship_Prof_Max_Prodessorial Day | NUMBER | 22 | 4 | Y |

## `M_ITEM_TARE_PROF_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_TARE_PROF_CODE` | Item_Tare_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_TARE_PROF_BK_NUM` | Item_Tare_Prof_Bkessorial Num | NUMBER | 22 | 2 | N |
| 5 | `ITEM_TARE_PROF_BK_VALUE` | Item_Tare_Prof_Bkessorial Value | NUMBER | 22 | 11 | Y |
| 6 | `ITEM_TARE_PROF_BK_TARE` | Item_Tare_Prof_Bkessorial Tare | NUMBER | 22 | 11 | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_TARE_PROF_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_TARE_PROF_CODE` | Item_Tare_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_TARE_PROF_DES` | Item_Tare_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_TARE_PROF_STAT` | Item_Tare_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_TARE_PROF_NUM_BK` | Item_Tare_Prof_Numessorial Bk | NUMBER | 22 | 2 | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ITEM_VAL_PROF`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ITEM_VAL_PROF_CODE` | Item_Val_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_VAL_PROF_DES` | Item_Val_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ITEM_VAL_PROF_STAT` | Item_Val_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MEAS_CODE` | Measessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_VAL` | Itemessorial Val | NUMBER | 22 | 16 | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_QTY_BKD_PROF_D`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `QTY_BKD_PROF_LEV_NUM` | Qty_Bkd_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 6 | `QTY_BKD_PROF_RCPT_PROS_FLAG` | Qty_Bkd_Prof_Rcpt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `QTY_BKD_PROF_SHIP_PROS_FLAG` | Qty_Bkd_Prof_Ship_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `QTY_BKD_PROF_REP_PROS_FLAG` | Qty_Bkd_Prof_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `QTY_BKD_PROF_LAY_REQ_FLAG` | Qty_Bkd_Prof_Lay_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `QTY_BKD_PROF_INV_REP_PROS_FLAG` | Qty_Bkd_Prof_Inv_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `QTY_BKD_PROF_ADJ_PROS_FLAG` | Qty_Bkd_Prof_Adj_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `QTY_BKD_PROF_FLT_LOC_FLAG` | Qty_Bkd_Prof_Flt_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `QTY_BKD_PROF_SHIP_RND_FLAG` | Qty_Bkd_Prof_Ship_Rndessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_QTY_BKD_PROF_H`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `QTY_BKD_PROF_DES` | Qty_Bkd_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `QTY_BKD_PROF_STAT` | Qty_Bkd_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `QUAL_CODE` | Qualessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SKU`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 4 | `SKU_DES` | Skuessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SKU_STAT` | Skuessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `SKU_VALUE` | Skuessorial Value | NUMBER | 22 | 16 | N |
| 7 | `QUAL_CODE` | Qualessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 9 | `SKU_BASE_SKU_CODE` | Sku_Base_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SKU_CLASS`

- **Tipo:** Master
- **Categoria:** Item
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 4 | `SKU_CLASS_DES` | Sku_Classessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `SKU_CLASS_DES_SHORT` | Sku_Class_Desessorial Short | VARCHAR2 | 4 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

