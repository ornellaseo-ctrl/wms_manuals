# Tabelas — Conveyence

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **26**.

## `S_CNV`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CNV_RTN` | Cnvessorial Rtn | VARCHAR2 | 20 |  | Y |
| 2 | `CNV_TP` | Cnvessorial Tp | VARCHAR2 | 20 |  | Y |
| 3 | `CNV_ROWID` | Cnvessorial Rowid | VARCHAR2 | 20 |  | Y |

## `S_COL`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COL_NAME` | Column Name | VARCHAR2 | 30 |  | N |
| 2 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `COL_TP` | Colessorial Tp | VARCHAR2 | 6 |  | N |
| 4 | `COL_NUM` | Column Name | NUMBER | 22 | 4 | N |

## `S_CONV_ALIT`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `ACC_ITEM_ACC_CODE` | Acc_Item_Accessorial Code | VARCHAR2 | 10 |  | Y |
| 3 | `ACC_ITEM_ACC_TP` | Acc_Item_Accessorial Tp | VARCHAR2 | 4 |  | Y |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 7 | `ACC_ITEM_CODE` | Accessorial Item Code | VARCHAR2 | 20 |  | Y |
| 8 | `ACC_ITEM_UPC` | Acc_Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 9 | `ACC_ITEM_DES1` | Acc_Itemessorial Des1 | VARCHAR2 | 40 |  | Y |
| 10 | `ACC_ITEM_DES2` | Acc_Itemessorial Des2 | VARCHAR2 | 60 |  | Y |
| 11 | `ACC_ITEM_QTY` | Acc_Itemessorial Qty | VARCHAR2 | 6 |  | Y |
| 12 | `ALT_TP_CODE` | Alt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |

## `S_CONV_ALTR`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | N |

## `S_CONV_AUD`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CONV_AUD_ACTN` | Conv_Audessorial Actn | VARCHAR2 | 10 |  | N |
| 2 | `CONV_AUD_DES` | Conv_Audessorial Des | VARCHAR2 | 60 |  | Y |
| 3 | `CONV_AUD_DATE` | Conv_Audessorial Date | DATE | 7 |  | N |
| 4 | `CONV_AUD_TABLE` | Conv_Audessorial Table | VARCHAR2 | 30 |  | Y |
| 5 | `CONV_AUD_RESULT` | Conv_Audessorial Result | VARCHAR2 | 60 |  | Y |

## `S_CONV_BAD`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CONV_PASS_NAME` | Conv_Passessorial Name | VARCHAR2 | 10 |  | N |
| 2 | `CONV_PASS_ROWID` | Conv_Passessorial Rowid | VARCHAR2 | 20 |  | N |
| 3 | `CONV_PASS_MES` | Conv_Passessorial Mes | VARCHAR2 | 120 |  | N |

## `S_CONV_BAL`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 36
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `CONV_UNIT` | Convessorial Unit | VARCHAR2 | 10 |  | Y |
| 6 | `CONV_WGT` | Convessorial Wgt | VARCHAR2 | 17 |  | Y |
| 7 | `RENW_QTY` | Renwessorial Qty | VARCHAR2 | 10 |  | Y |
| 8 | `RENW_WGT` | Renwessorial Wgt | VARCHAR2 | 17 |  | Y |
| 9 | `DATE_NXT` | Dateessorial Nxt | VARCHAR2 | 6 |  | Y |
| 10 | `DATE_LAST` | Dateessorial Last | VARCHAR2 | 6 |  | Y |
| 11 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | VARCHAR2 | 6 |  | Y |
| 12 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | VARCHAR2 | 6 |  | Y |
| 13 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 18 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 19 | `INVT_LEV2_DES` | Invt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 20 | `ORG_RCPT_NUM` | Org_Rcptessorial Num | VARCHAR2 | 9 |  | Y |
| 21 | `INVT_LEV3_DES` | Invt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV4_DES` | Invt_Lev4essorial Des | VARCHAR2 | 40 |  | Y |
| 23 | `INVT_LEV5_DES` | Invt_Lev5essorial Des | VARCHAR2 | 40 |  | Y |
| 24 | `INVT_CLS_DATE` | Invt_Clsessorial Date | VARCHAR2 | 6 |  | Y |
| 25 | `INVT_CLS_FLAG` | Invt_Clsessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `NUM_CASE_STOR_CALC` | Num_Case_Storessorial Calc | VARCHAR2 | 6 |  | Y |
| 27 | `CONV_WGT_NET` | Conv_Wgtessorial Net | VARCHAR2 | 17 |  | Y |
| 28 | `VAR_QTY_BKD_FACT` | Var_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 29 | `RENW_ORG_RATE` | Renw_Orgessorial Rate | VARCHAR2 | 10 |  | Y |
| 30 | `ORG_CHG_CODE` | Org_Chgessorial Code | VARCHAR2 | 4 |  | Y |
| 31 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `NUM_RENW_DAY` | Num_Renwessorial Day | VARCHAR2 | 4 |  | Y |
| 33 | `WGT_STOR_CALC` | Wgt_Storessorial Calc | VARCHAR2 | 17 |  | Y |
| 34 | `ITEM_BILL_PROF_CODE` | Item_Bill_Professorial Code | VARCHAR2 | 4 |  | Y |
| 35 | `CNVC_QTY` | Cnvcessorial Qty | VARCHAR2 | 6 |  | Y |
| 36 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_BAL_PROS`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `PROS1_CODE` | Pros1essorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `PROS1_VALUE` | Pros1essorial Value | VARCHAR2 | 250 |  | Y |
| 10 | `PROS2_CODE` | Pros2essorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `PROS2_VALUE` | Pros2essorial Value | VARCHAR2 | 250 |  | Y |
| 12 | `PROS3_CODE` | Pros3essorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `PROS3_VALUE` | Pros3essorial Value | VARCHAR2 | 250 |  | Y |
| 14 | `PROS_UNIQUE_FLAG` | Pros_Uniqueessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `PROS_UPD_FLAG` | Pros_Updessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_CARR`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 3 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 4 | `CARR_STAT` | Carressorial Stat | VARCHAR2 | 1 |  | Y |
| 5 | `CARR_ADD1` | Carressorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `CARR_ADD2` | Carressorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `CARR_ADD3` | Carressorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_WGT_MEAS_FLAG` | Carr_Wgt_Measessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 11 | `CARR_CODE_PAY` | Carr_Codeessorial Pay | VARCHAR2 | 10 |  | Y |
| 12 | `FRT_TP_CODE` | Frt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `CARR_LAST_ACT_DATE` | Carr_Last_Actessorial Date | VARCHAR2 | 6 |  | Y |
| 14 | `CARR_STD_ALPHA_CODE` | Carr_Std_Alphaessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CARR_TP_CODE` | Carr_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `GEN_NUM_PROF_CODE` | Gen_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `CARR_LAB_STD_MODY_NUM` | Carr_Lab_Std_Modyessorial Num | VARCHAR2 | 6 |  | Y |
| 19 | `CARR_ADD4` | Carressorial Add4 | VARCHAR2 | 30 |  | Y |
| 20 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 21 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `TRSPT_MODE_CODE` | Trspt_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 24 | `TRSPT_UNIT_VAL_HIST_FLAG` | Trspt_Unit_Val_Histessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `CARR_EXT_FRT_FLAG` | Carr_Ext_Frtessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | Y |
| 28 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 29 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |
| 30 | `CARR_ALLOW_BANDING_FLAG` | Carr_Allow_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `CARR_COMPL_LABEL_FLAG` | Carr_Compl_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `CARR_REQ_EDI_FLAG` | Carr_Req_Ediessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `SKU_CLASS_NUM` | Sku_Classessorial Num | VARCHAR2 | 1 |  | Y |
| 34 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_CCID`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 5 | `LAST_SHIP_EXPY_DATE` | Last_Ship_Expyessorial Date | VARCHAR2 | 6 |  | Y |

