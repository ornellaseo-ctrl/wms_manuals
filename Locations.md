# Tabelas — Locations

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **88**.

## `C_BLDG_ROUTE`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 6 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | N |
| 8 | `STOP_SEQ_NUM` | Stop_Seqessorial Num | NUMBER | 22 | 9 | N |
| 9 | `WHSE_CODE_VIA` | Warehouse Code Via | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE_VIA` | Loc_Codeessorial Via | VARCHAR2 | 12 |  | N |
| 11 | `DISTA` | Distaessorial Dista | NUMBER | 22 | 16 | N |
| 12 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_LAST_PUT_LOC`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, LOC_CODE, INVT_LEV2, INVT_LEV3, INVT_LEV4, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `LAST_PUT_DATE` | Last_Putessorial Date | DATE | 7 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 11 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |

## `C_LOC`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 46
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
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
| 19 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 20 | `UNALLOC_CAPC_PCENT` | Unalloc_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 21 | `INTRANS_CAPC_PCENT` | Intrans_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 22 | `ON_RCPT_CAPC_PCENT` | On_Rcpt_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 23 | `ON_ORD_CAPC_PCENT` | On_Ord_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 24 | `ON_HAND_CAPC_PCENT` | On_Hand_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 25 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 26 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 27 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 28 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 29 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 30 | `UNALLOC_CAPC_WGT` | Unalloc_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 31 | `INTRANS_CAPC_WGT` | Intrans_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 32 | `ON_RCPT_CAPC_WGT` | On_Rcpt_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 33 | `ON_ORD_CAPC_WGT` | On_Ord_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 34 | `ON_HAND_CAPC_WGT` | On_Hand_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 35 | `UNALLOC_CAPC_CUBE` | Unalloc_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 36 | `INTRANS_CAPC_CUBE` | Intrans_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 37 | `ON_RCPT_CAPC_CUBE` | On_Rcpt_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 38 | `ON_ORD_CAPC_CUBE` | On_Ord_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 39 | `ON_HAND_CAPC_CUBE` | On_Hand_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 40 | `LOC_RECD_TIME_STAMP` | Loc_Recd_Timeessorial Stamp | DATE | 7 |  | Y |
| 41 | `LOC_RECD_PICK_TIME_STAMP` | Loc_Recd_Pick_Timeessorial Stamp | DATE | 7 |  | Y |
| 42 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 43 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 45 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 46 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_LOC_DYN`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | N |
| 8 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 9 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 10 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 11 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 12 | `ON_RCPT_CAPC_PCENT` | On_Rcpt_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 13 | `ON_RCPT_CAPC_WGT` | On_Rcpt_Capcessorial Wgt | NUMBER | 22 | 15 | N |
| 14 | `ON_RCPT_CAPC_CUBE` | On_Rcpt_Capcessorial Cube | NUMBER | 22 | 15 | N |

## `C_LOC_LOCK`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `LOCK_DATE` | Lockessorial Date | DATE | 7 |  | N |

## `C_WHSE_LOC_ATTR_BLK`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_LOC_ATTR_NUM` | Warehouse Loc Attr Num | NUMBER | 22 | 1 | N |
| 4 | `WHSE_LOC_ATTR_BLK_DATE` | Warehouse Loc Attr Blk Date | DATE | 7 |  | N |

## `C_YARD_LOC_D`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | N |
| 4 | `YARD_LOC_VERT_LEV` | Yarehouse Loc Vert Lev | NUMBER | 22 | 2 | N |
| 5 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 7 | `ORD_FLAG` | Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `RCPT_FLAG` | Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `C_YARD_LOC_H`

- **Tipo:** Transactional
- **Categoria:** Locations
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | N |
| 4 | `ON_HAND` | Onessorial Hand | NUMBER | 22 | 3 | N |
| 5 | `ON_ORD` | Onessorial Ord | NUMBER | 22 | 3 | N |
| 6 | `ON_RCPT` | Onessorial Rcpt | NUMBER | 22 | 3 | N |
| 7 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |

## `H_LOC`

- **Tipo:** Historical
- **Categoria:** Locations
- **Campos:** 46
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
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
| 19 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 20 | `UNALLOC_CAPC_PCENT` | Unalloc_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 21 | `INTRANS_CAPC_PCENT` | Intrans_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 22 | `ON_RCPT_CAPC_PCENT` | On_Rcpt_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 23 | `ON_ORD_CAPC_PCENT` | On_Ord_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 24 | `ON_HAND_CAPC_PCENT` | On_Hand_Capcessorial Pcent | NUMBER | 22 | 15 | N |
| 25 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 26 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 27 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 28 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 29 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 30 | `UNALLOC_CAPC_WGT` | Unalloc_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 31 | `INTRANS_CAPC_WGT` | Intrans_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 32 | `ON_RCPT_CAPC_WGT` | On_Rcpt_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 33 | `ON_ORD_CAPC_WGT` | On_Ord_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 34 | `ON_HAND_CAPC_WGT` | On_Hand_Capcessorial Wgt | NUMBER | 22 | 14 | Y |
| 35 | `UNALLOC_CAPC_CUBE` | Unalloc_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 36 | `INTRANS_CAPC_CUBE` | Intrans_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 37 | `ON_RCPT_CAPC_CUBE` | On_Rcpt_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 38 | `ON_ORD_CAPC_CUBE` | On_Ord_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 39 | `ON_HAND_CAPC_CUBE` | On_Hand_Capcessorial Cube | NUMBER | 22 | 14 | Y |
| 40 | `LOC_RECD_TIME_STAMP` | Loc_Recd_Timeessorial Stamp | DATE | 7 |  | Y |
| 41 | `LOC_RECD_PICK_TIME_STAMP` | Loc_Recd_Pick_Timeessorial Stamp | DATE | 7 |  | Y |
| 42 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 43 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 45 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 46 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `LAB_COMP_PARA`

