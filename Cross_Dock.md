# Tabelas — Cross Dock

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **25**.

## `E_PROS_XDOCK_LOAD`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `LOAD_PROS_FLAG` | Load_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `LOAD_PRTY_NUM` | Load_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 6 | `LOAD_PROS_DATE` | Load_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `LOAD_PROS_SEQ_NUM` | Load_Pros_Seqessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `LOAD_SORT_CODE` | Load_Sortessorial Code | VARCHAR2 | 20 |  | Y |

## `E_XDOCK_LOAD_D1`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `STOP_NUM_STAT` | Stop_Numessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `STOP_NUM_REF1` | Stop_Numessorial Ref1 | VARCHAR2 | 30 |  | Y |
| 6 | `STOP_NUM_REF2` | Stop_Numessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 7 | `TOT_UNIT` | Totessorial Unit | NUMBER | 22 | 9 | N |
| 8 | `ORG_TOT_UNIT` | Org_Totessorial Unit | NUMBER | 22 | 9 | N |
| 9 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | N |
| 10 | `ORG_TOT_WGT` | Org_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 11 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | N |
| 12 | `ORG_TOT_CUBE` | Org_Totessorial Cube | NUMBER | 22 | 16 | N |
| 13 | `STOP_ARR_DATE` | Stop_Arressorial Date | DATE | 7 |  | Y |
| 14 | `STOP_DEPART_DATE` | Stop_Departessorial Date | DATE | 7 |  | Y |
| 15 | `STOP_TIME_ZONE` | Stop_Timeessorial Zone | VARCHAR2 | 2 |  | Y |

## `E_XDOCK_LOAD_D1D`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, ORD_NUM, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `RCPT_FLOW_PROS_CODE` | Rcpt_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 9 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 10 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 11 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 12 | `ORD_FLOW_PROS_CODE` | Ord_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `OPP_INB_OUTB_TP_LOAD_SEQ_NUM` | Opp_Inb_Outb_Tp_Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 14 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 15 | `UNQ_D4_REF_NUM` | Unq_D4_Refessorial Num | VARCHAR2 | 20 |  | N |
| 16 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 16 | N |
| 17 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 18 | `ORG_WGT` | Orgessorial Wgt | NUMBER | 22 | 16 | N |
| 19 | `ORG_WGT_MEAS_CODE` | Org_Wgt_Measessorial Code | VARCHAR2 | 4 |  | N |
| 20 | `UNIT` | Unitessorial Unit | NUMBER | 22 | 9 | N |
| 21 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 22 | `ORG_UNIT` | Orgessorial Unit | NUMBER | 22 | 9 | N |
| 23 | `ORG_SKU_CODE` | Org_Skuessorial Code | VARCHAR2 | 4 |  | N |
| 24 | `STOP_STAT` | Stopessorial Stat | VARCHAR2 | 1 |  | N |
| 25 | `UNIT_WGT_ALTER_FLAG` | Unit_Wgt_Alteressorial Flag | VARCHAR2 | 1 |  | N |

## `E_XDOCK_LOAD_D1DD1`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 8 | `REM_LINE_TEXT` | Rem_Lineessorial Text | VARCHAR2 | 60 |  | Y |

## `E_XDOCK_LOAD_D1DD2`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `REAS_DES` | Reasessorial Des | VARCHAR2 | 30 |  | N |
| 11 | `CHGN_TP` | Chgnessorial Tp | VARCHAR2 | 1 |  | N |
| 12 | `CHGN_SRCE` | Chgnessorial Srce | VARCHAR2 | 1 |  | N |
| 13 | `NEW_UNIT` | Newessorial Unit | NUMBER | 22 | 9 | Y |
| 14 | `ORG_UNIT` | Orgessorial Unit | NUMBER | 22 | 9 | Y |
| 15 | `NEW_SKU_CODE` | New_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `ORG_SKU_CODE` | Org_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `NEW_WGT` | Newessorial Wgt | NUMBER | 22 | 16 | Y |
| 18 | `ORG_WGT` | Orgessorial Wgt | NUMBER | 22 | 16 | Y |
| 19 | `NEW_WGT_MEAS_CODE` | New_Wgt_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `ORG_WGT_MEAS_CODE` | Org_Wgt_Measessorial Code | VARCHAR2 | 4 |  | Y |

## `E_XDOCK_LOAD_D2`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `TRSPT_EQP_TP_CODE` | Trspt_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 6 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 7 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |

## `E_XDOCK_LOAD_D2D`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `TRSPT_EQP_TP_CODE` | Trspt_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 6 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 7 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |

## `E_XDOCK_LOAD_D3`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `FLOW_DATE` | Flow Date | DATE | 7 |  | N |
| 4 | `FLOW_CODE` | Flowessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `FLOW_CODE_TP_FLAG` | Flow_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | N |
| 7 | `FLOW_INFO_DATE` | Flow_Infoessorial Date | DATE | 7 |  | Y |
| 8 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `SPOOL_FILE_NAME` | Spool_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 10 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_XDOCK_LOAD_D4`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 7 | `REF_QUAL_SEQ_NUM` | Ref_Qual_Seqessorial Num | NUMBER | 22 | 4 | N |
| 8 | `REF_QUAL_VAL` | Ref_Qualessorial Val | VARCHAR2 | 30 |  | N |
| 9 | `REF_TP` | Refessorial Tp | VARCHAR2 | 1 |  | N |
| 10 | `ORG_FLAG` | Orgessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `XDOCK_REF_QUAL_CODE` | Xarehouse Ref Qual Code | VARCHAR2 | 4 |  | N |
| 12 | `LOAD_INB_OUTB_TP` | Load_Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |

## `E_XDOCK_LOAD_D5`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `STAT_CHG_DATE` | Stat_Chgessorial Date | DATE | 7 |  | N |
| 8 | `ORG_STAT` | Orgessorial Stat | VARCHAR2 | 1 |  | N |
| 9 | `NEW_STAT` | Newessorial Stat | VARCHAR2 | 1 |  | N |
| 10 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `REAS_DES` | Reasessorial Des | VARCHAR2 | 30 |  | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `E_XDOCK_LOAD_D6`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 8 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 9 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `LOAD_DOC_PRT_STAT` | Load_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 11 | `LOAD_DOC_REPRT_CNT` | Load_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |

## `E_XDOCK_LOAD_H`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 36
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `LOAD_INB_OUTB_TP` | Load_Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 4 | `LOAD_PRTY_NUM` | Load_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 5 | `LOAD_CREATE_DATE` | Load_Createessorial Date | DATE | 7 |  | N |
| 6 | `LOAD_PICKUP_DATE` | Load_Pickupessorial Date | DATE | 7 |  | Y |
| 7 | `ROUTE_NUM` | Routeessorial Num | NUMBER | 22 | 6 | N |
| 8 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_PRO_NUM` | Carr_Proessorial Num | VARCHAR2 | 20 |  | Y |
| 10 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 11 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 12 | `EST_DATE` | Estessorial Date | DATE | 7 |  | N |
| 13 | `ACT_DATE` | Actessorial Date | DATE | 7 |  | Y |
| 14 | `TOT_UNIT` | Totessorial Unit | NUMBER | 22 | 9 | N |
| 15 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | N |
| 16 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | N |
| 17 | `SEAL_NUM1` | Sealessorial Num1 | VARCHAR2 | 20 |  | Y |
| 18 | `SEAL_NUM2` | Sealessorial Num2 | VARCHAR2 | 20 |  | Y |
| 19 | `SEAL_NUM3` | Sealessorial Num3 | VARCHAR2 | 20 |  | Y |
| 20 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 21 | `LOAD_STAT` | Loadessorial Stat | VARCHAR2 | 1 |  | N |
| 22 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | Y |
| 23 | `LOAD_CONF_DATE` | Load_Confessorial Date | DATE | 7 |  | Y |
| 24 | `DRIVER_NAME` | Driveressorial Name | VARCHAR2 | 20 |  | Y |
| 25 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `TRSPT_PRTY_CODE` | Trspt_Prtyessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `PLACD_CODE1` | Placdessorial Code1 | VARCHAR2 | 4 |  | Y |
| 28 | `PLACD_CODE2` | Placdessorial Code2 | VARCHAR2 | 4 |  | Y |
| 29 | `PLACD_CODE3` | Placdessorial Code3 | VARCHAR2 | 4 |  | Y |
| 30 | `XDOCK_LOAD_EDI_CREATE_FLAG` | Xarehouse Load Edi Create Flag | VARCHAR2 | 1 |  | N |
| 31 | `SEAL_NUM1_ENTRY` | Seal_Num1essorial Entry | VARCHAR2 | 20 |  | Y |
| 32 | `SEAL_NUM2_ENTRY` | Seal_Num2essorial Entry | VARCHAR2 | 20 |  | Y |
| 33 | `SEAL_NUM3_ENTRY` | Seal_Num3essorial Entry | VARCHAR2 | 20 |  | Y |
| 34 | `SEAL_NUM1_INTACT_FLAG` | Seal_Num1_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `SEAL_NUM2_INTACT_FLAG` | Seal_Num2_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `SEAL_NUM3_INTACT_FLAG` | Seal_Num3_Intactessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_XDOCK_TRANS_D1`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `PICKUP_DROP_NAME` | Pickup_Dropessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `PICKUP_DROP_ADD1` | Pickup_Dropessorial Add1 | VARCHAR2 | 30 |  | Y |
| 5 | `PICKUP_DROP_ADD2` | Pickup_Dropessorial Add2 | VARCHAR2 | 30 |  | Y |
| 6 | `PICKUP_DROP_ADD3` | Pickup_Dropessorial Add3 | VARCHAR2 | 30 |  | Y |
| 7 | `PICKUP_DROP_ADD4` | Pickup_Dropessorial Add4 | VARCHAR2 | 30 |  | Y |
| 8 | `ZIP_CODE_PICKUP_DROP` | Zarehouse Code Pickup Drop | VARCHAR2 | 10 |  | Y |
| 9 | `ZIP_CITY_PICKUP_DROP` | Zarehouse City Pickup Drop | VARCHAR2 | 30 |  | Y |
| 10 | `STATE_CODE_PICKUP_DROP` | State_Code_Pickupessorial Drop | VARCHAR2 | 4 |  | Y |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 12 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 13 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |

## `E_XDOCK_TRANS_D2`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 8
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `ITEM_ID` | Itemessorial Id | NUMBER | 22 | 9 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `REF_TP` | Refessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `REF_SEQ_NUM` | Ref_Seqessorial Num | NUMBER | 22 | 3 | N |
| 7 | `REF_QUAL` | Refessorial Qual | VARCHAR2 | 4 |  | N |
| 8 | `REF_NUM` | Refessorial Num | VARCHAR2 | 30 |  | N |

## `E_XDOCK_TRANS_D3`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 20
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `ITEM_ID` | Itemessorial Id | NUMBER | 22 | 9 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `PKG_CODE` | Pkgessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `TOT_UNIT` | Totessorial Unit | NUMBER | 22 | 9 | Y |
| 7 | `CUST_XREF_ITEM_ID` | Cust_Xref_Itemessorial Id | VARCHAR2 | 30 |  | Y |
| 8 | `LADING_DES` | Ladingessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `LEN_LINEAR_MEAS_CODE` | Len_Linear_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `LEN` | Lenessorial Len | NUMBER | 22 | 16 | Y |
| 11 | `WID_LINEAR_MEAS_CODE` | Warehouse Linear Meas Code | VARCHAR2 | 4 |  | Y |
| 12 | `WID` | Warehouse | NUMBER | 22 | 16 | Y |
| 13 | `HGT_LINEAR_MEAS_CODE` | Hgt_Linear_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `HGT` | Hgtessorial Hgt | NUMBER | 22 | 16 | Y |
| 15 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 17 | `CUBE_MEAS_CODE` | Cube_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | Y |
| 19 | `VOL_NUM` | Volessorial Num | NUMBER | 22 | 16 | Y |
| 20 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |

## `E_XDOCK_TRANS_D3D`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 6
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `ITEM_ID` | Itemessorial Id | NUMBER | 22 | 9 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 2 | N |
| 6 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |

## `E_XDOCK_TRANS_D4`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 4 | `REM_LINE_TEXT` | Rem_Lineessorial Text | VARCHAR2 | 45 |  | N |

## `E_XDOCK_TRANS_H`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 34
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DOCK_TRANS_SEQ_NUM` | Dock_Trans_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INB_OUTB_TP` | Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `DOCK_TRANS_STAT` | Dock_Transessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 5 | `UNQ_REF_NUM` | Unq_Refessorial Num | VARCHAR2 | 20 |  | N |
| 6 | `TENDER_DATE` | Tenderessorial Date | DATE | 7 |  | Y |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 8 | `PICKUP_DROP_CODE` | Pickup_Dropessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `PICKUP_DROP_CODE_EXTRA` | Pickup_Drop_Codeessorial Extra | VARCHAR2 | 10 |  | Y |
| 10 | `STOP_TP` | Stopessorial Tp | VARCHAR2 | 2 |  | Y |
| 11 | `PICKUP_DROP_CODE_INTMED` | Pickup_Drop_Codeessorial Intmed | VARCHAR2 | 10 |  | Y |
| 12 | `PICKUP_DROP_CODE_EXTRA_INTMED` | Pickup_Drop_Code_Extraessorial Intmed | VARCHAR2 | 10 |  | Y |
| 13 | `PICKUP_DROP_CODE_OPP` | Pickup_Drop_Codeessorial Opp | VARCHAR2 | 10 |  | Y |
| 14 | `STOP_TP_OPP` | Stop_Tpessorial Opp | VARCHAR2 | 2 |  | Y |
| 15 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 16 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `ROUTE_NUM` | Routeessorial Num | NUMBER | 22 | 6 | Y |
| 18 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 19 | `APPO_TP` | Appoessorial Tp | VARCHAR2 | 2 |  | Y |
| 20 | `READY_DATE` | Readyessorial Date | DATE | 7 |  | Y |
| 21 | `RQST_DATE` | Rqstessorial Date | DATE | 7 |  | Y |
| 22 | `OPEN_FROM_DATE` | Open_Fromessorial Date | DATE | 7 |  | Y |
| 23 | `OPEN_TIL_DATE` | Open_Tilessorial Date | DATE | 7 |  | Y |
| 24 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `EST_DATE` | Estessorial Date | DATE | 7 |  | Y |
| 26 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 27 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 28 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 29 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 30 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 31 | `BAT_DATE` | Batessorial Date | DATE | 7 |  | Y |
| 32 | `ASTRAY_ORD_FLAG` | Astray_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 34 | `DOCK_REF1` | Dockessorial Ref1 | VARCHAR2 | 40 |  | Y |

## `E_XDOCK_UNLOAD`

- **Tipo:** Transactional
- **Categoria:** Cross Dock
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `M_XDOCK_PARA`

- **Tipo:** Master
- **Categoria:** Cross Dock
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PICKUP_FLOW_PROS_CODE` | Pickup_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `ADV_PICKUP_FLOW_PROS_CODE` | Adv_Pickup_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `LOAD_DEPART_FLOW_PROS_CODE` | Load_Depart_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_SIGN_OFF_FLOW_PROS_CODE` | Load_Sign_Off_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `LOAD_CHECK_IN_FLOW_PROS_CODE` | Load_Check_In_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ADV_CHECK_IN_FLOW_PROS_CODE` | Adv_Check_In_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `LOAD_INFO_PROS_FLOW_PROS_CODE` | Load_Info_Pros_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `LOCK_CHECK_IN_FLOW_PROS_CODE` | Lock_Check_In_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 11 | `FLOW_PROS_CODE_OUTB_LOADING` | Flow_Pros_Code_Outbessorial Loading | VARCHAR2 | 4 |  | N |
| 12 | `OUTB_SEAL_REQ_FLAG` | Outb_Seal_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `FLOW_PROS_CODE_UNLOAD` | Flow_Pros_Codeessorial Unload | VARCHAR2 | 4 |  | N |
| 14 | `WHSE_CODE_CLOSE_OUTB_TRSPT` | Whse_Code_Close_Outbessorial Trspt | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_CODE_CLOSE_OUTB_TRSPT` | Loc_Code_Close_Outbessorial Trspt | VARCHAR2 | 12 |  | Y |
| 16 | `WHSE_CODE_OVFL_HOLD` | Whse_Code_Ovflessorial Hold | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE_OVFL_HOLD` | Loc_Code_Ovflessorial Hold | VARCHAR2 | 12 |  | Y |
| 18 | `LOAD_SEQ_NUM_UNASS_INB` | Load_Seq_Num_Unassessorial Inb | NUMBER | 22 | 6 | N |
| 19 | `LOAD_SEQ_NUM_UNASS_OUTB` | Load_Seq_Num_Unassessorial Outb | NUMBER | 22 | 6 | N |
| 20 | `REWEIGH_CHG_CODE` | Reweigh_Chgessorial Code | VARCHAR2 | 6 |  | N |
| 21 | `VNU_CHG_CODE` | Vnu_Chgessorial Code | VARCHAR2 | 6 |  | N |
| 22 | `FLOW_PROS_CODE_CLS_UNLOAD` | Flow_Pros_Code_Clsessorial Unload | VARCHAR2 | 4 |  | N |
| 23 | `FLOW_PROS_CODE_CLS_TRLR` | Flow_Pros_Code_Clsessorial Trlr | VARCHAR2 | 4 |  | N |
| 24 | `MIX_DELV_SERV_CENTER_FLAG` | Mix_Delv_Serv_Centeressorial Flag | VARCHAR2 | 1 |  | N |

