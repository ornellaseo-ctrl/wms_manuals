# Tabelas — EDI

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **40**.

## `C_EDI_ALLOC_ORD`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 10 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_ALLOC_STAT` | Ord_Allocessorial Stat | VARCHAR2 | 1 |  | N |

## `C_EDI_CHANGE`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `QTY` | Qtyessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |

## `C_EDI_CON_D1`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `CON_PREF_NUM` | Con_Prefessorial Num | NUMBER | 22 | 2 | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 4 | `SCAC_CODE` | Scacessorial Code | VARCHAR2 | 4 |  | Y |

## `C_EDI_CON_D2`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_SEQ_NUM_CNT` | Edi_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 3 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | Y |
| 5 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 6 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |

## `C_EDI_CON_D3`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_SEQ_NUM_CNT` | Edi_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 3 | `MES_LINE_TEXT` | Mes_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `C_EDI_CON_H`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 58
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 4 | `CON_ACTN_FLAG` | Con_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CON_CODE_MAST` | Con_Codeessorial Mast | VARCHAR2 | 20 |  | Y |
| 6 | `CON_CODE_MAST_FLAG` | Con_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 8 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 9 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 30 |  | Y |
| 10 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 30 |  | Y |
| 11 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 12 | `CON_ADD4` | Conessorial Add4 | VARCHAR2 | 30 |  | Y |
| 13 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | Y |
| 14 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 16 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 17 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 18 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 19 | `CON_LAST_ACT_DATE` | Con_Last_Actessorial Date | DATE | 7 |  | Y |
| 20 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 22 | `EXT_REF_NUM2` | Ext_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 23 | `EXT_REF_NUM3` | Ext_Refessorial Num3 | VARCHAR2 | 20 |  | Y |
| 24 | `EXT_REF_NUM4` | Ext_Refessorial Num4 | VARCHAR2 | 20 |  | Y |
| 25 | `CON_FRT_APPO_FLAG` | Con_Frt_Appoessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `CON_FRT_DISC_PCENT` | Con_Frt_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 27 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 28 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 30 | `PRTY_NUM` | Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 31 | `DAY_PROF_CODE` | Day_Professorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `CON_BORD_FLAG` | Con_Bordessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `CON_LAB_STD_MODY_NUM` | Con_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 34 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 35 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 36 | `CON_RETAIL_PROF_CODE` | Con_Retail_Professorial Code | VARCHAR2 | 4 |  | Y |
| 37 | `CON_COMPL_ORD_FLAG` | Con_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `CON_FRT_TER_FLAG` | Con_Frt_Teressorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 40 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 42 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 43 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 44 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 45 | `CON_ALLOW_BANDING_FLAG` | Con_Allow_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 46 | `CON_CONSL_TP` | Con_Conslessorial Tp | VARCHAR2 | 1 |  | Y |
| 47 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 48 | `CON_SPS_REQ_FLAG` | Con_Sps_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 50 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 51 | `CON_BANDING_SKU_CLASS_NUM` | Con_Banding_Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 52 | `CON_ASN_REP_TP` | Con_Asn_Repessorial Tp | VARCHAR2 | 1 |  | Y |
| 53 | `CON_MSDS_REQ_FLAG` | Con_Msds_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `CON_UCC128_LABEL_REQ_FLAG` | Con_Ucc128_Label_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 55 | `CON_SKIP_CARTZN_FLAG` | Con_Skip_Cartznessorial Flag | VARCHAR2 | 1 |  | Y |
| 56 | `CON_DATA_SERVICE_ID` | Con_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 57 | `CON_EMP_ID_NUM` | Con_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 58 | `CON_ASS_REST_BY_ITEM` | Con_Ass_Rest_Byessorial Item | VARCHAR2 | 1 |  | Y |

## `C_EDI_DATE_REF`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `EDI_LAST_DATE_REF` | Edi_Last_Dateessorial Ref | DATE | 7 |  | N |

## `C_EDI_ERR`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_ERR_SEQ_NUM` | Edi_Err_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EDI_SESSION_SEQ_NUM` | Edi_Session_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `EDI_FILE_NAME_FULL` | Edi_File_Nameessorial Full | VARCHAR2 | 250 |  | Y |
| 4 | `EDI_FILE_NAME` | Edi_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 5 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | Y |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 7 | `EDI_ERR_DATE` | Edi_Erressorial Date | DATE | 7 |  | N |
| 8 | `EDI_ERR_CODE` | Edi_Erressorial Code | VARCHAR2 | 6 |  | N |
| 9 | `EDI_ERR_TEXT` | Edi_Erressorial Text | VARCHAR2 | 1500 |  | Y |
| 10 | `EDI_ERR_REP_FILE_NAME_FULL` | Edi_Err_Rep_File_Nameessorial Full | VARCHAR2 | 250 |  | Y |
| 11 | `EDI_ERR_REF_NUM` | Edi_Err_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 12 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |

## `C_EDI_INB_QUEUE`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EDI_CREATE_DATE` | Edi_Createessorial Date | DATE | 7 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |

## `C_EDI_ITEM_D1`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 23
- **Campos-chave prováveis:** SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_QTY_BKD_LEV_NUM` | Item_Qty_Bkd_Levessorial Num | NUMBER | 22 | 1 | N |
| 3 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 4 | `ITEM_QTY_BKD_QTY` | Item_Qty_Bkdessorial Qty | NUMBER | 22 | 4 | Y |
| 5 | `ITEM_QTY_BKD_MIN_QTY` | Item_Qty_Bkd_Minessorial Qty | NUMBER | 22 | 4 | Y |
| 6 | `ITEM_QTY_BKD_BASE_FLAG` | Item_Qty_Bkd_Baseessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `ITEM_QTY_BKD_WHOLE_FLAG` | Item_Qty_Bkd_Wholeessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 9 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 10 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 11 | `ITEM_QTY_BKD_OVRR_CONFIG_FLAG` | Item_Qty_Bkd_Ovrr_Configessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `ITEM_QTY_BKD_HGT` | Item_Qty_Bkdessorial Hgt | NUMBER | 22 | 7 | Y |
| 14 | `ITEM_QTY_BKD_WID` | Item_Qty_Bkdessorial Wid | NUMBER | 22 | 7 | Y |
| 15 | `ITEM_QTY_BKD_LEN` | Item_Qty_Bkdessorial Len | NUMBER | 22 | 7 | Y |
| 16 | `ITEM_QTY_BKD_CUBE` | Item_Qty_Bkdessorial Cube | NUMBER | 22 | 9 | Y |
| 17 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_QTY_BKD_WGT_GROSS` | Item_Qty_Bkd_Wgtessorial Gross | NUMBER | 22 | 14 | Y |
| 19 | `ITEM_QTY_BKD_WGT_NET` | Item_Qty_Bkd_Wgtessorial Net | NUMBER | 22 | 14 | Y |
| 20 | `ITEM_QTY_BKD_WGT_TARE` | Item_Qty_Bkd_Wgtessorial Tare | NUMBER | 22 | 14 | Y |
| 21 | `ITEM_QTY_BKD_WGT_TLR_PCENT` | Item_Qty_Bkd_Wgt_Tlressorial Pcent | NUMBER | 22 | 2 | Y |
| 22 | `VOL_MEAS_CODE` | Vol_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `ITEM_QTY_BKD_VOL` | Item_Qty_Bkdessorial Vol | NUMBER | 22 | 14 | Y |

## `C_EDI_ITEM_D2`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_SUB_SEQ_NUM` | Item_Sub_Seqessorial Num | NUMBER | 22 | 2 | N |
| 3 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | Y |
| 4 | `ITEM_SUB_TP_FLAG` | Item_Sub_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `ITEM_SUB_CHAIN_FLAG` | Item_Sub_Chainessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_EDI_ITEM_D3`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ALT_INVT_REP_TP_DES` | Alt_Invt_Rep_Tpessorial Des | VARCHAR2 | 30 |  | Y |
| 4 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `ALT_INVT_REP_DES` | Alt_Invt_Repessorial Des | VARCHAR2 | 30 |  | Y |

## `C_EDI_ITEM_D4`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 11
- **Campos-chave prováveis:** HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_CODE_COMPN` | Item_Codeessorial Compn | VARCHAR2 | 20 |  | N |
| 3 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | NUMBER | 22 | 16 | Y |
| 4 | `ITEM_COMPN_ENT_QTY` | Item_Compn_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 5 | `ITEM_COMPN_SEQ_NUM` | Item_Compn_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 6 | `ITEM_COMPN_WGT` | Item_Compnessorial Wgt | NUMBER | 22 | 16 | Y |
| 7 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | Y |
| 8 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 9 | `ITEM_COMPN_PER_KIT_ENT_QTY` | Item_Compn_Per_Kit_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 10 | `ITEM_COMPN_PER_KIT_QTY` | Item_Compn_Per_Kitessorial Qty | NUMBER | 22 | 9 | Y |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `C_EDI_ITEM_D5`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 14
- **Campos-chave prováveis:** INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_SEQ_NUM_CNT` | Edi_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 3 | `ACC_ITEM_ACC_CODE` | Acc_Item_Accessorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `ACC_ITEM_ACC_TP` | Acc_Item_Accessorial Tp | VARCHAR2 | 4 |  | Y |
| 5 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 6 | `ACC_ITEM_CODE` | Accessorial Item Code | VARCHAR2 | 20 |  | Y |
| 7 | `ACC_ITEM_UPC` | Acc_Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 8 | `ACC_ITEM_DES1` | Acc_Itemessorial Des1 | VARCHAR2 | 40 |  | Y |
| 9 | `ACC_ITEM_DES2` | Acc_Itemessorial Des2 | VARCHAR2 | 60 |  | Y |
| 10 | `ALT_TP_CODE` | Alt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `ACC_ITEM_QTY` | Acc_Itemessorial Qty | NUMBER | 22 | 4 | Y |
| 12 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |

## `C_EDI_ITEM_H`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 69
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_ACTN_FLAG` | Item_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ITEM_CODE_MAST` | Item_Codeessorial Mast | VARCHAR2 | 20 |  | Y |
| 7 | `ITEM_CODE_MAST_FLAG` | Item_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | N |
| 9 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 10 | `ITEM_UPC` | Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 11 | `GENR_INFO_PROF_CODE` | Genr_Info_Professorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `ITEM_BILL_PROF_CODE1` | Item_Bill_Professorial Code1 | VARCHAR2 | 4 |  | Y |
| 13 | `ITEM_BILL_PROF_CODE2` | Item_Bill_Professorial Code2 | VARCHAR2 | 4 |  | Y |
| 14 | `ITEM_BILL_PROF_CODE3` | Item_Bill_Professorial Code3 | VARCHAR2 | 4 |  | Y |
| 15 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_HOLD_PROF_CODE` | Item_Hold_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `ITEM_TARE_PROF_CODE` | Item_Tare_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `WGT_TLR_PROF_CODE` | Wgt_Tlr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `PUT_PROF_CODE` | Put_Professorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `ITEM_VAL_PROF_CODE` | Item_Val_Professorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 28 | `ITEM_WGT_TP_CODE` | Item_Wgt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `ITEM_VALUE` | Itemessorial Value | NUMBER | 22 | 12 | Y |
| 30 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 31 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 6 |  | Y |
| 32 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 33 | `ITEM_CRS_DOCK_FLAG` | Item_Crs_Dockessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `ITEM_VAR_QTY_BKD_FLAG` | Item_Var_Qty_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `COMD_CODE` | N/A | VARCHAR2 | 6 |  | Y |
| 36 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | Y |
| 37 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | Y |
| 38 | `ITEM_OPEN_ENTI_NUM_DAY` | Item_Open_Enti_Numessorial Day | NUMBER | 22 | 2 | Y |
| 39 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 40 | `ITEM_DISC_FLAG` | Item_Discessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `ITEM_DISC_PROF_CODE` | Item_Disc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 42 | `SCAN_PARAM_CODE` | Scan_Paramessorial Code | VARCHAR2 | 4 |  | Y |
| 43 | `ITEM_KIT_FLAG` | Item_Kitessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `ITEM_ALLOW_ENTRY_LEV_NUM` | Item_Allow_Entry_Levessorial Num | NUMBER | 22 | 1 | Y |
| 45 | `ITEM_LAB_STD_MODY_NUM` | Item_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 46 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 47 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 48 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 49 | `ITEM_VAR_QTY_BKD_RENW_FLAG` | Item_Var_Qty_Bkd_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `ITEM_KIT_TP_FLAG` | Item_Kit_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 51 | `ITEM_ALLOW_MIX_PLT_FLAG` | Item_Allow_Mix_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 52 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 53 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 54 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 55 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 56 | `ITEM_HAZ_FLAG` | Item_Hazessorial Flag | VARCHAR2 | 1 |  | N |
| 57 | `ITEM_ALLOW_BAND_FLAG` | Item_Allow_Bandessorial Flag | VARCHAR2 | 1 |  | Y |
| 58 | `ITEM_BAND_SKU_CLASS_NUM` | Item_Band_Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 59 | `ITEM_BAND_MAX_QTY` | Item_Band_Maxessorial Qty | NUMBER | 22 | 9 | Y |
| 60 | `ITEM_CARTZN_PROF_CODE` | Item_Cartzn_Professorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `ITEM_DES_EXTN` | Item_Desessorial Extn | VARCHAR2 | 250 |  | Y |
| 62 | `ITEM_OVPI_IGNORE_CON_FLAG` | Item_Ovpi_Ignore_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 64 | `ITEM_OVERSIZE_FLAG` | Item_Oversizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 65 | `RFCH_SCAN_PROF_CODE` | Rfch_Scan_Professorial Code | VARCHAR2 | 4 |  | Y |
| 66 | `ITEM_STACK_TP_CODE` | Item_Stack_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 67 | `ITEM_STACK_STOR_QTY` | Item_Stack_Storessorial Qty | NUMBER | 22 | 4 | Y |
| 68 | `ITEM_REPI_MERGE_LOC_FLAG` | Item_Repi_Merge_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 69 | `ITEM_ALLOC_PLT_BY_ENTITY_FLAG` | Item_Alloc_Plt_By_Entityessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_EDI_ITEM_HAZ_D`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 64
- **Campos-chave prováveis:** SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `TRSPT_MODE_TP` | Trspt_Modeessorial Tp | VARCHAR2 | 4 |  | Y |
| 4 | `ITEM_HAZ_INNER_PACK_TP_CODE` | Item_Haz_Inner_Pack_Tpessorial Code | VARCHAR2 | 5 |  | Y |
| 5 | `ITEM_HAZ_INNER_PACK_TP_DES` | Item_Haz_Inner_Pack_Tpessorial Des | VARCHAR2 | 255 |  | Y |
| 6 | `ITEM_HAZ_INNER_PACK_QTY` | Item_Haz_Inner_Packessorial Qty | NUMBER | 22 | 5 | Y |
| 7 | `ITEM_HAZ_SHIP_NAME` | Item_Haz_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 8 | `ITEM_HAZ_NOS` | Item_Hazessorial Nos | VARCHAR2 | 4 |  | Y |
| 9 | `ITEM_HAZ_TECH_NAME` | Item_Haz_Techessorial Name | VARCHAR2 | 255 |  | Y |
| 10 | `ITEM_HAZ_MULTIPLIER` | Item_Hazessorial Multiplier | NUMBER | 22 | 5 | Y |
| 11 | `ITEM_HAZ_WGT_NET` | Item_Haz_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 12 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `ITEM_HAZ_QTY` | Item_Hazessorial Qty | NUMBER | 22 | 16 | Y |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 15 | `ITEM_HAZ_FLASHPOINT` | Item_Hazessorial Flashpoint | VARCHAR2 | 6 |  | Y |
| 16 | `ITEM_HAZ_ADR_UN_ID` | Item_Haz_Adr_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 17 | `ITEM_HAZ_ADR_PRIMARY_CLASS` | Item_Haz_Adr_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 18 | `ITEM_HAZ_ADR_VALUE` | Item_Haz_Adressorial Value | VARCHAR2 | 3 |  | Y |
| 19 | `ITEM_HAZ_ADR_SUB_RISK_CLASS` | Item_Haz_Adr_Sub_Riskessorial Class | VARCHAR2 | 3 |  | Y |
| 20 | `ITEM_HAZ_ADR_PRIMARY_LABEL` | Item_Haz_Adr_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 21 | `ITEM_HAZ_ADR_SECD_LABEL` | Item_Haz_Adr_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 22 | `ITEM_HAZ_ADR_TERTIARY_LABEL` | Item_Haz_Adr_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 23 | `ITEM_HAZ_ADR_PACK_GRP_CODE` | Item_Haz_Adr_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 24 | `ITEM_HAZ_ADR_SPC_REQ_CODE` | Item_Haz_Adr_Spc_Reqessorial Code | VARCHAR2 | 5 |  | Y |
| 25 | `ITEM_HAZ_IMO_UN_ID` | Item_Haz_Imo_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 26 | `ITEM_HAZ_IMO_PACK_GRP_CODE` | Item_Haz_Imo_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 27 | `ITEM_HAZ_IMO_PRIMARY_CLASS` | Item_Haz_Imo_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 28 | `ITEM_HAZ_IMO_SECD_CLASS` | Item_Haz_Imo_Secdessorial Class | VARCHAR2 | 3 |  | Y |
| 29 | `ITEM_HAZ_IMO_SHIP_NAME` | Item_Haz_Imo_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 30 | `ITEM_HAZ_IMDG_LIMIT_QTY_FLAG` | Item_Haz_Imdg_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `ITEM_HAZ_IMDG_PRIMARY_LABEL` | Item_Haz_Imdg_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 32 | `ITEM_HAZ_IMDG_SECD_LABEL` | Item_Haz_Imdg_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 33 | `ITEM_HAZ_IMDG_TERTIARY_LABEL` | Item_Haz_Imdg_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 34 | `ITEM_HAZ_MARINE_POLLUT_FLAG` | Item_Haz_Marine_Pollutessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `ITEM_HAZ_IMDG_CERTIFICATE` | Item_Haz_Imdgessorial Certificate | VARCHAR2 | 20 |  | Y |
| 36 | `ITEM_HAZ_IATA_UN_ID` | Item_Haz_Iata_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 37 | `ITEM_HAZ_IATA_PRIMARY_CLASS` | Item_Haz_Iata_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 38 | `ITEM_HAZ_IATA_PACK_GRP_CODE` | Item_Haz_Iata_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 39 | `ITEM_HAZ_IATA_SUB_RISK_CLASS` | Item_Haz_Iata_Sub_Riskessorial Class | VARCHAR2 | 3 |  | Y |
| 40 | `ITEM_HAZ_AIR_SHIP_NAME_1` | Item_Haz_Air_Ship_Nameessorial 1 | VARCHAR2 | 60 |  | Y |
| 41 | `ITEM_HAZ_AIR_SHIP_NAME_2` | Item_Haz_Air_Ship_Nameessorial 2 | VARCHAR2 | 60 |  | Y |
| 42 | `ITEM_HAZ_IATA_PRIMARY_LABEL` | Item_Haz_Iata_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 43 | `ITEM_HAZ_IATA_SECD_LABEL` | Item_Haz_Iata_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 44 | `ITEM_HAZ_IATA_TERTIARY_LABEL` | Item_Haz_Iata_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 45 | `ITEM_HAZ_IMOD_EMS` | Item_Haz_Imodessorial Ems | VARCHAR2 | 6 |  | Y |
| 46 | `ITEM_HAZ_EXT_REF_CODE` | Item_Haz_Ext_Refessorial Code | VARCHAR2 | 20 |  | Y |
| 47 | `ITEM_HAZ_OFC_CODE` | Item_Haz_Ofcessorial Code | VARCHAR2 | 5 |  | Y |
| 48 | `ITEM_HAZ_MAT_WORKCENTER_FLAG` | Item_Haz_Mat_Workcenteressorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `ITEM_HAZ_DOT_UN_ID` | Item_Haz_Dot_Unessorial Id | VARCHAR2 | 6 |  | Y |
| 50 | `ITEM_HAZ_DOT_ID` | Item_Haz_Dotessorial Id | VARCHAR2 | 6 |  | Y |
| 51 | `ITEM_HAZ_DOT_PRIMARY_CLASS` | Item_Haz_Dot_Primaryessorial Class | VARCHAR2 | 3 |  | Y |
| 52 | `ITEM_HAZ_DOT_SECD_CLASS` | Item_Haz_Dot_Secdessorial Class | VARCHAR2 | 3 |  | Y |
| 53 | `ITEM_HAZ_DOT_TERTIARY_CLASS` | Item_Haz_Dot_Tertiaryessorial Class | VARCHAR2 | 3 |  | Y |
| 54 | `ITEM_HAZ_DOT_PRIMARY_LABEL` | Item_Haz_Dot_Primaryessorial Label | VARCHAR2 | 2 |  | Y |
| 55 | `ITEM_HAZ_DOT_SECD_LABEL` | Item_Haz_Dot_Secdessorial Label | VARCHAR2 | 2 |  | Y |
| 56 | `ITEM_HAZ_DOT_TERTIARY_LABEL` | Item_Haz_Dot_Tertiaryessorial Label | VARCHAR2 | 2 |  | Y |
| 57 | `ITEM_HAZ_DOT_SHIP_NAME` | Item_Haz_Dot_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 58 | `ITEM_HAZ_DOT_PACK_GRP_CODE` | Item_Haz_Dot_Pack_Grpessorial Code | VARCHAR2 | 1 |  | Y |
| 59 | `ITEM_HAZ_DOT_LIMIT_QTY_FLAG` | Item_Haz_Dot_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 60 | `ITEM_HAZ_DOT_EXEMPTION_ID` | Item_Haz_Dot_Exemptionessorial Id | VARCHAR2 | 5 |  | Y |
| 61 | `ITEM_HAZ_MARINE_POLLUT_LABEL` | Item_Haz_Marine_Pollutessorial Label | VARCHAR2 | 2 |  | Y |
| 62 | `ITEM_HAZ_IMDG_SEGREG_GRP` | Item_Haz_Imdg_Segregessorial Grp | VARCHAR2 | 4 |  | Y |
| 63 | `ITEM_HAZ_IMDG_SEGREG_GRP_DES` | Item_Haz_Imdg_Segreg_Grpessorial Des | VARCHAR2 | 40 |  | Y |
| 64 | `ITEM_HAZ_IMDG_PHASES_ACID` | Item_Haz_Imdg_Phasesessorial Acid | VARCHAR2 | 2 |  | Y |