- **Tipo:** Misc
- **Categoria:** Locations
- **Campos:** 78
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_NUM_FIS_PER` | Comp_Num_Fisessorial Per | NUMBER | 22 | 2 | N |
| 3 | `COMP_FIRST_FIS_MON` | Comp_First_Fisessorial Mon | VARCHAR2 | 3 |  | N |
| 4 | `COMP_MULT_CUR_FLAG` | Comp_Mult_Curessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `COMP_CUR_CODE` | Comp_Curessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `COMP_FIN_INTFACE_CODE` | Comp_Fin_Intfaceessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `COMP_GL_ACTIVE_FLAG` | Comp_Gl_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `COMP_AP_ACTIVE_FLAG` | Comp_Ap_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `COMP_AP_GL_UPD_FLAG` | Comp_Ap_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `COMP_AR_ACTIVE_FLAG` | Comp_Ar_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `COMP_AR_GL_UPD_FLAG` | Comp_Ar_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `COMP_CC_ACTIVE_FLAG` | Comp_Cc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `COMP_CC_AR_UPD_FLAG` | Comp_Cc_Ar_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `COMP_PO_ACTIVE_FLAG` | Comp_Po_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `COMP_PO_AP_INTFACE_FLAG` | Comp_Po_Ap_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `COMP_PW_ACTIVE_FLAG` | Comp_Pw_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `COMP_NUM_DAY_RET_CON` | Comp_Num_Day_Retessorial Con | NUMBER | 22 | 4 | N |
| 18 | `COMP_PUB_PRVT_FLAG` | Comp_Pub_Prvtessorial Flag | VARCHAR2 | 2 |  | Y |
| 19 | `COMP_CUST_CODE` | Comp_Custessorial Code | VARCHAR2 | 10 |  | Y |
| 20 | `COMP_NUM_YEAR_RET_SALE_DATA` | Comp_Num_Year_Ret_Saleessorial Data | NUMBER | 22 | 1 | Y |
| 21 | `COMP_NUM_YEAR_RET_MANG_DATA` | Comp_Num_Year_Ret_Mangessorial Data | NUMBER | 22 | 1 | Y |
| 22 | `COMP_ALLOW_MAN_CON_FLAG` | Comp_Allow_Man_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `COMP_ALLOW_MAN_SHIP_FLAG` | Comp_Allow_Man_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `COMP_ALLOW_MAN_CARR_FLAG` | Comp_Allow_Man_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `COMP_DYN_LOC_RCPT_ACTIVE_FLAG` | Comp_Dyn_Loc_Rcpt_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `COMP_DYN_LOC_SHIP_ACTIVE_FLAG` | Comp_Dyn_Loc_Ship_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `COMP_FRT_ACTIVE_FLAG` | Comp_Frt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `COMP_TURN_ACTIVE_FLAG` | Comp_Turn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `COMP_NUM_YEAR_RET_TURN_DATA` | Comp_Num_Year_Ret_Turnessorial Data | NUMBER | 22 | 1 | Y |
| 30 | `COMP_TONN_ACTIVE_FLAG` | Comp_Tonn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `COMP_NUM_YEAR_RET_TONN_DATA` | Comp_Num_Year_Ret_Tonnessorial Data | NUMBER | 22 | 1 | Y |
| 32 | `COMP_BORD_ACTIVE_FLAG` | Comp_Bord_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `COMP_FORD_ACTIVE_FLAG` | Comp_Ford_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `COMP_INTRANS_ACTIVE_FLAG` | Comp_Intrans_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `COMP_SET_ASSEM_ACTIVE_FLAG` | Comp_Set_Assem_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 36 | `COMP_ITEM_PRI_ACTIVE_FLAG` | Comp_Item_Pri_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 37 | `COMP_DAY_ANAL_TP_FLAG` | Comp_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `COMP_DAY_DAY_ANAL_TP_FLAG` | Comp_Day_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `COMP_DAY_DOC_ANAL_TP_FLAG` | Comp_Day_Doc_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `COMP_DAY_CARR_ANAL_TP_FLAG` | Comp_Day_Carr_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `COMP_ALLOW_HOLD_RCPT_FLAG` | Comp_Allow_Hold_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `COMP_CUST_CRT_ORD_VER_FLAG` | Comp_Cust_Crt_Ord_Veressorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `COMP_FIN_INTFACE_COMP` | Comp_Fin_Intfaceessorial Comp | VARCHAR2 | 4 |  | Y |
| 44 | `FRT_DEST_TYPE` | Frt_Destessorial Type | VARCHAR2 | 1 |  | N |
| 45 | `FRT_PRO_RATE_FORUL` | Frt_Pro_Rateessorial Forul | VARCHAR2 | 10 |  | N |
| 46 | `COMP_FRT_DEF_FLAG` | Comp_Frt_Defessorial Flag | VARCHAR2 | 1 |  | N |
| 47 | `COMP_FRT_FLAT_AMT` | Comp_Frt_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 48 | `COMP_FRT_PCENT_SAV` | Comp_Frt_Pcentessorial Sav | NUMBER | 22 | 6 | Y |
| 49 | `COMP_FRT_PCENT_FRT` | Comp_Frt_Pcentessorial Frt | NUMBER | 22 | 6 | Y |
| 50 | `COMP_FRT_DEFI_AMT_FLAG` | Comp_Frt_Defi_Amtessorial Flag | VARCHAR2 | 2 |  | Y |
| 51 | `COMP_FRT_STOP_CHG_FLAG` | Comp_Frt_Stop_Chgessorial Flag | VARCHAR2 | 2 |  | Y |
| 52 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 53 | `COMP_PURGE_RET_MON` | Comp_Purge_Retessorial Mon | NUMBER | 22 | 2 | N |
| 54 | `COMP_ALERT_ORD_SHIP_FLAG` | Comp_Alert_Ord_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 55 | `COMP_ALLOW_WHSE_ORD_FLAG` | Comp_Allow_Whse_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 56 | `COMP_ALLOW_WHSE_RCPT_FLAG` | Comp_Allow_Whse_Rcptessorial Flag | VARCHAR2 | 1 |  | N |
| 57 | `COMP_ACCSS_FORCE_AUDIT_FLAG` | Comp_Accss_Force_Auditessorial Flag | VARCHAR2 | 1 |  | N |
| 58 | `SHIP_MAX_WGT` | Ship_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 59 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 60 | `COMP_BUS_START_TIME` | Comp_Bus_Startessorial Time | VARCHAR2 | 5 |  | Y |
| 61 | `COMP_BUS_END_TIME` | Comp_Bus_Endessorial Time | VARCHAR2 | 5 |  | Y |
| 62 | `COMP_APPO_TIME_SLICE` | Comp_Appo_Timeessorial Slice | NUMBER | 22 | 3 | Y |
| 63 | `FRT_VERS1_FLAG` | Frt_Vers1essorial Flag | VARCHAR2 | 1 |  | N |
| 64 | `COMP_ALLOW_MAN_SOLDTO_FLAG` | Comp_Allow_Man_Soldtoessorial Flag | VARCHAR2 | 1 |  | N |
| 65 | `COMP_DRMS_ACTIVE_FLAG` | Comp_Drms_Activeessorial Flag | CHAR | 1 |  | N |
| 66 | `COMP_PER_PROF_CODE` | Comp_Per_Professorial Code | CHAR | 4 |  | Y |
| 67 | `COMP_LAB_POST_DATE` | Comp_Lab_Postessorial Date | DATE | 7 |  | Y |
| 68 | `JOB_TP_CODE` | Job_Tpessorial Code | CHAR | 2 |  | Y |
| 69 | `FLOW_PROS_CODE` | Flow Process Code | CHAR | 4 |  | Y |
| 70 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 71 | `LAB_COST_CAT_CODE` | Lab_Cost_Catessorial Code | CHAR | 12 |  | Y |
| 72 | `COMP_LAB_STD_FLAG` | Comp_Lab_Stdessorial Flag | CHAR | 1 |  | Y |
| 73 | `LAB_STD_CALC_COL` | Lab_Std_Calcessorial Col | CHAR | 1 |  | Y |
| 74 | `MHE_COST_CAT_CODE` | Mhe_Cost_Catessorial Code | CHAR | 12 |  | Y |
| 75 | `COMP_ALLOW_ADJ_DATE_OVRR_FLAG` | Comp_Allow_Adj_Date_Ovrressorial Flag | VARCHAR2 | 1 |  | N |
| 76 | `COMP_PARA_LOC_SIZE_FLAG` | Comp_Para_Loc_Sizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 77 | `COMP_OUTB_SORT_CODE` | Comp_Outb_Sortessorial Code | VARCHAR2 | 4 |  | N |
| 78 | `COMP_PARA_EXT_INV_NUM_DES` | Comp_Para_Ext_Inv_Numessorial Des | VARCHAR2 | 12 |  | Y |

## `M_BLDG_APPO_SCH`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 3 | `BLDG_APPO_START_DATE` | Bldg_Appo_Startessorial Date | DATE | 7 |  | N |
| 4 | `BLDG_APPO_TIME_SLOT` | Bldg_Appo_Timeessorial Slot | NUMBER | 22 | 2 | N |
| 5 | `BLDG_APPO_NUM` | Bldg_Appoessorial Num | NUMBER | 22 | 2 | N |

## `M_BLDG_D1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `ROOM_SEQ_NUM` | Room_Seqessorial Num | NUMBER | 22 | 9 | N |
| 6 | `ROOM_NAME` | Roomessorial Name | VARCHAR2 | 40 |  | N |
| 7 | `LOC_CODE_INSIDE` | Loc_Codeessorial Inside | VARCHAR2 | 12 |  | N |
| 8 | `LOC_CODE_OUTSIDE` | Loc_Codeessorial Outside | VARCHAR2 | 12 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D2D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `ROOM_SEQ_NUM` | Room_Seqessorial Num | NUMBER | 22 | 9 | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D3`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_LOC_ATTR_CODE` | Warehouse Loc Attr Code | VARCHAR2 | 4 |  | N |
| 6 | `WHSE_LOC_ATTR_START_POS` | Warehouse Loc Attr Start Pos | NUMBER | 22 | 2 | N |
| 7 | `WHSE_LOC_ATTR_END_POS` | Warehouse Loc Attr End Pos | NUMBER | 22 | 2 | N |
| 8 | `ATTR_SEQ_NUM` | Attr_Seqessorial Num | NUMBER | 22 | 9 | N |
| 9 | `DEPTH_TP_FLAG` | Depth_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `SEQ_TP_FLAG` | Seq_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `DISTA` | Distaessorial Dista | NUMBER | 22 | 16 | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D3D1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_LOC_ATTR_CODE` | Warehouse Loc Attr Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE_SEG` | Loc_Codeessorial Seg | VARCHAR2 | 12 |  | N |
| 7 | `DISTA` | Distaessorial Dista | NUMBER | 22 | 16 | N |
| 8 | `LOC_CODE_SEG_SEQ_NUM` | Loc_Code_Seg_Seqessorial Num | NUMBER | 22 | 9 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D3D2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `ACCESSIBLE_FLAG` | Accessibleessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `INB_OUTB_ACCESS_FLAG` | Inb_Outb_Accessessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `LOC_CODE_SEG` | Loc_Codeessorial Seg | VARCHAR2 | 12 |  | N |
| 8 | `DISTA` | Distaessorial Dista | NUMBER | 22 | 16 | N |
| 9 | `LOC_CODE_SEG_SEQ_NUM` | Loc_Code_Seg_Seqessorial Num | NUMBER | 22 | 9 | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D4`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `INB_OUTB_PND_FLAG` | Inb_Outb_Pndessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_D4D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE_1` | Whse_Codeessorial 1 | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE_1` | Loc_Codeessorial 1 | VARCHAR2 | 12 |  | N |
| 6 | `WHSE_CODE_2` | Whse_Codeessorial 2 | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_2` | Loc_Codeessorial 2 | VARCHAR2 | 12 |  | N |
| 8 | `DISTA` | Distaessorial Dista | NUMBER | 22 | 16 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BLDG_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `BLDG_DES` | Bldgessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `BLDG_STAT` | Bldgessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 7 | `BLDG_APPO_NUM_MAX_DAY` | Bldg_Appo_Num_Maxessorial Day | NUMBER | 22 | 4 | Y |
| 8 | `BLDG_APPO_DOOR_REQ_FLAG` | Bldg_Appo_Door_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `BLDG_APPO_START_TIME` | Bldg_Appo_Startessorial Time | VARCHAR2 | 5 |  | Y |
| 10 | `BLDG_APPO_END_TIME` | Bldg_Appo_Endessorial Time | VARCHAR2 | 5 |  | Y |
| 11 | `BLDG_APPO_TIME_SLICE` | Bldg_Appo_Timeessorial Slice | NUMBER | 22 | 3 | Y |
| 12 | `BLDG_APPO_ADV_FLOW_FLAG` | Bldg_Appo_Adv_Flowessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `BLDG_APPO_DEF_LOAD_TP` | Bldg_Appo_Def_Loadessorial Tp | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 19 | `BLDG_DATA_SERVICE_ID` | Bldg_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 20 | `BLDG_APPO_LOAD_CREATE_FLAG` | Bldg_Appo_Load_Createessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `BLDG_COR_FLAG` | Bldg_Coressorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `DOC_CODE_COR` | Doc_Codeessorial Cor | VARCHAR2 | 4 |  | Y |
| 23 | `BLDG_DUP_INB_DOC_FLAG` | Bldg_Dup_Inb_Docessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `BLDG_MULTI_OUTB_LOAD_FLAG` | Bldg_Multi_Outb_Loadessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_COMD_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | N |
| 5 | `COMD_LINE_NUM` | Comd_Lineessorial Num | NUMBER | 22 | 5 | N |
| 6 | `COMD_LINE_CONN_NUM` | Comd_Line_Connessorial Num | NUMBER | 22 | 5 | N |
| 7 | `COMD_LINE_ROOT_FLAG` | Comd_Line_Rootessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `COMD_LINE_TEXT` | Comd_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMD_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | N |
| 5 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 6 | `COMD_STAT` | Comdessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `COMD_TEXT` | Comdessorial Text | VARCHAR2 | 2000 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMP_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_CODE_ROLLUP` | Comp_Codeessorial Rollup | VARCHAR2 | 2 |  | N |
| 4 | `COMP_ROLLUP_REP_FLAG` | Comp_Rollup_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `COMP_ROLLUP_INV_FLAG` | Comp_Rollup_Invessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMP_FRT_INTFACE_PROF`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_FRT_INTFACE_PROF_CODE` | Comp_Frt_Intface_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_FRT_INTFACE_PROF_DES` | Comp_Frt_Intface_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `COMP_FRT_INTFACE_PROF_STAT` | Comp_Frt_Intface_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `COMP_FRT_INTFACE_PROF_TP` | Comp_Frt_Intface_Professorial Tp | VARCHAR2 | 4 |  | N |
| 7 | `COMP_FRT_INTFACE_ALLOW_CHANGE` | Comp_Frt_Intface_Allowessorial Change | VARCHAR2 | 1 |  | N |
| 8 | `INTFACE_DIR` | Intfaceessorial Dir | VARCHAR2 | 60 |  | Y |
| 9 | `INTFACE_FILE_PREX` | Intface_Fileessorial Prex | VARCHAR2 | 30 |  | Y |
| 10 | `INTFACE_FILE_SUFX` | Intface_Fileessorial Sufx | VARCHAR2 | 30 |  | Y |
| 11 | `INTFACE_ARCH_DIR` | Intface_Archessorial Dir | VARCHAR2 | 60 |  | Y |
| 12 | `EMAIL_ADD` | Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 13 | `ALERT_TP` | Alertessorial Tp | VARCHAR2 | 1 |  | Y |
| 14 | `COMP_FRT_INTFACE_ADV_FLOW` | Comp_Frt_Intface_Advessorial Flow | VARCHAR2 | 1 |  | Y |
| 15 | `COMP_FRT_INTFACE_SEND_EXT_EDI` | Comp_Frt_Intface_Send_Extessorial Edi | VARCHAR2 | 1 |  | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMP_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_NAME` | Compessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `COMP_STAT` | Compessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `GLOBAL_CODE` | Globalessorial Code | VARCHAR2 | 2 |  | Y |
| 6 | `COMP_ADD1` | Compessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `COMP_ADD2` | Compessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `COMP_ADD3` | Compessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `COMP_DATE_FMT` | Comp_Dateessorial Fmt | VARCHAR2 | 9 |  | N |
| 11 | `COMP_DEF_DATE_FLAG` | Comp_Def_Dateessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `COMP_DATE` | Compessorial Date | DATE | 7 |  | N |
| 13 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 10 |  | Y |
| 14 | `COMP_CUST_DES` | Comp_Custessorial Des | VARCHAR2 | 9 |  | Y |
| 15 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 16 | `COMP_ROLLUP_TP_FLAG` | Comp_Rollup_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `COMP_ADD4` | Compessorial Add4 | VARCHAR2 | 30 |  | Y |
| 18 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 19 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 20 | `COMP_AUTO_PROS_SEQ_NUM` | Comp_Auto_Pros_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 21 | `COMP_OVRR_EDI_FLAG` | Comp_Ovrr_Ediessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `ACC_REF_NUM1` | Acc_Refessorial Num1 | VARCHAR2 | 10 |  | Y |
| 23 | `COMP_DATA_SERVICE_ID` | Comp_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 29 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |
| 30 | `COMP_TZ_NAME` | Comp_Tzessorial Name | VARCHAR2 | 64 |  | Y |
| 31 | `COMP_NAME_EXTN` | Comp_Nameessorial Extn | VARCHAR2 | 250 |  | Y |

## `M_COMP_HOL`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_HOL_DATE` | Comp_Holessorial Date | DATE | 7 |  | N |
| 3 | `HOL_CODE` | Holessorial Code | VARCHAR2 | 4 |  | N |

## `M_COMP_PARA`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 177
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_NUM_FIS_PER` | Comp_Num_Fisessorial Per | NUMBER | 22 | 2 | N |
| 4 | `COMP_FIRST_FIS_MON` | Comp_First_Fisessorial Mon | VARCHAR2 | 3 |  | N |
| 5 | `COMP_MULT_CUR_FLAG` | Comp_Mult_Curessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `COMP_CUR_CODE` | Comp_Curessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `COMP_FIN_INTFACE_CODE` | Comp_Fin_Intfaceessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `COMP_GL_ACTIVE_FLAG` | Comp_Gl_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `COMP_AP_ACTIVE_FLAG` | Comp_Ap_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `COMP_AP_GL_UPD_FLAG` | Comp_Ap_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `COMP_AR_ACTIVE_FLAG` | Comp_Ar_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `COMP_AR_GL_UPD_FLAG` | Comp_Ar_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `COMP_CC_ACTIVE_FLAG` | Comp_Cc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `COMP_CC_AR_UPD_FLAG` | Comp_Cc_Ar_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `COMP_PO_ACTIVE_FLAG` | Comp_Po_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `COMP_PO_AP_INTFACE_FLAG` | Comp_Po_Ap_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `COMP_PW_ACTIVE_FLAG` | Comp_Pw_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `COMP_NUM_DAY_RET_CON` | Comp_Num_Day_Retessorial Con | NUMBER | 22 | 4 | N |
| 19 | `COMP_PUB_PRVT_FLAG` | Comp_Pub_Prvtessorial Flag | VARCHAR2 | 2 |  | Y |
| 20 | `COMP_CUST_CODE` | Comp_Custessorial Code | VARCHAR2 | 10 |  | Y |
| 21 | `COMP_NUM_YEAR_RET_SALE_DATA` | Comp_Num_Year_Ret_Saleessorial Data | NUMBER | 22 | 1 | Y |
| 22 | `COMP_NUM_YEAR_RET_MANG_DATA` | Comp_Num_Year_Ret_Mangessorial Data | NUMBER | 22 | 1 | Y |
| 23 | `COMP_ALLOW_MAN_CON_FLAG` | Comp_Allow_Man_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `COMP_ALLOW_MAN_SHIP_FLAG` | Comp_Allow_Man_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `COMP_ALLOW_MAN_CARR_FLAG` | Comp_Allow_Man_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `COMP_DYN_LOC_RCPT_ACTIVE_FLAG` | Comp_Dyn_Loc_Rcpt_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `COMP_DYN_LOC_SHIP_ACTIVE_FLAG` | Comp_Dyn_Loc_Ship_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `COMP_FRT_ACTIVE_FLAG` | Comp_Frt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `COMP_TURN_ACTIVE_FLAG` | Comp_Turn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `COMP_NUM_YEAR_RET_TURN_DATA` | Comp_Num_Year_Ret_Turnessorial Data | NUMBER | 22 | 1 | Y |
| 31 | `COMP_TONN_ACTIVE_FLAG` | Comp_Tonn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `COMP_NUM_YEAR_RET_TONN_DATA` | Comp_Num_Year_Ret_Tonnessorial Data | NUMBER | 22 | 1 | Y |
| 33 | `COMP_BORD_ACTIVE_FLAG` | Comp_Bord_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `COMP_FORD_ACTIVE_FLAG` | Comp_Ford_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `COMP_INTRANS_ACTIVE_FLAG` | Comp_Intrans_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 36 | `COMP_SET_ASSEM_ACTIVE_FLAG` | Comp_Set_Assem_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 37 | `COMP_ITEM_PRI_ACTIVE_FLAG` | Comp_Item_Pri_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 38 | `COMP_DAY_ANAL_TP_FLAG` | Comp_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `COMP_DAY_DAY_ANAL_TP_FLAG` | Comp_Day_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `COMP_DAY_DOC_ANAL_TP_FLAG` | Comp_Day_Doc_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `COMP_DAY_CARR_ANAL_TP_FLAG` | Comp_Day_Carr_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `COMP_ALLOW_HOLD_RCPT_FLAG` | Comp_Allow_Hold_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `COMP_CUST_CRT_ORD_VER_FLAG` | Comp_Cust_Crt_Ord_Veressorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `COMP_FIN_INTFACE_COMP` | Comp_Fin_Intfaceessorial Comp | VARCHAR2 | 4 |  | Y |
| 45 | `FRT_DEST_TYPE` | Frt_Destessorial Type | VARCHAR2 | 1 |  | N |
| 46 | `FRT_PRO_RATE_FORUL` | Frt_Pro_Rateessorial Forul | VARCHAR2 | 10 |  | N |
| 47 | `COMP_FRT_DEF_FLAG` | Comp_Frt_Defessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `COMP_FRT_FLAT_AMT` | Comp_Frt_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 49 | `COMP_FRT_PCENT_SAV` | Comp_Frt_Pcentessorial Sav | NUMBER | 22 | 6 | Y |
| 50 | `COMP_FRT_PCENT_FRT` | Comp_Frt_Pcentessorial Frt | NUMBER | 22 | 6 | Y |
| 51 | `COMP_FRT_DEFI_AMT_FLAG` | Comp_Frt_Defi_Amtessorial Flag | VARCHAR2 | 2 |  | Y |
| 52 | `COMP_FRT_STOP_CHG_FLAG` | Comp_Frt_Stop_Chgessorial Flag | VARCHAR2 | 2 |  | Y |
| 53 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 54 | `COMP_PURGE_RET_MON` | Comp_Purge_Retessorial Mon | NUMBER | 22 | 2 | N |
| 55 | `COMP_ALERT_ORD_SHIP_FLAG` | Comp_Alert_Ord_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 56 | `COMP_ALLOW_WHSE_ORD_FLAG` | Comp_Allow_Whse_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 57 | `COMP_ALLOW_WHSE_RCPT_FLAG` | Comp_Allow_Whse_Rcptessorial Flag | VARCHAR2 | 1 |  | N |
| 58 | `COMP_ACCSS_FORCE_AUDIT_FLAG` | Comp_Accss_Force_Auditessorial Flag | VARCHAR2 | 1 |  | N |
| 59 | `SHIP_MAX_WGT` | Ship_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 60 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 61 | `COMP_BUS_START_TIME` | Comp_Bus_Startessorial Time | VARCHAR2 | 5 |  | Y |
| 62 | `COMP_BUS_END_TIME` | Comp_Bus_Endessorial Time | VARCHAR2 | 5 |  | Y |
| 63 | `COMP_APPO_TIME_SLICE` | Comp_Appo_Timeessorial Slice | NUMBER | 22 | 3 | Y |
| 64 | `FRT_VERS1_FLAG` | Frt_Vers1essorial Flag | VARCHAR2 | 1 |  | N |
| 65 | `COMP_ALLOW_MAN_SOLDTO_FLAG` | Comp_Allow_Man_Soldtoessorial Flag | VARCHAR2 | 1 |  | N |
| 66 | `COMP_DRMS_ACTIVE_FLAG` | Comp_Drms_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 67 | `COMP_PER_PROF_CODE` | Comp_Per_Professorial Code | VARCHAR2 | 4 |  | Y |
| 68 | `COMP_LAB_POST_DATE` | Comp_Lab_Postessorial Date | DATE | 7 |  | Y |
| 69 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 70 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 71 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 72 | `LAB_COST_CAT_CODE` | Lab_Cost_Catessorial Code | VARCHAR2 | 12 |  | Y |
| 73 | `COMP_LAB_STD_FLAG` | Comp_Lab_Stdessorial Flag | VARCHAR2 | 1 |  | Y |
| 74 | `LAB_STD_MEAS` | Lab_Stdessorial Meas | VARCHAR2 | 4 |  | Y |
| 75 | `MHE_COST_CAT_CODE` | Mhe_Cost_Catessorial Code | VARCHAR2 | 12 |  | Y |
| 76 | `COMP_ALLOW_ADJ_DATE_OVRR_FLAG` | Comp_Allow_Adj_Date_Ovrressorial Flag | VARCHAR2 | 1 |  | N |
| 77 | `COMP_PARA_LOC_SIZE_FLAG` | Comp_Para_Loc_Sizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 78 | `COMP_OUTB_SORT_CODE` | Comp_Outb_Sortessorial Code | VARCHAR2 | 4 |  | N |
| 79 | `COMP_PARA_EXT_INV_NUM_DES` | Comp_Para_Ext_Inv_Numessorial Des | VARCHAR2 | 12 |  | Y |
| 80 | `COMP_PARA_SALE_EXT_INV_FLAG` | Comp_Para_Sale_Ext_Invessorial Flag | VARCHAR2 | 1 |  | Y |
| 81 | `COMP_PARA_OP_PWORD_EXPY_NUM` | Comp_Para_Op_Pword_Expyessorial Num | NUMBER | 22 | 3 | Y |
| 82 | `COMP_DRMS_PHASE3_ACTIVE_FLAG` | Comp_Drms_Phase3_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 83 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 84 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 85 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 86 | `COMP_FLT_LOC_ACTIVE_FLAG` | Comp_Flt_Loc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 87 | `COMP_CAPC_WGT_ACTIVE_FLAG` | Comp_Capc_Wgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 88 | `COMP_DEXION_INTFACE_FLAG` | Comp_Dexion_Intfaceessorial Flag | VARCHAR2 | 1 |  | N |
| 89 | `COMP_LOOSE_WHSE_CODE_STATIC` | Comp_Loose_Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 90 | `COMP_LOOSE_LOC_CODE_STATIC` | Comp_Loose_Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 91 | `COMP_LOOSE_ISOL_CODE` | Comp_Loose_Isolessorial Code | VARCHAR2 | 4 |  | Y |
| 92 | `REG_PRT_CNT` | Reg_Prtessorial Cnt | NUMBER | 22 | 2 | Y |
| 93 | `COMP_PARA_REST_PALL_FLAG` | Comp_Para_Rest_Pallessorial Flag | VARCHAR2 | 1 |  | Y |
| 94 | `COMP_EXE_JAVA` | Comp_Exeessorial Java | VARCHAR2 | 20 |  | Y |
| 95 | `COMP_CAPC_CUBE_ACTIVE_FLAG` | Comp_Capc_Cube_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 96 | `COMP_CONSL_METH` | Comp_Conslessorial Meth | NUMBER | 22 | 1 | Y |
| 97 | `COMP_DRMS_AUTO_WAVE_FLAG` | Comp_Drms_Auto_Waveessorial Flag | VARCHAR2 | 1 |  | Y |
| 98 | `COMP_YARD_MGT_ACTIVE_FLAG` | Comp_Yard_Mgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 99 | `COMP_MAX_NUM_BAT_ORD` | Comp_Max_Num_Batessorial Ord | NUMBER | 22 | 4 | Y |
| 100 | `COMP_XDOCK_MGT_ACTIVE_FLAG` | Comp_Xdock_Mgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 101 | `COMP_PARA_NUM_REC_INB` | Comp_Para_Num_Recessorial Inb | NUMBER | 22 | 6 | Y |
| 102 | `COMP_PARA_NUM_REC_OUTB` | Comp_Para_Num_Recessorial Outb | NUMBER | 22 | 6 | Y |
| 103 | `COMP_PARA_CART_ACTIVE_FLAG` | Comp_Para_Cart_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 104 | `COMP_VEND_SHIP_FLAG` | Comp_Vend_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 105 | `CARR_EQUAL_TRSPT_EQP_OWN_FLAG` | Carr_Equal_Trspt_Eqp_Ownessorial Flag | VARCHAR2 | 1 |  | N |
| 106 | `COMP_UPDOWNSTREAM_TP` | Comp_Updownstreamessorial Tp | VARCHAR2 | 1 |  | Y |
| 107 | `COMP_USE_EXT_LOAD_NUM_FLAG` | Comp_Use_Ext_Load_Numessorial Flag | VARCHAR2 | 1 |  | Y |
| 108 | `COMP_FRT_INTFACE_PROF_CODE` | Comp_Frt_Intface_Professorial Code | VARCHAR2 | 4 |  | Y |
| 109 | `COMP_PURGE_ARCHIVE_DIR` | Comp_Purge_Archiveessorial Dir | VARCHAR2 | 250 |  | Y |
| 110 | `COMP_WHSE_ATTR_PROF_CODE` | Comp_Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 111 | `COMP_MGMT_HOLD_TP` | Comp_Mgmt_Holdessorial Tp | VARCHAR2 | 20 |  | Y |
| 112 | `COMP_APPO_ALLOW_UPD_CONF_FLAG` | Comp_Appo_Allow_Upd_Confessorial Flag | VARCHAR2 | 1 |  | Y |
| 113 | `COMP_UPDOWNSTRM_PROS_FRT_FLAG` | Comp_Updownstrm_Pros_Frtessorial Flag | VARCHAR2 | 1 |  | Y |
| 114 | `COMP_REPI_FROM_PICK_LOC_FLAG` | Comp_Repi_From_Pick_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 115 | `COMP_PRT_BACKGRND_ACTIVE_FLAG` | Comp_Prt_Backgrnd_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 116 | `COMP_EDI_REP_EMAIL_ADD` | Comp_Edi_Rep_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 117 | `COMP_EDI_ERR_REP_EMAIL_ADD` | Comp_Edi_Err_Rep_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 118 | `COMP_EXT_FRT_INTFACE_PROF_CODE` | Comp_Ext_Frt_Intface_Professorial Code | VARCHAR2 | 4 |  | Y |
| 119 | `COMP_EAN_UCC_PREX` | Comp_Ean_Uccessorial Prex | VARCHAR2 | 20 |  | Y |
| 120 | `COMP_MOVE_INB_ACTIVE_FLAG` | Comp_Move_Inb_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 121 | `COMP_MOVE_STOCK_ACTIVE_FLAG` | Comp_Move_Stock_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 122 | `COMP_ALLOW_ZERO_CO_MVT_FLAG` | Comp_Allow_Zero_Co_Mvtessorial Flag | VARCHAR2 | 1 |  | Y |
| 123 | `COMP_EXT_FRT_VERS1_IGNORE_FLAG` | Comp_Ext_Frt_Vers1_Ignoreessorial Flag | VARCHAR2 | 1 |  | Y |
| 124 | `COMP_PARA_ACTIVE_SCH_FLAG` | Comp_Para_Active_Schessorial Flag | VARCHAR2 | 1 |  | Y |
| 125 | `COMP_AUTODOC_ASS_LOC_FLOW_FLAG` | Comp_Autodoc_Ass_Loc_Flowessorial Flag | VARCHAR2 | 1 |  | Y |
| 126 | `COMP_PARA_INV_WHSE_REST_FLAG` | Comp_Para_Inv_Whse_Restessorial Flag | VARCHAR2 | 1 |  | Y |
| 127 | `COMP_PARA_INV_WHSE_REST_MAND` | Comp_Para_Inv_Whse_Restessorial Mand | VARCHAR2 | 1 |  | Y |
| 128 | `COMP_PARA_REM_BY_LINE_FLAG` | Comp_Para_Rem_By_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 129 | `COMP_PARA_RELO_WARE_REST_FLAG` | Comp_Para_Relo_Ware_Restessorial Flag | VARCHAR2 | 1 |  | Y |
| 130 | `COMP_PARA_WAVE_LABEL_DOC_CODE` | Comp_Para_Wave_Label_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 131 | `COMP_PARCEL_INTFACE_PROF_CODE` | Comp_Parcel_Intface_Professorial Code | VARCHAR2 | 4 |  | Y |
| 132 | `COMP_ORD_LOG_FLAG` | Comp_Ord_Logessorial Flag | VARCHAR2 | 1 |  | Y |
| 133 | `COMP_WAVE_PICK_METH_ASS_TP` | Comp_Wave_Pick_Meth_Assessorial Tp | VARCHAR2 | 4 |  | Y |
| 134 | `COMP_CHG_DECIMAL_NUM` | Comp_Chg_Decimalessorial Num | NUMBER | 22 | 1 | Y |
| 135 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 136 | `COMP_CONSL_R_ORD_D5D1_FLAG` | Comp_Consl_R_Ord_D5D1essorial Flag | VARCHAR2 | 1 |  | Y |
| 137 | `COMP_WHSE_REQD_FLAG` | Comp_Whse_Reqdessorial Flag | VARCHAR2 | 1 |  | Y |
| 138 | `COMP_PARA_ORD_TP` | Comp_Para_Ordessorial Tp | VARCHAR2 | 1 |  | Y |
| 139 | `COMP_PARA_RCPT_TP` | Comp_Para_Rcptessorial Tp | VARCHAR2 | 1 |  | Y |
| 140 | `COMP_PARA_DISP_CHG_CUST_FLAG` | Comp_Para_Disp_Chg_Custessorial Flag | VARCHAR2 | 1 |  | Y |
| 141 | `COMP_A1SCH_ACTIVE_FLAG` | Comp_A1Sch_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 142 | `COMP_A1SHIP_SHIP_ID_COMP_FLAG` | Comp_A1Ship_Ship_Id_Compessorial Flag | VARCHAR2 | 1 |  | Y |
| 143 | `COMP_PARA_UPD_CHG_QTY_SKU_FLAG` | Comp_Para_Upd_Chg_Qty_Skuessorial Flag | VARCHAR2 | 1 |  | Y |
| 144 | `COMP_FIN_DEPT_ENTRY_FLAG` | Comp_Fin_Dept_Entryessorial Flag | VARCHAR2 | 1 |  | Y |
| 145 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 146 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 147 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 148 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 149 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 150 | `COMP_PARA_MHE_FLAG` | Comp_Para_Mheessorial Flag | VARCHAR2 | 1 |  | Y |
| 151 | `COMP_REAS_ENTRY_ENBLD_FLAG` | Comp_Reas_Entry_Enbldessorial Flag | VARCHAR2 | 1 |  | Y |
| 152 | `COMP_TASK_GEN_ACTIVE_FLAG` | Comp_Task_Gen_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 153 | `COMP_EXT_LAB_SWARE_ACTIVE_FLAG` | Comp_Ext_Lab_Sware_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 154 | `COMP_ALLOC_TRACE_TP` | Comp_Alloc_Traceessorial Tp | VARCHAR2 | 1 |  | Y |
| 155 | `COMP_PALL_METH_CART_FLAG` | Comp_Pall_Meth_Cartessorial Flag | VARCHAR2 | 1 |  | Y |
| 156 | `COMP_VALID_APPO_STARTDATE_FLAG` | Comp_Valid_Appo_Startdateessorial Flag | VARCHAR2 | 1 |  | Y |
| 157 | `COMP_ALLOW_RESW_FLAG` | Comp_Allow_Reswessorial Flag | VARCHAR2 | 1 |  | Y |
| 158 | `COMP_PARA_PURGE_MIN_MONTH` | Comp_Para_Purge_Minessorial Month | NUMBER | 22 | 3 | Y |
| 159 | `COMP_PARA_PURGE_MULTI_SEL` | Comp_Para_Purge_Multiessorial Sel | VARCHAR2 | 1 |  | Y |
| 160 | `COMP_UPD_CARR_FROM_VBOL_FLAG` | Comp_Upd_Carr_From_Vbolessorial Flag | VARCHAR2 | 1 |  | Y |
| 161 | `COMP_PARA_PROS_RFSC_SPC_MODE` | Comp_Para_Pros_Rfsc_Spcessorial Mode | VARCHAR2 | 1 |  | Y |
| 162 | `COMP_AUTO_PROS_BILL_TP` | Comp_Auto_Pros_Billessorial Tp | VARCHAR2 | 1 |  | Y |
| 163 | `COMP_PARA_AUD_FLAG` | Comp_Para_Audessorial Flag | VARCHAR2 | 1 |  | Y |
| 164 | `COMP_APPO_UPD_CARR_FLAG` | Comp_Appo_Upd_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 165 | `COMP_APPO_UPD_LOAD_TP_FLAG` | Comp_Appo_Upd_Load_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 166 | `COMP_PARA_AUTO_MAIL_INV_FLAG` | Comp_Para_Auto_Mail_Invessorial Flag | VARCHAR2 | 1 |  | Y |
| 167 | `COMP_RF_DEVICE_ENABLE_FLAG` | Comp_Rf_Device_Enableessorial Flag | VARCHAR2 | 1 |  | Y |
| 168 | `COMP_ORD_CANCEL_ENABLE_FLAG` | Comp_Ord_Cancel_Enableessorial Flag | VARCHAR2 | 1 |  | Y |
| 169 | `COMP_PARA_RFPIC_SKIP_WHSE` | Comp_Para_Rfpic_Skipessorial Whse | VARCHAR2 | 1 |  | Y |
| 170 | `COMP_APPO_REAS_CODE_REQ` | Comp_Appo_Reas_Codeessorial Req | VARCHAR2 | 1 |  | Y |
| 171 | `COMP_OPID_MIX_ITEM_FLAG` | Comp_Opid_Mix_Itemessorial Flag | VARCHAR2 | 1 |  | Y |
| 172 | `COMP_RFOA_SKIP_ORD_FLAG` | Comp_Rfoa_Skip_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 173 | `COMP_EVENT_CYC_CNT_PER_WHSE` | Comp_Event_Cyc_Cnt_Peressorial Whse | VARCHAR2 | 1 |  | Y |
| 174 | `COMP_PARA_OPID_RET_DAYS` | Comp_Para_Opid_Retessorial Days | NUMBER | 22 | 4 | Y |
| 175 | `COMP_PARA_RCPT_LINE_TP` | Comp_Para_Rcpt_Lineessorial Tp | VARCHAR2 | 1 |  | Y |
| 176 | `COMP_PARA_RFPR_NOT_DISP_QTY` | Comp_Para_Rfpr_Not_Dispessorial Qty | VARCHAR2 | 1 |  | Y |
| 177 | `COMP_PARA_WAVE_SUSP_TASK_FLAG` | Comp_Para_Wave_Susp_Taskessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_COMP_PARA_TEMP`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 53
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_NUM_FIS_PER` | Comp_Num_Fisessorial Per | NUMBER | 22 | 2 | N |
| 3 | `COMP_FIRST_FIS_MON` | Comp_First_Fisessorial Mon | VARCHAR2 | 3 |  | N |
| 4 | `COMP_MULT_CUR_FLAG` | Comp_Mult_Curessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `COMP_CUR_CODE` | Comp_Curessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `COMP_FIN_INTFACE_CODE` | Comp_Fin_Intfaceessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `COMP_GL_ACTIVE_FLAG` | Comp_Gl_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `COMP_AP_ACTIVE_FLAG` | Comp_Ap_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `COMP_AP_GL_UPD_FLAG` | Comp_Ap_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `COMP_AR_ACTIVE_FLAG` | Comp_Ar_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `COMP_AR_GL_UPD_FLAG` | Comp_Ar_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `COMP_CC_ACTIVE_FLAG` | Comp_Cc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `COMP_CC_AR_UPD_FLAG` | Comp_Cc_Ar_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `COMP_PO_ACTIVE_FLAG` | Comp_Po_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `COMP_PO_AP_INTFACE_FLAG` | Comp_Po_Ap_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `COMP_PW_ACTIVE_FLAG` | Comp_Pw_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `COMP_NUM_DAY_RET_CON` | Comp_Num_Day_Retessorial Con | NUMBER | 22 | 4 | N |
| 18 | `COMP_PUB_PRVT_FLAG` | Comp_Pub_Prvtessorial Flag | VARCHAR2 | 2 |  | Y |
| 19 | `COMP_CUST_CODE` | Comp_Custessorial Code | VARCHAR2 | 10 |  | Y |
| 20 | `COMP_NUM_YEAR_RET_SALE_DATA` | Comp_Num_Year_Ret_Saleessorial Data | NUMBER | 22 | 1 | Y |
| 21 | `COMP_NUM_YEAR_RET_MANG_DATA` | Comp_Num_Year_Ret_Mangessorial Data | NUMBER | 22 | 1 | Y |
| 22 | `COMP_ALLOW_MAN_CON_FLAG` | Comp_Allow_Man_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `COMP_ALLOW_MAN_SHIP_FLAG` | Comp_Allow_Man_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `COMP_ALLOW_MAN_CARR_FLAG` | Comp_Allow_Man_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `COMP_DYN_LOC_RCPT_ACTIVE_FLAG` | Comp_Dyn_Loc_Rcpt_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `COMP_DYN_LOC_SHIP_ACTIVE_FLAG` | Comp_Dyn_Loc_Ship_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `COMP_FRT_ACTIVE_FLAG` | Comp_Frt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `COMP_TURN_ACTIVE_FLAG` | Comp_Turn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `COMP_NUM_YEAR_RET_TURN_DATA` | Comp_Num_Year_Ret_Turnessorial Data | NUMBER | 22 | 1 | Y |
| 30 | `COMP_TONN_ACTIVE_FLAG` | Comp_Tonn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `COMP_NUM_YEAR_RET_TONN_DATA` | Comp_Num_Year_Ret_Tonnessorial Data | NUMBER | 22 | 1 | Y |
| 32 | `COMP_BORD_ACTIVE_FLAG` | Comp_Bord_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `COMP_FORD_ACTIVE_FLAG` | Comp_Ford_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `COMP_INTRANS_ACTIVE_FLAG` | Comp_Intrans_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `COMP_SET_ASSEM_ACTIVE_FLAG` | Comp_Set_Assem_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 36 | `COMP_ITEM_PRI_ACTIVE_FLAG` | Comp_Item_Pri_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 37 | `COMP_DAY_ANAL_TP_FLAG` | Comp_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `COMP_DAY_DAY_ANAL_TP_FLAG` | Comp_Day_Day_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `COMP_DAY_DOC_ANAL_TP_FLAG` | Comp_Day_Doc_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `COMP_DAY_CARR_ANAL_TP_FLAG` | Comp_Day_Carr_Anal_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `COMP_ALLOW_HOLD_RCPT_FLAG` | Comp_Allow_Hold_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `COMP_CUST_CRT_ORD_VER_FLAG` | Comp_Cust_Crt_Ord_Veressorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `COMP_CODE_FIN` | Comp_Codeessorial Fin | VARCHAR2 | 2 |  | Y |
| 44 | `FRT_DEST_TYPE` | Frt_Destessorial Type | VARCHAR2 | 1 |  | N |
| 45 | `FRT_PRO_RATE_FORUL` | Frt_Pro_Rateessorial Forul | VARCHAR2 | 10 |  | N |
| 46 | `COMP_FRT_DEST_CODE` | Comp_Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 47 | `COMP_FRT_DEF_FLAG` | Comp_Frt_Defessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `COMP_FRT_FLAT_AMT` | Comp_Frt_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 49 | `COMP_FRT_PCENT_SAV` | Comp_Frt_Pcentessorial Sav | NUMBER | 22 | 6 | Y |
| 50 | `COMP_FRT_PCENT_FRT` | Comp_Frt_Pcentessorial Frt | NUMBER | 22 | 6 | Y |
| 51 | `COMP_FRT_DEFI_AMT_FLAG` | Comp_Frt_Defi_Amtessorial Flag | VARCHAR2 | 2 |  | Y |
| 52 | `COMP_FRT_STOP_CHG_FLAG` | Comp_Frt_Stop_Chgessorial Flag | VARCHAR2 | 2 |  | Y |
| 53 | `COMP_FRT_COMP_CODE` | Comp_Frt_Compessorial Code | VARCHAR2 | 2 |  | N |

## `M_COMP_PROF_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `COMP_PROF_CODE` | Comp_Professorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `COMP_PROF_DES` | Comp_Professorial Des | VARCHAR2 | 30 |  | Y |
| 4 | `COMP_PROF_VAL` | Comp_Professorial Val | VARCHAR2 | 20 |  | Y |
| 5 | `COMP_PARA_FLD` | Comp_Paraessorial Fld | VARCHAR2 | 100 |  | Y |
| 6 | `COMP_PROF_STR` | Comp_Professorial Str | VARCHAR2 | 100 |  | Y |
| 7 | `COMP_PROF_TAB` | Comp_Professorial Tab | VARCHAR2 | 80 |  | Y |
| 8 | `COMP_PROF_TAB_FLD` | Comp_Prof_Tabessorial Fld | VARCHAR2 | 80 |  | Y |

## `M_COMP_PROF_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `COMP_PROF_CODE` | Comp_Professorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `COMP_PROF_DES` | Comp_Professorial Des | VARCHAR2 | 30 |  | Y |
| 4 | `COMP_PROF_VAL` | Comp_Professorial Val | VARCHAR2 | 20 |  | Y |
| 5 | `COMP_PARA_FLD` | Comp_Paraessorial Fld | VARCHAR2 | 100 |  | Y |
| 6 | `COMP_PROF_STR` | Comp_Professorial Str | VARCHAR2 | 100 |  | Y |
| 7 | `COMP_PROF_TAB` | Comp_Professorial Tab | VARCHAR2 | 80 |  | Y |
| 8 | `COMP_PROF_TAB_FLD` | Comp_Prof_Tabessorial Fld | VARCHAR2 | 80 |  | Y |

## `M_COMP_SEL`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMP_TZNAME_CHANGE`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `COMP_TZ_NAME_PRV` | Comp_Tz_Nameessorial Prv | VARCHAR2 | 64 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COMP_VIRT`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE_VIRT` | Comp_Codeessorial Virt | VARCHAR2 | 2 |  | N |
| 3 | `COMP_VIRT_RCPT_LEV_NUM` | Comp_Virt_Rcpt_Levessorial Num | NUMBER | 22 | 1 | N |
| 4 | `COMP_VIRT_ORD_LEV_NUM` | Comp_Virt_Ord_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `CUST_CODE_ORD` | Cust_Codeessorial Ord | VARCHAR2 | 10 |  | Y |
| 6 | `FLOW_PROS_CODE_ORD` | Flow_Pros_Codeessorial Ord | VARCHAR2 | 4 |  | N |
| 7 | `FLOW_PROS_CODE_RCPT` | Flow_Pros_Codeessorial Rcpt | VARCHAR2 | 4 |  | N |
| 8 | `COMP_VIRT_ORD_REF` | Comp_Virt_Ordessorial Ref | VARCHAR2 | 30 |  | N |
| 9 | `EXE_JOB_CODE_RCPT` | Exe_Job_Codeessorial Rcpt | VARCHAR2 | 10 |  | N |

