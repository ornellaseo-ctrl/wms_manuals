# Tabelas — Freight

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **73**.

## `C_FRT_CHANGE`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |

## `C_FRT_CHANGE_EXT_CARR`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |

## `C_FRT_EXTRA_CHG`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 4 | `TOT_UNIT_WGT_CUBE` | Tot_Unit_Wgtessorial Cube | NUMBER | 22 | 16 | Y |

## `C_FRT_ORD`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `E_FRT_DELV_GRP`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 4 | `DELV_GRP_DES` | Delv_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DELV_GRP_DEST_CODE_ORIGIN` | Delv_Grp_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 6 | `DELV_GRP_DEST_CODE` | Delv_Grp_Destessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `DELV_GRP_DELV_FLAG` | Delv_Grp_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `DELV_GRP_ENTRY_DATE` | Delv_Grp_Entryessorial Date | DATE | 7 |  | Y |
| 9 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |

## `E_FRT_LOAD_D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_UNIT` | Loadessorial Unit | NUMBER | 22 | 9 | Y |
| 6 | `LOAD_WGT` | Loadessorial Wgt | NUMBER | 22 | 11 | Y |
| 7 | `LOAD_CUBE` | Loadessorial Cube | NUMBER | 22 | 12 | Y |
| 8 | `LOAD_COST_ASWGT` | Load_Costessorial Aswgt | NUMBER | 22 | 11 | Y |
| 9 | `SKU_CODE_COST` | Sku_Codeessorial Cost | VARCHAR2 | 4 |  | Y |
| 10 | `LOAD_COST_RATE` | Load_Costessorial Rate | NUMBER | 22 | 9 | Y |
| 11 | `LOAD_COST_AMT` | Load_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `LOAD_COST_DISC_PCENT` | Load_Cost_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 13 | `LOAD_COST_FLAG` | Load_Costessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `LOAD_BILL_ASWGT` | Load_Billessorial Aswgt | NUMBER | 22 | 11 | Y |
| 15 | `SKU_CODE_BILL` | Sku_Codeessorial Bill | VARCHAR2 | 4 |  | Y |
| 16 | `LOAD_BILL_RATE` | Load_Billessorial Rate | NUMBER | 22 | 9 | Y |
| 17 | `LOAD_BILL_AMT` | Load_Billessorial Amt | NUMBER | 22 | 9 | Y |
| 18 | `LOAD_BILL_DISC_PCENT` | Load_Bill_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 19 | `LOAD_BILL_FLAG` | Load_Billessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 8 | `LOAD_CHG_DES` | Load_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `LOAD_CHG_QTY` | Load_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `LOAD_CHG_RATE` | Load_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 11 | `LOAD_CHG_COST_AMT` | Load_Chg_Costessorial Amt | NUMBER | 22 | 9 | Y |

## `E_FRT_LOAD_D4`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 8 | `LOAD_CHG_DES` | Load_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `LOAD_CHG_QTY` | Load_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `LOAD_CHG_RATE` | Load_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 11 | `LOAD_CHG_BILL_AMT` | Load_Chg_Billessorial Amt | NUMBER | 22 | 9 | Y |

## `E_FRT_LOAD_D5`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `LOAD_INTRA_FLAG` | Load_Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `LOAD_COST_AMT` | Load_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 7 | `LOAD_ADDI_COST_AMT` | Load_Addi_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 8 | `LOAD_DISC_PCENT` | Load_Discessorial Pcent | NUMBER | 22 | 9 | Y |
| 9 | `LOAD_DISTA` | Loadessorial Dista | NUMBER | 22 | 9 | Y |
| 10 | `LOAD_LINEAR_RATE` | Load_Linearessorial Rate | NUMBER | 22 | 9 | Y |
| 11 | `LOAD_FLAT_AMT` | Load_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `LOAD_STOP_RATE` | Load_Stopessorial Rate | NUMBER | 22 | 9 | Y |
| 13 | `LOAD_SKU_RATE` | Load_Skuessorial Rate | NUMBER | 22 | 9 | Y |
| 14 | `LOAD_RATE_LEV` | Load_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 15 | `LOAD_RATE_BY_FLAG` | Load_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `LOAD_CARR_INV_NUM` | Load_Carr_Invessorial Num | VARCHAR2 | 10 |  | Y |
| 17 | `LOAD_CARR_INV_DATE` | Load_Carr_Invessorial Date | DATE | 7 |  | Y |
| 18 | `LOAD_ASWGT` | Loadessorial Aswgt | NUMBER | 22 | 11 | Y |
| 19 | `LOAD_AMT` | Loadessorial Amt | NUMBER | 22 | 9 | Y |
| 20 | `LOAD_ADDI_AMT` | Load_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 21 | `LOAD_BILL_TABLE` | Load_Billessorial Table | VARCHAR2 | 10 |  | Y |
| 22 | `LOAD_BILL_INTRA_FLAG` | Load_Bill_Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `LOAD_BILL_DISC_PCENT` | Load_Bill_Discessorial Pcent | NUMBER | 22 | 9 | Y |
| 24 | `LOAD_RATE_BILL_LEV` | Load_Rate_Billessorial Lev | VARCHAR2 | 5 |  | Y |
| 25 | `LOAD_BILL_RATE_BY_FLAG` | Load_Bill_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |

## `E_FRT_LOAD_D6D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | N |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 7 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 8 | `LOAD_GRP_UNIT` | Load_Grpessorial Unit | NUMBER | 22 | 9 | Y |
| 9 | `LOAD_GRP_WGT` | Load_Grpessorial Wgt | NUMBER | 22 | 11 | Y |
| 10 | `LOAD_GRP_CUBE` | Load_Grpessorial Cube | NUMBER | 22 | 12 | Y |
| 11 | `LOAD_GRP_ASWGT` | Load_Grpessorial Aswgt | NUMBER | 22 | 11 | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOAD_GRP_RATE` | Load_Grpessorial Rate | NUMBER | 22 | 9 | Y |
| 14 | `LOAD_GRP_COST_AMT` | Load_Grp_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `LOAD_GRP_DISC_PCENT` | Load_Grp_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 16 | `LOAD_GRP_FLAG` | Load_Grpessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_D6D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | N |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 7 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 10 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 11 | `LOAD_GRP_CHG_DES` | Load_Grp_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 12 | `LOAD_GRP_CHG_QTY` | Load_Grp_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `LOAD_GRP_CHG_RATE` | Load_Grp_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 14 | `LOAD_GRP_CHG_AMT` | Load_Grp_Chgessorial Amt | NUMBER | 22 | 9 | N |

## `E_FRT_LOAD_D6H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | N |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 7 | `LOAD_GRP_DEST_CODE_ORIGIN` | Load_Grp_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 8 | `LOAD_GRP_DEST_CODE` | Load_Grp_Destessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `GRP_ASSIGN_FLAG` | Grp_Assignessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `LOAD_GRP_TOT_COST_AMT` | Load_Grp_Tot_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `LOAD_GRP_TOT_ADDI_AMT` | Load_Grp_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 13 | `LOAD_GRP_INTRA_FLAG` | Load_Grp_Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `LOAD_GRP_DISC_PCENT` | Load_Grp_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 15 | `LOAD_GRP_ASWGT` | Load_Grpessorial Aswgt | NUMBER | 22 | 11 | Y |
| 16 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 17 | `LOAD_GRP_TO_SHIP_DATE_SCH` | Load_Grp_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 18 | `LOAD_GRP_TO_SHIP_DATE_ACT` | Load_Grp_To_Ship_Dateessorial Act | DATE | 7 |  | Y |
| 19 | `LOAD_GRP_TO_ARR_DATE_SCH` | Load_Grp_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 20 | `LOAD_GRP_TO_ARR_DATE_ACT` | Load_Grp_To_Arr_Dateessorial Act | DATE | 7 |  | Y |
| 21 | `LOAD_GRP_RATE_LEV` | Load_Grp_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 22 | `LOAD_GRP_RATE_BY_FLAG` | Load_Grp_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 24 | `LOAD_GRP_FLOW_STAT` | Load_Grp_Flowessorial Stat | VARCHAR2 | 10 |  | Y |
| 25 | `LOAD_GRP_CARR_INV_NUM` | Load_Grp_Carr_Invessorial Num | VARCHAR2 | 10 |  | Y |
| 26 | `LOAD_GRP_CARR_INV_DATE` | Load_Grp_Carr_Invessorial Date | DATE | 7 |  | Y |
| 27 | `LOAD_GRP_SEG_NUM` | Load_Grp_Segessorial Num | NUMBER | 22 | 4 | Y |
| 28 | `FINAL_LEG_FLAG` | Final_Legessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_D7D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 8 | `LOAD_ORD_UNIT` | Load_Ordessorial Unit | NUMBER | 22 | 9 | Y |
| 9 | `LOAD_ORD_WGT` | Load_Ordessorial Wgt | NUMBER | 22 | 11 | Y |
| 10 | `LOAD_ORD_CUBE` | Load_Ordessorial Cube | NUMBER | 22 | 12 | Y |
| 11 | `LOAD_ORD_ASWGT` | Load_Ordessorial Aswgt | NUMBER | 22 | 11 | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOAD_ORD_RATE` | Load_Ordessorial Rate | NUMBER | 22 | 9 | Y |
| 14 | `LOAD_ORD_COST_AMT` | Load_Ord_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `LOAD_ORD_DISC_PCENT` | Load_Ord_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 16 | `LOAD_ORD_AMT_FLAG` | Load_Ord_Amtessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_D7D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 9 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 10 | `LOAD_ORD_CHG_DES` | Load_Ord_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 11 | `LOAD_ORD_CHG_QTY` | Load_Ord_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `LOAD_ORD_CHG_RATE` | Load_Ord_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 13 | `LOAD_ORD_CHG_AMT` | Load_Ord_Chgessorial Amt | NUMBER | 22 | 9 | N |

## `E_FRT_LOAD_D7H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `LOAD_ORD_DEST_CODE_ORIGIN` | Load_Ord_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 7 | `LOAD_ORD_DEST_CODE` | Load_Ord_Destessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `LOAD_ORD_RATE_LEV` | Load_Ord_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 9 | `LOAD_ORD_RATE_BY_FLAG` | Load_Ord_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `ORD_ASSIGN_FLAG` | Ord_Assignessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `LOAD_ORD_COST_AMT` | Load_Ord_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `LOAD_ORD_ADDI_COST_AMT` | Load_Ord_Addi_Costessorial Amt | NUMBER | 22 | 9 | Y |
| 13 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 14 | `LOAD_ORD_INTRA_FLAG` | Load_Ord_Intraessorial Flag | VARCHAR2 | 5 |  | Y |
| 15 | `LOAD_ORD_DISC_PCENT` | Load_Ord_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 16 | `LOAD_ORD_ASWGT` | Load_Ordessorial Aswgt | NUMBER | 22 | 11 | Y |
| 17 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 18 | `LOAD_ORD_TO_SHIP_DATE_SCH` | Load_Ord_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 19 | `LOAD_ORD_TO_SHIP_DATE_ACT` | Load_Ord_To_Ship_Dateessorial Act | DATE | 7 |  | Y |
| 20 | `LOAD_ORD_TO_ARR_DATE_SCH` | Load_Ord_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 21 | `LOAD_ORD_TO_ARR_DATE_ACT` | Load_Ord_To_Arr_Dateessorial Act | DATE | 7 |  | Y |
| 22 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 23 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `LOAD_ORD_FLOW_STAT` | Load_Ord_Flowessorial Stat | VARCHAR2 | 10 |  | Y |
| 25 | `LOAD_ORD_UNIT_SHORT` | Load_Ord_Unitessorial Short | NUMBER | 22 | 9 | Y |
| 26 | `LOAD_ORD_UNIT_OVER` | Load_Ord_Unitessorial Over | NUMBER | 22 | 9 | Y |
| 27 | `LOAD_ORD_UNIT_DAMAGE` | Load_Ord_Unitessorial Damage | NUMBER | 22 | 9 | Y |
| 28 | `LOAD_ORD_CARR_INV_NUM` | Load_Ord_Carr_Invessorial Num | VARCHAR2 | 10 |  | Y |
| 29 | `LOAD_ORD_CARR_INV_DATE` | Load_Ord_Carr_Invessorial Date | DATE | 7 |  | Y |
| 30 | `LOAD_ORD_SEG_NUM` | Load_Ord_Segessorial Num | NUMBER | 22 | 4 | Y |
| 31 | `FINAL_LEG_FLAG` | Final_Legessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_D8`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 7 | `STOP_NAME` | Stop Name | VARCHAR2 | 30 |  | Y |
| 8 | `STOP_ADD1` | Stopessorial Add1 | VARCHAR2 | 30 |  | Y |
| 9 | `STOP_ADD2` | Stopessorial Add2 | VARCHAR2 | 30 |  | Y |
| 10 | `STOP_ZIP_CODE` | Stop_Zipessorial Code | VARCHAR2 | 10 |  | Y |
| 11 | `STOP_REMARK` | Stopessorial Remark | VARCHAR2 | 50 |  | Y |
| 12 | `STOP_TO_SHIP_DATE` | Stop_To_Shipessorial Date | DATE | 7 |  | Y |
| 13 | `STOP_TO_ARR_DATE` | Stop_To_Arressorial Date | DATE | 7 |  | Y |

## `E_FRT_LOAD_D9`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | N |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 7 | `LOAD_REM_LINE_NUM` | Load_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 8 | `LOAD_REM_LINE_TEXT` | Load_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_FRT_LOAD_H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `LOAD_REF_NUM` | Load_Refessorial Num | NUMBER | 22 | 6 | N |
| 5 | `LOAD_TYPE` | Loadessorial Type | VARCHAR2 | 1 |  | N |
| 6 | `LOAD_FLOW_STAT` | Load_Flowessorial Stat | VARCHAR2 | 4 |  | N |
| 7 | `FRT_DEST_CODE_ORIGIN` | Frt_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 8 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 10 | `LOAD_DES` | Loadessorial Des | VARCHAR2 | 30 |  | Y |
| 11 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 13 | `LOAD_DATE` | Loadessorial Date | DATE | 7 |  | Y |
| 14 | `LOAD_FRONT_TEMP` | Load_Frontessorial Temp | VARCHAR2 | 5 |  | Y |
| 15 | `LOAD_MID_TEMP` | Load_Midessorial Temp | VARCHAR2 | 5 |  | Y |
| 16 | `LOAD_BACK_TEMP` | Load_Backessorial Temp | VARCHAR2 | 5 |  | Y |
| 17 | `TRACTOR_NUM` | Tractoressorial Num | VARCHAR2 | 10 |  | Y |
| 18 | `UNIT_NUM` | Unitessorial Num | VARCHAR2 | 10 |  | Y |
| 19 | `LOAD_DRIVER_NAME` | Load_Driveressorial Name | VARCHAR2 | 30 |  | Y |
| 20 | `LOAD_TO_SHIP_DATE_ORG` | Load_To_Ship_Dateessorial Org | DATE | 7 |  | Y |
| 21 | `LOAD_TO_SHIP_DATE_SCH` | Load_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 22 | `LOAD_TO_SHIP_DATE_ACT` | Load_To_Ship_Dateessorial Act | DATE | 7 |  | Y |
| 23 | `LOAD_TO_CONF_DATE` | Load_To_Confessorial Date | DATE | 7 |  | Y |
| 24 | `LOAD_TO_ARR_DATE_SCH` | Load_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 25 | `LOAD_TO_ARR_DATE_ACT` | Load_To_Arr_Dateessorial Act | DATE | 7 |  | Y |
| 26 | `EQP_TP_CODE` | Eqp_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 28 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |

## `E_FRT_LOAD_MAN`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 7 | `FRT_LOAD_SHIP_DATE` | Frt_Load_Shipessorial Date | DATE | 7 |  | N |
| 8 | `LOAD_NUM_EXT_REF` | Load_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 9 | `LOAD_NUM_EXT_REF_CODE` | Load_Num_Ext_Refessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 11 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 12 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `LOAD_STAT` | Loadessorial Stat | VARCHAR2 | 1 |  | Y |
| 14 | `FRT_LOAD_SUSP_FLAG` | Frt_Load_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `LOAD_APPO_DATE` | Load_Appoessorial Date | DATE | 7 |  | Y |
| 16 | `FRT_LOAD_CARR_PRO_NUM` | Frt_Load_Carr_Proessorial Num | VARCHAR2 | 20 |  | Y |
| 17 | `FRT_LOAD_POOL_FLAG` | Frt_Load_Poolessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CARR_CODE_POOL` | Carr_Codeessorial Pool | VARCHAR2 | 10 |  | Y |
| 19 | `CON_CODE_POOL` | Con_Codeessorial Pool | VARCHAR2 | 10 |  | Y |
| 20 | `ALLOW_OVRR_IPRO_FLAG` | Allow_Ovrr_Iproessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `LOAD_A1INSPECTION_STAT_MES` | Load_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 22 | `LOAD_A1INSPECTION_DATE` | Load_A1Inspectionessorial Date | DATE | 7 |  | Y |
| 23 | `LOAD_A1INSPECTION_MES` | Load_A1Inspectionessorial Mes | VARCHAR2 | 100 |  | Y |
| 24 | `LOAD_NUM_TRANS_REF` | Load_Num_Transessorial Ref | VARCHAR2 | 20 |  | Y |
| 25 | `FRT_LOAD_START_CHECK_LIST_CODE` | Frt_Load_Start_Check_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `FRT_LOAD_END_CHECK_LIST_CODE` | Frt_Load_End_Check_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `FRT_LOAD_LOAD_TP_NUM_OVRR` | Frt_Load_Load_Tp_Numessorial Ovrr | NUMBER | 22 | 1 | Y |
| 28 | `FRT_LOAD_MAX_NUM_PAL_POS` | Frt_Load_Max_Num_Palessorial Pos | NUMBER | 22 | 2 | Y |
| 29 | `FRT_LOAD_MAX_WGT` | Frt_Load_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 30 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 31 | `FRT_LOAD_MAX_CUBE` | Frt_Load_Maxessorial Cube | NUMBER | 22 | 16 | Y |
| 32 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |

## `E_FRT_LOAD_MAN_CARR`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOAD_POW_UNIT_NUM` | Load_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `LOAD_CARRY_UNIT_NUM` | Load_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `LOAD_VES` | Loadessorial Ves | VARCHAR2 | 20 |  | Y |
| 9 | `LOAD_VOY` | Loadessorial Voy | VARCHAR2 | 20 |  | Y |
| 10 | `LOAD_SEAL1` | Loadessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 11 | `LOAD_SEAL2` | Loadessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 12 | `LOAD_TEMP_FRONT` | Load_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 13 | `LOAD_TEMP_MID` | Load_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 14 | `LOAD_TEMP_BACK` | Load_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 15 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 16 | `LOAD_TEMP_SET` | Load_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 17 | `LOAD_TEMP_AMB` | Load_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 18 | `LOAD_SEAL1_INTACT` | Load_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |

## `E_FRT_LOAD_MAN_CON_REST`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 7 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_FRT_LOAD_PALL_D`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `PALL_ID` | Pallessorial Id | VARCHAR2 | 40 |  | N |
| 6 | `PALL_POS` | Pallessorial Pos | VARCHAR2 | 5 |  | N |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 8 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |

## `E_FRT_LOAD_PALL_H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `PALL_ID` | Pallessorial Id | VARCHAR2 | 40 |  | N |
| 6 | `PALL_POS` | Pallessorial Pos | VARCHAR2 | 5 |  | N |
| 7 | `PALL_TP` | Pallessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 3 | N |

## `E_FRT_ORD_D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 6 | `FRT_CLASS_DES` | Frt_Classessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `ORD_UNIT` | Ordessorial Unit | NUMBER | 22 | 9 | N |
| 8 | `ORD_WGT` | Ordessorial Wgt | NUMBER | 22 | 11 | N |
| 9 | `ORD_CUBE` | Ordessorial Cube | NUMBER | 22 | 12 | Y |
| 10 | `ORD_TL_ASWGT` | Ord_Tlessorial Aswgt | NUMBER | 22 | 11 | Y |
| 11 | `ORD_TL_RATE` | Ord_Tlessorial Rate | NUMBER | 22 | 9 | Y |
| 12 | `SKU_CODE_TL` | Sku_Codeessorial Tl | VARCHAR2 | 4 |  | Y |
| 13 | `ORD_TL_AMT` | Ord_Tlessorial Amt | NUMBER | 22 | 9 | Y |
| 14 | `ORD_TL_DISC_PCENT` | Ord_Tl_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 15 | `ORD_TL_FLAG` | Ord_Tlessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `ORD_LTL_ASWGT` | Ord_Ltlessorial Aswgt | NUMBER | 22 | 11 | Y |
| 17 | `ORD_LTL_RATE` | Ord_Ltlessorial Rate | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CODE_LTL` | Sku_Codeessorial Ltl | VARCHAR2 | 4 |  | Y |
| 19 | `ORD_LTL_AMT` | Ord_Ltlessorial Amt | NUMBER | 22 | 9 | Y |
| 20 | `ORD_LTL_DISC_PCENT` | Ord_Ltl_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 21 | `ORD_LTL_FLAG` | Ord_Ltlessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `ORD_PALL` | Ordessorial Pall | NUMBER | 22 | 11 | Y |

## `E_FRT_ORD_D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `ORD_CHG_DES` | Ord_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `ORD_CHG_QTY` | Ord_Chgessorial Qty | NUMBER | 22 | 9 | Y |
| 8 | `ORD_CHG_RATE` | Ord_Chgessorial Rate | NUMBER | 22 | 9 | Y |
| 9 | `ORD_CHG_AMT` | Ord_Chgessorial Amt | NUMBER | 22 | 9 | Y |
| 10 | `ORD_CHG_INV_FLAG` | Ord_Chg_Invessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_ORD_D3`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_REM_LINE_NUM` | Ord_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 5 | `ORD_REM_LINE_TEXT` | Ord_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_FRT_ORD_D4`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `LOAD_TYPE` | Loadessorial Type | VARCHAR2 | 1 |  | N |
| 7 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 9 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 10 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 11 | `LOAD_NUM_EXT_REF` | Load_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 12 | `ORD_PROS_STAT` | Ord_Prosessorial Stat | VARCHAR2 | 1 |  | Y |
| 13 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 14 | `LOAD_NUM_TRANS_REF` | Load_Num_Transessorial Ref | VARCHAR2 | 20 |  | Y |

## `E_FRT_ORD_D5`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FRT_TER_CODE_DELV` | Frt_Ter_Codeessorial Delv | VARCHAR2 | 4 |  | N |
| 5 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |

## `E_FRT_ORD_D7`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 30
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_INTRA_FLAG` | Ord_Intraessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `ORD_RATE_LEV` | Ord_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 6 | `ORD_RATE_BY` | Ord_Rateessorial By | VARCHAR2 | 1 |  | Y |
| 7 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 9 | `ORD_INV_NUM` | Ord_Invessorial Num | NUMBER | 22 | 9 | Y |
| 10 | `ORD_INV_PREX` | Ord_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 11 | `ORD_INV_SUFX` | Ord_Invessorial Sufx | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_INV_DATE` | Ord_Invessorial Date | DATE | 7 |  | Y |
| 13 | `ORD_TOT_AMT` | Ord_Totessorial Amt | NUMBER | 22 | 9 | Y |
| 14 | `ORD_TOT_ADDI_AMT` | Ord_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `ORD_TOT_DISC_PCENT` | Ord_Tot_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 16 | `ORD_TOT_ASWGT` | Ord_Totessorial Aswgt | NUMBER | 22 | 11 | Y |
| 17 | `ORD_TOT_COST` | Ord_Totessorial Cost | NUMBER | 22 | 9 | Y |
| 18 | `ORD_TOT_ADDI_COST` | Ord_Tot_Addiessorial Cost | NUMBER | 22 | 9 | Y |
| 19 | `ORD_INV_NUM_ADJ` | Ord_Inv_Numessorial Adj | NUMBER | 22 | 9 | Y |
| 20 | `ORD_INV_PREX_ADJ` | Ord_Inv_Prexessorial Adj | VARCHAR2 | 4 |  | Y |
| 21 | `ORD_INV_SUFX_ADJ` | Ord_Inv_Sufxessorial Adj | VARCHAR2 | 4 |  | Y |
| 22 | `ORD_INV_DATE_ADJ` | Ord_Inv_Dateessorial Adj | DATE | 7 |  | Y |
| 23 | `ORD_TOT_ADJ_AMT` | Ord_Tot_Adjessorial Amt | NUMBER | 22 | 9 | Y |
| 24 | `TAX_CODE` | Tax Code | VARCHAR2 | 5 |  | Y |
| 25 | `TAX_TOT_AMT1` | Tax_Totessorial Amt1 | NUMBER | 22 | 9 | Y |
| 26 | `TAX_TOT_AMT2` | Tax_Totessorial Amt2 | NUMBER | 22 | 9 | Y |
| 27 | `ORD_LTL_TOT_AMT` | Ord_Ltl_Totessorial Amt | NUMBER | 22 | 9 | Y |
| 28 | `ORD_LTL_TOT_ADDI_AMT` | Ord_Ltl_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 29 | `ORD_LTL_TOT_DISC_PCENT` | Ord_Ltl_Tot_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 30 | `ORD_LTL_TOT_ASWGT` | Ord_Ltl_Totessorial Aswgt | NUMBER | 22 | 11 | Y |

## `E_FRT_ORD_D8`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `ORD_REM_TEXT` | Ord_Remessorial Text | VARCHAR2 | 45 |  | Y |