## `C_EDI_ITEM_HAZ_DD`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_HAZ_ADR_SHIP_NAME` | Item_Haz_Adr_Shipessorial Name | VARCHAR2 | 80 |  | Y |
| 5 | `ITEM_HAZ_TEXT_1` | Item_Haz_Textessorial 1 | VARCHAR2 | 255 |  | Y |
| 6 | `ITEM_HAZ_TEXT_2` | Item_Haz_Textessorial 2 | VARCHAR2 | 255 |  | Y |
| 7 | `ITEM_HAZ_TEXT_3` | Item_Haz_Textessorial 3 | VARCHAR2 | 255 |  | Y |

## `C_EDI_ITEM_HAZ_H`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 18

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `ITEM_HAZ_MULTIPART_FLAG` | Item_Haz_Multipartessorial Flag | VARCHAR2 | 1 |  | Y |
| 3 | `ITEM_HAZ_PACK_TP_CODE` | Item_Haz_Pack_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `ITEM_HAZ_PACK_TP_DES` | Item_Haz_Pack_Tpessorial Des | VARCHAR2 | 255 |  | Y |
| 5 | `ITEM_HAZ_IMO_EMS_NUM` | Item_Haz_Imo_Emsessorial Num | VARCHAR2 | 6 |  | Y |
| 6 | `ITEM_HAZ_IMO_MFAG_NUM` | Item_Haz_Imo_Mfagessorial Num | NUMBER | 22 | 3 | Y |
| 7 | `ITEM_HAZ_FLASHPOINT` | Item_Hazessorial Flashpoint | VARCHAR2 | 6 |  | Y |
| 8 | `ITEM_HAZ_ADR_LIMIT_QTY_FLAG` | Item_Haz_Adr_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ITEM_HAZ_DOT_LIMIT_QTY_FLAG` | Item_Haz_Dot_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `ITEM_HAZ_RQ_LIMIT_QTY_FLAG` | Item_Haz_Rq_Limit_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ITEM_HAZ_IATA_PACK_INS` | Item_Haz_Iata_Packessorial Ins | VARCHAR2 | 5 |  | Y |
| 12 | `ITEM_HAZ_LABEL_CODE_1` | Item_Haz_Label_Codeessorial 1 | VARCHAR2 | 2 |  | Y |
| 13 | `ITEM_HAZ_LABEL_CODE_2` | Item_Haz_Label_Codeessorial 2 | VARCHAR2 | 2 |  | Y |
| 14 | `ITEM_HAZ_ACID_FLAG` | Item_Haz_Acidessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `ITEM_HAZ_AIR_STAT_CODE` | Item_Haz_Air_Statessorial Code | VARCHAR2 | 1 |  | Y |
| 16 | `ITEM_HAZ_OVER_LABEL_CODE` | Item_Haz_Over_Labelessorial Code | VARCHAR2 | 1 |  | Y |
| 17 | `ITEM_HAZ_TREM_CARD_NUM` | Item_Haz_Trem_Cardessorial Num | NUMBER | 22 | 9 | Y |
| 18 | `ITEM_HAZ_ACCESSIBLE_FLAG` | Item_Haz_Accessibleessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_EDI_OUTB_LOAD`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `C_EDI_OUTB_QUEUE`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EDI_CREATE_DATE` | Edi_Createessorial Date | DATE | 7 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |

## `C_EDI_PO_ADD`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_PO_ADD_QUAL_CODE` | Edi_Po_Add_Qualessorial Code | VARCHAR2 | 2 |  | N |
| 3 | `EDI_PO_ADD_CODE` | Edi_Po_Addessorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `EDI_PO_ADD_NAME` | Edi_Po_Addessorial Name | VARCHAR2 | 30 |  | Y |
| 5 | `EDI_PO_ADD_ADD1` | Edi_Po_Addessorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `EDI_PO_ADD_ADD2` | Edi_Po_Addessorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `EDI_PO_ADD_ADD3` | Edi_Po_Addessorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `EDI_PO_ADD_ADD4` | Edi_Po_Addessorial Add4 | VARCHAR2 | 30 |  | Y |
| 9 | `EDI_PO_ADD_ZIP_CITY` | Edi_Po_Add_Zipessorial City | VARCHAR2 | 30 |  | Y |
| 10 | `EDI_PO_ADD_STATE_CODE` | Edi_Po_Add_Stateessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `EDI_PO_ADD_ZIP_CODE` | Edi_Po_Add_Zipessorial Code | VARCHAR2 | 10 |  | Y |
| 12 | `EDI_PO_ADD_COUNTRY_CODE` | Edi_Po_Add_Countryessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `EDI_PO_ADD_EXT_REF` | Edi_Po_Add_Extessorial Ref | VARCHAR2 | 20 |  | Y |