## `M_DOOR_D1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOOR_D2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 5 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 6 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOOR_D3`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOOR_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 5 | `DOOR_TP_FLAG` | Door_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DOOR_DES` | Dooressorial Des | VARCHAR2 | 30 |  | N |
| 7 | `DOOR_INB_START_TIME` | Door_Inb_Startessorial Time | VARCHAR2 | 5 |  | Y |
| 8 | `DOOR_INB_END_TIME` | Door_Inb_Endessorial Time | VARCHAR2 | 5 |  | Y |
| 9 | `DOOR_OUTB_START_TIME` | Door_Outb_Startessorial Time | VARCHAR2 | 5 |  | Y |
| 10 | `DOOR_OUTB_END_TIME` | Door_Outb_Endessorial Time | VARCHAR2 | 5 |  | Y |
| 11 | `DOOR_STAT` | Dooressorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 14 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | Y |
| 15 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | Y |
| 16 | `STAG_WHSE_CODE` | Stag_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `STAG_LOC_CODE` | Stag_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 18 | `YARD_LOC_VERT_LEV` | Yarehouse Loc Vert Lev | NUMBER | 22 | 2 | Y |
| 19 | `RFID_READER_ID` | Rfid_Readeressorial Id | VARCHAR2 | 20 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 25 | `DOOR_DATA_SERVICE_ID` | Door_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |

## `M_DOOR_VEH_TP`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 5 | `VEH_TP_CODE` | Veh_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 47
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `LOC_DES` | Locessorial Des | VARCHAR2 | 30 |  | Y |
| 6 | `LOC_STAT` | Locessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 8 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 9 | `LOC_HGT` | Locessorial Hgt | NUMBER | 22 | 7 | N |
| 10 | `LOC_WID` | Locessorial Wid | NUMBER | 22 | 7 | N |
| 11 | `LOC_LEN` | Locessorial Len | NUMBER | 22 | 7 | N |
| 12 | `LOC_CUBE` | Locessorial Cube | NUMBER | 22 | 10 | N |
| 13 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 14 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 15 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 16 | `LOC_MAX_SKU_CAPC` | Loc_Max_Skuessorial Capc | VARCHAR2 | 4 |  | N |
| 17 | `SKU_CAPC_PCENT` | Sku_Capcessorial Pcent | NUMBER | 22 |  | N |
| 18 | `SPACE_CAPC_PCENT` | Space_Capcessorial Pcent | NUMBER | 22 |  | N |
| 19 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 22 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 24 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 25 | `LOC_WGT` | Locessorial Wgt | NUMBER | 22 | 14 | N |
| 26 | `LOC_CODE_WGT_MAST` | Loc_Code_Wgtessorial Mast | VARCHAR2 | 12 |  | Y |
| 27 | `LOC_STRUCT_TP_CODE` | Loc_Struct_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 28 | `LOC_SHIP_UNIT_ID` | Loc_Ship_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 29 | `LOC_CODE_STATIC_EMPTY_DEF` | Loc_Code_Static_Emptyessorial Def | VARCHAR2 | 12 |  | Y |
| 30 | `LOC_USE_LAST_PUT_FLAG` | Loc_Use_Last_Putessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `LOC_VERT_HGT_FACT_CODE` | Loc_Vert_Hgt_Factessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `LOC_VOICE_CHK_DIGIT1` | Loc_Voice_Chkessorial Digit1 | NUMBER | 22 | 5 | Y |
| 33 | `LOC_VOICE_CHK_DIGIT2` | Loc_Voice_Chkessorial Digit2 | NUMBER | 22 | 5 | Y |
| 34 | `LOC_VOICE_CHK_DIGIT3` | Loc_Voice_Chkessorial Digit3 | NUMBER | 22 | 5 | Y |
| 35 | `PICK_SEQ_NUM` | Pick_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 36 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 37 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 38 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 39 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 40 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 41 | `LOC_AISLE_REF` | Loc_Aisleessorial Ref | VARCHAR2 | 4 |  | Y |
| 42 | `LOC_FACING_REF` | Loc_Facingessorial Ref | VARCHAR2 | 4 |  | Y |
| 43 | `LOC_FRONT_ALIAS` | Loc_Frontessorial Alias | VARCHAR2 | 12 |  | Y |
| 44 | `LOC_FRONT_ALIAS_CHK_DIGIT` | Loc_Front_Alias_Chkessorial Digit | NUMBER | 22 | 5 | Y |
| 45 | `LOC_BACK_ALIAS` | Loc_Backessorial Alias | VARCHAR2 | 12 |  | Y |
| 46 | `LOC_BACK_ALIAS_CHK_DIGIT` | Loc_Back_Alias_Chkessorial Digit | NUMBER | 22 | 5 | Y |
| 47 | `PUT_SEQ_NUM` | Put_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `M_LOC_BILL`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_BILL_DES` | Loc_Billessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LOC_BILL_STAT` | Loc_Billessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 12 | `LOC_BILL_OPID_FLAG` | Loc_Bill_Opidessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_LOC_BILL_WHSE`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 4 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_BILL_WHSE_REST`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_PICK_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 8 | `SKU_CODE_PICK` | Sku_Codeessorial Pick | VARCHAR2 | 4 |  | N |
| 9 | `OVFL_SEQ_NUM` | Ovfl_Seqessorial Num | NUMBER | 22 | 2 | N |
| 10 | `WHSE_CODE_OVFL` | Whse_Codeessorial Ovfl | VARCHAR2 | 4 |  | N |
| 11 | `LOC_CODE_OVFL` | Loc_Codeessorial Ovfl | VARCHAR2 | 12 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_PICK_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 8 | `SKU_CODE_PICK` | Sku_Codeessorial Pick | VARCHAR2 | 4 |  | N |
| 9 | `LOC_PICK_REPL_QTY` | Loc_Pick_Replessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `SKU_CODE_REPL` | Sku_Codeessorial Repl | VARCHAR2 | 4 |  | N |
| 11 | `LOC_PICK_MIN_QTY` | Loc_Pick_Minessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `LOC_PICK_LAST_PICK_DATE` | Loc_Pick_Last_Pickessorial Date | DATE | 7 |  | Y |
| 13 | `LOC_PICK_REPL_FLAG` | Loc_Pick_Replessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `LOC_PICK_REPL_QTY_RND_METH` | Loc_Pick_Repl_Qty_Rndessorial Meth | VARCHAR2 | 1 |  | Y |
| 15 | `LOC_PICK_PRO_ACTIVE_FLAG` | Loc_Pick_Pro_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `LOC_PICK_FORCE_TO_GEN_FLAG` | Loc_Pick_Force_To_Genessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `LOC_PICK_NOT_USE_DAY` | Loc_Pick_Not_Useessorial Day | NUMBER | 22 | 4 | Y |
| 18 | `LOC_PICK_ALERT_QTY` | Loc_Pick_Alertessorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 24 | `LOC_PICK_ALLOW_HOLD_INVT_FLAG` | Loc_Pick_Allow_Hold_Invtessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_LOC_PRT_PROF_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 5 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_PRT_PROF_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_PRT_PROF_DES` | Loc_Prt_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LOC_PRT_PROF_STAT` | Loc_Prt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_SIZE_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_SIZE_OVFL_NUM` | Loc_Size_Ovflessorial Num | NUMBER | 22 | 2 | N |
| 5 | `LOC_SIZE_CODE_OVFL` | Loc_Size_Codeessorial Ovfl | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_SIZE_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_SIZE_DES` | Loc_Sizeessorial Des | VARCHAR2 | 40 |  | N |
| 5 | `LOC_SIZE_STAT` | Loc_Sizeessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOC_TMP`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `LOC_DES` | Locessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `LOC_STAT` | Locessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 7 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_HGT` | Locessorial Hgt | NUMBER | 22 | 7 | N |
| 9 | `LOC_WID` | Locessorial Wid | NUMBER | 22 | 7 | N |
| 10 | `LOC_LEN` | Locessorial Len | NUMBER | 22 | 7 | N |
| 11 | `LOC_CUBE` | Locessorial Cube | NUMBER | 22 | 10 | N |
| 12 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 15 | `LOC_MAX_SKU_CAPC` | Loc_Max_Skuessorial Capc | NUMBER | 22 | 3 | N |
| 16 | `SKU_CAPC_PCENT` | Sku_Capcessorial Pcent | FLOAT | 22 | 30 | N |
| 17 | `SPACE_CAPC_PCENT` | Space_Capcessorial Pcent | FLOAT | 22 | 30 | N |
| 18 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `LOC_NUM` | Locessorial Num | NUMBER | 22 | 6 | N |
| 20 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 22 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 24 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 25 | `LOC_WGT` | Locessorial Wgt | NUMBER | 22 | 14 | N |
| 26 | `LOC_CODE_WGT_MAST` | Loc_Code_Wgtessorial Mast | VARCHAR2 | 12 |  | Y |
| 27 | `LOC_STRUCT_TP_CODE` | Loc_Struct_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 28 | `LOC_SHIP_UNIT_ID` | Loc_Ship_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 29 | `LOC_CODE_STATIC_EMPTY_DEF` | Loc_Code_Static_Emptyessorial Def | VARCHAR2 | 12 |  | Y |

## `M_LOC_TP`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_TP_DES` | Loc_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LOC_TP_STAT` | Loc_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LOC_TP_SEQ` | Loc_Tpessorial Seq | NUMBER | 22 | 4 | N |
| 7 | `LOC_TP_DYN_PUT_FLAG` | Loc_Tp_Dyn_Putessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LOC_TP_PICK_FLAG` | Loc_Tp_Pickessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `LOC_TP_DYN_PICK_FLAG` | Loc_Tp_Dyn_Pickessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `LOC_TP_STAGE_FLAG` | Loc_Tp_Stageessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `LOC_TP_LAB_STD_MODY_NUM` | Loc_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 12 | `LOC_TP_ASS_FLT_FLAG` | Loc_Tp_Ass_Fltessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `LOC_TP_STAG_ALLOW_PICK` | Loc_Tp_Stag_Allowessorial Pick | VARCHAR2 | 1 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 19 | `LOC_TP_PRTY_PICK_FLAG` | Loc_Tp_Prty_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `LOC_TP_STAGE_SGL_FUNC_FLAG` | Loc_Tp_Stage_Sgl_Funcessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `LOC_TP_NOT_ALLOW_MIX_LEV_NUM` | Loc_Tp_Not_Allow_Mix_Levessorial Num | VARCHAR2 | 1 |  | Y |
| 22 | `LOC_TP_STAGE_TP_CODE` | Loc_Tp_Stage_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_TP_RES_FOR_PARTL_PLT_FLAG` | Loc_Tp_Res_For_Partl_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `LOC_TP_DISABLE_THREE_STEP_PUT` | Loc_Tp_Disable_Three_Stepessorial Put | VARCHAR2 | 1 |  | Y |
| 25 | `LOC_TP_ENBLD_LOC_ALIAS` | Loc_Tp_Enbld_Locessorial Alias | VARCHAR2 | 1 |  | Y |
| 26 | `LOC_TP_SUPPRESS_REPI_MERGE_LOC` | Loc_Tp_Suppress_Repi_Mergeessorial Loc | VARCHAR2 | 1 |  | Y |

## `M_WHSE_ACT_TP_NUM_PRTY`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 5 | `PRTY_NUM` | Prtyessorial Num | NUMBER | 22 | 2 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_ATTR_PROF_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_ATTR_TP_NUM` | Whse_Attr_Tpessorial Num | NUMBER | 22 | 3 | N |
| 5 | `WHSE_ATTR_TP_OPT_NUM` | Whse_Attr_Tp_Optessorial Num | NUMBER | 22 | 3 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_ATTR_PROF_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_ATTR_PROF_DES` | Whse_Attr_Professorial Des | VARCHAR2 | 40 |  | N |
| 5 | `WHSE_ATTR_PROF_STAT` | Whse_Attr_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 11 | `LOAD_MAX_WGT` | Load_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 12 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOAD_MAX_CUBE` | Load_Maxessorial Cube | NUMBER | 22 | 16 | Y |
| 14 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |

## `M_WHSE_CHEP_ATTR`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `COMNCTR_COUNTRY` | Comnctressorial Country | VARCHAR2 | 2 |  | Y |
| 5 | `COMNCTR_CODE` | Comnctressorial Code | VARCHAR2 | 18 |  | Y |
| 6 | `LAYOUT_VERS` | Layoutessorial Vers | VARCHAR2 | 4 |  | Y |
| 7 | `INFRM_COUNTRY_CODE` | Infrm_Countryessorial Code | VARCHAR2 | 2 |  | Y |
| 8 | `SENDER_CODE_QUAL` | Sender_Codeessorial Qual | VARCHAR2 | 2 |  | Y |
| 9 | `SENDER_CODE` | Senderessorial Code | VARCHAR2 | 30 |  | Y |
| 10 | `RECVR_CODE_QUAL` | Recvr_Codeessorial Qual | VARCHAR2 | 2 |  | Y |
| 11 | `RECVR_CODE_PREX` | Recvr_Codeessorial Prex | VARCHAR2 | 2 |  | Y |
| 12 | `EQP_CODE_QUAL` | Eqp_Codeessorial Qual | VARCHAR2 | 2 |  | Y |
| 13 | `REF1_PREX` | Ref1essorial Prex | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_CUST_CON_OPID_RULE`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `OPID_MIX_ITEM_FLAG` | Opid_Mix_Itemessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_CUST_SCAN_UI_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `WHSE_CUST_SCAN_UI_FLAG` | Warehouse Cust Scan Ui Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_CUST_SCAN_UI_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `WHSE_CUST_SCAN_UI_FLAG` | Warehouse Cust Scan Ui Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_D1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE_CHAR_SEQ_NUM` | Loc_Code_Char_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `LOC_CODE_CHAR_VAL_CHAR` | Loc_Code_Char_Valessorial Char | VARCHAR2 | 50 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_D2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 2 |  | N |
| 4 | `WHSE_LOC_ATTR_NUM` | Warehouse Loc Attr Num | NUMBER | 22 | 2 | N |
| 5 | `WHSE_LOC_ATTR_NAME` | Warehouse Loc Attr Name | VARCHAR2 | 30 |  | N |
| 6 | `WHSE_LOC_ATTR_START_POS` | Warehouse Loc Attr Start Pos | NUMBER | 22 | 2 | N |
| 7 | `WHSE_LOC_ATTR_END_POS` | Warehouse Loc Attr End Pos | NUMBER | 22 | 2 | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WHSE_D3`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_LOC_ATTR_CODE` | Warehouse Loc Attr Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_LOC_ATTR_START_POS` | Warehouse Loc Attr Start Pos | NUMBER | 22 | 2 | N |
| 6 | `WHSE_LOC_ATTR_END_POS` | Warehouse Loc Attr End Pos | NUMBER | 22 | 2 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 12 | `PROXIMITY_SEQ_NUM` | Proximity_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 13 | `PROXIMITY_LOCAL` | Proximityessorial Local | VARCHAR2 | 2 |  | Y |

## `M_WHSE_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 33
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_NAME` | Warehouse Name | VARCHAR2 | 30 |  | N |
| 5 | `WHSE_STAT` | Warehouse Stat | VARCHAR2 | 1 |  | N |
| 6 | `WHSE_ADD1` | Whseessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `WHSE_ADD2` | Whseessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `WHSE_ADD3` | Whseessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `WHSE_LOC_CODE_LEN` | Warehouse Loc Code Len | NUMBER | 22 | 2 | N |
| 11 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `WHSE_LAB_CAPT_FLAG` | Warehouse Lab Capt Flag | VARCHAR2 | 1 |  | N |
| 13 | `WHSE_LAB_STD_MODY_NUM` | Warehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 14 | `WHSE_ADD4` | Whseessorial Add4 | VARCHAR2 | 30 |  | Y |
| 15 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 16 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 17 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 18 | `MOVE_ATTR_PROF_CODE` | Move_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `WHSE_VOICE_CHK_DIGIT_LEV_FLAG` | Warehouse Voice Chk Digit Lev Flag | VARCHAR2 | 2 |  | Y |
| 20 | `WHSE_VOICE_CHK_DIGIT1_DAY_STR` | Warehouse Voice Chk Digit Day Str | VARCHAR2 | 7 |  | Y |
| 21 | `WHSE_VOICE_CHK_DIGIT2_DAY_STR` | Warehouse Voice Chk Digit Day Str | VARCHAR2 | 7 |  | Y |
| 22 | `WHSE_VOICE_CHK_DIGIT3_DAY_STR` | Warehouse Voice Chk Digit Day Str | VARCHAR2 | 7 |  | Y |
| 23 | `WHSE_ESTAB_NUM` | Warehouse Estab Num | VARCHAR2 | 20 |  | Y |
| 24 | `WHSE_COUNTRY_ORIGIN` | Warehouse Country Origin | VARCHAR2 | 4 |  | Y |
| 25 | `EXT_FILE_SEQ_NUM` | Ext_File_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 26 | `WHSE_ALLOW_CREATE_LOC_FLAG` | Whse_Allow_Create_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `LOC_CODE_DEF` | Loc_Codeessorial Def | VARCHAR2 | 12 |  | Y |
| 28 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 29 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 30 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 31 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 32 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 33 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_WHSE_LOC_ATTR_BLK`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_LOC_ATTR_NUM` | Warehouse Loc Attr Num | NUMBER | 22 | 1 | N |
| 4 | `WHSE_LOC_ALLOW_BLK` | Warehouse Loc Allow Blk | VARCHAR2 | 1 |  | N |
| 5 | `WHSE_LOC_ATTR_BLK_CL_MI` | Warehouse Loc Attr Blk Cl Mi | NUMBER | 22 | 4 | Y |

## `M_WHSE_SHIFT`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_SHIFT_DES` | Warehouse Shift Description | VARCHAR2 | 30 |  | N |
| 6 | `WHSE_SHIFT_STAT` | Warehouse Shift Stat | VARCHAR2 | 1 |  | N |
| 7 | `WHSE_SHIFT_START_TIME` | Warehouse Shift Start Time | VARCHAR2 | 5 |  | Y |
| 8 | `WHSE_SHIFT_END_TIME` | Warehouse Shift End Time | VARCHAR2 | 5 |  | Y |
| 9 | `WHSE_SHIFT_EXT_REF_NUM1` | Warehouse Shift Ext Ref Num | VARCHAR2 | 100 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_YARD_ATTR_TP_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |
| 4 | `YARD_ATTR_DES` | Yard Attitbute Description | VARCHAR2 | 30 |  | N |
| 5 | `YARD_ATTR_STAT` | Yarehouse Attr Stat | VARCHAR2 | 1 |  | N |
| 6 | `YARD_ATTR_MEAS_CODE` | Yarehouse Attr Meas Code | VARCHAR2 | 4 |  | Y |
| 7 | `YARD_ATTR_VAL` | Yarehouse Attr Val | NUMBER | 22 | 16 | Y |

## `M_YARD_ATTR_TP_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_ATTR_TP_DES` | Yarehouse Attr Tp Des | VARCHAR2 | 30 |  | N |
| 4 | `YARD_ATTR_TP_STAT` | Yarehouse Attr Tp Stat | VARCHAR2 | 1 |  | N |
| 5 | `YARD_ATTR_TP_MAND_ENTRY_FLAG` | Yarehouse Attr Tp Mand Entry Flag | VARCHAR2 | 3 |  | N |
| 6 | `QUAL_CODE` | Qualessorial Code | VARCHAR2 | 4 |  | Y |

## `M_YARD_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_PARTIT_NUM` | Yarehouse Loc Partit Num | NUMBER | 22 | 2 | N |
| 4 | `YARD_LOC_PARTIT_DES` | Yarehouse Loc Partit Des | VARCHAR2 | 30 |  | N |
| 5 | `YARD_LOC_PARTIT_LEN` | Yarehouse Loc Partit Len | NUMBER | 22 | 2 | N |
| 6 | `YARD_LOC_PARTIT_EXACT_LEN_FLAG` | Yarehouse Loc Partit Exact Len Flag | VARCHAR2 | 1 |  | N |
| 7 | `YARD_LOC_PARTIT_TASK_BLK_FLAG` | Yarehouse Loc Partit Task Blk Flag | VARCHAR2 | 1 |  | N |
| 8 | `YARD_LOC_PARTIT_TASK_SAME_FLAG` | Yarehouse Loc Partit Task Same Flag | VARCHAR2 | 1 |  | N |
| 9 | `YARD_LOC_PARTIT_VAL_CHAR_FLAG` | Yarehouse Loc Partit Val Char Flag | VARCHAR2 | 1 |  | N |

## `M_YARD_DD`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_PARTIT_NUM` | Yarehouse Loc Partit Num | NUMBER | 22 | 2 | N |
| 4 | `YARD_LOC_PARTIT_CHAR_SEQ_NUM` | Yarehouse Loc Partit Char Seq Num | NUMBER | 22 | 2 | N |
| 5 | `YARD_LOC_PARTIT_CHAR_VAL_CHAR` | Yarehouse Loc Partit Char Val Char | VARCHAR2 | 50 |  | Y |

## `M_YARD_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 4 | `YARD_NAME` | Yarehouse Name | VARCHAR2 | 30 |  | N |
| 5 | `YARD_STAT` | Yarehouse Stat | VARCHAR2 | 1 |  | N |
| 6 | `YARD_ADD1` | Yarehouse Add | VARCHAR2 | 30 |  | N |
| 7 | `YARD_ADD2` | Yarehouse Add | VARCHAR2 | 30 |  | Y |
| 8 | `YARD_ADD3` | Yarehouse Add | VARCHAR2 | 30 |  | Y |
| 9 | `YARD_ADD4` | Yarehouse Add | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 13 | `YARD_LOC_NUM_PARTIT` | Yarehouse Loc Num Partit | NUMBER | 22 | 2 | N |
| 14 | `YARD_LOC_CODE_LEN` | Yarehouse Loc Code Len | NUMBER | 22 | 2 | N |
| 15 | `YARD_LAB_STD_MODY_NUM` | Yarehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 16 | `YARD_EXT_REF_NUM1` | Yarehouse Ext Ref Num | VARCHAR2 | 20 |  | Y |
| 17 | `RF_HOSTLER_ACT_FLAG` | Rf_Hostler_Actessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 23 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_YARD_INFO_FLOW_PROF_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INFO_FLOW_INB_OUTB_FLAG` | Yarehouse Info Flow Inb Outb Flag | VARCHAR2 | 1 |  | N |
| 4 | `YARD_INFO_FLOW_SEQ_NUM` | Yarehouse Info Flow Seq Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `YARD_INFO_FLOW_PROS_MAND_FLAG` | Yarehouse Info Flow Pros Mand Flag | VARCHAR2 | 1 |  | N |
| 7 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 9 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `YARD_INFO_FLOW_CR_PROF_FLAG` | Yarehouse Info Flow Cr Prof Flag | VARCHAR2 | 1 |  | Y |
| 11 | `YARD_INFO_FLOW_CR_DRMS_FLAG` | Yarehouse Info Flow Cr Drms Flag | VARCHAR2 | 1 |  | N |

## `M_YARD_INFO_FLOW_PROF_DD1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INFO_FLOW_INB_OUTB_FLAG` | Yarehouse Info Flow Inb Outb Flag | VARCHAR2 | 1 |  | N |
| 4 | `YARD_INFO_FLOW_SEQ_NUM` | Yarehouse Info Flow Seq Num | NUMBER | 22 | 2 | N |
| 5 | `YARD_INFO_FLOW_DOC_SEQ_NUM` | Yarehouse Info Flow Doc Seq Num | NUMBER | 22 | 2 | N |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 8 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `M_YARD_INFO_FLOW_PROF_DD2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INFO_FLOW_INB_OUTB_FLAG` | Yarehouse Info Flow Inb Outb Flag | VARCHAR2 | 1 |  | N |
| 4 | `YARD_INFO_FLOW_SEQ_NUM` | Yarehouse Info Flow Seq Num | NUMBER | 22 | 2 | N |
| 5 | `YARD_INFO_FLOW_SV_SEQ_NUM` | Yarehouse Info Flow Sv Seq Num | NUMBER | 22 | 2 | N |
| 6 | `SPC_VER_CODE` | Spc_Veressorial Code | VARCHAR2 | 4 |  | N |
| 7 | `YARD_INFO_FLOW_SV_COMPL_FLAG` | Yarehouse Info Flow Sv Compl Flag | VARCHAR2 | 1 |  | N |
| 8 | `YARD_INFO_FLOW_SV_SEQ_FLAG` | Yarehouse Info Flow Sv Seq Flag | VARCHAR2 | 1 |  | N |
| 9 | `YARD_INFO_FLOW_SV_DISP_FLAG` | Yarehouse Info Flow Sv Disp Flag | VARCHAR2 | 1 |  | N |

## `M_YARD_INFO_FLOW_PROF_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INFO_FLOW_PROF_DES` | Yarehouse Info Flow Prof Des | VARCHAR2 | 30 |  | N |
| 4 | `YARD_INFO_FLOW_PROF_STAT` | Yarehouse Info Flow Prof Stat | VARCHAR2 | 1 |  | N |

## `M_YARD_LOC_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | N |
| 4 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 5 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |

## `M_YARD_LOC_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | N |
| 4 | `YARD_LOC_DES` | Yarehouse Loc Des | VARCHAR2 | 30 |  | Y |
| 5 | `YARD_LOC_STAT` | Yarehouse Loc Stat | VARCHAR2 | 1 |  | N |
| 6 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 8 | `YARD_LOC_STACK_FLAG` | Yarehouse Loc Stack Flag | VARCHAR2 | 1 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `YARD_LOC_LAB_STD_MODY_NUM` | Yarehouse Loc Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 11 | `YARD_LOC_VERT_LEV` | Yarehouse Loc Vert Lev | NUMBER | 22 | 2 | N |

## `M_YARD_LOC_PROF_D`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_LOC_PROF_CODE` | Yarehouse Loc Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INB_OUTB_CODE` | Yarehouse Inb Outb Code | VARCHAR2 | 4 |  | N |
| 4 | `YARD_LOC_PROF_SEQ_NUM` | Yarehouse Loc Prof Seq Num | NUMBER | 22 | 2 | N |
| 5 | `YARD_LOC_PROF_SEQ_DES` | Yarehouse Loc Prof Seq Des | VARCHAR2 | 30 |  | N |
| 6 | `YARD_CODE_REST` | Yarehouse Code Rest | VARCHAR2 | 80 |  | Y |
| 7 | `YARD_LOC_CODE_REST` | Yarehouse Loc Code Rest | VARCHAR2 | 80 |  | Y |

## `M_YARD_LOC_PROF_DD`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_LOC_PROF_CODE` | Yarehouse Loc Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_INB_OUTB_CODE` | Yarehouse Inb Outb Code | VARCHAR2 | 4 |  | N |
| 4 | `YARD_LOC_PROF_SEQ_NUM` | Yarehouse Loc Prof Seq Num | NUMBER | 22 | 2 | N |
| 5 | `YARD_INB_OUTB_PARA_NUM` | Yarehouse Inb Outb Para Num | NUMBER | 22 | 2 | N |
| 6 | `YARD_INB_OUTB_PARA_OPT_NUM` | Yarehouse Inb Outb Para Opt Num | NUMBER | 22 | 2 | N |

## `M_YARD_LOC_PROF_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_LOC_PROF_CODE` | Yarehouse Loc Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_LOC_PROF_DES` | Yarehouse Loc Prof Des | VARCHAR2 | 30 |  | N |
| 4 | `YARD_LOC_PROF_STAT` | Yarehouse Loc Prof Stat | VARCHAR2 | 1 |  | N |
| 5 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | Y |
| 6 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | Y |

## `M_YARD_PARA`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `YARD_INFO_FLOW_PROF_CODE` | Yarehouse Info Flow Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `YARD_CODE_CHECK_IN` | Yarehouse Code Check In | VARCHAR2 | 4 |  | N |
| 4 | `YARD_LOC_CODE_CHECK_IN` | Yarehouse Loc Code Check In | VARCHAR2 | 12 |  | N |
| 5 | `YARD_LOC_VERT_LEV_CHECK_IN` | Yarehouse Loc Vert Lev Check In | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE_TRSPT_TO_DOOR` | Flow_Pros_Code_Trspt_Toessorial Door | VARCHAR2 | 4 |  | N |
| 7 | `FLOW_PROS_CODE_TRSPT_TO_YARD` | Flow_Pros_Code_Trspt_Toessorial Yard | VARCHAR2 | 4 |  | N |
| 8 | `FLOW_PROS_CODE_TRSPT_CLOSED` | Flow_Pros_Code_Trsptessorial Closed | VARCHAR2 | 4 |  | N |
| 9 | `FLOW_PROS_CODE_IN_YARD_LOADED` | Flow_Pros_Code_In_Yardessorial Loaded | VARCHAR2 | 4 |  | N |
| 10 | `FLOW_PROS_CODE_TRSPT_CHECK_IN` | Flow_Pros_Code_Trspt_Checkessorial In | VARCHAR2 | 4 |  | N |
| 11 | `YARD_INB_LOAD_FLAG` | Yarehouse Inb Load Flag | VARCHAR2 | 1 |  | N |
| 12 | `YARD_OUTB_LOAD_FLAG` | Yarehouse Outb Load Flag | VARCHAR2 | 1 |  | N |
| 13 | `YARD_CHECK_IN_INFO_FLAG` | Yarehouse Check In Info Flag | VARCHAR2 | 1 |  | N |

## `M_ZONE_D1`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `ZONE_INB_OUTB_FLAG` | Zarehouse Inb Outb Flag | VARCHAR2 | 1 |  | N |
| 7 | `ZONE_TP_CODE` | Zarehouse Tp Code | VARCHAR2 | 4 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ZONE_D2`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 4 | `ZONE_CODE_SPAN` | Zarehouse Code Span | VARCHAR2 | 4 |  | N |
| 5 | `ZONE_TP_CODE` | Zarehouse Tp Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ZONE_D3`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 4 | `ZONE_INB_OUTB_FLAG` | Zarehouse Inb Outb Flag | VARCHAR2 | 1 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `ZONE_SEQ_NUM` | Zarehouse Seq Num | NUMBER | 22 | 2 | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ZONE_D4`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 4 | `ZONE_OVFL_NUM` | Zarehouse Ovfl Num | NUMBER | 22 | 9 | N |
| 5 | `ZONE_CODE_OVFL` | Zarehouse Code Ovfl | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ZONE_H`

- **Tipo:** Master
- **Categoria:** Locations
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 4 | `ZONE_DES` | Zarehouse Des | VARCHAR2 | 30 |  | N |
| 5 | `ZONE_STAT` | Zarehouse Stat | VARCHAR2 | 1 |  | N |
| 6 | `ZONE_LAB_STD_MODY_NUM` | Zarehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 7 | `ZONE_COMM_REF` | Zarehouse Comm Ref | VARCHAR2 | 20 |  | Y |
| 8 | `ZONE_SORT_VALUE` | Zarehouse Sort Value | NUMBER | 22 | 4 | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 11 | `ZONE_TP_CODE` | Zarehouse Tp Code | VARCHAR2 | 4 |  | N |
| 12 | `MHE_TP_CODE_INB` | Mhe_Tp_Codeessorial Inb | VARCHAR2 | 4 |  | Y |
| 13 | `MHE_TP_CODE_OUTB_EMPTY` | Mhe_Tp_Code_Outbessorial Empty | VARCHAR2 | 4 |  | Y |
| 14 | `MHE_TP_CODE_OUTB_PART` | Mhe_Tp_Code_Outbessorial Part | VARCHAR2 | 4 |  | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 20 | `ZONE_TASK_GEN_ACTIVE_FLAG` | Zarehouse Task Gen Active Flag | VARCHAR2 | 1 |  | Y |

## `S_LOC_TP`

- **Tipo:** System Setup Related
- **Categoria:** Locations
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `LOC_TP_DES` | Loc_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `LOC_TP_STAT` | Loc_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `S_YARD_INB_OUTB_PARA`

- **Tipo:** System Setup Related
- **Categoria:** Locations
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `YARD_INB_OUTB_CODE` | Yarehouse Inb Outb Code | VARCHAR2 | 4 |  | N |
| 2 | `YARD_INB_OUTB_PARA_NUM` | Yarehouse Inb Outb Para Num | NUMBER | 22 | 2 | N |
| 3 | `YARD_INB_OUTB_PARA_OPT_NUM` | Yarehouse Inb Outb Para Opt Num | NUMBER | 22 | 2 | N |
| 4 | `YARD_INB_OUTB_PARA_OPT_DES` | Yarehouse Inb Outb Para Opt Des | VARCHAR2 | 75 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 6 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | Y |

## `T_COMP`

- **Tipo:** Temporary
- **Categoria:** Locations
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_NAME` | Compessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `COMP_STAT` | Compessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `COMP_ADD1` | Compessorial Add1 | VARCHAR2 | 30 |  | N |
| 5 | `COMP_ADD2` | Compessorial Add2 | VARCHAR2 | 30 |  | Y |
| 6 | `COMP_ADD3` | Compessorial Add3 | VARCHAR2 | 30 |  | Y |
| 7 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 8 | `COMP_DATE_FMT` | Comp_Dateessorial Fmt | VARCHAR2 | 9 |  | N |
| 9 | `COMP_DEF_DATE_FLAG` | Comp_Def_Dateessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `COMP_DATE` | Compessorial Date | DATE | 7 |  | N |
| 11 | `GL_MODY_COMP` | Gl_Modyessorial Comp | VARCHAR2 | 4 |  | Y |
| 12 | `COMP_GLOBAL_FLAG` | Comp_Globalessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `COMP_CUST_DES` | Comp_Custessorial Des | VARCHAR2 | 9 |  | N |
| 14 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 15 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 4 |  | Y |

## `T_COMP_SEL`

- **Tipo:** Temporary
- **Categoria:** Locations
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |

## `T_CONV_ALL`

- **Tipo:** Temporary
- **Categoria:** Locations
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CONV_STR` | Convessorial Str | VARCHAR2 | 1000 |  | N |

