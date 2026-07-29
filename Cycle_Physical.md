# Tabelas — Cycle/Physical

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **3**.

## `C_CYC_CNT_CHG`

- **Tipo:** Transactional
- **Categoria:** Cycle/Physical
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_REC_TP` | Cyc_Cnt_Recessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 7 | `COMP_DATE` | Compessorial Date | DATE | 7 |  | N |

## `C_CYC_CNT_EVENT`

- **Tipo:** Transactional
- **Categoria:** Cycle/Physical
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

## `M_CYC_CNT_PROF`

- **Tipo:** Master
- **Categoria:** Cycle/Physical
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CYC_CNT_PROF_DES` | Cyc_Cnt_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CYC_CNT_PROF_STAT` | Cyc_Cnt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CYC_CNT_CURR_PER_START_DATE` | Cyc_Cnt_Curr_Per_Startessorial Date | DATE | 7 |  | N |
| 7 | `CYC_CNT_CURR_PER_END_DATE` | Cyc_Cnt_Curr_Per_Endessorial Date | DATE | 7 |  | N |
| 8 | `CYC_CNT_NXT_PER_START_DATE` | Cyc_Cnt_Nxt_Per_Startessorial Date | DATE | 7 |  | N |
| 9 | `CYC_CNT_NXT_PER_END_DATE` | Cyc_Cnt_Nxt_Per_Endessorial Date | DATE | 7 |  | Y |
| 10 | `CYC_CNT_PROF_TP` | Cyc_Cnt_Professorial Tp | VARCHAR2 | 1 |  | N |
| 11 | `CYC_CNT_PROF_CNT_NUM` | Cyc_Cnt_Prof_Cntessorial Num | NUMBER | 22 | 6 | N |
| 12 | `CYC_CNT_PROF_CNT_PER_ENT_NUM` | Cyc_Cnt_Prof_Cnt_Per_Entessorial Num | NUMBER | 22 | 6 | N |
| 13 | `CYC_CNT_VARI` | Cyc_Cntessorial Vari | NUMBER | 22 | 5 | N |
| 14 | `DATE_PROF_CODE` | Date_Professorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CYC_CNT_PROF_FRQ_CODE` | Cyc_Cnt_Prof_Frqessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `CYC_CNT_PROF_FRQ_NUM` | Cyc_Cnt_Prof_Frqessorial Num | NUMBER | 22 | 3 | Y |
| 17 | `CYC_CNT_PROF_NXT_DATE` | Cyc_Cnt_Prof_Nxtessorial Date | DATE | 7 |  | N |
| 18 | `CYC_CNT_PROF_CNT_ON_DAY_FLAG` | Cyc_Cnt_Prof_Cnt_On_Dayessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `CYC_CNT_PROF_VARI_BASE` | Cyc_Cnt_Prof_Variessorial Base | VARCHAR2 | 1 |  | N |
| 20 | `CYC_CNT_PROF_CNT_CYC` | Cyc_Cnt_Prof_Cntessorial Cyc | NUMBER | 22 | 3 | N |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |

