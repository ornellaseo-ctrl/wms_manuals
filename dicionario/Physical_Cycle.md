# Tabelas — Physical/Cycle

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **26**.

## `E_CYC_CNT_D1`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CYC_CNT_REC_TP` | Cyc_Cnt_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 9 | `CYC_CNT_VARI_CHOSE` | Cyc_Cnt_Variessorial Chose | VARCHAR2 | 1 |  | N |

## `E_CYC_CNT_D2`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 7 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
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
| 20 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 21 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 22 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |

## `E_CYC_CNT_D3`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_TERMGY_CODE_LEV1` | Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 5 | `INVT_TERMGY_DES_LEV1` | Invt_Termgy_Desessorial Lev1 | VARCHAR2 | 20 |  | N |
| 6 | `INVT_TERMGY_CODE_LEV2` | Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 7 | `INVT_TERMGY_DES_LEV2` | Invt_Termgy_Desessorial Lev2 | VARCHAR2 | 20 |  | Y |
| 8 | `INVT_TERMGY_CODE_LEV3` | Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 9 | `INVT_TERMGY_DES_LEV3` | Invt_Termgy_Desessorial Lev3 | VARCHAR2 | 20 |  | Y |
| 10 | `INVT_TERMGY_CODE_LEV4` | Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 11 | `INVT_TERMGY_DES_LEV4` | Invt_Termgy_Desessorial Lev4 | VARCHAR2 | 20 |  | Y |

## `E_CYC_CNT_D4`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CYC_CNT_DATE_SCHD` | Cyc_Cnt_Dateessorial Schd | DATE | 7 |  | Y |
| 5 | `CYC_CNT_DATE_CREATE` | Cyc_Cnt_Dateessorial Create | DATE | 7 |  | N |
| 6 | `CYC_CNT_DATE_ACT` | Cyc_Cnt_Dateessorial Act | DATE | 7 |  | Y |
| 7 | `CYC_CNT_RAND_SPCF_FLAG` | Cyc_Cnt_Rand_Spcfessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CYC_CNT_INCL_PREV_CNT_VARI` | Cyc_Cnt_Incl_Prev_Cntessorial Vari | VARCHAR2 | 1 |  | N |
| 9 | `CYC_CNT_INCL_VARI_IN_ACT` | Cyc_Cnt_Incl_Vari_Inessorial Act | VARCHAR2 | 1 |  | N |
| 10 | `CYC_CNT_PROJ_CNT_NUM` | Cyc_Cnt_Proj_Cntessorial Num | NUMBER | 22 | 6 | N |
| 11 | `CYC_CNT_ACT_CNT_NUM` | Cyc_Cnt_Act_Cntessorial Num | NUMBER | 22 | 6 | N |
| 12 | `CYC_CNT_PROF_TP` | Cyc_Cnt_Professorial Tp | VARCHAR2 | 1 |  | Y |

## `E_CYC_CNT_D5`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_VALUE` | Itemessorial Value | NUMBER | 22 | 12 | N |
| 6 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |

## `E_CYC_CNT_H`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_UPD_PROTECT` | Cyc_Cnt_Updessorial Protect | NUMBER | 22 | 2 | Y |
| 4 | `CYC_CNT_ARBT_SCHD_FLAG` | Cyc_Cnt_Arbt_Schdessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CYC_CNT_TRANS_DATE` | Cyc_Cnt_Transessorial Date | DATE | 7 |  | Y |
| 6 | `CYC_CNT_CNT_FLAG` | Cyc_Cnt_Cntessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CYC_CNT_START_TICK_NUM` | Cyc_Cnt_Start_Tickessorial Num | NUMBER | 22 | 6 | N |
| 8 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CYC_CNT_STAT` | Cyc_Cntessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 12 | `CYC_CNT_INCL_EMPTY_LOC_FLAG` | Cyc_Cnt_Incl_Empty_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CYC_CNT_ALLOW_DUP_PER_LOC_FLAG` | Cyc_Cnt_Allow_Dup_Per_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CYC_CNT_SHOW_INVT_LEV1_FLAG` | Cyc_Cnt_Show_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `CYC_CNT_SHOW_INVT_LEV2_FLAG` | Cyc_Cnt_Show_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CYC_CNT_SHOW_INVT_LEV3_FLAG` | Cyc_Cnt_Show_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `CYC_CNT_SHOW_INVT_LEV4_FLAG` | Cyc_Cnt_Show_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | N |

## `E_CYC_CNT_ITEM_LOC`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_REC_TP` | Cyc_Cnt_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 7 | `NUM_OF_CNT` | Num_Ofessorial Cnt | NUMBER | 22 | 3 | N |

## `E_CYC_CNT_NXT`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_REC_TP` | Cyc_Cnt_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | Y |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |

## `E_CYC_CNT_TICK`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_TICK_NUM` | Cyc_Cnt_Tickessorial Num | NUMBER | 22 | 6 | N |
| 4 | `CYC_CNT_CNT_FLAG` | Cyc_Cnt_Cntessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CYC_CNT_PRT_FLAG` | Cyc_Cnt_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CYC_CNT_TICK_TP_FLAG` | Cyc_Cnt_Tick_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CYC_CNT_ENT_FLAG` | Cyc_Cnt_Entessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CYC_CNT_ENT_QTY` | Cyc_Cnt_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 9 | `CYC_CNT_QTY` | Cyc_Cntessorial Qty | NUMBER | 22 | 6 | Y |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 13 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 14 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 17 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 18 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 19 | `CYC_CNT_BAL_FLAG` | Cyc_Cnt_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `CYC_CNT_FORCED_BAL_FLAG` | Cyc_Cnt_Forced_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `CYC_CNT_ON_HAND_QTY` | Cyc_Cnt_On_Handessorial Qty | NUMBER | 22 | 9 | Y |
| 22 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 24 | `CYC_CNT_REPRT_CNT` | Cyc_Cnt_Reprtessorial Cnt | NUMBER | 22 | 2 | Y |
| 25 | `SUPERVISOR_CNT_FLAG` | Supervisor_Cntessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `SUPERVISOR_OP_CODE` | Supervisor_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 27 | `SUPERVISOR_CNT_DATE` | Supervisor_Cntessorial Date | DATE | 7 |  | Y |
| 28 | `CYC_CNT_TICK_CREATE_DATE` | Cyc_Cnt_Tick_Createessorial Date | DATE | 7 |  | Y |
| 29 | `CYC_CNT_TICK_ENT_DATE` | Cyc_Cnt_Tick_Entessorial Date | DATE | 7 |  | Y |
| 30 | `CYC_CNT_UPD_STAT` | Cyc_Cnt_Updessorial Stat | VARCHAR2 | 1 |  | Y |
| 31 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 32 | `CYC_CNT_TICK_PRTY_NUM` | Cyc_Cnt_Tick_Prtyessorial Num | NUMBER | 22 | 1 | Y |

## `E_PHYS_COLLR`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 10
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PHYS_TICK_NUM` | Phys_Tickessorial Num | NUMBER | 22 | 6 | Y |
| 2 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 3 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 4 | `PHYS_QTY` | Physessorial Qty | NUMBER | 22 | 5 | Y |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 6 | `PHYS_COLLR_FLAG` | Phys_Collressorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `PHYS_COLLR_OP_INIT` | Phys_Collr_Opessorial Init | VARCHAR2 | 3 |  | Y |
| 8 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | Y |
| 9 | `PHYS_COLLR_UPD_FLAG` | Phys_Collr_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `E_PHYS_D`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_TERMGY_CODE_LEV1` | Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 5 | `INVT_TERMGY_DES_LEV1` | Invt_Termgy_Desessorial Lev1 | VARCHAR2 | 20 |  | N |
| 6 | `INVT_TERMGY_CODE_LEV2` | Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 7 | `INVT_TERMGY_DES_LEV2` | Invt_Termgy_Desessorial Lev2 | VARCHAR2 | 20 |  | Y |
| 8 | `INVT_TERMGY_CODE_LEV3` | Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 9 | `INVT_TERMGY_DES_LEV3` | Invt_Termgy_Desessorial Lev3 | VARCHAR2 | 20 |  | Y |
| 10 | `INVT_TERMGY_CODE_LEV4` | Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 11 | `INVT_TERMGY_DES_LEV4` | Invt_Termgy_Desessorial Lev4 | VARCHAR2 | 20 |  | Y |
| 12 | `INVT_TERMGY_CODE_LEV5` | Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 13 | `INVT_TERMGY_DES_LEV5` | Invt_Termgy_Desessorial Lev5 | VARCHAR2 | 20 |  | Y |