## `S_CONV_CON`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 45
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 3 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 4 | `CON_STAT` | Conessorial Stat | VARCHAR2 | 1 |  | Y |
| 5 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `CON_ADD4` | Conessorial Add4 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 10 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 11 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | Y |
| 12 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `STATE_DES` | Stateessorial Des | VARCHAR2 | 30 |  | Y |
| 14 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 15 | `CON_LAST_ACT_DATE` | Con_Last_Actessorial Date | VARCHAR2 | 6 |  | Y |
| 16 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `CON_FRT_APPO_FLAG` | Con_Frt_Appoessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CON_FRT_DISC_PCENT` | Con_Frt_Discessorial Pcent | VARCHAR2 | 6 |  | Y |
| 19 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 20 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | Y |
| 22 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 23 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |
| 24 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 25 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 27 | `CON_BORD_FLAG` | Con_Bordessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `CON_COMPL_ORD_FLAG` | Con_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `CON_CODE_MAST` | Con_Codeessorial Mast | VARCHAR2 | 10 |  | Y |
| 30 | `CON_CODE_MAST_FLAG` | Con_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 32 | `EXT_REF_NUM2` | Ext_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 33 | `EXT_REF_NUM3` | Ext_Refessorial Num3 | VARCHAR2 | 20 |  | Y |
| 34 | `EXT_REF_NUM4` | Ext_Refessorial Num4 | VARCHAR2 | 20 |  | Y |
| 35 | `CON_ALLOW_BANDING_FLAG` | Con_Allow_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `CON_BANDING_SKU_CLASS_NUM` | Con_Banding_Sku_Classessorial Num | VARCHAR2 | 1 |  | Y |
| 37 | `CON_CONSL_TP` | Con_Conslessorial Tp | VARCHAR2 | 1 |  | Y |
| 38 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 39 | `CON_SPS_REQ_FLAG` | Con_Sps_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `CON_ASN_REP_TP` | Con_Asn_Repessorial Tp | VARCHAR2 | 1 |  | Y |
| 41 | `CON_MSDS_REQ_FLAG` | Con_Msds_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 43 | `SKU_CLASS_NUM` | Sku_Classessorial Num | VARCHAR2 | 1 |  | Y |
| 44 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `CON_UCC128_LABEL_REQ_FLAG` | Con_Ucc128_Label_Reqessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_CUST`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 57
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | Y |
| 4 | `CUST_STAT` | Customer Status | VARCHAR2 | 1 |  | Y |
| 5 | `CUST_ADD1` | Custessorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `CUST_ADD2` | Custessorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `CUST_ADD3` | Custessorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 9 | `SMAN_CODE` | Smanessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `CUST_TP_FLAG` | Cust_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 10 |  | Y |
| 13 | `CUST_CODE_PAY_OFFC` | Cust_Code_Payessorial Offc | VARCHAR2 | 10 |  | Y |
| 14 | `CUST_BILL_PROF_CODE` | Cust_Bill_Professorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CUST_OPS_PROF_CODE` | Cust_Ops_Professorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 17 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `CUST_ITEM_PROF_CODE` | Cust_Item_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 20 | `CUST_START_BUS_DATE` | Cust_Start_Busessorial Date | VARCHAR2 | 6 |  | Y |
| 21 | `CUST_LAST_ACT_DATE` | Cust_Last_Actessorial Date | VARCHAR2 | 6 |  | Y |
| 22 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `FRT_PAY_OFFC_CODE` | Frt_Pay_Offcessorial Code | VARCHAR2 | 10 |  | Y |
| 24 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `CUST_UPC_PREX` | Cust_Upcessorial Prex | VARCHAR2 | 6 |  | Y |
| 26 | `CUST_TRF_PROF_CODE` | Cust_Trf_Professorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `CUST_DEF_RCPT_SKU_FLAG` | Cust_Def_Rcpt_Skuessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `CUST_DEF_ORD_SKU_FLAG` | Cust_Def_Ord_Skuessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `CUST_DEF_ADJ_SKU_FLAG` | Cust_Def_Adj_Skuessorial Flag | VARCHAR2 | 1 |  | Y |
| 30 | `CUST_LAB_CAPT_JOB_LEV_FLAG` | Cust_Lab_Capt_Job_Levessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `CUST_ORD_LEV_RES_NUM` | Cust_Ord_Lev_Resessorial Num | VARCHAR2 | 1 |  | Y |
| 32 | `CUST_CNVC_NUM` | Cust_Cnvcessorial Num | VARCHAR2 | 1 |  | Y |
| 33 | `CUST_LAB_STD_MODY_NUM` | Cust_Lab_Std_Modyessorial Num | VARCHAR2 | 6 |  | Y |
| 34 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 35 | `CUST_ADD4` | Custessorial Add4 | VARCHAR2 | 30 |  | Y |
| 36 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 37 | `INVT_TERMGY_CODE_I1` | Invt_Termgy_Codeessorial I1 | VARCHAR2 | 4 |  | Y |
| 38 | `INVT_TERMGY_CODE_I2` | Invt_Termgy_Codeessorial I2 | VARCHAR2 | 4 |  | Y |
| 39 | `INVT_TERMGY_CODE_I3` | Invt_Termgy_Codeessorial I3 | VARCHAR2 | 4 |  | Y |
| 40 | `INVT_TERMGY_CODE_I4` | Invt_Termgy_Codeessorial I4 | VARCHAR2 | 4 |  | Y |
| 41 | `INVT_TERMGY_CODE_I5` | Invt_Termgy_Codeessorial I5 | VARCHAR2 | 4 |  | Y |
| 42 | `INVT_TERMGY_CODE_O1` | Invt_Termgy_Codeessorial O1 | VARCHAR2 | 4 |  | Y |
| 43 | `INVT_TERMGY_CODE_O2` | Invt_Termgy_Codeessorial O2 | VARCHAR2 | 4 |  | Y |
| 44 | `INVT_TERMGY_CODE_O3` | Invt_Termgy_Codeessorial O3 | VARCHAR2 | 4 |  | Y |
| 45 | `INVT_TERMGY_CODE_O4` | Invt_Termgy_Codeessorial O4 | VARCHAR2 | 4 |  | Y |
| 46 | `INVT_TERMGY_CODE_O5` | Invt_Termgy_Codeessorial O5 | VARCHAR2 | 4 |  | Y |
| 47 | `RF_PROF_CODE` | Rf_Professorial Code | VARCHAR2 | 4 |  | Y |
| 48 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 50 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | Y |
| 51 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 52 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |
| 53 | `CUST_ALLOC_CONSL_TP_CODE` | Cust_Alloc_Consl_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 54 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | Y |
| 55 | `TEL_CONTACT_EMAIL_ADD` | Tel_Contact_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 56 | `CUST_EAN_UCC_COMP_PREX` | Cust_Ean_Ucc_Compessorial Prex | VARCHAR2 | 20 |  | Y |
| 57 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |

## `S_CONV_DLVP`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `LEV_VER_PROF_LEV2_CODE` | Lev_Ver_Prof_Lev2essorial Code | VARCHAR2 | 40 |  | Y |
| 5 | `LEV_VER_PROF_LEV3_CODE` | Lev_Ver_Prof_Lev3essorial Code | VARCHAR2 | 40 |  | Y |
| 6 | `LEV_VER_PROF_LEV4_CODE` | Lev_Ver_Prof_Lev4essorial Code | VARCHAR2 | 40 |  | Y |
| 7 | `ACC_ITEM_UPC` | Acc_Itemessorial Upc | VARCHAR2 | 20 |  | Y |
| 8 | `ALT_TP_CODE` | Alt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `ACC_ITEM_CODE` | Accessorial Item Code | VARCHAR2 | 20 |  | Y |
| 10 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_HAZA`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 4 | `ITEM_HAZ_CPG_FLAG` | Item_Haz_Cpgessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `ITEM_HAZ_PHYS_MATTER_TP` | Item_Haz_Phys_Matteressorial Tp | VARCHAR2 | 4 |  | Y |
| 6 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 7 | `ITEM_HAZ_TECH_NAME` | Item_Haz_Techessorial Name | VARCHAR2 | 255 |  | Y |
| 8 | `ITEM_HAZ_MULTIPLIER` | Item_Hazessorial Multiplier | VARCHAR2 | 6 |  | Y |
| 9 | `ITEM_HAZ_WGT_NET` | Item_Haz_Wgtessorial Net | VARCHAR2 | 17 |  | Y |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 11 | `ITEM_HAZ_EXT_REF_CODE` | Item_Haz_Ext_Refessorial Code | VARCHAR2 | 20 |  | Y |
| 12 | `TRSPT_MODE_TP` | Trspt_Modeessorial Tp | VARCHAR2 | 4 |  | Y |