## `M_XDOCK_REF_QUAL`

- **Tipo:** Master
- **Categoria:** Cross Dock
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `XDOCK_REF_QUAL_CODE` | Xarehouse Ref Qual Code | VARCHAR2 | 4 |  | N |
| 3 | `XDOCK_REF_QUAL_DES` | Xarehouse Ref Qual Des | VARCHAR2 | 30 |  | N |
| 4 | `XDOCK_REF_QUAL_STAT` | Xarehouse Ref Qual Stat | VARCHAR2 | 1 |  | N |
| 5 | `XDOCK_REF_MAND_ENTRY_FLAG` | Xarehouse Ref Mand Entry Flag | VARCHAR2 | 1 |  | N |

## `T_INB_OUTB_XDOCK_LOAD_PRTY`

- **Tipo:** Temporary
- **Categoria:** Cross Dock
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INB_OUTB_XDOCK_LOAD_SEQ_NUM` | Inb_Outb_Xdock_Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `INB_LOAD_SEQ_NUM` | Inb_Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 5 | `INB_STOP_NUM` | Inb_Stopessorial Num | NUMBER | 22 | 4 | Y |
| 6 | `OUTB_LOAD_SEQ_NUM` | Outb_Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 7 | `OUTB_STOP_NUM` | Outb_Stopessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `UNQ_REF_NUM` | Unq_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 10 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |

## `T_INB_XDOCK_LOAD_PRTY`

- **Tipo:** Temporary
- **Categoria:** Cross Dock
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INB_XDOCK_LOAD_SEQ_NUM` | Inb_Xdock_Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 6 | `ATTR` | Attressorial Attr | VARCHAR2 | 8 |  | Y |
| 7 | `MVT_CNT_AT_DOOR` | Mvt_Cnt_Atessorial Door | NUMBER | 22 | 6 | Y |
| 8 | `UNIT_AT_DOOR` | Unit_Atessorial Door | NUMBER | 22 | 9 | Y |
| 9 | `WGT_AT_DOOR` | Wgt_Atessorial Door | NUMBER | 22 | 16 | Y |
| 10 | `CUBE_AT_DOOR` | Cube_Atessorial Door | NUMBER | 22 | 16 | Y |
| 11 | `MVT_CNT_AT_DOOR_PCT` | Mvt_Cnt_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |
| 12 | `UNIT_AT_DOOR_PCT` | Unit_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |
| 13 | `WGT_AT_DOOR_PCT` | Wgt_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |
| 14 | `CUBE_AT_DOOR_PCT` | Cube_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |
| 15 | `ARRV_DATE` | Arrvessorial Date | DATE | 7 |  | Y |
| 16 | `DEPART_DATE` | Departessorial Date | DATE | 7 |  | Y |
| 17 | `PROS_TIME` | Prosessorial Time | NUMBER | 22 | 6 | Y |