## `E_PHYS_H`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 5 | `PHYS_TP_FLAG` | Phys_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `PHYS_DATE` | Physessorial Date | DATE | 7 |  | N |
| 7 | `PHYS_STAT` | Physessorial Stat | VARCHAR2 | 1 |  | N |
| 8 | `PHYS_ALLOW_DUP_LOC_FLAG` | Phys_Allow_Dup_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `SHOW_INVT_QTY_FLAG` | Show_Invt_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `PHYS_CRNT_TICK_NUM` | Phys_Crnt_Tickessorial Num | NUMBER | 22 | 6 | N |
| 11 | `INVT_TERMGY_CODE_LEV1` | Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 12 | `INVT_TERMGY_DES_LEV1` | Invt_Termgy_Desessorial Lev1 | VARCHAR2 | 20 |  | N |
| 13 | `SHOW_INVT_LEV1_FLAG` | Show_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `INVT_TERMGY_CODE_LEV2` | Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 15 | `INVT_TERMGY_DES_LEV2` | Invt_Termgy_Desessorial Lev2 | VARCHAR2 | 20 |  | Y |
| 16 | `SHOW_INVT_LEV2_FLAG` | Show_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `INVT_TERMGY_CODE_LEV3` | Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 18 | `INVT_TERMGY_DES_LEV3` | Invt_Termgy_Desessorial Lev3 | VARCHAR2 | 20 |  | Y |
| 19 | `SHOW_INVT_LEV3_FLAG` | Show_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `INVT_TERMGY_CODE_LEV4` | Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 21 | `INVT_TERMGY_DES_LEV4` | Invt_Termgy_Desessorial Lev4 | VARCHAR2 | 20 |  | Y |
| 22 | `SHOW_INVT_LEV4_FLAG` | Show_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `INVT_TERMGY_CODE_LEV5` | Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 24 | `INVT_TERMGY_DES_LEV5` | Invt_Termgy_Desessorial Lev5 | VARCHAR2 | 20 |  | Y |
| 25 | `SHOW_INVT_LEV5_FLAG` | Show_Invt_Lev5essorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `PHYS_INVT_LEV1_ENT_MASK` | Phys_Invt_Lev1_Entessorial Mask | VARCHAR2 | 10 |  | Y |
| 27 | `PHYS_EMPTY_LOC_FLAG` | Phys_Empty_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 29 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 30 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 31 | `ADJ_CODE` | Adjessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 33 | `CLR_NON_TICKET_INVT_FLAG` | Clr_Non_Ticket_Invtessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `IGNORE_N_FLAG_TICKET` | Ignore_N_Flagessorial Ticket | VARCHAR2 | 1 |  | Y |