## `E_FRT_ORD_H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 83
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 5 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 6 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 7 | `FRT_ORD_FLAG` | Frt_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ORD_CONF_FLAG` | Ord_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `FRT_GOODS_TP_CODE` | Frt_Goods_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 12 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 13 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 14 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 15 | `FRT_DEST_CODE_ORIGIN` | Frt_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 16 | `FRT_DEST_CODE_FINAL` | Frt_Dest_Codeessorial Final | VARCHAR2 | 10 |  | N |
| 17 | `FRT_ORD_ENTRY_DATE` | Frt_Ord_Entryessorial Date | DATE | 7 |  | Y |
| 18 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 19 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 20 | `FRT_ORD_COD_AMT` | Frt_Ord_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 21 | `ORD_TEMP_FRONT` | Ord_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 22 | `ORD_TEMP_MID` | Ord_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 23 | `ORD_TEMP_BACK` | Ord_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 24 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 25 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 26 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 27 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 28 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | Y |
| 29 | `ORD_TOT_UNIT` | Ord_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 30 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 11 | Y |
| 31 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 12 | Y |
| 32 | `ORD_TOT_FRT_AMT` | Ord_Tot_Frtessorial Amt | NUMBER | 22 | 9 | Y |
| 33 | `CON_NAME_MAN` | Con_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 34 | `CON_ADD1_MAN` | Con_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 35 | `CON_ADD2_MAN` | Con_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 36 | `CON_ADD3_MAN` | Con_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 37 | `ZIP_CITY_CON_MAN` | Zarehouse City Con Man | VARCHAR2 | 30 |  | Y |
| 38 | `STATE_CODE_CON_MAN` | State_Code_Conessorial Man | VARCHAR2 | 4 |  | Y |
| 39 | `ZIP_CODE_CON_MAN` | Zarehouse Code Con Man | VARCHAR2 | 10 |  | Y |
| 40 | `SHIP_NAME_MAN` | Ship_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 41 | `SHIP_ADD1_MAN` | Ship_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 42 | `SHIP_ADD2_MAN` | Ship_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 43 | `SHIP_ADD3_MAN` | Ship_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 44 | `ZIP_CITY_SHIP_MAN` | Zarehouse City Ship Man | VARCHAR2 | 30 |  | Y |
| 45 | `STATE_CODE_SHIP_MAN` | State_Code_Shipessorial Man | VARCHAR2 | 4 |  | Y |
| 46 | `ZIP_CODE_SHIP_MAN` | Zarehouse Code Ship Man | VARCHAR2 | 10 |  | Y |
| 47 | `ORD_SCH_FLAG` | Ord_Schessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `ORD_ASS_FLAG` | Ord_Assessorial Flag | VARCHAR2 | 1 |  | N |
| 49 | `ORD_SHIP_FLAG` | Ord_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 50 | `ORD_RATE_FLAG` | Ord_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 51 | `ORD_INV_FLAG` | Ord_Invessorial Flag | VARCHAR2 | 1 |  | N |
| 52 | `ORD_DELV_FLAG` | Ord_Delvessorial Flag | VARCHAR2 | 1 |  | N |
| 53 | `ORD_COST_FLAG` | Ord_Costessorial Flag | VARCHAR2 | 1 |  | N |
| 54 | `ORD_RECON_FLAG` | Ord_Reconessorial Flag | VARCHAR2 | 1 |  | N |
| 55 | `ORD_TO_SHIP_DATE_SCH` | Ord_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 56 | `ORD_TO_SHIP_DATE_ACT` | Ord_To_Ship_Dateessorial Act | DATE | 7 |  | Y |
| 57 | `ORD_TO_ARR_DATE_SCH` | Ord_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 58 | `ORD_TO_ARR_DATE_ACT` | Ord_To_Arr_Dateessorial Act | DATE | 7 |  | Y |
| 59 | `DELV_TOT_UNIT_OVER` | Delv_Tot_Unitessorial Over | NUMBER | 22 | 9 | Y |
| 60 | `DELV_TOT_UNIT_SHORT` | Delv_Tot_Unitessorial Short | NUMBER | 22 | 9 | Y |
| 61 | `DELV_TOT_UNIT_DAMAGE` | Delv_Tot_Unitessorial Damage | NUMBER | 22 | 9 | Y |
| 62 | `ORD_TOT_ADDI_AMT` | Ord_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 63 | `ORD_PICK_UP_NUM` | Ord_Pick_Upessorial Num | VARCHAR2 | 20 |  | Y |
| 64 | `ORD_TOT_PALL` | Ord_Totessorial Pall | NUMBER | 22 | 11 | Y |
| 65 | `COMP_CODE_LOAD_FINAL` | Comp_Code_Loadessorial Final | VARCHAR2 | 2 |  | Y |
| 66 | `FRT_TER_CODE_LOAD_FINAL` | Frt_Ter_Code_Loadessorial Final | VARCHAR2 | 4 |  | Y |
| 67 | `LOAD_NUM_LOAD_FINAL` | Load_Num_Loadessorial Final | NUMBER | 22 | 6 | Y |
| 68 | `ORD_SHIP_PLT` | Ord_Shipessorial Plt | NUMBER | 22 | 9 | Y |
| 69 | `ORD_SHIP_UNIT` | Ord_Shipessorial Unit | NUMBER | 22 | 9 | Y |
| 70 | `CON_ADD4_MAN` | Con_Add4essorial Man | VARCHAR2 | 30 |  | Y |
| 71 | `COUNTRY_CODE_CON_MAN` | Country_Code_Conessorial Man | VARCHAR2 | 4 |  | Y |
| 72 | `SHIP_ADD4_MAN` | Ship_Add4essorial Man | VARCHAR2 | 30 |  | Y |
| 73 | `COUNTRY_CODE_SHIP_MAN` | Country_Code_Shipessorial Man | VARCHAR2 | 4 |  | Y |
| 74 | `ORD_INV_NUM` | Ord_Invessorial Num | NUMBER | 22 | 9 | Y |
| 75 | `ORD_INV_PREX` | Ord_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 76 | `ORD_INV_SUFX` | Ord_Invessorial Sufx | VARCHAR2 | 4 |  | Y |
| 77 | `ORD_INV_DATE` | Ord_Invessorial Date | DATE | 7 |  | Y |
| 78 | `ORD_INV_NUM_ADJ` | Ord_Inv_Numessorial Adj | NUMBER | 22 | 9 | Y |
| 79 | `ORD_INV_PREX_ADJ` | Ord_Inv_Prexessorial Adj | VARCHAR2 | 4 |  | Y |
| 80 | `ORD_INV_SUFX_ADJ` | Ord_Inv_Sufxessorial Adj | VARCHAR2 | 4 |  | Y |
| 81 | `ORD_INV_DATE_ADJ` | Ord_Inv_Dateessorial Adj | DATE | 7 |  | Y |
| 82 | `ORD_TOT_ADJ_AMT` | Ord_Tot_Adjessorial Amt | NUMBER | 22 | 9 | Y |
| 83 | `ORD_TOT_COST` | Ord_Totessorial Cost | NUMBER | 22 | 9 | Y |

## `E_FRT_ORD_REST`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_FRT_ORD_VERS1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `E_FRT_RATE_BILL_D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 6 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 8 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | Y |
| 10 | `CLASS_DES` | Class Description | VARCHAR2 | 30 |  | Y |
| 11 | `BILL_CLASS_UNIT` | Bill_Classessorial Unit | NUMBER | 22 | 9 | Y |
| 12 | `BILL_CLASS_WGT` | Bill_Classessorial Wgt | NUMBER | 22 | 11 | Y |
| 13 | `BILL_CLASS_CUBE` | Bill_Classessorial Cube | NUMBER | 22 | 12 | Y |
| 14 | `BILL_CLASS_ASWGT` | Bill_Classessorial Aswgt | NUMBER | 22 | 11 | Y |
| 15 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 16 | `BILL_CLASS_RATE` | Bill_Classessorial Rate | NUMBER | 22 | 9 | Y |
| 17 | `BILL_CLASS_AMT` | Bill_Classessorial Amt | NUMBER | 22 | 9 | Y |
| 18 | `BILL_CLASS_FLAG` | Bill_Classessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_RATE_BILL_D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 6 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 8 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 10 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 11 | `CHG_DES` | Chgessorial Des | VARCHAR2 | 30 |  | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `BILL_CHG_QTY` | Bill_Chgessorial Qty | NUMBER | 22 | 9 | Y |
| 14 | `BILL_CHG_RATE` | Bill_Chgessorial Rate | NUMBER | 22 | 9 | Y |
| 15 | `BILL_CHG_AMT` | Bill_Chgessorial Amt | NUMBER | 22 | 9 | Y |