## `S_CONV_HIST`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 31
- **Campos-chave prováveis:** MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | Y |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 12 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | VARCHAR2 | 6 |  | Y |
| 13 | `MVT_UNIT` | Mvtessorial Unit | VARCHAR2 | 9 |  | Y |
| 14 | `MVT_CNVC_QTY` | Mvt_Cnvcessorial Qty | VARCHAR2 | 6 |  | Y |
| 15 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `TRANS_WGT` | Transessorial Wgt | VARCHAR2 | 16 |  | Y |
| 17 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | VARCHAR2 | 16 |  | Y |
| 18 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 19 | `TRANS_CUBE` | Transessorial Cube | VARCHAR2 | 16 |  | Y |
| 20 | `DOC_NUM` | Document Number | VARCHAR2 | 9 |  | Y |
| 21 | `DOC_LINE_NUM` | Document Line Number | VARCHAR2 | 4 |  | Y |
| 22 | `DOC_LOC_LINE_NUM` | Document Location Line Number | VARCHAR2 | 4 |  | Y |
| 23 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 24 | `MVT_REF1` | Mvtessorial Ref1 | VARCHAR2 | 10 |  | Y |
| 25 | `MVT_REF2` | Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 26 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 27 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 28 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 29 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 30 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 31 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |

## `S_CONV_IAPR`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | Y |
| 9 | `INVT_ATTR_VAL` | Invt_Attressorial Val | VARCHAR2 | 40 |  | Y |
| 10 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_ITEM`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 134
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 4 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | Y |
| 5 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 6 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | Y |
| 7 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | VARCHAR2 | 3 |  | Y |
| 8 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | VARCHAR2 | 3 |  | Y |
| 9 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | VARCHAR2 | 3 |  | Y |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 11 | `ITEM_QTY_BKD_WGT_GROSS` | Item_Qty_Bkd_Wgtessorial Gross | VARCHAR2 | 15 |  | Y |
| 12 | `ITEM_QTY_BKD_LEN` | Item_Qty_Bkdessorial Len | VARCHAR2 | 8 |  | Y |
| 13 | `ITEM_QTY_BKD_WID` | Item_Qty_Bkdessorial Wid | VARCHAR2 | 8 |  | Y |
| 14 | `ITEM_QTY_BKD_HGT` | Item_Qty_Bkdessorial Hgt | VARCHAR2 | 8 |  | Y |
| 15 | `ITEM_QTY_BKD_WGT_NET` | Item_Qty_Bkd_Wgtessorial Net | VARCHAR2 | 15 |  | Y |
| 16 | `ITEM_QTY_BKD_WGT_TARE` | Item_Qty_Bkd_Wgtessorial Tare | VARCHAR2 | 15 |  | Y |
| 17 | `PALL_QTY` | Pallessorial Qty | VARCHAR2 | 6 |  | Y |
| 18 | `GENR_INFO_PROF_CODE` | Genr_Info_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `ITEM_BILL_PROF_CODE1` | Item_Bill_Professorial Code1 | VARCHAR2 | 4 |  | Y |
| 20 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | Y |
| 22 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | Y |
| 23 | `ITEM_QTY_BKD_CUBE` | Item_Qty_Bkdessorial Cube | VARCHAR2 | 10 |  | Y |
| 24 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 25 | `ITEM_VAR_QTY_BKD_FLAG` | Item_Var_Qty_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `ITEM_WGT_TP_CODE` | Item_Wgt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | Y |
| 28 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 29 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 30 | `ITEM_VALUE` | Itemessorial Value | VARCHAR2 | 13 |  | Y |
| 31 | `ITEM_QTY_BKD_BASE_NUM` | Item_Qty_Bkd_Baseessorial Num | VARCHAR2 | 1 |  | Y |
| 32 | `VAR_QTY_BKD_QTY1` | Var_Qty_Bkdessorial Qty1 | VARCHAR2 | 4 |  | Y |
| 33 | `VAR_QTY_BKD_QTY2` | Var_Qty_Bkdessorial Qty2 | VARCHAR2 | 4 |  | Y |
| 34 | `VAR_QTY_BKD_QTY3` | Var_Qty_Bkdessorial Qty3 | VARCHAR2 | 4 |  | Y |
| 35 | `VAR_QTY_BKD_QTY4` | Var_Qty_Bkdessorial Qty4 | VARCHAR2 | 4 |  | Y |
| 36 | `VAR_QTY_BKD_QTY5` | Var_Qty_Bkdessorial Qty5 | VARCHAR2 | 4 |  | Y |
| 37 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | Y |
| 38 | `SHIP_PROF_CODE` | Ship_Professorial Code | VARCHAR2 | 4 |  | Y |
| 39 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 41 | `ALT_INVT_REP_UPC_CODE` | Alt_Invt_Rep_Upcessorial Code | VARCHAR2 | 20 |  | Y |
| 42 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `NUM_OPEN_DAY` | Num_Openessorial Day | VARCHAR2 | 3 |  | Y |
| 44 | `ITEM_BILL_PROF_CODE2` | Item_Bill_Professorial Code2 | VARCHAR2 | 4 |  | Y |
| 45 | `ITEM_BILL_PROF_CODE3` | Item_Bill_Professorial Code3 | VARCHAR2 | 4 |  | Y |
| 46 | `ITEM_VAL_PROF_CODE` | Item_Val_Professorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `VOL_MEAS_CODE` | Vol_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 48 | `ITEM_QTY_BKD_VOL` | Item_Qty_Bkdessorial Vol | VARCHAR2 | 15 |  | Y |
| 49 | `ALLOW_ENTRY_LEV_NUM` | Allow_Entry_Levessorial Num | VARCHAR2 | 1 |  | Y |
| 50 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 51 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 52 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 53 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 6 |  | Y |
| 54 | `ITEM_CRS_DOCK_FLAG` | Item_Crs_Dockessorial Flag | VARCHAR2 | 1 |  | Y |
| 55 | `ITEM_KIT_FLAG` | Item_Kitessorial Flag | VARCHAR2 | 1 |  | Y |
| 56 | `ITEM_KIT_TP_FLAG` | Item_Kit_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 57 | `ITEM_QTY_BKD_WHOLE_FLAG` | Item_Qty_Bkd_Wholeessorial Flag | VARCHAR2 | 1 |  | Y |
| 58 | `ITEM_CODE_MAST_FLAG` | Item_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 59 | `ITEM_HOLD_PROF_CODE` | Item_Hold_Professorial Code | VARCHAR2 | 4 |  | Y |
| 60 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `ITEM_QTY_BKD_NUM_LAY_2` | Item_Qty_Bkd_Num_Layessorial 2 | VARCHAR2 | 3 |  | Y |
| 62 | `ITEM_QTY_BKD_QTY_PER_LAY_2` | Item_Qty_Bkd_Qty_Per_Layessorial 2 | VARCHAR2 | 3 |  | Y |
| 63 | `ITEM_QTY_BKD_QTY_ODD_LAY_2` | Item_Qty_Bkd_Qty_Odd_Layessorial 2 | VARCHAR2 | 3 |  | Y |
| 64 | `ITEM_QTY_BKD_WHOLE_FLAG_2` | Item_Qty_Bkd_Whole_Flagessorial 2 | VARCHAR2 | 1 |  | Y |
| 65 | `WGT_MEAS_CODE_2` | Wgt_Meas_Codeessorial 2 | VARCHAR2 | 4 |  | Y |
| 66 | `ITEM_QTY_BKD_WGT_GROSS_2` | Item_Qty_Bkd_Wgt_Grossessorial 2 | VARCHAR2 | 15 |  | Y |
| 67 | `ITEM_QTY_BKD_WGT_NET_2` | Item_Qty_Bkd_Wgt_Netessorial 2 | VARCHAR2 | 15 |  | Y |
| 68 | `ITEM_QTY_BKD_WGT_TARE_2` | Item_Qty_Bkd_Wgt_Tareessorial 2 | VARCHAR2 | 15 |  | Y |
| 69 | `LINEAR_MEAS_CODE_2` | Linear_Meas_Codeessorial 2 | VARCHAR2 | 4 |  | Y |
| 70 | `ITEM_QTY_BKD_HGT_2` | Item_Qty_Bkd_Hgtessorial 2 | VARCHAR2 | 8 |  | Y |
| 71 | `ITEM_QTY_BKD_WID_2` | Item_Qty_Bkd_Widessorial 2 | VARCHAR2 | 8 |  | Y |
| 72 | `ITEM_QTY_BKD_LEN_2` | Item_Qty_Bkd_Lenessorial 2 | VARCHAR2 | 8 |  | Y |
| 73 | `ITEM_QTY_BKD_CUBE_2` | Item_Qty_Bkd_Cubeessorial 2 | VARCHAR2 | 10 |  | Y |
| 74 | `VOL_MEAS_CODE_2` | Vol_Meas_Codeessorial 2 | VARCHAR2 | 4 |  | Y |
| 75 | `ITEM_QTY_BKD_VOL_2` | Item_Qty_Bkd_Volessorial 2 | VARCHAR2 | 15 |  | Y |
| 76 | `ITEM_QTY_BKD_NUM_LAY_3` | Item_Qty_Bkd_Num_Layessorial 3 | VARCHAR2 | 3 |  | Y |
| 77 | `ITEM_QTY_BKD_QTY_PER_LAY_3` | Item_Qty_Bkd_Qty_Per_Layessorial 3 | VARCHAR2 | 3 |  | Y |
| 78 | `ITEM_QTY_BKD_QTY_ODD_LAY_3` | Item_Qty_Bkd_Qty_Odd_Layessorial 3 | VARCHAR2 | 3 |  | Y |
| 79 | `ITEM_QTY_BKD_WHOLE_FLAG_3` | Item_Qty_Bkd_Whole_Flagessorial 3 | VARCHAR2 | 1 |  | Y |
| 80 | `WGT_MEAS_CODE_3` | Wgt_Meas_Codeessorial 3 | VARCHAR2 | 4 |  | Y |
| 81 | `ITEM_QTY_BKD_WGT_GROSS_3` | Item_Qty_Bkd_Wgt_Grossessorial 3 | VARCHAR2 | 15 |  | Y |
| 82 | `ITEM_QTY_BKD_WGT_NET_3` | Item_Qty_Bkd_Wgt_Netessorial 3 | VARCHAR2 | 15 |  | Y |
| 83 | `ITEM_QTY_BKD_WGT_TARE_3` | Item_Qty_Bkd_Wgt_Tareessorial 3 | VARCHAR2 | 15 |  | Y |
| 84 | `LINEAR_MEAS_CODE_3` | Linear_Meas_Codeessorial 3 | VARCHAR2 | 4 |  | Y |
| 85 | `ITEM_QTY_BKD_HGT_3` | Item_Qty_Bkd_Hgtessorial 3 | VARCHAR2 | 8 |  | Y |
| 86 | `ITEM_QTY_BKD_WID_3` | Item_Qty_Bkd_Widessorial 3 | VARCHAR2 | 8 |  | Y |
| 87 | `ITEM_QTY_BKD_LEN_3` | Item_Qty_Bkd_Lenessorial 3 | VARCHAR2 | 8 |  | Y |
| 88 | `ITEM_QTY_BKD_CUBE_3` | Item_Qty_Bkd_Cubeessorial 3 | VARCHAR2 | 10 |  | Y |
| 89 | `VOL_MEAS_CODE_3` | Vol_Meas_Codeessorial 3 | VARCHAR2 | 4 |  | Y |
| 90 | `ITEM_QTY_BKD_VOL_3` | Item_Qty_Bkd_Volessorial 3 | VARCHAR2 | 15 |  | Y |
| 91 | `ITEM_QTY_BKD_NUM_LAY_4` | Item_Qty_Bkd_Num_Layessorial 4 | VARCHAR2 | 3 |  | Y |
| 92 | `ITEM_QTY_BKD_QTY_PER_LAY_4` | Item_Qty_Bkd_Qty_Per_Layessorial 4 | VARCHAR2 | 3 |  | Y |
| 93 | `ITEM_QTY_BKD_QTY_ODD_LAY_4` | Item_Qty_Bkd_Qty_Odd_Layessorial 4 | VARCHAR2 | 3 |  | Y |
| 94 | `ITEM_QTY_BKD_WHOLE_FLAG_4` | Item_Qty_Bkd_Whole_Flagessorial 4 | VARCHAR2 | 1 |  | Y |
| 95 | `WGT_MEAS_CODE_4` | Wgt_Meas_Codeessorial 4 | VARCHAR2 | 4 |  | Y |
| 96 | `ITEM_QTY_BKD_WGT_GROSS_4` | Item_Qty_Bkd_Wgt_Grossessorial 4 | VARCHAR2 | 15 |  | Y |
| 97 | `ITEM_QTY_BKD_WGT_NET_4` | Item_Qty_Bkd_Wgt_Netessorial 4 | VARCHAR2 | 15 |  | Y |
| 98 | `ITEM_QTY_BKD_WGT_TARE_4` | Item_Qty_Bkd_Wgt_Tareessorial 4 | VARCHAR2 | 15 |  | Y |
| 99 | `LINEAR_MEAS_CODE_4` | Linear_Meas_Codeessorial 4 | VARCHAR2 | 4 |  | Y |
| 100 | `ITEM_QTY_BKD_HGT_4` | Item_Qty_Bkd_Hgtessorial 4 | VARCHAR2 | 8 |  | Y |
| 101 | `ITEM_QTY_BKD_WID_4` | Item_Qty_Bkd_Widessorial 4 | VARCHAR2 | 8 |  | Y |
| 102 | `ITEM_QTY_BKD_LEN_4` | Item_Qty_Bkd_Lenessorial 4 | VARCHAR2 | 8 |  | Y |
| 103 | `ITEM_QTY_BKD_CUBE_4` | Item_Qty_Bkd_Cubeessorial 4 | VARCHAR2 | 10 |  | Y |
| 104 | `VOL_MEAS_CODE_4` | Vol_Meas_Codeessorial 4 | VARCHAR2 | 4 |  | Y |
| 105 | `ITEM_QTY_BKD_VOL_4` | Item_Qty_Bkd_Volessorial 4 | VARCHAR2 | 15 |  | Y |
| 106 | `ITEM_QTY_BKD_NUM_LAY_5` | Item_Qty_Bkd_Num_Layessorial 5 | VARCHAR2 | 3 |  | Y |
| 107 | `ITEM_QTY_BKD_QTY_PER_LAY_5` | Item_Qty_Bkd_Qty_Per_Layessorial 5 | VARCHAR2 | 3 |  | Y |
| 108 | `ITEM_QTY_BKD_QTY_ODD_LAY_5` | Item_Qty_Bkd_Qty_Odd_Layessorial 5 | VARCHAR2 | 3 |  | Y |
| 109 | `ITEM_QTY_BKD_WHOLE_FLAG_5` | Item_Qty_Bkd_Whole_Flagessorial 5 | VARCHAR2 | 1 |  | Y |
| 110 | `WGT_MEAS_CODE_5` | Wgt_Meas_Codeessorial 5 | VARCHAR2 | 4 |  | Y |
| 111 | `ITEM_QTY_BKD_WGT_GROSS_5` | Item_Qty_Bkd_Wgt_Grossessorial 5 | VARCHAR2 | 15 |  | Y |
| 112 | `ITEM_QTY_BKD_WGT_NET_5` | Item_Qty_Bkd_Wgt_Netessorial 5 | VARCHAR2 | 15 |  | Y |
| 113 | `ITEM_QTY_BKD_WGT_TARE_5` | Item_Qty_Bkd_Wgt_Tareessorial 5 | VARCHAR2 | 15 |  | Y |
| 114 | `LINEAR_MEAS_CODE_5` | Linear_Meas_Codeessorial 5 | VARCHAR2 | 4 |  | Y |
| 115 | `ITEM_QTY_BKD_HGT_5` | Item_Qty_Bkd_Hgtessorial 5 | VARCHAR2 | 8 |  | Y |
| 116 | `ITEM_QTY_BKD_WID_5` | Item_Qty_Bkd_Widessorial 5 | VARCHAR2 | 8 |  | Y |
| 117 | `ITEM_QTY_BKD_LEN_5` | Item_Qty_Bkd_Lenessorial 5 | VARCHAR2 | 8 |  | Y |
| 118 | `ITEM_QTY_BKD_CUBE_5` | Item_Qty_Bkd_Cubeessorial 5 | VARCHAR2 | 10 |  | Y |
| 119 | `VOL_MEAS_CODE_5` | Vol_Meas_Codeessorial 5 | VARCHAR2 | 4 |  | Y |
| 120 | `ITEM_QTY_BKD_VOL_5` | Item_Qty_Bkd_Volessorial 5 | VARCHAR2 | 15 |  | Y |
| 121 | `ITEM_HAZ_FLAG` | Item_Hazessorial Flag | VARCHAR2 | 1 |  | Y |
| 122 | `ITEM_ALLOW_BAND_FLAG` | Item_Allow_Bandessorial Flag | VARCHAR2 | 1 |  | Y |
| 123 | `ITEM_BAND_SKU_CLASS_NUM` | Item_Band_Sku_Classessorial Num | VARCHAR2 | 1 |  | Y |
| 124 | `ITEM_BAND_MAX_QTY` | Item_Band_Maxessorial Qty | VARCHAR2 | 9 |  | Y |
| 125 | `ITEM_ALLOW_MIX_PLT_FLAG` | Item_Allow_Mix_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 126 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 127 | `ACC_ITEM_DES1` | Acc_Itemessorial Des1 | VARCHAR2 | 40 |  | Y |
| 128 | `SCAN_PARAM_CODE` | Scan_Paramessorial Code | VARCHAR2 | 4 |  | Y |
| 129 | `ITEM_CARTZN_PROF_CODE` | Item_Cartzn_Professorial Code | VARCHAR2 | 4 |  | Y |
| 130 | `ITEM_DES_EXTN` | Item_Desessorial Extn | VARCHAR2 | 250 |  | Y |
| 131 | `ITEM_VAR_QTY_BKD_RENW_FLAG` | Item_Var_Qty_Bkd_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 132 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 133 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 134 | `ITEM_REPI_MERGE_LOC_FLAG` | Item_Repi_Merge_Locessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_KIT`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 4 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | Y |
| 5 | `ITEM_CODE_COMPN` | Item_Codeessorial Compn | VARCHAR2 | 20 |  | Y |
| 6 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | VARCHAR2 | 9 |  | Y |
| 7 | `ITEM_COMPN_PER_KIT_QTY` | Item_Compn_Per_Kitessorial Qty | VARCHAR2 | 9 |  | Y |
| 8 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 9 | `ITEM_COMPN_WGT` | Item_Compnessorial Wgt | VARCHAR2 | 17 |  | Y |
| 10 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 11 | `ITEM_COMPN_SEQ_NUM` | Item_Compn_Seqessorial Num | VARCHAR2 | 2 |  | Y |