## `C_EDI_PO_D1`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_SEQ_NUM_CNT` | Edi_Seq_Numessorial Cnt | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `PO_REM_CODE` | Po_Remessorial Code | VARCHAR2 | 4 |  | Y |
| 5 | `PO_REM_LINE_NUM` | Po_Rem_Lineessorial Num | NUMBER | 22 | 3 | Y |
| 6 | `PO_REM_LINE_TEXT` | Po_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `C_EDI_PO_D2`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 35
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_PO_LINE_NUM` | Edi_Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `EDI_PO_LINE_ACTN` | Edi_Po_Lineessorial Actn | VARCHAR2 | 1 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 8 | `PO_LINE_REF_NUM` | Po_Line_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `PO_ORD_QTY` | Po_Ordessorial Qty | NUMBER | 22 | 9 | Y |
| 10 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 11 | `PO_TLR_OVER` | Po_Tlressorial Over | NUMBER | 22 | 9 | Y |
| 12 | `PO_TLR_UNDER` | Po_Tlressorial Under | NUMBER | 22 | 9 | Y |
| 13 | `PO_TLR_TP_FLAG` | Po_Tlr_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | Y |
| 15 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `PO_LINE_EXPT_DATE` | Po_Line_Exptessorial Date | DATE | 7 |  | Y |
| 18 | `PO_LINE_PRICE` | Po_Lineessorial Price | NUMBER | 22 | 12 | Y |
| 19 | `PO_LINE_COST` | Po_Lineessorial Cost | NUMBER | 22 | 12 | Y |
| 20 | `PO_LINE_DISC_PRICE` | Po_Line_Discessorial Price | NUMBER | 22 | 12 | Y |
| 21 | `PO_LINE_ISO_UOM` | Po_Line_Isoessorial Uom | VARCHAR2 | 4 |  | Y |
| 22 | `PO_LINE_EXPY_DATE` | Po_Line_Expyessorial Date | DATE | 7 |  | Y |
| 23 | `EDI_PO_LINE_CONSIGN_FLAG` | Edi_Po_Line_Consignessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `PO_LINE_BAT_ID` | Po_Line_Batessorial Id | VARCHAR2 | 40 |  | Y |
| 25 | `PO_LINE_EXPY_DATE_STR` | Po_Line_Expy_Dateessorial Str | VARCHAR2 | 8 |  | Y |
| 26 | `PO_LINE_SER` | Po_Lineessorial Ser | VARCHAR2 | 40 |  | Y |
| 27 | `PO_LINE_PAL_ID` | Po_Line_Palessorial Id | VARCHAR2 | 40 |  | Y |
| 28 | `HOLD_CODE_EXT_REF` | Hold_Code_Extessorial Ref | VARCHAR2 | 4 |  | Y |
| 29 | `PO_LINE_MATERIAL_RES_NUM` | Po_Line_Material_Resessorial Num | VARCHAR2 | 30 |  | Y |
| 30 | `PO_ORD_WGT` | Po_Ordessorial Wgt | NUMBER | 22 | 16 | Y |
| 31 | `PO_ORD_WGT_NET` | Po_Ord_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 32 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 33 | `PO_ORD_VALUE_ORG` | Po_Ord_Valueessorial Org | NUMBER | 22 | 16 | Y |
| 34 | `PO_ORD_VALUE_FACT` | Po_Ord_Valueessorial Fact | NUMBER | 22 | 16 | Y |
| 35 | `PO_ORD_UOM` | Po_Ordessorial Uom | VARCHAR2 | 20 |  | Y |

## `C_EDI_PO_D2D3`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_PO_LINE_NUM` | Edi_Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `EDI_PO_SCH_LINE_NUM` | Edi_Po_Sch_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `EDI_PO_LINE_ORD_SCH_QTY` | Edi_Po_Line_Ord_Schessorial Qty | NUMBER | 22 | 9 | N |
| 5 | `EDI_PO_LINE_SCH_DATE` | Edi_Po_Line_Schessorial Date | DATE | 7 |  | N |

## `C_EDI_PO_D4`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |

## `C_EDI_PO_H`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_PO_ACTN` | Edi_Poessorial Actn | VARCHAR2 | 1 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `PO_DATE` | Poessorial Date | DATE | 7 |  | Y |
| 6 | `PO_EXPY_DATE` | Po_Expyessorial Date | DATE | 7 |  | Y |
| 7 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 8 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 9 | `PO_REF1` | Poessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 10 | `PO_REF2` | Poessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 11 | `PO_REF3` | Poessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 12 | `PO_REF4` | Poessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 13 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 14 | `TRANS_TP_CODE` | Trans_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 16 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 18 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 19 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |

## `C_EDI_SHIP_D`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `EDI_SEQ_NUM_CNT` | Edi_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 3 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | Y |
| 5 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 6 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |

## `C_EDI_SHIP_H`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_SEQ_NUM` | EDI Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_ACTN_FLAG` | Ship_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SHIP_CODE_MAST` | Ship_Codeessorial Mast | VARCHAR2 | 10 |  | Y |
| 6 | `SHIP_CODE_MAST_FLAG` | Ship_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 8 | `SHIP_NAME` | Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 9 | `SHIP_ADD1` | Shipessorial Add1 | VARCHAR2 | 30 |  | Y |
| 10 | `SHIP_ADD2` | Shipessorial Add2 | VARCHAR2 | 30 |  | Y |
| 11 | `SHIP_ADD3` | Shipessorial Add3 | VARCHAR2 | 30 |  | Y |
| 12 | `SHIP_ADD4` | Shipessorial Add4 | VARCHAR2 | 30 |  | Y |
| 13 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | Y |
| 14 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 16 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 17 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 18 | `SHIP_TP_CODE` | Ship_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 20 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 21 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 25 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 27 | `SHIP_ESTAB_NUM` | Ship_Estabessorial Num | VARCHAR2 | 20 |  | Y |
| 28 | `SHIP_COUNTRY_ORIGIN` | Ship_Countryessorial Origin | VARCHAR2 | 4 |  | Y |
| 29 | `VEND_CODE` | Vendessorial Code | VARCHAR2 | 10 |  | Y |
| 30 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 31 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 33 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 34 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 35 | `SHIP_EMP_ID_NUM` | Ship_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |

## `E_EDI_DOC_QUEUE`

- **Tipo:** Transactional
- **Categoria:** EDI
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `DOC_QUEUE_TRANS_DATE` | Doc_Queue_Transessorial Date | DATE | 7 |  | N |
| 4 | `REC_TP_CODE` | Rec_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 7 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |

## `M_EDI_CUST_INV_DOC`

- **Tipo:** Master
- **Categoria:** EDI
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INV_TP` | Invessorial Tp | VARCHAR2 | 4 |  | N |
| 5 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_EDI_PROF_D`

- **Tipo:** Master
- **Categoria:** EDI
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_EDI_PROF_DD`

- **Tipo:** Master
- **Categoria:** EDI
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `EDI_DATA_ID_DES` | Edi_Data_Idessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `EDI_PROG_ROUT_CASE_CODE` | Edi_Prog_Rout_Caseessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `EDI_DATA_ID_SEND_FLAG` | Edi_Data_Id_Sendessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EDI_DATA_ID_ENTRY_TP_FLAG` | Edi_Data_Id_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `EDI_DATA_ID_LINE_ENTRY_FLAG` | Edi_Data_Id_Line_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EDI_DATA_ID_MAND_FLAG` | Edi_Data_Id_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EDI_DATA_ID_LEN` | Edi_Data_Idessorial Len | VARCHAR2 | 6 |  | N |
| 13 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_EDI_PROF_DDD`

- **Tipo:** Master
- **Categoria:** EDI
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `EDI_TRANS_SET_CODE_OUTB` | Edi_Trans_Set_Codeessorial Outb | VARCHAR2 | 4 |  | N |
| 7 | `EDI_DATA_ID_CODE_OUTB` | Edi_Data_Id_Codeessorial Outb | VARCHAR2 | 20 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_EDI_PROF_H`