## `E_PHYS_INVT`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `PHYS_TICK_NUM` | Phys_Tickessorial Num | NUMBER | 22 | 6 | N |
| 4 | `PHYS_COUNT_FLAG` | Phys_Countessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `PHYS_PRT_FLAG` | Phys_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `PHYS_TICK_TP_FLAG` | Phys_Tick_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `PHYS_ENT_FLAG` | Phys_Entessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 12 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 13 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 14 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 15 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 17 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 18 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 19 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 20 | `PHYS_ENT_QTY` | Phys_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 21 | `PHYS_QTY` | Physessorial Qty | NUMBER | 22 | 9 | Y |
| 22 | `PHYS_SEL_QTY` | Phys_Selessorial Qty | NUMBER | 22 | 9 | Y |
| 23 | `PHYS_REPRT_CNT` | Phys_Reprtessorial Cnt | NUMBER | 22 | 2 | Y |
| 24 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_PHYS_INVT_D5D2`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `PHYS_TICK_NUM` | Phys_Tickessorial Num | NUMBER | 22 | 4 | N |
| 4 | `PHYS_COUNT_FLAG` | Phys_Countessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 7 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 10 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 12 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |

## `E_PHYS_INVT_NEW`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 5 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 6 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV2_DES` | Invt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV3_DES` | Invt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV4_DES` | Invt_Lev4essorial Des | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV5_DES` | Invt_Lev5essorial Des | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |

## `E_PROS_CYC_CNT`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROS_FLAG` | Cyc_Cnt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `E_PROS_CYC_CNT_TICK`

- **Tipo:** Transactional
- **Categoria:** Physical/Cycle
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_TICK_NUM` | Cyc_Cnt_Tickessorial Num | NUMBER | 22 | 6 | N |
| 4 | `CYC_CNT_CNT_FLAG` | Cyc_Cnt_Cntessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `CYC_CNT_PROS_DATE` | Cyc_Cnt_Prosessorial Date | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `H_CYC_CNT_D1`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CYC_CNT_REC_TP` | Cyc_Cnt_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 9 | `CYC_CNT_VARI_CHOSE` | Cyc_Cnt_Variessorial Chose | VARCHAR2 | 1 |  | N |

## `H_CYC_CNT_D2`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 7 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
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
| 20 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |

## `H_CYC_CNT_D3`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_TERMGY_CODE_LEV1` | Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 5 | `INVT_TERMGY_DES_LEV1` | Invt_Termgy_Desessorial Lev1 | VARCHAR2 | 20 |  | N |
| 6 | `INVT_TERMGY_CODE_LEV2` | Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 7 | `INVT_TERMGY_DES_LEV2` | Invt_Termgy_Desessorial Lev2 | VARCHAR2 | 20 |  | Y |
| 8 | `INVT_TERMGY_CODE_LEV3` | Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 9 | `INVT_TERMGY_DES_LEV3` | Invt_Termgy_Desessorial Lev3 | VARCHAR2 | 20 |  | Y |
| 10 | `INVT_TERMGY_CODE_LEV4` | Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 11 | `INVT_TERMGY_DES_LEV4` | Invt_Termgy_Desessorial Lev4 | VARCHAR2 | 20 |  | Y |

## `H_CYC_CNT_D4`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CYC_CNT_DATE_SCHD` | Cyc_Cnt_Dateessorial Schd | DATE | 7 |  | Y |
| 5 | `CYC_CNT_DATE_CREATE` | Cyc_Cnt_Dateessorial Create | DATE | 7 |  | N |
| 6 | `CYC_CNT_DATE_ACT` | Cyc_Cnt_Dateessorial Act | DATE | 7 |  | Y |
| 7 | `CYC_CNT_RAND_SPCF_FLAG` | Cyc_Cnt_Rand_Spcfessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CYC_CNT_INCL_PREV_CNT_VARI` | Cyc_Cnt_Incl_Prev_Cntessorial Vari | VARCHAR2 | 1 |  | N |
| 9 | `CYC_CNT_INCL_VARI_IN_ACT` | Cyc_Cnt_Incl_Vari_Inessorial Act | VARCHAR2 | 1 |  | N |
| 10 | `CYC_CNT_PROJ_CNT_NUM` | Cyc_Cnt_Proj_Cntessorial Num | NUMBER | 22 | 6 | N |
| 11 | `CYC_CNT_ACT_CNT_NUM` | Cyc_Cnt_Act_Cntessorial Num | NUMBER | 22 | 6 | N |
| 12 | `CYC_CNT_PROF_TP` | Cyc_Cnt_Professorial Tp | VARCHAR2 | 1 |  | Y |

## `H_CYC_CNT_D5`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ITEM_VALUE` | Itemessorial Value | NUMBER | 22 | 12 | N |
| 6 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |

## `H_CYC_CNT_EVENT`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 14 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 15 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 16 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 17 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | Y |

## `H_CYC_CNT_H`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_UPD_PROTECT` | Cyc_Cnt_Updessorial Protect | NUMBER | 22 | 2 | Y |
| 4 | `CYC_CNT_ARBT_SCHD_FLAG` | Cyc_Cnt_Arbt_Schdessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CYC_CNT_TRANS_DATE` | Cyc_Cnt_Transessorial Date | DATE | 7 |  | Y |
| 6 | `CYC_CNT_CNT_FLAG` | Cyc_Cnt_Cntessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CYC_CNT_START_TICK_NUM` | Cyc_Cnt_Start_Tickessorial Num | NUMBER | 22 | 6 | N |
| 8 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CYC_CNT_STAT` | Cyc_Cntessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 12 | `CYC_CNT_INCL_EMPTY_LOC_FLAG` | Cyc_Cnt_Incl_Empty_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CYC_CNT_ALLOW_DUP_PER_LOC_FLAG` | Cyc_Cnt_Allow_Dup_Per_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CYC_CNT_SHOW_INVT_LEV1_FLAG` | Cyc_Cnt_Show_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `CYC_CNT_SHOW_INVT_LEV2_FLAG` | Cyc_Cnt_Show_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CYC_CNT_SHOW_INVT_LEV3_FLAG` | Cyc_Cnt_Show_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `CYC_CNT_SHOW_INVT_LEV4_FLAG` | Cyc_Cnt_Show_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | N |

## `H_CYC_CNT_TICK`

- **Tipo:** Historical
- **Categoria:** Physical/Cycle
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_TICK_NUM` | Cyc_Cnt_Tickessorial Num | NUMBER | 22 | 6 | N |
| 4 | `CYC_CNT_CNT_FLAG` | Cyc_Cnt_Cntessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CYC_CNT_PRT_FLAG` | Cyc_Cnt_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CYC_CNT_TICK_TP_FLAG` | Cyc_Cnt_Tick_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CYC_CNT_ENT_FLAG` | Cyc_Cnt_Entessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CYC_CNT_ENT_QTY` | Cyc_Cnt_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 9 | `CYC_CNT_QTY` | Cyc_Cntessorial Qty | NUMBER | 22 | 6 | Y |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 13 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 14 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 17 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 18 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 19 | `CYC_CNT_BAL_FLAG` | Cyc_Cnt_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `CYC_CNT_FORCED_BAL_FLAG` | Cyc_Cnt_Forced_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `CYC_CNT_ON_HAND_QTY` | Cyc_Cnt_On_Handessorial Qty | NUMBER | 22 | 9 | Y |
| 22 | `CYC_CNT_REPRT_CNT` | Cyc_Cnt_Reprtessorial Cnt | NUMBER | 22 | 2 | Y |
| 23 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 25 | `SUPERVISOR_CNT_FLAG` | Supervisor_Cntessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `SUPERVISOR_OP_CODE` | Supervisor_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 27 | `SUPERVISOR_CNT_DATE` | Supervisor_Cntessorial Date | DATE | 7 |  | Y |
| 28 | `CYC_CNT_TICK_CREATE_DATE` | Cyc_Cnt_Tick_Createessorial Date | DATE | 7 |  | Y |
| 29 | `CYC_CNT_TICK_ENT_DATE` | Cyc_Cnt_Tick_Entessorial Date | DATE | 7 |  | Y |
| 30 | `CYC_CNT_UPD_STAT` | Cyc_Cnt_Updessorial Stat | VARCHAR2 | 1 |  | Y |
| 31 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 32 | `CYC_CNT_TICK_PRTY_NUM` | Cyc_Cnt_Tick_Prtyessorial Num | NUMBER | 22 | 1 | Y |

## `T_PHYS_SORT`

- **Tipo:** Temporary
- **Categoria:** Physical/Cycle
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, HOLD_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PHYS_NUM` | Physessorial Num | NUMBER | 22 | 6 | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 6 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 13 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | Y |