## `S_CONV_LOC`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 40
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 4 | `LOC_DES` | Locessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `LOC_STAT` | Locessorial Stat | VARCHAR2 | 1 |  | Y |
| 6 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 7 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_HGT` | Locessorial Hgt | VARCHAR2 | 8 |  | Y |
| 9 | `LOC_WID` | Locessorial Wid | VARCHAR2 | 8 |  | Y |
| 10 | `LOC_LEN` | Locessorial Len | VARCHAR2 | 8 |  | Y |
| 11 | `LOC_CUBE` | Locessorial Cube | VARCHAR2 | 11 |  | Y |
| 12 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_MAX_SKU_CAPC` | Loc_Max_Skuessorial Capc | VARCHAR2 | 4 |  | Y |
| 16 | `SKU_CAPC_PCENT` | Sku_Capcessorial Pcent | VARCHAR2 | 6 |  | Y |
| 17 | `SPACE_CAPC_PCENT` | Space_Capcessorial Pcent | VARCHAR2 | 6 |  | Y |
| 18 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 21 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | VARCHAR2 | 4 |  | Y |
| 23 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_WGT` | Locessorial Wgt | VARCHAR2 | 15 |  | Y |
| 25 | `LOC_CODE_WGT_MAST` | Loc_Code_Wgtessorial Mast | VARCHAR2 | 12 |  | Y |
| 26 | `LOC_STRUCT_TP_CODE` | Loc_Struct_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `LOC_SHIP_UNIT_ID` | Loc_Ship_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 28 | `LOC_USE_LAST_PUT_FLAG` | Loc_Use_Last_Putessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `PICK_SEQ_NUM` | Pick_Seqessorial Num | VARCHAR2 | 9 |  | Y |
| 30 | `LOC_VOICE_CHK_DIGIT1` | Loc_Voice_Chkessorial Digit1 | VARCHAR2 | 5 |  | Y |
| 31 | `LOC_VOICE_CHK_DIGIT2` | Loc_Voice_Chkessorial Digit2 | VARCHAR2 | 5 |  | Y |
| 32 | `LOC_VOICE_CHK_DIGIT3` | Loc_Voice_Chkessorial Digit3 | VARCHAR2 | 5 |  | Y |
| 33 | `LOC_AISLE_REF` | Loc_Aisleessorial Ref | VARCHAR2 | 4 |  | Y |
| 34 | `LOC_FACING_REF` | Loc_Facingessorial Ref | VARCHAR2 | 4 |  | Y |
| 35 | `LOC_FRONT_ALIAS` | Loc_Frontessorial Alias | VARCHAR2 | 12 |  | Y |
| 36 | `LOC_FRONT_ALIAS_CHK_DIGIT` | Loc_Front_Alias_Chkessorial Digit | VARCHAR2 | 5 |  | Y |
| 37 | `LOC_BACK_ALIAS` | Loc_Backessorial Alias | VARCHAR2 | 12 |  | Y |
| 38 | `LOC_BACK_ALIAS_CHK_DIGIT` | Loc_Back_Alias_Chkessorial Digit | VARCHAR2 | 5 |  | Y |
| 39 | `PUT_SEQ_NUM` | Put_Seqessorial Num | VARCHAR2 | 9 |  | Y |
| 40 | `LOC_VERT_HGT_FACT_CODE` | Loc_Vert_Hgt_Factessorial Code | VARCHAR2 | 4 |  | Y |

## `S_CONV_MAIL`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | Y |
| 4 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | Y |
| 5 | `ACC_TP_CODE` | Acc_Tpessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `FAX_ACC_CODE` | Fax_Accessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_EFF_DATE` | Cust_Effessorial Date | VARCHAR2 | 6 |  | Y |
| 8 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 60 |  | Y |
| 9 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 250 |  | Y |
| 10 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 250 |  | Y |
| 11 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | Y |
| 12 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | Y |
| 13 | `FAX_COMMENT1` | Faxessorial Comment1 | VARCHAR2 | 60 |  | Y |
| 14 | `FAX_COMMENT2` | Faxessorial Comment2 | VARCHAR2 | 60 |  | Y |
| 15 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `FAX_OVERLAY_CODE` | Fax_Overlayessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `CUST_BAT_FLAG` | Cust_Batessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `FAX_WEEK_DAY` | Fax_Weekessorial Day | VARCHAR2 | 10 |  | Y |
| 19 | `FAX_OCCR_TIME` | Fax_Occressorial Time | VARCHAR2 | 5 |  | Y |
| 20 | `FAX_TIME` | Faxessorial Time | VARCHAR2 | 5 |  | Y |