- **Tipo:** Master
- **Categoria:** EDI
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_PROF_DES` | Edi_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `EDI_PROF_STAT` | Edi_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_EDI_DATA_ID`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `EDI_DATA_ID_DES` | Edi_Data_Idessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `EDI_DATA_ID_STAT` | Edi_Data_Idessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `EDI_DATA_ID_START_POS` | Edi_Data_Id_Startessorial Pos | NUMBER | 22 | 3 | N |
| 8 | `EDI_DATA_ID_LEN` | Edi_Data_Idessorial Len | NUMBER | 22 | 3 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_EDI_HIST_D`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_HIST_CONT_NUM` | Edi_Hist_Contessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EDI_HIST_DOC_TP` | Edi_Hist_Docessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `EDI_HIST_INB_OUTB_FLAG` | Edi_Hist_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `EDI_HIST_PROS_DATE` | Edi_Hist_Prosessorial Date | DATE | 7 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `EDI_HIST_ERROR_FLAG` | Edi_Hist_Erroressorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `EDI_HIST_ERROR_MES_CODE` | Edi_Hist_Error_Mesessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `EDI_HIST_ERROR_MES` | Edi_Hist_Erroressorial Mes | VARCHAR2 | 250 |  | Y |
| 9 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 10 | `EDI_HIST_PARTNER_CODE` | Edi_Hist_Partneressorial Code | VARCHAR2 | 10 |  | Y |
| 11 | `EDI_HIST_ENTITY_CODE` | Edi_Hist_Entityessorial Code | VARCHAR2 | 10 |  | Y |
| 12 | `EDI_HIST_ENTITY_CODE_TP` | Edi_Hist_Entity_Codeessorial Tp | VARCHAR2 | 4 |  | Y |
| 13 | `EDI_HIST_DOC_NUM` | Edi_Hist_Docessorial Num | NUMBER | 22 | 6 | Y |
| 14 | `EDI_HIST_DOC_NUM_TP` | Edi_Hist_Doc_Numessorial Tp | VARCHAR2 | 1 |  | Y |
| 15 | `EDI_HIST_REF_NUM` | Edi_Hist_Refessorial Num | VARCHAR2 | 20 |  | Y |

## `S_EDI_HIST_H`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_HIST_CONT_NUM` | Edi_Hist_Contessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EDI_HIST_DOC_TP` | Edi_Hist_Docessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `EDI_HIST_DOC_STAT` | Edi_Hist_Docessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `EDI_HIST_INB_OUTB_FLAG` | Edi_Hist_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `EDI_HIST_ACK_FLAG` | Edi_Hist_Ackessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EDI_HIST_FILE_EXACT` | Edi_Hist_Fileessorial Exact | VARCHAR2 | 20 |  | Y |
| 7 | `EDI_HIST_FILE_DIR` | Edi_Hist_Fileessorial Dir | VARCHAR2 | 40 |  | Y |
| 8 | `EDI_HIST_GRP_CONT_NUM` | Edi_Hist_Grp_Contessorial Num | NUMBER | 22 | 9 | Y |
| 9 | `EDI_HIST_BAT_CONT_NUM` | Edi_Hist_Bat_Contessorial Num | NUMBER | 22 | 9 | Y |
| 10 | `EDI_HIST_PARTNER_GRP_NUM` | Edi_Hist_Partner_Grpessorial Num | VARCHAR2 | 9 |  | Y |
| 11 | `EDI_HIST_PARTNER_BAT_NUM` | Edi_Hist_Partner_Batessorial Num | VARCHAR2 | 9 |  | Y |
| 12 | `EDI_HIST_PARTNER_SET_NUM` | Edi_Hist_Partner_Setessorial Num | VARCHAR2 | 9 |  | Y |
| 13 | `EDI_HIST_EDI_VERS_CODE` | Edi_Hist_Edi_Versessorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `EDI_HIST_EDI_SET_CODE` | Edi_Hist_Edi_Setessorial Code | VARCHAR2 | 6 |  | Y |
| 15 | `EDI_HIST_ACK_DATE` | Edi_Hist_Ackessorial Date | DATE | 7 |  | Y |

## `S_EDI_PROG_ROUT_CASE`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `EDI_PROG_ROUT_CASE_CODE` | Edi_Prog_Rout_Caseessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `EDI_PROG_ROUT_CASE_DES` | Edi_Prog_Rout_Caseessorial Des | VARCHAR2 | 60 |  | N |
| 4 | `EDI_PROG_ROUT_CASE_STAT` | Edi_Prog_Rout_Caseessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_EDI_PURGE_H`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EDI_PURGE_PURGE_AUTO_FLAG` | Edi_Purge_Purge_Autoessorial Flag | VARCHAR2 | 1 |  | Y |
| 2 | `EDI_PURGE_RETEN_PER` | Edi_Purge_Retenessorial Per | NUMBER | 22 | 3 | Y |

## `S_EDI_TRANS_SET`

- **Tipo:** System Setup Related
- **Categoria:** EDI
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `EDI_TRANS_SET_DES` | Edi_Trans_Setessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `EDI_TRANS_SET_STAT` | Edi_Trans_Setessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `EDI_TP_CODE` | Edi_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