## `E_FRT_RATE_BILL_H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 6 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 8 | `INTRA_FLAG` | Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 10 | `BILL_AMT` | Billessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `BILL_ADDI_AMT` | Bill_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `BILL_DISC_PCENT` | Bill_Discessorial Pcent | NUMBER | 22 | 9 | Y |
| 13 | `BILL_DISC_AMT` | Bill_Discessorial Amt | NUMBER | 22 | 9 | Y |
| 14 | `BILL_FLAT_AMT` | Bill_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `BILL_RATE_LEV` | Bill_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 16 | `BILL_RATE_BY_FLAG` | Bill_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `BILL_ASWGT` | Billessorial Aswgt | NUMBER | 22 | 11 | Y |
| 18 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 19 | `FRT_TER_CODE_BILL` | Frt_Ter_Codeessorial Bill | VARCHAR2 | 4 |  | Y |

## `E_FRT_RATE_COST_D1`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 7 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 8 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 9 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | Y |
| 10 | `CLASS_DES` | Class Description | VARCHAR2 | 30 |  | Y |
| 11 | `COST_CLASS_UNIT` | Cost_Classessorial Unit | NUMBER | 22 | 9 | Y |
| 12 | `COST_CLASS_WGT` | Cost_Classessorial Wgt | NUMBER | 22 | 11 | Y |
| 13 | `COST_CLASS_CUBE` | Cost_Classessorial Cube | NUMBER | 22 | 12 | Y |
| 14 | `COST_CLASS_ASWGT` | Cost_Classessorial Aswgt | NUMBER | 22 | 11 | Y |
| 15 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 16 | `COST_CLASS_RATE` | Cost_Classessorial Rate | NUMBER | 22 | 9 | Y |
| 17 | `COST_CLASS_AMT` | Cost_Classessorial Amt | NUMBER | 22 | 9 | Y |
| 18 | `COST_CLASS_FLAG` | Cost_Classessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_FRT_RATE_COST_D2`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 7 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 8 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 9 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 11 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `CHG_DES` | Chgessorial Des | VARCHAR2 | 30 |  | Y |
| 14 | `COST_CHG_QTY` | Cost_Chgessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `COST_CHG_RATE` | Cost_Chgessorial Rate | NUMBER | 22 | 9 | Y |
| 16 | `COST_CHG_AMT` | Cost_Chgessorial Amt | NUMBER | 22 | 9 | Y |

## `E_FRT_RATE_COST_H`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 4 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 5 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 7 | `FRT_TER_CODE_ORD` | Frt_Ter_Codeessorial Ord | VARCHAR2 | 4 |  | Y |
| 8 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 9 | `INTRA_FLAG` | Intraessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 11 | `COST_AMT` | Costessorial Amt | NUMBER | 22 | 9 | Y |
| 12 | `COST_ADDI_AMT` | Cost_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 13 | `COST_DISC_PCENT` | Cost_Discessorial Pcent | NUMBER | 22 | 9 | Y |
| 14 | `COST_DISC_AMT` | Cost_Discessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `COST_DISTA` | Costessorial Dista | NUMBER | 22 | 9 | Y |
| 16 | `COST_LINEAR_RATE` | Cost_Linearessorial Rate | NUMBER | 22 | 9 | Y |
| 17 | `COST_FLAT_AMT` | Cost_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 18 | `COST_STOP_RATE` | Cost_Stopessorial Rate | NUMBER | 22 | 9 | Y |
| 19 | `COST_SKU_RATE` | Cost_Skuessorial Rate | NUMBER | 22 | 9 | Y |
| 20 | `COST_RATE_LEV` | Cost_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 21 | `COST_RATE_BY_FLAG` | Cost_Rate_Byessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `COST_ASWGT` | Costessorial Aswgt | NUMBER | 22 | 11 | Y |
| 23 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 24 | `FRT_TER_CODE_COST` | Frt_Ter_Codeessorial Cost | VARCHAR2 | 4 |  | Y |

## `E_FRT_SERV_UPD`

- **Tipo:** Transactional
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `SERV_DATE` | Servessorial Date | DATE | 7 |  | N |
| 6 | `SERV_PROG` | Servessorial Prog | VARCHAR2 | 10 |  | Y |
| 7 | `SERV_TEXT` | Servessorial Text | VARCHAR2 | 70 |  | Y |
| 8 | `SERV_STAT_FLAG` | Serv_Statessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `H_FRT_LOAD_MAN`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 27
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 7 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 8 | `FRT_LOAD_SHIP_DATE` | Frt_Load_Shipessorial Date | DATE | 7 |  | N |
| 9 | `LOAD_NUM_EXT_REF` | Load_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 10 | `LOAD_NUM_EXT_REF_CODE` | Load_Num_Ext_Refessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 12 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 13 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `LOAD_STAT` | Loadessorial Stat | VARCHAR2 | 1 |  | Y |
| 15 | `FRT_LOAD_SUSP_FLAG` | Frt_Load_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `LOAD_APPO_DATE` | Load_Appoessorial Date | DATE | 7 |  | Y |
| 17 | `FRT_LOAD_CARR_PRO_NUM` | Frt_Load_Carr_Proessorial Num | VARCHAR2 | 20 |  | Y |
| 18 | `FRT_LOAD_POOL_FLAG` | Frt_Load_Poolessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CARR_CODE_POOL` | Carr_Codeessorial Pool | VARCHAR2 | 10 |  | Y |
| 20 | `CON_CODE_POOL` | Con_Codeessorial Pool | VARCHAR2 | 10 |  | Y |
| 21 | `ALLOW_OVRR_IPRO_FLAG` | Allow_Ovrr_Iproessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `LOAD_A1INSPECTION_STAT_MES` | Load_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 23 | `LOAD_A1INSPECTION_DATE` | Load_A1Inspectionessorial Date | DATE | 7 |  | Y |
| 24 | `LOAD_A1INSPECTION_MES` | Load_A1Inspectionessorial Mes | VARCHAR2 | 100 |  | Y |
| 25 | `LOAD_NUM_TRANS_REF` | Load_Num_Transessorial Ref | VARCHAR2 | 20 |  | Y |
| 26 | `FRT_LOAD_START_CHECK_LIST_CODE` | Frt_Load_Start_Check_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `FRT_LOAD_END_CHECK_LIST_CODE` | Frt_Load_End_Check_Listessorial Code | VARCHAR2 | 4 |  | Y |

## `H_FRT_LOAD_MAN_CARR`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 6 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 7 | `LOAD_POW_UNIT_NUM` | Load_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `LOAD_CARRY_UNIT_NUM` | Load_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `LOAD_VES` | Loadessorial Ves | VARCHAR2 | 20 |  | Y |
| 10 | `LOAD_VOY` | Loadessorial Voy | VARCHAR2 | 20 |  | Y |
| 11 | `LOAD_SEAL1` | Loadessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 12 | `LOAD_SEAL2` | Loadessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 13 | `LOAD_TEMP_FRONT` | Load_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 14 | `LOAD_TEMP_MID` | Load_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 15 | `LOAD_TEMP_BACK` | Load_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 16 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 17 | `LOAD_TEMP_SET` | Load_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 18 | `LOAD_TEMP_AMB` | Load_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 19 | `LOAD_SEAL1_INTACT` | Load_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |

## `H_FRT_LOAD_PALL_D`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 6 | `PALL_ID` | Pallessorial Id | VARCHAR2 | 40 |  | N |
| 7 | `PALL_POS` | Pallessorial Pos | VARCHAR2 | 5 |  | N |
| 8 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 9 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |

## `H_FRT_LOAD_PALL_H`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 6 | `PALL_ID` | Pallessorial Id | VARCHAR2 | 40 |  | N |
| 7 | `PALL_POS` | Pallessorial Pos | VARCHAR2 | 5 |  | N |
| 8 | `PALL_TP` | Pallessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 3 | N |

## `H_FRT_ORD_D1`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 7 | `FRT_CLASS_DES` | Frt_Classessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `ORD_UNIT` | Ordessorial Unit | NUMBER | 22 | 9 | N |
| 9 | `ORD_WGT` | Ordessorial Wgt | NUMBER | 22 | 11 | N |
| 10 | `ORD_CUBE` | Ordessorial Cube | NUMBER | 22 | 12 | Y |
| 11 | `ORD_TL_ASWGT` | Ord_Tlessorial Aswgt | NUMBER | 22 | 11 | Y |
| 12 | `ORD_TL_RATE` | Ord_Tlessorial Rate | NUMBER | 22 | 9 | Y |
| 13 | `SKU_CODE_TL` | Sku_Codeessorial Tl | VARCHAR2 | 4 |  | Y |
| 14 | `ORD_TL_AMT` | Ord_Tlessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `ORD_TL_DISC_PCENT` | Ord_Tl_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 16 | `ORD_TL_FLAG` | Ord_Tlessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `ORD_LTL_ASWGT` | Ord_Ltlessorial Aswgt | NUMBER | 22 | 11 | Y |
| 18 | `ORD_LTL_RATE` | Ord_Ltlessorial Rate | NUMBER | 22 | 9 | Y |
| 19 | `SKU_CODE_LTL` | Sku_Codeessorial Ltl | VARCHAR2 | 4 |  | Y |
| 20 | `ORD_LTL_AMT` | Ord_Ltlessorial Amt | NUMBER | 22 | 9 | Y |
| 21 | `ORD_LTL_DISC_PCENT` | Ord_Ltl_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 22 | `ORD_LTL_FLAG` | Ord_Ltlessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `ORD_PALL` | Ordessorial Pall | NUMBER | 22 | 11 | Y |

## `H_FRT_ORD_D2`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `ORD_CHG_DES` | Ord_Chgessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `ORD_CHG_QTY` | Ord_Chgessorial Qty | NUMBER | 22 | 9 | Y |
| 9 | `ORD_CHG_RATE` | Ord_Chgessorial Rate | NUMBER | 22 | 9 | Y |
| 10 | `ORD_CHG_AMT` | Ord_Chgessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `ORD_CHG_INV_FLAG` | Ord_Chg_Invessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_FRT_ORD_D3`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_REM_LINE_NUM` | Ord_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 6 | `ORD_REM_LINE_TEXT` | Ord_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `H_FRT_ORD_D4`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 4 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 6 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 8 | `LOAD_TYPE` | Loadessorial Type | VARCHAR2 | 1 |  | N |
| 9 | `BILL_DELV_GRP_FLAG` | Bill_Delv_Grpessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `FRT_TER_CODE_GRP` | Frt_Ter_Codeessorial Grp | VARCHAR2 | 4 |  | Y |
| 11 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 12 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 13 | `LOAD_NUM_EXT_REF` | Load_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 14 | `ORD_PROS_STAT` | Ord_Prosessorial Stat | VARCHAR2 | 1 |  | Y |
| 15 | `LOAD_NUM_TRANS_REF` | Load_Num_Transessorial Ref | VARCHAR2 | 20 |  | Y |

## `H_FRT_ORD_D5`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `FRT_TER_CODE_DELV` | Frt_Ter_Codeessorial Delv | VARCHAR2 | 4 |  | N |
| 6 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |

## `H_FRT_ORD_D7`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_INTRA_FLAG` | Ord_Intraessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ORD_RATE_LEV` | Ord_Rateessorial Lev | VARCHAR2 | 5 |  | Y |
| 7 | `ORD_RATE_BY` | Ord_Rateessorial By | VARCHAR2 | 1 |  | Y |
| 8 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 10 | `ORD_INV_NUM` | Ord_Invessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `ORD_INV_PREX` | Ord_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_INV_SUFX` | Ord_Invessorial Sufx | VARCHAR2 | 4 |  | Y |
| 13 | `ORD_INV_DATE` | Ord_Invessorial Date | DATE | 7 |  | Y |
| 14 | `ORD_TOT_AMT` | Ord_Totessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `ORD_TOT_ADDI_AMT` | Ord_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 16 | `ORD_TOT_DISC_PCENT` | Ord_Tot_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 17 | `ORD_TOT_ASWGT` | Ord_Totessorial Aswgt | NUMBER | 22 | 11 | Y |
| 18 | `ORD_TOT_COST` | Ord_Totessorial Cost | NUMBER | 22 | 9 | Y |
| 19 | `ORD_TOT_ADDI_COST` | Ord_Tot_Addiessorial Cost | NUMBER | 22 | 9 | Y |
| 20 | `ORD_INV_NUM_ADJ` | Ord_Inv_Numessorial Adj | NUMBER | 22 | 9 | Y |
| 21 | `ORD_INV_PREX_ADJ` | Ord_Inv_Prexessorial Adj | VARCHAR2 | 4 |  | Y |
| 22 | `ORD_INV_SUFX_ADJ` | Ord_Inv_Sufxessorial Adj | VARCHAR2 | 4 |  | Y |
| 23 | `ORD_INV_DATE_ADJ` | Ord_Inv_Dateessorial Adj | DATE | 7 |  | Y |
| 24 | `ORD_TOT_ADJ_AMT` | Ord_Tot_Adjessorial Amt | NUMBER | 22 | 9 | Y |
| 25 | `TAX_CODE` | Tax Code | VARCHAR2 | 5 |  | Y |
| 26 | `TAX_TOT_AMT1` | Tax_Totessorial Amt1 | NUMBER | 22 | 9 | Y |
| 27 | `TAX_TOT_AMT2` | Tax_Totessorial Amt2 | NUMBER | 22 | 9 | Y |
| 28 | `ORD_LTL_TOT_AMT` | Ord_Ltl_Totessorial Amt | NUMBER | 22 | 9 | Y |
| 29 | `ORD_LTL_TOT_ADDI_AMT` | Ord_Ltl_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 30 | `ORD_LTL_TOT_DISC_PCENT` | Ord_Ltl_Tot_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 31 | `ORD_LTL_TOT_ASWGT` | Ord_Ltl_Totessorial Aswgt | NUMBER | 22 | 11 | Y |

## `H_FRT_ORD_D8`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 6 | `FRT_ORD_LINE_NUM` | Frt_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `ORD_REM_TEXT` | Ord_Remessorial Text | VARCHAR2 | 45 |  | Y |

## `H_FRT_ORD_H`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 84
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 8 | `FRT_ORD_FLAG` | Frt_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ORD_CONF_FLAG` | Ord_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `FRT_GOODS_TP_CODE` | Frt_Goods_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 14 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 15 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 16 | `FRT_DEST_CODE_ORIGIN` | Frt_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 17 | `FRT_DEST_CODE_FINAL` | Frt_Dest_Codeessorial Final | VARCHAR2 | 10 |  | N |
| 18 | `FRT_ORD_ENTRY_DATE` | Frt_Ord_Entryessorial Date | DATE | 7 |  | Y |
| 19 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 20 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 21 | `FRT_ORD_COD_AMT` | Frt_Ord_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 22 | `ORD_TEMP_FRONT` | Ord_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 23 | `ORD_TEMP_MID` | Ord_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 24 | `ORD_TEMP_BACK` | Ord_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 25 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 26 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 27 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 28 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 29 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | Y |
| 30 | `ORD_TOT_UNIT` | Ord_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 31 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 11 | Y |
| 32 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 12 | Y |
| 33 | `ORD_TOT_FRT_AMT` | Ord_Tot_Frtessorial Amt | NUMBER | 22 | 9 | Y |
| 34 | `CON_NAME_MAN` | Con_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 35 | `CON_ADD1_MAN` | Con_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 36 | `CON_ADD2_MAN` | Con_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 37 | `CON_ADD3_MAN` | Con_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 38 | `ZIP_CITY_CON_MAN` | Zarehouse City Con Man | VARCHAR2 | 30 |  | Y |
| 39 | `STATE_CODE_CON_MAN` | State_Code_Conessorial Man | VARCHAR2 | 4 |  | Y |
| 40 | `ZIP_CODE_CON_MAN` | Zarehouse Code Con Man | VARCHAR2 | 10 |  | Y |
| 41 | `SHIP_NAME_MAN` | Ship_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 42 | `SHIP_ADD1_MAN` | Ship_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 43 | `SHIP_ADD2_MAN` | Ship_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 44 | `SHIP_ADD3_MAN` | Ship_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 45 | `ZIP_CITY_SHIP_MAN` | Zarehouse City Ship Man | VARCHAR2 | 30 |  | Y |
| 46 | `STATE_CODE_SHIP_MAN` | State_Code_Shipessorial Man | VARCHAR2 | 4 |  | Y |
| 47 | `ZIP_CODE_SHIP_MAN` | Zarehouse Code Ship Man | VARCHAR2 | 10 |  | Y |
| 48 | `ORD_SCH_FLAG` | Ord_Schessorial Flag | VARCHAR2 | 1 |  | N |
| 49 | `ORD_ASS_FLAG` | Ord_Assessorial Flag | VARCHAR2 | 1 |  | N |
| 50 | `ORD_SHIP_FLAG` | Ord_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 51 | `ORD_RATE_FLAG` | Ord_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 52 | `ORD_INV_FLAG` | Ord_Invessorial Flag | VARCHAR2 | 1 |  | N |
| 53 | `ORD_DELV_FLAG` | Ord_Delvessorial Flag | VARCHAR2 | 1 |  | N |
| 54 | `ORD_COST_FLAG` | Ord_Costessorial Flag | VARCHAR2 | 1 |  | N |
| 55 | `ORD_RECON_FLAG` | Ord_Reconessorial Flag | VARCHAR2 | 1 |  | N |
| 56 | `ORD_TO_SHIP_DATE_SCH` | Ord_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 57 | `ORD_TO_SHIP_DATE_ACT` | Ord_To_Ship_Dateessorial Act | DATE | 7 |  | Y |
| 58 | `ORD_TO_ARR_DATE_SCH` | Ord_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 59 | `ORD_TO_ARR_DATE_ACT` | Ord_To_Arr_Dateessorial Act | DATE | 7 |  | Y |
| 60 | `DELV_TOT_UNIT_OVER` | Delv_Tot_Unitessorial Over | NUMBER | 22 | 9 | Y |
| 61 | `DELV_TOT_UNIT_SHORT` | Delv_Tot_Unitessorial Short | NUMBER | 22 | 9 | Y |
| 62 | `DELV_TOT_UNIT_DAMAGE` | Delv_Tot_Unitessorial Damage | NUMBER | 22 | 9 | Y |
| 63 | `ORD_TOT_ADDI_AMT` | Ord_Tot_Addiessorial Amt | NUMBER | 22 | 9 | Y |
| 64 | `ORD_PICK_UP_NUM` | Ord_Pick_Upessorial Num | VARCHAR2 | 20 |  | Y |
| 65 | `ORD_INV_NUM` | Ord_Invessorial Num | NUMBER | 22 | 9 | Y |
| 66 | `ORD_INV_PREX` | Ord_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 67 | `ORD_INV_SUFX` | Ord_Invessorial Sufx | VARCHAR2 | 4 |  | Y |
| 68 | `ORD_INV_DATE` | Ord_Invessorial Date | DATE | 7 |  | Y |
| 69 | `ORD_INV_NUM_ADJ` | Ord_Inv_Numessorial Adj | NUMBER | 22 | 9 | Y |
| 70 | `ORD_INV_PREX_ADJ` | Ord_Inv_Prexessorial Adj | VARCHAR2 | 4 |  | Y |
| 71 | `ORD_INV_SUFX_ADJ` | Ord_Inv_Sufxessorial Adj | VARCHAR2 | 4 |  | Y |
| 72 | `ORD_INV_DATE_ADJ` | Ord_Inv_Dateessorial Adj | DATE | 7 |  | Y |
| 73 | `ORD_TOT_ADJ_AMT` | Ord_Tot_Adjessorial Amt | NUMBER | 22 | 9 | Y |
| 74 | `ORD_TOT_COST` | Ord_Totessorial Cost | NUMBER | 22 | 9 | Y |
| 75 | `ORD_TOT_PALL` | Ord_Totessorial Pall | NUMBER | 22 | 11 | Y |
| 76 | `COMP_CODE_LOAD_FINAL` | Comp_Code_Loadessorial Final | VARCHAR2 | 2 |  | Y |
| 77 | `FRT_TER_CODE_LOAD_FINAL` | Frt_Ter_Code_Loadessorial Final | VARCHAR2 | 4 |  | Y |
| 78 | `LOAD_NUM_LOAD_FINAL` | Load_Num_Loadessorial Final | NUMBER | 22 | 6 | Y |
| 79 | `ORD_SHIP_PLT` | Ord_Shipessorial Plt | NUMBER | 22 | 9 | Y |
| 80 | `ORD_SHIP_UNIT` | Ord_Shipessorial Unit | NUMBER | 22 | 9 | Y |
| 81 | `CON_ADD4_MAN` | Con_Add4essorial Man | VARCHAR2 | 30 |  | Y |
| 82 | `COUNTRY_CODE_CON_MAN` | Country_Code_Conessorial Man | VARCHAR2 | 4 |  | Y |
| 83 | `SHIP_ADD4_MAN` | Ship_Add4essorial Man | VARCHAR2 | 30 |  | Y |
| 84 | `COUNTRY_CODE_SHIP_MAN` | Country_Code_Shipessorial Man | VARCHAR2 | 4 |  | Y |

## `H_FRT_SERV_UPD`

- **Tipo:** Historical
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `SERV_DATE` | Servessorial Date | DATE | 7 |  | N |
| 7 | `SERV_PROG` | Servessorial Prog | VARCHAR2 | 10 |  | Y |
| 8 | `SERV_TEXT` | Servessorial Text | VARCHAR2 | 70 |  | Y |
| 9 | `SERV_STAT_FLAG` | Serv_Statessorial Flag | VARCHAR2 | 1 |  | Y |

## `L_ASL_FRT_CHG`

- **Tipo:** Custom
- **Categoria:** Freight
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | N |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 4 | `FRT_CHG_QTY` | Frt_Chgessorial Qty | NUMBER | 22 | 9 | N |
| 5 | `FRT_CHG_WGT` | Frt_Chgessorial Wgt | NUMBER | 22 | 9 | N |
| 6 | `FRT_CHG_RATE` | Frt_Chgessorial Rate | NUMBER | 22 | 9 | N |
| 7 | `FRT_CHG_AMT` | Frt_Chgessorial Amt | NUMBER | 22 | 9 | N |
| 8 | `TAX_CODE1` | Taxessorial Code1 | VARCHAR2 | 4 |  | Y |
| 9 | `TAX_AMT1` | Taxessorial Amt1 | NUMBER | 22 | 9 | Y |
| 10 | `TAX_CODE2` | Taxessorial Code2 | VARCHAR2 | 4 |  | Y |
| 11 | `TAX_AMT2` | Taxessorial Amt2 | NUMBER | 22 | 9 | Y |
| 12 | `REC_TP` | Recessorial Tp | VARCHAR2 | 1 |  | Y |
| 13 | `FRT_CHG_DATE` | Frt_Chgessorial Date | DATE | 7 |  | N |
| 14 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |

## `L_ASL_FRT_CLASS`

- **Tipo:** Custom
- **Categoria:** Freight
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | N |
| 3 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_CLASS_QTY` | Frt_Classessorial Qty | NUMBER | 22 | 9 | N |
| 5 | `FRT_CLASS_WGT` | Frt_Classessorial Wgt | NUMBER | 22 | 9 | N |
| 6 | `FRT_CLASS_RATE` | Frt_Classessorial Rate | NUMBER | 22 | 9 | N |
| 7 | `FRT_CLASS_AMT` | Frt_Classessorial Amt | NUMBER | 22 | 9 | N |
| 8 | `FRT_CHG_CODE` | Frt_Chgessorial Code | VARCHAR2 | 6 |  | Y |
| 9 | `TAX_CODE1` | Taxessorial Code1 | VARCHAR2 | 4 |  | Y |
| 10 | `TAX_AMT1` | Taxessorial Amt1 | NUMBER | 22 | 9 | Y |
| 11 | `TAX_CODE2` | Taxessorial Code2 | VARCHAR2 | 4 |  | Y |
| 12 | `TAX_AMT2` | Taxessorial Amt2 | NUMBER | 22 | 9 | Y |
| 13 | `REC_TP` | Recessorial Tp | VARCHAR2 | 1 |  | Y |
| 14 | `FRT_CLASS_DATE` | Frt_Classessorial Date | DATE | 7 |  | N |
| 15 | `FRT_CLASS_ASWGT` | Frt_Classessorial Aswgt | NUMBER | 22 | 9 | Y |
| 16 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |

## `M_FRT_DEST`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `FRT_DEST_DES` | Frt_Destessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FRT_DEST_STAT` | Frt_Destessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `FRT_DEST_GRP_CODE` | Frt_Dest_Grpessorial Code | VARCHAR2 | 4 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FRT_DEST_GRP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `FRT_DEST_GRP_CODE` | Frt_Dest_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FRT_DEST_GRP_DES` | Frt_Dest_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FRT_DEST_GRP_STAT` | Frt_Dest_Grpessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FRT_GOODS_TP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FRT_GOODS_TP_CODE` | Frt_Goods_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `FRT_GOODS_TP_DES` | Frt_Goods_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `FRT_GOODS_TEMP_FLAG` | Frt_Goods_Tempessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `FRT_GOODS_TP_STAT` | Frt_Goods_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_FRT_PAY_OFFC`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_PAY_OFFC_CODE` | Frt_Pay_Offcessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `FRT_PAY_OFFC_NAME` | Frt_Pay_Offcessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `FRT_PAY_OFFC_STAT` | Frt_Pay_Offcessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `FRT_PAY_OFFC_ADD1` | Frt_Pay_Offcessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `FRT_PAY_OFFC_ADD2` | Frt_Pay_Offcessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `FRT_PAY_OFFC_ADD3` | Frt_Pay_Offcessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `FRT_PAY_OFFC_LAST_ACT_DATE` | Frt_Pay_Offc_Last_Actessorial Date | DATE | 7 |  | Y |
| 11 | `FRT_PAY_OFFC_ADD4` | Frt_Pay_Offcessorial Add4 | VARCHAR2 | 30 |  | Y |
| 12 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 18 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_FRT_POINT_D`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_POINT_DEST_FROM` | Frt_Point_Destessorial From | VARCHAR2 | 10 |  | N |
| 3 | `FRT_POINT_DEST_TO` | Frt_Point_Destessorial To | VARCHAR2 | 10 |  | N |
| 4 | `FRT_POINT_BC_FLAG` | Frt_Point_Bcessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 7 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | N |
| 8 | `FRT_POINT_TYPE_FLAG` | Frt_Point_Typeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | Y |
| 10 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | Y |

## `M_FRT_POINT_D_TEMP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_POINT_DEST_FROM` | Frt_Point_Destessorial From | VARCHAR2 | 10 |  | N |
| 3 | `FRT_POINT_DEST_TO` | Frt_Point_Destessorial To | VARCHAR2 | 10 |  | N |
| 4 | `FRT_POINT_BC_FLAG` | Frt_Point_Bcessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 7 | `FRT_POINT_ZONE_CODE` | Frt_Point_Zoneessorial Code | VARCHAR2 | 6 |  | N |
| 8 | `FRT_POINT_TYPE_FLAG` | Frt_Point_Typeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 10 |  | Y |

## `M_FRT_POINT_H`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_POINT_DEST_FROM` | Frt_Point_Destessorial From | VARCHAR2 | 10 |  | N |
| 3 | `FRT_POINT_DEST_TO` | Frt_Point_Destessorial To | VARCHAR2 | 10 |  | N |
| 4 | `FRT_POINT_STAT` | Frt_Pointessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 6 | `FRT_POINT_DISTA` | Frt_Pointessorial Dista | NUMBER | 22 | 11 | Y |

## `M_FRT_QTY_BK_D`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FRT_QTY_BK_BK_NUM` | Frt_Qty_Bk_Bkessorial Num | NUMBER | 22 | 2 | N |
| 4 | `FRT_QTY_BK_VALUE` | Frt_Qty_Bkessorial Value | NUMBER | 22 | 11 | Y |

## `M_FRT_QTY_BK_H`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FRT_QTY_BK_DES` | Frt_Qty_Bkessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FRT_QTY_BK_STAT` | Frt_Qty_Bkessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `FRT_QTY_BK_NUM_BK` | Frt_Qty_Bk_Numessorial Bk | NUMBER | 22 | 2 | N |

## `M_FRT_TABLE_D`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | N |
| 3 | `FRT_TABLE_EFF_DATE` | Frt_Table_Effessorial Date | DATE | 7 |  | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `FRT_TABLE_NUM_BK` | Frt_Table_Numessorial Bk | NUMBER | 22 | 2 | N |
| 6 | `FRT_TABLE_BK_FACT` | Frt_Table_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 7 | `FRT_TABLE_VALUE_FACT` | Frt_Table_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `FRT_TABLE_RATE_FACT` | Frt_Table_Rateessorial Fact | VARCHAR2 | 240 |  | N |
| 9 | `FRT_TABLE_FLAT_FACT` | Frt_Table_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 10 | `FRT_TABLE_MIN_FACT` | Frt_Table_Minessorial Fact | VARCHAR2 | 240 |  | N |
| 11 | `FRT_TABLE_MAX_FACT` | Frt_Table_Maxessorial Fact | VARCHAR2 | 240 |  | N |

## `M_FRT_TABLE_D_TEMP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `FRT_TABLE_EFF_DATE` | Frt_Table_Effessorial Date | DATE | 7 |  | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `FRT_QTY_BK_NUM_BK` | Frt_Qty_Bk_Numessorial Bk | NUMBER | 22 | 2 | N |
| 6 | `FRT_TABLE_BK_FACT` | Frt_Table_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 7 | `FRT_TABLE_VAL_FACT` | Frt_Table_Valessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `FRT_TABLE_RATE_FACT` | Frt_Table_Rateessorial Fact | VARCHAR2 | 240 |  | N |
| 9 | `FRT_TABLE_FLAT_FACT` | Frt_Table_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 10 | `FRT_TABLE_MIN_FACT` | Frt_Table_Minessorial Fact | VARCHAR2 | 240 |  | N |
| 11 | `FRT_TABLE_MAX_FACT` | Frt_Table_Maxessorial Fact | VARCHAR2 | 240 |  | N |

## `M_FRT_TABLE_H`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TABLE_CODE` | Frt_Tableessorial Code | VARCHAR2 | 15 |  | N |
| 3 | `FRT_TABLE_DES` | Frt_Tableessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FRT_TABLE_EFF_DATE` | Frt_Table_Effessorial Date | DATE | 7 |  | N |
| 5 | `FRT_TABLE_STAT` | Frt_Tableessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 8 | `FRT_TABLE_MIN_AMT` | Frt_Table_Minessorial Amt | NUMBER | 22 | 9 | Y |
| 9 | `FRT_TABLE_MAX_AMT` | Frt_Table_Maxessorial Amt | NUMBER | 22 | 9 | Y |
| 10 | `FRT_TABLE_TL_AMT` | Frt_Table_Tlessorial Amt | NUMBER | 22 | 9 | Y |
| 11 | `FRT_TABLE_MILE_RATE` | Frt_Table_Mileessorial Rate | NUMBER | 22 | 9 | Y |

## `M_FRT_TERMINAL_TEMP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FRT_TER_DES` | Frt_Teressorial Des | VARCHAR2 | 30 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `FRT_TER_STAT` | Frt_Teressorial Stat | VARCHAR2 | 1 |  | N |

## `M_FRT_TER_D`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FRT_TER_H`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_TER_DES` | Frt_Teressorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FRT_TER_ADD1` | Frt_Teressorial Add1 | VARCHAR2 | 30 |  | N |
| 6 | `FRT_TER_ADD2` | Frt_Teressorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 8 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 10 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 11 | `FRT_TER_STAT` | Frt_Teressorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 12 |  | Y |
| 13 | `FAX_NUM` | Faxessorial Num | VARCHAR2 | 12 |  | Y |
| 14 | `CUBE_PALL_CONV_FACT` | Cube_Pall_Convessorial Fact | NUMBER | 22 | 9 | Y |
| 15 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 16 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 17 | `FRT_TER_CARR_ORD_UPD_FLAG` | Frt_Ter_Carr_Ord_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `FRT_TER_ADD3` | Frt_Teressorial Add3 | VARCHAR2 | 30 |  | Y |
| 19 | `FRT_TER_ADD4` | Frt_Teressorial Add4 | VARCHAR2 | 30 |  | Y |
| 20 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 21 | `FRT_TER_INDUCT_FLAG` | Frt_Ter_Inductessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `FRT_TER_FINAL_FLAG` | Frt_Ter_Finalessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 24 | `CHK_IN_WINDOW_INB_LOAD_FLAG` | Chk_In_Window_Inb_Loadessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `CHK_IN_WINDOW_INB_UNIT_FLAG` | Chk_In_Window_Inb_Unitessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `CHK_OUT_WINDOW_FLAG` | Chk_Out_Windowessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `MV_TRLR_FLAG` | Mv_Trlressorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `YARD_CODE_MV_TRLR` | Yarehouse Code Mv Trlr | VARCHAR2 | 4 |  | Y |
| 29 | `LOC_CODE_YARD_MV_TRLR` | Loc_Code_Yard_Mvessorial Trlr | VARCHAR2 | 12 |  | Y |
| 30 | `TIME_ZONE_CODE` | Time_Zoneessorial Code | VARCHAR2 | 4 |  | Y |
| 31 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 32 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 33 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 34 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 35 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 36 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 37 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_FRT_TP`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TP_CODE` | Frt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_TP_DES` | Frt_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FRT_TP_STAT` | Frt_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FRT_ZONE_D`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `FRT_ZONE_STOP_NUM` | Frt_Zone_Stopessorial Num | NUMBER | 22 | 4 | N |
| 4 | `FRT_DEST_CODE_FROM` | Frt_Dest_Codeessorial From | VARCHAR2 | 10 |  | N |
| 5 | `FRT_DEST_CODE_TO` | Frt_Dest_Codeessorial To | VARCHAR2 | 10 |  | N |

## `M_FRT_ZONE_H`

- **Tipo:** Master
- **Categoria:** Freight
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `FRT_ZONE_DES` | Frt_Zoneessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FRT_ZONE_STAT` | Frt_Zoneessorial Stat | VARCHAR2 | 1 |  | N |