## `S_CONV_MVT`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 31
- **Campos-chave prováveis:** MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 12 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 13 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 14 | `MVT_CNVC_QTY` | Mvt_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 15 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 16 | `TRANS_WGT` | Transessorial Wgt | NUMBER | 22 | 16 | N |
| 17 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 18 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 19 | `TRANS_CUBE` | Transessorial Cube | NUMBER | 22 | 16 | N |
| 20 | `DOC_NUM` | Document Number | NUMBER | 22 | 6 | N |
| 21 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 22 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 23 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 24 | `MVT_REF1` | Mvtessorial Ref1 | VARCHAR2 | 10 |  | N |
| 25 | `MVT_REF2` | Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 26 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 27 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 28 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 29 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 30 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 31 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |

## `S_CONV_PIIT`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 7 | `SKU_CODE_PICK` | Sku_Codeessorial Pick | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_PICK_REPL_QTY` | Loc_Pick_Replessorial Qty | VARCHAR2 | 9 |  | Y |
| 9 | `SKU_CODE_REPL` | Sku_Codeessorial Repl | VARCHAR2 | 4 |  | Y |
| 10 | `LOC_PICK_MIN_QTY` | Loc_Pick_Minessorial Qty | VARCHAR2 | 9 |  | Y |
| 11 | `LOC_PICK_LAST_PICK_DATE` | Loc_Pick_Last_Pickessorial Date | VARCHAR2 | 6 |  | Y |
| 12 | `LOC_PICK_REPL_FLAG` | Loc_Pick_Replessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `LOC_PICK_REPL_QTY_RND_METH` | Loc_Pick_Repl_Qty_Rndessorial Meth | VARCHAR2 | 1 |  | Y |
| 14 | `LOC_PICK_PRO_ACTIVE_FLAG` | Loc_Pick_Pro_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `LOC_PICK_FORCE_TO_GEN_FLAG` | Loc_Pick_Force_To_Genessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `LOC_PICK_NOT_USE_DAY` | Loc_Pick_Not_Useessorial Day | NUMBER | 22 | 4 | Y |
| 17 | `LOC_PICK_ALERT_QTY` | Loc_Pick_Alertessorial Qty | NUMBER | 22 | 9 | Y |