## `T_OUTB_INB_XDOCK_LOAD_PRTY`

- **Tipo:** Temporary
- **Categoria:** Cross Dock
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OUTB_INB_XDOCK_LOAD_SEQ_NUM` | Outb_Inb_Xdock_Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 4 | `INB_LOAD_SEQ_NUM` | Inb_Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 5 | `INB_STOP_NUM` | Inb_Stopessorial Num | NUMBER | 22 | 4 | Y |
| 6 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 7 | `UNQ_REF_NUM` | Unq_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `TOT_UNIT` | Totessorial Unit | NUMBER | 22 | 9 | Y |
| 9 | `TOT_WGT` | Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 10 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | Y |
| 11 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |

## `T_OUTB_XDOCK_LOAD_PRTY`

- **Tipo:** Temporary
- **Categoria:** Cross Dock
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OUTB_XDOCK_LOAD_SEQ_NUM` | Outb_Xdock_Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 4 | `OUTB_LOAD_SEQ_NUM` | Outb_Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 5 | `DEPART_DATE` | Departessorial Date | DATE | 7 |  | Y |
| 6 | `PROS_TIME` | Prosessorial Time | NUMBER | 22 | 6 | Y |
| 7 | `UNIT_STAGED` | Unitessorial Staged | NUMBER | 22 | 9 | Y |
| 8 | `UNIT_STAGED_PCT` | Unit_Stagedessorial Pct | NUMBER | 22 | 5 | Y |
| 9 | `UNIT_AT_DOOR` | Unit_Atessorial Door | NUMBER | 22 | 9 | Y |
| 10 | `UNIT_AT_DOOR_PCT` | Unit_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |
| 11 | `UNIT_NOT_AT_DOOR` | Unit_Not_Atessorial Door | NUMBER | 22 | 9 | Y |
| 12 | `UNIT_NOT_AT_DOOR_PCT` | Unit_Not_At_Dooressorial Pct | NUMBER | 22 | 5 | Y |