## `S_CONV_RATE`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 4 | `CHG_DATE` | Charge Date | VARCHAR2 | 6 |  | Y |
| 5 | `CHG_DATE_PCENT` | Chg_Dateessorial Pcent | VARCHAR2 | 8 |  | Y |
| 6 | `CHG_DATE_FLAT_AMT` | Chg_Date_Flatessorial Amt | VARCHAR2 | 13 |  | Y |
| 7 | `CHG_DATE_FLAT_BK_TOT` | Chg_Date_Flat_Bkessorial Tot | VARCHAR2 | 2 |  | Y |
| 8 | `CHG_DATE_BK_TOT` | Chg_Date_Bkessorial Tot | VARCHAR2 | 2 |  | Y |
| 9 | `CHG_DATE_MIN_AMT` | Chg_Date_Minessorial Amt | VARCHAR2 | 13 |  | Y |
| 10 | `CHG_DATE_MAX_AMT` | Chg_Date_Maxessorial Amt | VARCHAR2 | 13 |  | Y |
| 11 | `CHG_SUPPRESS_SURCHG_FLAG` | Chg_Suppress_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | Y |
| 13 | `SKU_CODE_CHG_RND_FLAG` | Sku_Code_Chg_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | Y |
| 15 | `SKU_CODE_QUAL_RND_FLAG` | Sku_Code_Qual_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `CHG_SUPPRESS_RCPT_SURCHG_FLAG` | Chg_Suppress_Rcpt_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `CHG_SUPPRESS_RENW_SURCHG_FLAG` | Chg_Suppress_Renw_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CHG_SUPPRESS_ACCS_SURCHG_FLAG` | Chg_Suppress_Accs_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CHG_SUPPRESS_IINV_SURCHG_FLAG` | Chg_Suppress_Iinv_Surchgessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `CHG_DATE_BK_NUM` | Chg_Date_Bkessorial Num | VARCHAR2 | 2 |  | Y |
| 21 | `CHG_DATE_BK_QTY` | Chg_Date_Bkessorial Qty | VARCHAR2 | 13 |  | Y |
| 22 | `CHG_DATE_BK_AMT` | Chg_Date_Bkessorial Amt | VARCHAR2 | 16 |  | Y |

## `S_CONV_REVN`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | Y |
| 4 | `REVN_DATE` | Revnessorial Date | VARCHAR2 | 6 |  | Y |
| 5 | `REVN_AMT` | Revnessorial Amt | VARCHAR2 | 10 |  | Y |
| 6 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_CONV_SHIP`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 3 | `SHIP_NAME` | Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 4 | `SHIP_STAT` | Shipessorial Stat | VARCHAR2 | 1 |  | Y |
| 5 | `SHIP_ADD1` | Shipessorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `SHIP_ADD2` | Shipessorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `SHIP_ADD3` | Shipessorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 9 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 10 | `SHIP_LAST_ACT_DATE` | Ship_Last_Actessorial Date | VARCHAR2 | 6 |  | Y |
| 11 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 13 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 14 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 15 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | VARCHAR2 | 6 |  | Y |
| 16 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `SHIP_ADD4` | Shipessorial Add4 | VARCHAR2 | 30 |  | Y |
| 18 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 19 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 20 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `SHIP_ESTAB_NUM` | Ship_Estabessorial Num | VARCHAR2 | 20 |  | Y |
| 23 | `SHIP_TP_CODE` | Ship_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `S_CONV_ZIP`

- **Tipo:** System Setup Related
- **Categoria:** Conveyence
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 2 | `ZIP_CITY` | Zarehouse City | VARCHAR2 | 30 |  | Y |
| 3 | `ZIP_STAT` | Zarehouse Stat | VARCHAR2 | 1 |  | Y |
| 4 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | Y |
| 5 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 6 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |

