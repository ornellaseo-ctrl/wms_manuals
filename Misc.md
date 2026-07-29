# Tabelas — Misc

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **514**.

## `ARUNTEST`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `A` | A | NUMBER | 22 |  | Y |
| 2 | `B` | Bessorial B | VARCHAR2 | 10 |  | Y |

## `ASSIGNED_TABLE_NUMBERS`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TABLE_NUMBER` | Tableessorial Number | VARCHAR2 | 3 |  | N |
| 2 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 40 |  | N |

## `CREATE$JAVA$LOB$TABLE`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `NAME` | Nameessorial Name | VARCHAR2 | 700 |  | Y |
| 2 | `LOB` | Lobessorial Lob | BLOB | 4000 |  | Y |
| 3 | `LOADTIME` | Loadtimeessorial Loadtime | DATE | 7 |  | Y |

## `C_A1SCH_INTFACE_RUN`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LAST_RUN_DATE` | Last_Runessorial Date | DATE | 7 |  | N |

## `C_A1SCH_INTFACE_RUN_FM`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LAST_RUN_FM_DATE` | Last_Run_Fmessorial Date | DATE | 7 |  | N |

## `C_A1SCH_INTFC_APPO_STAT_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `C_ACT_FIELD_D`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_SEQ_NUM` | Act_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `ACT_PARENT_LINE_NUM` | Act_Parent_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `ACT_BLOCK_CODE` | Act_Blockessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `ACT_REC_LINE_NUM` | Act_Rec_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ACT_FIELD_CODE` | Act_Fieldessorial Code | VARCHAR2 | 30 |  | N |
| 6 | `ACT_FIELD_VAL` | Act_Fieldessorial Val | VARCHAR2 | 2000 |  | Y |
| 7 | `ACT_FIELD_DATE_VAL` | Act_Field_Dateessorial Val | DATE | 7 |  | Y |

## `C_ACT_FIELD_H`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_SEQ_NUM` | Act_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `ACT_CODE` | Actessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ACT_COMP_CODE` | Act_Compessorial Code | VARCHAR2 | 2 |  | Y |
| 4 | `ACT_DOC_TP` | Act_Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 5 | `ACT_DOC_NUM` | Act_Docessorial Num | NUMBER | 22 | 9 | Y |
| 6 | `ACT_OP_CODE` | Act_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `ACT_RUN_DATE` | Act_Runessorial Date | DATE | 7 |  | Y |
| 8 | `ACT_STAT` | Actessorial Stat | VARCHAR2 | 1 |  | N |
| 9 | `ACT_ERR_CODE` | Act_Erressorial Code | VARCHAR2 | 6 |  | Y |
| 10 | `ACT_ERR_TEXT` | Act_Erressorial Text | VARCHAR2 | 1500 |  | Y |

## `C_ALERT_PROS`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALERT_CODE` | Alert Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `ALERT_ID_LIST` | Alert_Idessorial List | VARCHAR2 | 100 |  | N |
| 4 | `ALERT_ROW_STAT` | Alert_Rowessorial Stat | NUMBER | 22 | 4 | N |
| 5 | `ALERT_ROW_DATE` | Alert_Rowessorial Date | DATE | 7 |  | N |

## `C_ASS`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `DATE_START` | Dateessorial Start | DATE | 7 |  | N |
| 5 | `DATE_END` | Dateessorial End | DATE | 7 |  | N |
| 6 | `DATE_PURGE` | Dateessorial Purge | DATE | 7 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 12 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 13 | `INVT_LEV_VALUE` | Invt_Levessorial Value | VARCHAR2 | 40 |  | N |

## `C_AUD_KEY`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `MVT_TRANS_DATE` | Mvt_Transessorial Date | DATE | 7 |  | N |
| 5 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 6 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 7 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 8 | `ADJ_AUD_NUM` | Adj_Audessorial Num | NUMBER | 22 | 6 | N |
| 9 | `ROW_ID` | Rowessorial Id | VARCHAR2 | 26 |  | N |

## `C_AUD_MEAS`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 2 | `IN_MEAS_CODE` | In_Measessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `AUD_DATE` | Audessorial Date | DATE | 7 |  | N |

## `C_DRMS_ERR`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_ERR_PROC` | Drms_Erressorial Proc | VARCHAR2 | 20 |  | Y |
| 2 | `DRMS_ERR_PKG` | Drms_Erressorial Pkg | VARCHAR2 | 20 |  | Y |
| 3 | `DRMS_ERR_DATE` | Drms_Erressorial Date | DATE | 7 |  | Y |
| 4 | `DRMS_ERR_CODE` | Drms_Erressorial Code | NUMBER | 22 | 6 | Y |
| 5 | `DRMS_ERR_MES` | Drms_Erressorial Mes | VARCHAR2 | 50 |  | Y |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 7 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 8 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |

## `C_ERROR`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `MESSAGE` | Messageessorial Message | VARCHAR2 | 2000 |  | Y |

## `C_ERR_LOG`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ROUTINE_CODE` | Routineessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `ERR_LOG_DOC_TP_FLAG` | Err_Log_Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 5 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 6 | `ERR_LOG_DATE` | Err_Logessorial Date | DATE | 7 |  | N |
| 7 | `ERR_LOG_VIEW_FLAG` | Err_Log_Viewessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ERR_SEQ_NUM` | Err_Seqessorial Num | NUMBER | 22 | 10 | N |
| 9 | `ERR_SEQ_LINE_NUM` | Err_Seq_Lineessorial Num | NUMBER | 22 | 4 | N |
| 10 | `ERR_LOG_LINE_TEXT` | Err_Log_Lineessorial Text | VARCHAR2 | 150 |  | Y |
| 11 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 12 | `ERR_LOG_VIEW_DATE` | Err_Log_Viewessorial Date | DATE | 7 |  | Y |

## `C_EXPY_ERR_LOG`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ITEM_SHIP_PROF_CODE` | Item_Ship_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `ERR_LOG_DATE` | Err_Logessorial Date | DATE | 7 |  | N |
| 10 | `ERR_LOG_VIEW_FLAG` | Err_Log_Viewessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ERR_SEQ_NUM` | Err_Seqessorial Num | NUMBER | 22 | 10 | N |
| 12 | `ERR_SEQ_LINE_NUM` | Err_Seq_Lineessorial Num | NUMBER | 22 | 9 | N |
| 13 | `ERR_LOG_LINE_TEXT` | Err_Log_Lineessorial Text | VARCHAR2 | 160 |  | Y |
| 14 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 15 | `ERR_LOG_VIEW_DATE` | Err_Log_Viewessorial Date | DATE | 7 |  | Y |

## `C_INTFACE_ATTEND`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 18

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INTFACE_ATTEND_DATE` | Intface_Attendessorial Date | DATE | 7 |  | N |
| 3 | `OP_EXT_REF_NUM1` | Op_Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 4 | `INTFACE_ATTEND_START_DATE` | Intface_Attend_Startessorial Date | DATE | 7 |  | Y |
| 5 | `INTFACE_ATTEND_END_DATE` | Intface_Attend_Endessorial Date | DATE | 7 |  | Y |
| 6 | `WHSE_SHIFT_EXT_REF_NUM1` | Warehouse Shift Ext Ref Num | VARCHAR2 | 100 |  | Y |
| 7 | `ATTEND_SHIFT_START_FLAG` | Attend_Shift_Startessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ATTEND_SHIFT_END_FLAG` | Attend_Shift_Endessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `INTFACE_ATTEND_FILE_NAME` | Intface_Attend_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 10 | `INTFACE_ATTEND_CREATE_DATE` | Intface_Attend_Createessorial Date | DATE | 7 |  | N |
| 11 | `INTFACE_ATTEND_PROS_FLAG` | Intface_Attend_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `INTFACE_ATTEND_PROS_DATE` | Intface_Attend_Prosessorial Date | DATE | 7 |  | Y |
| 13 | `INTFACE_ATTEND_ERR_TEXT` | Intface_Attend_Erressorial Text | VARCHAR2 | 1500 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INTFACE_EXCEL_COL`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 58

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_SEQ_NUM` | Act_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EXCEL_LINE_NUM` | Excel_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `INTFACE_DATE` | Intfaceessorial Date | DATE | 7 |  | Y |
| 4 | `INTFACE_TP_CODE` | Intface_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 5 | `INTFACE_ROUTINE` | Intfaceessorial Routine | VARCHAR2 | 30 |  | Y |
| 6 | `COL_A` | Colessorial A | VARCHAR2 | 80 |  | Y |
| 7 | `COL_B` | Colessorial B | VARCHAR2 | 80 |  | Y |
| 8 | `COL_C` | Colessorial C | VARCHAR2 | 80 |  | Y |
| 9 | `COL_D` | Colessorial D | VARCHAR2 | 80 |  | Y |
| 10 | `COL_E` | Colessorial E | VARCHAR2 | 80 |  | Y |
| 11 | `COL_F` | Colessorial F | VARCHAR2 | 80 |  | Y |
| 12 | `COL_G` | Colessorial G | VARCHAR2 | 80 |  | Y |
| 13 | `COL_H` | Colessorial H | VARCHAR2 | 80 |  | Y |
| 14 | `COL_I` | Colessorial I | VARCHAR2 | 80 |  | Y |
| 15 | `COL_J` | Colessorial J | VARCHAR2 | 80 |  | Y |
| 16 | `COL_K` | Colessorial K | VARCHAR2 | 80 |  | Y |
| 17 | `COL_L` | Colessorial L | VARCHAR2 | 80 |  | Y |
| 18 | `COL_M` | Colessorial M | VARCHAR2 | 80 |  | Y |
| 19 | `COL_N` | Colessorial N | VARCHAR2 | 80 |  | Y |
| 20 | `COL_O` | Colessorial O | VARCHAR2 | 80 |  | Y |
| 21 | `COL_P` | Colessorial P | VARCHAR2 | 80 |  | Y |
| 22 | `COL_Q` | Colessorial Q | VARCHAR2 | 80 |  | Y |
| 23 | `COL_R` | Colessorial R | VARCHAR2 | 80 |  | Y |
| 24 | `COL_S` | Colessorial S | VARCHAR2 | 80 |  | Y |
| 25 | `COL_T` | Colessorial T | VARCHAR2 | 80 |  | Y |
| 26 | `COL_U` | Colessorial U | VARCHAR2 | 80 |  | Y |
| 27 | `COL_V` | Colessorial V | VARCHAR2 | 80 |  | Y |
| 28 | `COL_W` | Colessorial W | VARCHAR2 | 80 |  | Y |
| 29 | `COL_X` | Colessorial X | VARCHAR2 | 80 |  | Y |
| 30 | `COL_Y` | Colessorial Y | VARCHAR2 | 80 |  | Y |
| 31 | `COL_Z` | Colessorial Z | VARCHAR2 | 80 |  | Y |
| 32 | `COL_AA` | Colessorial Aa | VARCHAR2 | 80 |  | Y |
| 33 | `COL_AB` | Colessorial Ab | VARCHAR2 | 80 |  | Y |
| 34 | `COL_AC` | Colessorial Ac | VARCHAR2 | 80 |  | Y |
| 35 | `COL_AD` | Colessorial Ad | VARCHAR2 | 80 |  | Y |
| 36 | `COL_AE` | Colessorial Ae | VARCHAR2 | 80 |  | Y |
| 37 | `COL_AF` | Colessorial Af | VARCHAR2 | 80 |  | Y |
| 38 | `COL_AG` | Colessorial Ag | VARCHAR2 | 80 |  | Y |
| 39 | `COL_AH` | Colessorial Ah | VARCHAR2 | 80 |  | Y |
| 40 | `COL_AI` | Colessorial Ai | VARCHAR2 | 80 |  | Y |
| 41 | `COL_AJ` | Colessorial Aj | VARCHAR2 | 80 |  | Y |
| 42 | `COL_AK` | Colessorial Ak | VARCHAR2 | 80 |  | Y |
| 43 | `COL_AL` | Colessorial Al | VARCHAR2 | 80 |  | Y |
| 44 | `COL_AM` | Colessorial Am | VARCHAR2 | 80 |  | Y |
| 45 | `COL_AN` | Colessorial An | VARCHAR2 | 80 |  | Y |
| 46 | `COL_AO` | Colessorial Ao | VARCHAR2 | 80 |  | Y |
| 47 | `COL_AP` | Colessorial Ap | VARCHAR2 | 80 |  | Y |
| 48 | `COL_AQ` | Colessorial Aq | VARCHAR2 | 80 |  | Y |
| 49 | `COL_AR` | Colessorial Ar | VARCHAR2 | 80 |  | Y |
| 50 | `COL_AS` | Colessorial As | VARCHAR2 | 80 |  | Y |
| 51 | `COL_AT` | Colessorial At | VARCHAR2 | 80 |  | Y |
| 52 | `COL_AU` | Colessorial Au | VARCHAR2 | 80 |  | Y |
| 53 | `COL_AV` | Colessorial Av | VARCHAR2 | 80 |  | Y |
| 54 | `COL_AW` | Colessorial Aw | VARCHAR2 | 80 |  | Y |
| 55 | `COL_AX` | Colessorial Ax | VARCHAR2 | 80 |  | Y |
| 56 | `COL_AY` | Colessorial Ay | VARCHAR2 | 80 |  | Y |
| 57 | `COL_AZ` | Colessorial Az | VARCHAR2 | 80 |  | Y |
| 58 | `COL_LONG_TEXT` | Col_Longessorial Text | VARCHAR2 | 2000 |  | Y |

## `C_INTFACE_EXCEL_LINE`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_SEQ_NUM` | Act_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EXCEL_LINE_NUM` | Excel_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `EXCEL_LINE_TEXT` | Excel_Lineessorial Text | VARCHAR2 | 2000 |  | Y |
| 4 | `INTFACE_EXCEL_LINE_FILE_NAME` | Intface_Excel_Line_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |

## `C_TAB_AUD`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 14

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TAB_ID_REF` | Tab_Idessorial Ref | RAW | 32 |  | N |
| 3 | `TAB_AUD_TP_CODE` | Tab_Aud_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 5 | `COL_NAME` | Column Name | VARCHAR2 | 40 |  | N |
| 6 | `COL_VALUE_OLD` | Col_Valueessorial Old | VARCHAR2 | 2000 |  | Y |
| 7 | `COL_VALUE_NEW` | Col_Valueessorial New | VARCHAR2 | 2000 |  | Y |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `TAB_AUD_DATE` | Tab_Audessorial Date | DATE | 7 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_TRSPT_UNIT_D1`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `INB_OUTB_FLAG` | Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 6 | `POW_UNIT_TRSPT_EQP_OWN_CODE` | Pow_Unit_Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `POW_UNIT_TRSPT_UNIT_ID` | Pow_Unit_Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 8 | `SEAL_NUM1` | Sealessorial Num1 | VARCHAR2 | 20 |  | Y |
| 9 | `SEAL_NUM2` | Sealessorial Num2 | VARCHAR2 | 20 |  | Y |
| 10 | `SEAL_NUM3` | Sealessorial Num3 | VARCHAR2 | 20 |  | Y |
| 11 | `SEAL_NUM1_ENTRY` | Seal_Num1essorial Entry | VARCHAR2 | 20 |  | Y |
| 12 | `SEAL_NUM2_ENTRY` | Seal_Num2essorial Entry | VARCHAR2 | 20 |  | Y |
| 13 | `SEAL_NUM3_ENTRY` | Seal_Num3essorial Entry | VARCHAR2 | 20 |  | Y |
| 14 | `SEAL_NUM1_INTACT_FLAG` | Seal_Num1_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `SEAL_NUM2_INTACT_FLAG` | Seal_Num2_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `SEAL_NUM3_INTACT_FLAG` | Seal_Num3_Intactessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_TRSPT_UNIT_D2`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 2 | N |
| 5 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 6 | `LOAD_INB_OUTB_TP` | Load_Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |

## `C_TRSPT_UNIT_D3`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 5 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |

## `C_TRSPT_UNIT_D4`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `FLOW_DATE` | Flow Date | DATE | 7 |  | N |
| 5 | `FLOW_CODE` | Flowessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `FLOW_CODE_TP_FLAG` | Flow_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | N |
| 8 | `FLOW_INFO_DATE` | Flow_Infoessorial Date | DATE | 7 |  | Y |
| 9 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 10 | `SPOOL_FILE_NAME` | Spool_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 11 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `C_TRSPT_UNIT_D5`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `FINAL_DEST_CODE` | Final_Destessorial Code | VARCHAR2 | 10 |  | N |

## `C_TRSPT_UNIT_D6`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 8 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 9 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 10 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `TRSPT_DOC_PRT_STAT` | Trspt_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 12 | `TRSPT_DOC_REPRT_CNT` | Trspt_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |

## `C_TRSPT_UNIT_H`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `TRSPT_UNIT_STAT` | Trspt_Unitessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `TRSPT_UNIT_ACTN_FLAG` | Trspt_Unit_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TRSPT_TP` | Trsptessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `TRSPT_EQP_TP_CODE` | Trspt_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 11 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 12 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | Y |
| 13 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | Y |
| 14 | `YARD_LOC_BLK_FLAG` | Yarehouse Loc Blk Flag | VARCHAR2 | 1 |  | Y |
| 15 | `YARD_LOC_VERT_LEV` | Yarehouse Loc Vert Lev | NUMBER | 22 | 2 | Y |
| 16 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 17 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 18 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 19 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 20 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `TRSPT_UNIT_REF_NUM1` | Trspt_Unit_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 22 | `TRSPT_UNIT_REF_NUM2` | Trspt_Unit_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 23 | `TRSPT_UNIT_EDI_CREATE_FLAG` | Trspt_Unit_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |

## `C_TRSPT_UNIT_UNLOAD`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 5 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 6 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |

## `C_UPDOWNSTREAM_CLNT_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |

## `C_UPDOWNSTREAM_CLNT_TRANS_D`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `LINE_NUM` | Lineessorial Num | NUMBER | 22 | 6 | N |
| 3 | `TEXT` | Textessorial Text | VARCHAR2 | 250 |  | Y |

## `C_UPDOWNSTREAM_CLNT_TRANS_H`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 5 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 7 | `INTFACE_SEQ_NUM_FA` | Intface_Seq_Numessorial Fa | NUMBER | 22 | 9 | Y |
| 8 | `SEND_ID` | Sendessorial Id | VARCHAR2 | 20 |  | Y |
| 9 | `RECV_ID` | Recvessorial Id | VARCHAR2 | 20 |  | Y |
| 10 | `ERR_NUM` | Erressorial Num | NUMBER | 22 | 6 | Y |
| 11 | `ERR_TEXT` | Error Text | VARCHAR2 | 2000 |  | Y |

## `C_UPDOWNSTREAM_ERR`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |
| 4 | `ERR_DATE` | Error Code | DATE | 7 |  | N |
| 5 | `ERR_NUM` | Erressorial Num | NUMBER | 22 | 6 | Y |
| 6 | `ERR_TEXT` | Error Text | VARCHAR2 | 2000 |  | Y |

## `C_UPDOWNSTREAM_SRVR_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |

## `C_UPDOWNSTREAM_SRVR_TRANS_D`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `LINE_NUM` | Lineessorial Num | NUMBER | 22 | 6 | N |
| 3 | `TEXT` | Textessorial Text | VARCHAR2 | 250 |  | Y |

## `C_UPDOWNSTREAM_SRVR_TRANS_H`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 5 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 7 | `INTFACE_SEQ_NUM_CLNT` | Intface_Seq_Numessorial Clnt | NUMBER | 22 | 9 | Y |
| 8 | `ACT_SEQ_NUM` | Act_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 9 | `ERR_NUM` | Erressorial Num | NUMBER | 22 | 6 | Y |
| 10 | `ERR_TEXT` | Error Text | VARCHAR2 | 2000 |  | Y |
| 11 | `SEND_ID` | Sendessorial Id | VARCHAR2 | 20 |  | Y |
| 12 | `RECV_ID` | Recvessorial Id | VARCHAR2 | 20 |  | Y |

## `DANA`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |

## `DANA_C_LAST_PUT_LOC`

- **Tipo:** Misc
- **Categoria:** Misc
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

## `DANA_M_LABEL_ML`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 6 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | Y |
| 7 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |

## `DANA_S_LABEL_ML`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | N |
| 6 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |
| 7 | `LABEL_ID` | Labelessorial Id | NUMBER | 22 | 4 | Y |

## `DEPT`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DEPTNO` | Deptnoessorial Deptno | NUMBER | 22 | 2 | N |
| 2 | `DNAME` | Dnameessorial Dname | VARCHAR2 | 14 |  | Y |
| 3 | `LOC` | Locessorial Loc | VARCHAR2 | 13 |  | Y |

## `E_EXE_JOB_LOG`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DATE_TIME` | Dateessorial Time | DATE | 7 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `LOG_ACTION` | Logessorial Action | VARCHAR2 | 80 |  | N |
| 8 | `LOG_MESSAGE` | Logessorial Message | VARCHAR2 | 80 |  | Y |

## `E_WO_D1`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | N |
| 2 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `REM_LINE_ROOT_FLAG` | Rem_Line_Rootessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `REM_LINE_CONN_NUM` | Rem_Line_Connessorial Num | NUMBER | 22 | 3 | N |
| 6 | `REM_LINE_TEXT` | Rem_Lineessorial Text | VARCHAR2 | 60 |  | Y |

## `E_WO_D2`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 6 | N |
| 3 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `QUOTE_DATE` | Quoteessorial Date | DATE | 7 |  | N |
| 6 | `CHG_FLAG` | Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `EST_TIME` | Estessorial Time | NUMBER | 22 | 9 | N |
| 8 | `EST_VALUE` | Estessorial Value | NUMBER | 22 | 10 | N |
| 9 | `CHG_TIME` | Chgessorial Time | NUMBER | 22 | 9 | N |
| 10 | `CHG_VALUE` | Chgessorial Value | NUMBER | 22 | 10 | N |
| 11 | `REM_FLAG` | Remessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 10 | N |

## `E_WO_D2D`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `E_WO_D2D_SEQ` | E_Wo_D2Dessorial Seq | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 6 | N |
| 4 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 6 | `WORK_GRP_CODE` | Warehouse Grp Code | VARCHAR2 | 4 |  | N |
| 7 | `CHG_TIME` | Chgessorial Time | NUMBER | 22 | 9 | N |
| 8 | `CHG_CODE` | Charge Code | VARCHAR2 | 4 |  | N |
| 9 | `CHG_SKU_CODE` | Chg_Skuessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 9 | N |
| 11 | `CHG_VALUE` | Chgessorial Value | NUMBER | 22 | 10 | N |
| 12 | `EST_TIME` | Estessorial Time | NUMBER | 22 | 9 | N |
| 13 | `EST_CODE` | Estessorial Code | VARCHAR2 | 4 |  | N |
| 14 | `EST_SKU_CODE` | Est_Skuessorial Code | VARCHAR2 | 4 |  | N |
| 15 | `EST_RATE` | Estessorial Rate | NUMBER | 22 | 9 | Y |
| 16 | `EST_VALUE` | Estessorial Value | NUMBER | 22 | 10 | N |
| 17 | `WO_D1_SQ` | Warehouse D Sq | NUMBER | 22 | 10 | N |
| 18 | `REM_FLAG` | Remessorial Flag | VARCHAR2 | 1 |  | N |

## `E_WO_D3`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 6 | N |
| 3 | `ENTER_DATE` | Enteressorial Date | DATE | 7 |  | Y |
| 4 | `BILL_TO_DATE` | Bill_Toessorial Date | DATE | 7 |  | Y |
| 5 | `FLOW_PROS_SEQ_NUM` | Flow_Pros_Seqessorial Num | NUMBER | 22 | 3 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_DAY_MODY` | Info_Flow_Dayessorial Mody | NUMBER | 22 | 3 | N |
| 8 | `THRSHOLD_TIME_PCENT` | Thrshold_Timeessorial Pcent | NUMBER | 22 | 5 | Y |
| 9 | `BILL_AMT` | Billessorial Amt | NUMBER | 22 | 10 | Y |
| 10 | `BILL_PCENT` | Billessorial Pcent | NUMBER | 22 | 5 | Y |
| 11 | `T_AND_M_FLAG` | T_And_Messorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `CONF_DATE` | Confessorial Date | DATE | 7 |  | Y |
| 13 | `BILL_DATE` | Billessorial Date | DATE | 7 |  | Y |
| 14 | `INVOICE_DATE` | Invoiceessorial Date | DATE | 7 |  | Y |
| 15 | `PROG_BILL_STAT` | Prog_Billessorial Stat | VARCHAR2 | 1 |  | N |

## `E_WO_D5`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WO_D5_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 6 | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `TRANS_START_DATE` | Trans_Startessorial Date | DATE | 7 |  | N |
| 6 | `TRANS_END_DATE` | Trans_Endessorial Date | DATE | 7 |  | Y |
| 7 | `LINE_TP_CODE` | Line_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `LINE_TP_TRANS_TP` | Line_Tp_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | Y |
| 11 | `ENTRY_DATE` | Entryessorial Date | DATE | 7 |  | N |

## `E_WO_D5D1`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WO_D5_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | N |
| 2 | `WO_D5_D5D1_SEQ` | Warehouse D D Seq | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TRAN_TIME` | Tranessorial Time | NUMBER | 22 | 9 | Y |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 4 |  | Y |
| 6 | `CHG_SKU_CODE` | Chg_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 5 | N |
| 8 | `CHG_VALUE` | Chgessorial Value | NUMBER | 22 | 10 | Y |
| 9 | `CHG_FLAG` | Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `COST_CODE` | Costessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `COST_SKU_CODE` | Cost_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `COST_RATE` | Costessorial Rate | NUMBER | 22 | 5 | N |
| 13 | `COST_VALUE` | Costessorial Value | NUMBER | 22 | 10 | Y |
| 14 | `COST_FLAG` | Costessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `TRNSF_DATE` | Trnsfessorial Date | DATE | 7 |  | Y |
| 16 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | Y |

## `E_WO_D5D2`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WO_D5_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | N |
| 2 | `WO_D5_D5D2_SEQ` | Warehouse D D Seq | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TRANS_QTY` | Transessorial Qty | NUMBER | 22 | 9 | Y |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 4 |  | Y |
| 6 | `CHG_SKU_CODE` | Chg_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CHG_RATE` | Charge Rate | NUMBER | 22 | 5 | N |
| 8 | `CHG_VALUE` | Chgessorial Value | NUMBER | 22 | 10 | Y |
| 9 | `CHG_FLAG` | Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `COST_CODE` | Costessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `COST_SKU_CODE` | Cost_Skuessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `COST_RATE` | Costessorial Rate | NUMBER | 22 | 5 | N |
| 13 | `COST_VALUE` | Costessorial Value | NUMBER | 22 | 10 | Y |
| 14 | `COST_FLAG` | Costessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `TRNSF_DATE` | Trnsfessorial Date | DATE | 7 |  | Y |
| 16 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | Y |

## `E_WO_D6`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 10 | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 8 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 9 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `WO_DOC_PRT_STAT` | Warehouse Doc Prt Stat | VARCHAR2 | 1 |  | Y |
| 11 | `WO_DOC_REPRT_CNT` | Warehouse Doc Reprt Cnt | NUMBER | 22 | 4 | Y |

## `E_WO_H`

- **Tipo:** Transactional
- **Categoria:** Misc
- **Campos:** 52
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_NUM` | Warehouse Num | NUMBER | 22 | 6 | N |
| 3 | `WO_PREX` | Warehouse Prex | VARCHAR2 | 4 |  | N |
| 4 | `WO_SUFX` | Warehouse Sufx | VARCHAR2 | 4 |  | Y |
| 5 | `WO_DES` | Warehouse Des | VARCHAR2 | 30 |  | N |
| 6 | `WO_STAT` | Warehouse Stat | VARCHAR2 | 1 |  | N |
| 7 | `WO_TP_CODE` | Warehouse Tp Code | VARCHAR2 | 4 |  | N |
| 8 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `CUST_CODE_SITE` | Cust_Codeessorial Site | VARCHAR2 | 10 |  | N |
| 11 | `WO_ENTRY_DATE` | Warehouse Entry Date | DATE | 7 |  | N |
| 12 | `WO_EXPY1_DATE` | Warehouse Expy Date | DATE | 7 |  | Y |
| 13 | `WO_EXPY2_DATE` | Warehouse Expy Date | DATE | 7 |  | N |
| 14 | `WO_REQ_BY` | Warehouse Req By | VARCHAR2 | 30 |  | N |
| 15 | `WO_REQ_BY_TEL_NUM` | Warehouse Req By Tel Num | VARCHAR2 | 10 |  | Y |
| 16 | `WO_REQ_BY_TEL_NUM_EXT` | Warehouse Req By Tel Num Ext | VARCHAR2 | 10 |  | Y |
| 17 | `WO_REQ_DATE` | Warehouse Req Date | DATE | 7 |  | N |
| 18 | `WO_PRTY_NUM` | Warehouse Prty Num | NUMBER | 22 | 1 | N |
| 19 | `WO_CONTACT` | Warehouse Contact | VARCHAR2 | 30 |  | N |
| 20 | `WO_CONTACT_TEL_NUM` | Warehouse Contact Tel Num | VARCHAR2 | 10 |  | Y |
| 21 | `WO_CONTACT_TEL_NUM_EXT` | Warehouse Contact Tel Num Ext | VARCHAR2 | 10 |  | Y |
| 22 | `WO_INT_RESP_OP_CODE` | Warehouse Int Resp Op Code | VARCHAR2 | 4 |  | N |
| 23 | `WO_REF_1` | Warehouse Ref 1 | VARCHAR2 | 30 |  | Y |
| 24 | `WO_REF_2` | Warehouse Ref 2 | VARCHAR2 | 30 |  | Y |
| 25 | `WO_REF_3` | Warehouse Ref 3 | VARCHAR2 | 30 |  | Y |
| 26 | `WO_REF_4` | Warehouse Ref 4 | VARCHAR2 | 30 |  | Y |
| 27 | `WO_REF_5` | Warehouse Ref 5 | VARCHAR2 | 30 |  | Y |
| 28 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 29 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 30 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 31 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 32 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 33 | `WO_D1_SEQ` | Warehouse D Seq | NUMBER | 22 | 9 | Y |
| 34 | `WO_CHG_TIME` | Warehouse Chg Time | NUMBER | 22 | 9 | Y |
| 35 | `WO_CHG_VALUE` | Warehouse Chg Value | NUMBER | 22 | 10 | N |
| 36 | `WO_BILL_VALUE` | Warehouse Bill Value | NUMBER | 22 | 10 | N |
| 37 | `WO_BILL_TIME` | Warehouse Bill Time | NUMBER | 22 | 9 | Y |
| 38 | `WO_EST_TIME` | Warehouse Est Time | NUMBER | 22 | 9 | Y |
| 39 | `WO_EST_VALUE` | Warehouse Est Value | NUMBER | 22 | 10 | N |
| 40 | `WO_COST_FLAG` | Warehouse Cost Flag | VARCHAR2 | 1 |  | Y |
| 41 | `PROG_BILL_PROF_CODE` | Prog_Bill_Professorial Code | VARCHAR2 | 4 |  | Y |
| 42 | `WO_NUM_MASTER` | Warehouse Num Master | NUMBER | 22 | 6 | Y |
| 43 | `FLOW_PROS_CODE_APPR` | Flow_Pros_Codeessorial Appr | VARCHAR2 | 4 |  | Y |
| 44 | `WO_APPR_DATE` | Warehouse Appr Date | DATE | 7 |  | N |
| 45 | `FLOW_PROS_CODE_CLOSE` | Flow_Pros_Codeessorial Close | VARCHAR2 | 4 |  | Y |
| 46 | `WO_CLOSE_DATE` | Warehouse Close Date | DATE | 7 |  | N |
| 47 | `WO_T_AND_M_FLAG` | Warehouse T And M Flag | VARCHAR2 | 1 |  | N |
| 48 | `WO_PCENT_COMPL_TIME_ALERT` | Warehouse Pcent Compl Time Alert | NUMBER | 22 | 3 | Y |
| 49 | `WO_ON_LINE_ALERT_TIME_FLAG` | Warehouse On Line Alert Time Flag | VARCHAR2 | 1 |  | N |
| 50 | `WO_PCENT_COMPL_VALUE_ALERT` | Warehouse Pcent Compl Value Alert | NUMBER | 22 | 3 | Y |
| 51 | `WO_ON_LINE_ALERT_VALUE_FLAG` | Warehouse On Line Alert Value Flag | VARCHAR2 | 1 |  | N |
| 52 | `WO_CONSISTENT_FLAG` | Warehouse Consistent Flag | VARCHAR2 | 1 |  | N |

## `H_ACCSS_D1`

- **Tipo:** Historical
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 7 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 8 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 9 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 10 | `ACCSS_QTY` | Access Quantity | NUMBER | 22 | 9 | N |
| 11 | `ACCSS_RATE` | Access Rate | NUMBER | 22 | 9 | N |
| 12 | `ACCSS_AMT` | Accssessorial Amt | NUMBER | 22 | 10 | N |

## `H_ACCSS_D2`

- **Tipo:** Historical
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `ACCSS_REM_NUM` | Accss_Remessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ACCSS_REM_TEXT` | Accss_Remessorial Text | VARCHAR2 | 45 |  | Y |

## `H_ACCSS_H`

- **Tipo:** Historical
- **Categoria:** Misc
- **Campos:** 85
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 4 | `ACCSS_STAT` | Accssessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ACCSS_DATE` | Access Date | DATE | 7 |  | N |
| 7 | `ACCSS_REM_FLAG` | Accss_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `BAT_NUM_ACCSS` | Bat_Numessorial Accss | NUMBER | 22 | 9 | N |
| 10 | `BAT_NUM_RENW` | Bat_Numessorial Renw | NUMBER | 22 | 9 | N |
| 11 | `ACCSS_SRCE_REF_FLAG` | Accss_Srce_Refessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `ACCSS_SRCE_REF_CHG_TP_FLAG` | Accss_Srce_Ref_Chg_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `ACCSS_SRCE_REF_NUM` | Accss_Srce_Refessorial Num | NUMBER | 22 | 9 | N |
| 14 | `ACCSS_SRCE_REF_LINE_NUM` | Accss_Srce_Ref_Lineessorial Num | NUMBER | 22 | 4 | N |
| 15 | `ACCSS_SRCE_REF_CONF_FLAG` | Accss_Srce_Ref_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CHG_SEQ_NUM` | Chg_Seqessorial Num | NUMBER | 22 | 2 | N |
| 17 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 18 | `CHG_DATE` | Charge Date | DATE | 7 |  | N |
| 19 | `CHG_TP_CODE` | Chg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 20 | `INV_TP_CODE` | Inv_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 21 | `CHG_PRT_FLAG` | Chg_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `GL_ACC_CODE` | Gl_Accessorial Code | VARCHAR2 | 12 |  | N |
| 23 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 24 | `SKU_CODE_QUAL` | Sku_Codeessorial Qual | VARCHAR2 | 4 |  | N |
| 25 | `QUAL_QTY` | Qualessorial Qty | NUMBER | 22 | 16 | N |
| 26 | `SKU_CODE_CHG` | Sku_Codeessorial Chg | VARCHAR2 | 4 |  | N |
| 27 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 28 | `CHG_FLAT_RATE_FLAG` | Chg_Flat_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `CHG_RATE_ORG` | Chg_Rateessorial Org | NUMBER | 22 | 15 | N |
| 30 | `CHG_RATE_CRNT` | Chg_Rateessorial Crnt | NUMBER | 22 | 15 | N |
| 31 | `CHG_TOT` | Charge Total | NUMBER | 22 | 16 | N |
| 32 | `CHG_MIN_FLAG` | Chg_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `CHG_MAX_FLAG` | Chg_Maxessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `ACCSS_AUDIT_FLAG` | Accss_Auditessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `GL_MODY_SUB_MODY` | Gl_Mody_Subessorial Mody | VARCHAR2 | 10 |  | Y |
| 36 | `ACCSS_REF_DES` | Accss_Refessorial Des | VARCHAR2 | 40 |  | Y |
| 37 | `ACCSS_REF_NUM` | Accss_Refessorial Num | VARCHAR2 | 40 |  | Y |
| 38 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | Y |
| 39 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | Y |
| 40 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 41 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 42 | `CHG_TAX1` | Chgessorial Tax1 | NUMBER | 22 | 13 | Y |
| 43 | `CHG_TAX2` | Chgessorial Tax2 | NUMBER | 22 | 13 | Y |
| 44 | `CUST_CODE_INVT` | Cust_Codeessorial Invt | VARCHAR2 | 10 |  | Y |
| 45 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 46 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 47 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 48 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 49 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 50 | `RENW_DATE_CRNT` | Renw_Dateessorial Crnt | DATE | 7 |  | Y |
| 51 | `RENW_DATE_NXT` | Renw_Dateessorial Nxt | DATE | 7 |  | Y |
| 52 | `ENT_QTY` | Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 53 | `QTY` | Qtyessorial Qty | NUMBER | 22 | 9 | Y |
| 54 | `CNVC_QTY` | Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 55 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 56 | `WGT` | Wgtessorial Wgt | NUMBER | 22 | 16 | Y |
| 57 | `WGT_NET` | Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 58 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 59 | `CUBE` | Cubeessorial Cube | NUMBER | 22 | 16 | Y |
| 60 | `OP_CODE_AUDIT` | Op_Codeessorial Audit | VARCHAR2 | 20 |  | Y |
| 61 | `ACCSS_AUDIT_DATE` | Accss_Auditessorial Date | DATE | 7 |  | Y |
| 62 | `ACCSS_AUDIT_PRT_CNT` | Accss_Audit_Prtessorial Cnt | NUMBER | 22 | 2 | Y |
| 63 | `COMP_CODE_ROLLUP` | Comp_Codeessorial Rollup | VARCHAR2 | 2 |  | Y |
| 64 | `INV_NUM_ROLLUP` | Inv_Numessorial Rollup | NUMBER | 22 | 9 | Y |
| 65 | `INV_PREX_ROLLUP` | Inv_Prexessorial Rollup | VARCHAR2 | 4 |  | Y |
| 66 | `INV_SUFX_ROLLUP` | Inv_Sufxessorial Rollup | VARCHAR2 | 4 |  | Y |
| 67 | `BAT_NUM_ACCSS_ROLLUP` | Bat_Num_Accssessorial Rollup | NUMBER | 22 | 9 | Y |
| 68 | `BAT_NUM_RENW_ROLLUP` | Bat_Num_Renwessorial Rollup | NUMBER | 22 | 9 | Y |
| 69 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 70 | `BAT_NUM_EXCH` | Bat_Numessorial Exch | NUMBER | 22 | 9 | Y |
| 71 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 72 | `ACCSS_AUDIT_NUM` | Accss_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 73 | `SURCHG_INCL_FLAG` | Surchg_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 74 | `CRT_FLAG` | Crtessorial Flag | VARCHAR2 | 1 |  | Y |
| 75 | `REPROS_DLRE_FLAG` | Repros_Dlreessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `NUM_OF_FREE_DAYS` | Num_Of_Freeessorial Days | NUMBER | 22 | 4 | Y |
| 77 | `CHG_TOT_CUR_BASE` | Chg_Tot_Curessorial Base | NUMBER | 22 | 16 | Y |
| 78 | `CHG_TOT_CUR` | Chg_Totessorial Cur | NUMBER | 22 | 20 | Y |
| 79 | `BAT_NUM_INV_MIN` | Bat_Num_Invessorial Min | NUMBER | 22 | 9 | Y |
| 80 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 81 | `DEPT_CODE` | Deptessorial Code | VARCHAR2 | 10 |  | Y |
| 82 | `BAT_NUM_PRO_FORMA` | Bat_Num_Proessorial Forma | NUMBER | 22 | 9 | Y |
| 83 | `BAT_NUM_PRE_RENW` | Bat_Num_Preessorial Renw | NUMBER | 22 | 9 | Y |
| 84 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 85 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | Y |

## `H_ARCH_C_LAB`

- **Tipo:** Historical
- **Categoria:** Misc
- **Campos:** 55
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LAB_DATE` | Labessorial Date | DATE | 7 |  | N |
| 6 | `LAB_TP_FLAG` | Lab_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 8 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 9 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 10 | `LAB_START_DATE` | Lab_Startessorial Date | DATE | 7 |  | Y |
| 11 | `LAB_END_DATE` | Lab_Endessorial Date | DATE | 7 |  | Y |
| 12 | `LAB_SYS_FLAG` | Lab_Sysessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `LAB_DES` | Labessorial Des | VARCHAR2 | 40 |  | Y |
| 14 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `LAB_UNIT` | Labessorial Unit | NUMBER | 22 | 9 | Y |
| 16 | `SESSION_ID` | Sessionessorial Id | VARCHAR2 | 16 |  | Y |
| 17 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 18 | `LAB_UNIQUE_SEQ_NUM` | Lab_Unique_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 19 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 20 | `DOC_LINE_PICK_METH` | Doc_Line_Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 21 | `LAB_GOAL_TIME` | Lab_Goalessorial Time | NUMBER | 22 | 16 | Y |
| 22 | `LAB_DIRECT_TIME` | Lab_Directessorial Time | NUMBER | 22 | 16 | Y |
| 23 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 24 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 25 | `EMP_HOURLY_PAY` | Emp_Hourlyessorial Pay | NUMBER | 22 | 8 | Y |
| 26 | `LAB_INDIRECT_TIME` | Lab_Indirectessorial Time | NUMBER | 22 | 16 | Y |
| 27 | `LAB_IDLE_TIME` | Lab_Idleessorial Time | NUMBER | 22 | 16 | Y |
| 28 | `LAB_ACTUAL_TIME` | Lab_Actualessorial Time | NUMBER | 22 | 16 | Y |
| 29 | `LAB_CUST_TIME` | Lab_Custessorial Time | NUMBER | 22 | 16 | Y |
| 30 | `LAB_ADJACENT_CUST_TIME` | Lab_Adjacent_Custessorial Time | NUMBER | 22 | 16 | Y |
| 31 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 32 | `LAB_ACT_NOT_PROS_FLAG` | Lab_Act_Not_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 34 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 35 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 36 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 37 | `LAB_WGT` | Labessorial Wgt | NUMBER | 22 | 16 | Y |
| 38 | `LAB_WGT_NET` | Lab_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 39 | `LAB_CUBE` | Labessorial Cube | NUMBER | 22 | 12 | Y |
| 40 | `LAB_LOC_FROM_ENTER_DATE` | Lab_Loc_From_Enteressorial Date | DATE | 7 |  | Y |
| 41 | `LAB_UI_ENTER_DATE` | Lab_Ui_Enteressorial Date | DATE | 7 |  | Y |
| 42 | `LAB_QTY_ENTER_DATE` | Lab_Qty_Enteressorial Date | DATE | 7 |  | Y |
| 43 | `LAB_PICK_SHORT_QTY` | Lab_Pick_Shortessorial Qty | NUMBER | 22 | 9 | Y |
| 44 | `LAB_PICK_AVAIL_QTY_LOC_FROM` | Lab_Pick_Avail_Qty_Locessorial From | NUMBER | 22 | 9 | Y |
| 45 | `LAB_ENTITY_CNT_LOC_FROM` | Lab_Entity_Cnt_Locessorial From | NUMBER | 22 | 9 | Y |
| 46 | `LAB_ENTITY_CNT_LOC_TO` | Lab_Entity_Cnt_Locessorial To | NUMBER | 22 | 9 | Y |
| 47 | `LAB_PICK_RESIDUAL_QTY` | Lab_Pick_Residualessorial Qty | NUMBER | 22 | 9 | Y |
| 48 | `LAB_PICK_QTY_HANDL_MANUAL` | Lab_Pick_Qty_Handlessorial Manual | NUMBER | 22 | 9 | Y |
| 49 | `MHE_MOVE_GRP_SEQ_NUM` | Mhe_Move_Grp_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 50 | `LAB_EXT_SWARE_ASS_ID` | Lab_Ext_Sware_Assessorial Id | VARCHAR2 | 100 |  | Y |
| 51 | `LAB_EXT_SWARE_GOAL_TIME` | Lab_Ext_Sware_Goalessorial Time | NUMBER | 22 | 9 | Y |
| 52 | `LAB_AUDIT_NUM` | Lab_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 53 | `LAB_AUDIT_DATE` | Lab_Auditessorial Date | DATE | 7 |  | Y |
| 54 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 55 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |

## `H_ARCH_C_LAB_TIME`

- **Tipo:** Historical
- **Categoria:** Misc
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LAB_TIME_SEQ_NUM` | Lab_Time_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `LAB_UNIQUE_SEQ_NUM` | Lab_Unique_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `LAB_TIME_DATE` | Lab_Timeessorial Date | DATE | 7 |  | N |
| 5 | `LAB_TIME_TP_CODE` | Lab_Time_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | Y |
| 8 | `LAB_TIME_PROS_FLAG` | Lab_Time_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 10 | `LAB_TIME_NEXT_STAMP` | Lab_Time_Nextessorial Stamp | NUMBER | 22 | 16 | Y |
| 11 | `LAB_TIME_DIRECT_TIME` | Lab_Time_Directessorial Time | NUMBER | 22 | 16 | Y |
| 12 | `LAB_TIME_INDIRECT_TIME` | Lab_Time_Indirectessorial Time | NUMBER | 22 | 16 | Y |
| 13 | `LAB_TIME_IDLE_TIME` | Lab_Time_Idleessorial Time | NUMBER | 22 | 16 | Y |
| 14 | `LAB_TIME_CUST_TIME` | Lab_Time_Custessorial Time | NUMBER | 22 | 16 | Y |
| 15 | `LAB_TIME_ADJACENT_CUST_TIME` | Lab_Time_Adjacent_Custessorial Time | NUMBER | 22 | 16 | Y |

## `JAVA$OPTIONS`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WHAT` | Whatessorial What | VARCHAR2 | 128 |  | Y |
| 2 | `OPT` | Optessorial Opt | VARCHAR2 | 20 |  | Y |
| 3 | `VALUE` | Valueessorial Value | VARCHAR2 | 128 |  | Y |

## `LISTEX`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ENAME` | Enameessorial Ename | VARCHAR2 | 10 |  | Y |
| 2 | `MARITAL_STATUS` | Maritalessorial Status | VARCHAR2 | 1 |  | Y |

## `L_ADILOG_GRID`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `ADILOG_GRID_TP` | Adilog_Gridessorial Tp | VARCHAR2 | 1 |  | N |
| 4 | `ADILOG_GRID_LINE_NUM` | Adilog_Grid_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ADILOG_GRID_LINE_TP` | Adilog_Grid_Lineessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `ADILOG_GRID_BASE_LINE_NUM` | Adilog_Grid_Base_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `ADILOG_GRID_LINE_QTY` | Adilog_Grid_Lineessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `ITEM_STYLE` | Itemessorial Style | VARCHAR2 | 20 |  | N |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV1_COL1` | Invt_Lev1essorial Col1 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV3_COL1` | Invt_Lev3essorial Col1 | VARCHAR2 | 40 |  | Y |
| 13 | `QTY_COL1` | Qtyessorial Col1 | NUMBER | 22 | 9 | Y |
| 14 | `INVT_LEV1_COL2` | Invt_Lev1essorial Col2 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV3_COL2` | Invt_Lev3essorial Col2 | VARCHAR2 | 40 |  | Y |
| 16 | `QTY_COL2` | Qtyessorial Col2 | NUMBER | 22 | 9 | Y |
| 17 | `INVT_LEV1_COL3` | Invt_Lev1essorial Col3 | VARCHAR2 | 40 |  | Y |
| 18 | `INVT_LEV3_COL3` | Invt_Lev3essorial Col3 | VARCHAR2 | 40 |  | Y |
| 19 | `QTY_COL3` | Qtyessorial Col3 | NUMBER | 22 | 9 | Y |
| 20 | `INVT_LEV1_COL4` | Invt_Lev1essorial Col4 | VARCHAR2 | 40 |  | Y |
| 21 | `INVT_LEV3_COL4` | Invt_Lev3essorial Col4 | VARCHAR2 | 40 |  | Y |
| 22 | `QTY_COL4` | Qtyessorial Col4 | NUMBER | 22 | 9 | Y |
| 23 | `INVT_LEV1_COL5` | Invt_Lev1essorial Col5 | VARCHAR2 | 40 |  | Y |
| 24 | `INVT_LEV3_COL5` | Invt_Lev3essorial Col5 | VARCHAR2 | 40 |  | Y |
| 25 | `QTY_COL5` | Qtyessorial Col5 | NUMBER | 22 | 9 | Y |
| 26 | `INVT_LEV1_COL6` | Invt_Lev1essorial Col6 | VARCHAR2 | 40 |  | Y |
| 27 | `INVT_LEV3_COL6` | Invt_Lev3essorial Col6 | VARCHAR2 | 40 |  | Y |
| 28 | `QTY_COL6` | Qtyessorial Col6 | NUMBER | 22 | 9 | Y |
| 29 | `INVT_LEV1_COL7` | Invt_Lev1essorial Col7 | VARCHAR2 | 40 |  | Y |
| 30 | `INVT_LEV3_COL7` | Invt_Lev3essorial Col7 | VARCHAR2 | 40 |  | Y |
| 31 | `QTY_COL7` | Qtyessorial Col7 | NUMBER | 22 | 9 | Y |
| 32 | `INVT_LEV1_COL8` | Invt_Lev1essorial Col8 | VARCHAR2 | 40 |  | Y |
| 33 | `INVT_LEV3_COL8` | Invt_Lev3essorial Col8 | VARCHAR2 | 40 |  | Y |
| 34 | `QTY_COL8` | Qtyessorial Col8 | NUMBER | 22 | 9 | Y |

## `L_ALPAR_ASN_D1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `ALPAR_PO_NUM` | Alpar_Poessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 7 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | Y |
| 8 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `L_ALPAR_ASN_D2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 30
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `ASN_RCPT_EXPT_QTY` | Asn_Rcpt_Exptessorial Qty | NUMBER | 22 | 9 | N |
| 7 | `RCPT_QTY` | Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `ASN_TICK_PRICE` | Asn_Tickessorial Price | NUMBER | 22 | 8 | N |
| 9 | `GUIA_TICK_PRICE` | Guia_Tickessorial Price | NUMBER | 22 | 8 | N |
| 10 | `FINAL_TICK_PRICE` | Final_Tickessorial Price | NUMBER | 22 | 8 | N |
| 11 | `ASN_PRICE_CHG_FLAG` | Asn_Price_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `GUIA_PRICE_CHG_FLAG` | Guia_Price_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `FINAL_PRICE_CHG_FLAG` | Final_Price_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `ASN_CART_QTY` | Asn_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 15 | `GUIA_CART_QTY` | Guia_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 16 | `FINAL_CART_QTY` | Final_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 17 | `TALLY_BAL_FLAG` | Tally_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `SGL_TALLY_FLAG` | Sgl_Tallyessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `GUIA_RCPT_EXPT_QTY` | Guia_Rcpt_Exptessorial Qty | NUMBER | 22 | 9 | N |
| 20 | `TALLY_FLAG` | Tallyessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `ASN_KIT_FLAG` | Asn_Kitessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 23 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `ASN_PRT_TICK_FLAG` | Asn_Prt_Tickessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `GUIA_PRT_TICK_FLAG` | Guia_Prt_Tickessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `FINAL_PRT_TICK_FLAG` | Final_Prt_Tickessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 28 | `ASN_HTP_CODE` | Asn_Htpessorial Code | VARCHAR2 | 1 |  | N |
| 29 | `GUIA_HTP_CODE` | Guia_Htpessorial Code | VARCHAR2 | 1 |  | N |
| 30 | `KIT_INVT_LEV1` | Kit_Invtessorial Lev1 | VARCHAR2 | 40 |  | Y |

## `L_ALPAR_ASN_D2D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | N |
| 7 | `TALLY_SEQ_NUM_CNT` | Tally_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 8 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `RCPT_QTY` | Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `PUTA_FLAG` | Putaessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `PUT_PROF_PICKL_FLAG` | Put_Prof_Picklessorial Flag | VARCHAR2 | 1 |  | Y |

## `L_ALPAR_ASN_D3`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `GUIA_NUM` | Guiaessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `GUIA_TOT_QTY` | Guia_Totessorial Qty | NUMBER | 22 | 9 | N |
| 6 | `GUIA_TP_CODE` | Guia_Tpessorial Code | VARCHAR2 | 1 |  | N |

## `L_ALPAR_ASN_D4`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | N |
| 5 | `TALLY_SEQ_NUM_CNT` | Tally_Seq_Numessorial Cnt | NUMBER | 22 | 4 | N |
| 6 | `TALLY_PRT_CNT` | Tally_Prtessorial Cnt | NUMBER | 22 | 4 | N |
| 7 | `TALLY_REL_FLAG` | Tally_Relessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 9 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 11 | `ITEM_CODE` | Item Code | VARCHAR2 | 40 |  | N |
| 12 | `NUM_OF_CART` | Num_Ofessorial Cart | NUMBER | 22 | 6 | N |
| 13 | `TALLY_COMPL_FLAG` | Tally_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `ASN_TALLY_TICK_PRT_FLAG` | Asn_Tally_Tick_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `ASN_TALLY_REM_TEXT` | Asn_Tally_Remessorial Text | VARCHAR2 | 45 |  | Y |
| 16 | `ASN_TALLY_START_DATE` | Asn_Tally_Startessorial Date | DATE | 7 |  | Y |
| 17 | `ASN_TALLY_END_DATE` | Asn_Tally_Endessorial Date | DATE | 7 |  | Y |
| 18 | `OP_CODE_FINAL` | Op_Codeessorial Final | VARCHAR2 | 20 |  | Y |
| 19 | `TALLY_QTY` | Tallyessorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `TALLY_CREATE_DATE` | Tally_Createessorial Date | DATE | 7 |  | N |
| 21 | `RCPT_CREATE_DATE` | Rcpt_Createessorial Date | DATE | 7 |  | Y |

## `L_ALPAR_ASN_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 4 | `ASN_RCPT_DATE` | Asn_Rcptessorial Date | DATE | 7 |  | N |
| 5 | `ASN_DELV_DATE` | Asn_Delvessorial Date | DATE | 7 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `ASN_RECD_FLAG` | Asn_Recdessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `GUIA_COMPL_FLAG` | Guia_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ASN_COMPL_FLAG` | Asn_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `ASN_CONSL_FLAG` | Asn_Conslessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `ASN_CART_QTY` | Asn_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 12 | `GUIA_CART_QTY` | Guia_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 13 | `FINAL_CART_QTY` | Final_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 14 | `ASN_TRAIN_CNT` | Asn_Trainessorial Cnt | NUMBER | 22 | 4 | N |
| 15 | `OP_CODE_ENTRY` | Op_Codeessorial Entry | VARCHAR2 | 20 |  | N |
| 16 | `ASN_COMPL_DATE` | Asn_Complessorial Date | DATE | 7 |  | Y |
| 17 | `ASN_AUDIT_SEQ_NUM` | Asn_Audit_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 18 | `RF_RECV_FLAG` | Rf_Recvessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ALPAR_ASN_LOCK`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 8 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `L_ALPAR_ASN_TALLY_PROS`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, RCPT_NUM, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ASN_SEQ_NUM` | Asn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `TER_CODE_ORG` | Ter_Codeessorial Org | VARCHAR2 | 10 |  | N |
| 8 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 9 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 10 | `ALPAR_ASN_TALLY_PROS_MODE` | Alpar_Asn_Tally_Prosessorial Mode | VARCHAR2 | 4 |  | Y |
| 11 | `ALPAR_ASN_TALLY_CREATE_DATE` | Alpar_Asn_Tally_Createessorial Date | DATE | 7 |  | N |
| 12 | `ALPAR_ASN_TALLY_PROS_FLAG` | Alpar_Asn_Tally_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `ALPAR_ASN_TALLY_PROS_DATE` | Alpar_Asn_Tally_Prosessorial Date | DATE | 7 |  | Y |
| 14 | `ALPAR_ASN_TALLY_ERR_CODE` | Alpar_Asn_Tally_Erressorial Code | VARCHAR2 | 6 |  | Y |
| 15 | `ALPAR_ASN_TALLY_ERR_TEXT1` | Alpar_Asn_Tally_Erressorial Text1 | VARCHAR2 | 250 |  | Y |
| 16 | `ALPAR_ASN_TALLY_ERR_TEXT2` | Alpar_Asn_Tally_Erressorial Text2 | VARCHAR2 | 250 |  | Y |

## `L_ALPAR_CUTTING_ROOM_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 5 | `ITEM_CODE_ENTRY` | Item_Codeessorial Entry | VARCHAR2 | 20 |  | N |
| 6 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 7 | `CHECK_FLAG` | Checkessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `L_ALPAR_CUTTING_ROOM_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_CODE_ENTRY` | Item_Codeessorial Entry | VARCHAR2 | 20 |  | N |
| 5 | `AVAIL_QTY` | Availessorial Qty | NUMBER | 22 | 9 | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `L_ALPAR_LOAD_INVT`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALPAR_LOAD_INVT_SEQ_NUM` | Alpar_Load_Invt_Seqessorial Num | NUMBER | 22 | 12 | N |
| 2 | `ALPAR_LOAD_INVT_DEP_NUM` | Alpar_Load_Invt_Depessorial Num | NUMBER | 22 | 3 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `ALPAR_LOAD_INVT_QTY` | Alpar_Load_Invtessorial Qty | NUMBER | 22 | 9 | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | Y |
| 11 | `LOAD_INVT_ENTRY_DATE` | Load_Invt_Entryessorial Date | DATE | 7 |  | N |
| 12 | `LOAD_INVT_PROS_FLAG` | Load_Invt_Prosessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ALPAR_RES_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ALPAR_RES_QTY` | Alpar_Resessorial Qty | NUMBER | 22 | 9 | N |
| 6 | `ALPAR_RES_QTY_ORG` | Alpar_Res_Qtyessorial Org | NUMBER | 22 | 9 | Y |

## `L_ALPAR_RES_DD1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 7 | `ALPAR_RES_LOC_QTY` | Alpar_Res_Locessorial Qty | NUMBER | 22 | 9 | N |

## `L_ALPAR_RES_DD2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 7 | `ORD_LINE_QTY` | Ord_Lineessorial Qty | NUMBER | 22 | 9 | N |

## `L_ALPAR_RES_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 4 | `ALPAR_RES_NUM` | Alpar_Resessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `ALPAR_RES_NUM_ORG` | Alpar_Res_Numessorial Org | VARCHAR2 | 20 |  | Y |
| 6 | `ALPAR_RES_CREATE_DATE` | Alpar_Res_Createessorial Date | DATE | 7 |  | N |
| 7 | `ALPAR_RES_CHG_DATE` | Alpar_Res_Chgessorial Date | DATE | 7 |  | Y |
| 8 | `ALPAR_RES_COMPL_FLAG` | Alpar_Res_Complessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ALPAR_TRAIN`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_CODE_STYLE` | Item_Codeessorial Style | VARCHAR2 | 20 |  | N |
| 5 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `NUM_CART_PER_TRAIN` | Num_Cart_Peressorial Train | NUMBER | 22 | 6 | N |
| 7 | `NUM_GOH_PER_TROLLEY` | Num_Goh_Peressorial Trolley | NUMBER | 22 | 6 | N |
| 8 | `NUM_TROLLEY_PER_TRAIN` | Num_Trolley_Peressorial Train | NUMBER | 22 | 6 | N |

## `L_AP_ABC`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | Ap_Custessorial Code | NUMBER | 22 | 3 | N |
| 4 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 5 | `ABC_CODE` | ABC Code | VARCHAR2 | 20 |  | N |
| 6 | `ABC_TOT_REC_CNT` | ABC Total Received  | NUMBER | 22 | 6 | N |
| 7 | `ABC_ENTRY_DATE` | ABC Entry Date | DATE | 7 |  | N |
| 8 | `ABC_PROS_FLAG` | ABC Process Flag | VARCHAR2 | 1 |  | N |
| 9 | `ABC_PROS_DATE` | ABC Process Date | DATE | 7 |  | Y |
| 10 | `ABC_ACT_FLAG` | ABC Activation Flag | VARCHAR2 | 1 |  | N |

## `L_AP_ASN_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | Y |
| 2 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | Y |

## `L_AP_ASN_DD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ASN_QTY` | Asnessorial Qty | NUMBER | 22 | 9 | N |
| 5 | `ASN_CART_QTY` | Asn_Cartessorial Qty | NUMBER | 22 | 6 | Y |

## `L_AP_ASN_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 4 | `ASN_CONSL_FLAG` | Asn_Conslessorial Flag | VARCHAR2 | 2 |  | N |
| 5 | `ASN_CART_QTY` | Asn_Cartessorial Qty | NUMBER | 22 | 6 | N |
| 6 | `ASN_ENTRY_DATE` | Asn_Entryessorial Date | DATE | 7 |  | N |
| 7 | `ASN_PROS_FLAG` | Asn_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ASN_PROS_DATE` | Asn_Prosessorial Date | DATE | 7 |  | Y |

## `L_AP_BARCODE_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `BARCODE_TP` | Barcodeessorial Tp | VARCHAR2 | 4 |  | N |
| 3 | `BARCODE` | Barcodeessorial Barcode | VARCHAR2 | 20 |  | N |
| 4 | `BARCODE_QTY` | Barcodeessorial Qty | NUMBER | 22 | 4 | Y |
| 5 | `BARCODE_VENDOR_CODE` | Barcode_Vendoressorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `BARCODE_VENDOR_ITEM_CODE` | Barcode_Vendor_Itemessorial Code | VARCHAR2 | 20 |  | Y |

## `L_AP_BARCODE_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `JDA_ACTIVE_FLAG` | Jda_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 6 | `BARCODE_TOT_REC_CNT` | Barcode_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `BARCODE_ENTRY_DATE` | Barcode_Entryessorial Date | DATE | 7 |  | N |
| 8 | `BARCODE_PROS_FLAG` | Barcode_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `BARCODE_PROS_DATE` | Barcode_Prosessorial Date | DATE | 7 |  | Y |
| 10 | `BARCODE_ACT_FLAG` | Barcode_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_CART_CONF_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | N |

## `L_AP_CART_CONF_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CART_CONF_TOT_REC_CNT` | Cart_Conf_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 4 | `CART_CONF_ENTRY_DATE` | Cart_Conf_Entryessorial Date | DATE | 7 |  | N |
| 5 | `CART_CONF_PROS_FLAG` | Cart_Conf_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CART_CONF_PROS_DATE` | Cart_Conf_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `CART_CONF_ACT_FLAG` | Cart_Conf_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_CLNT_TRANS_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_CLNT_TRANS_LINE_NUM` | Ap_Clnt_Trans_Lineessorial Num | NUMBER | 22 | 9 | N |
| 3 | `AP_CLNT_TRANS_TEXT` | Ap_Clnt_Transessorial Text | VARCHAR2 | 250 |  | Y |

## `L_AP_CLNT_TRANS_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_MES_CODE` | Ap_Mesessorial Code | VARCHAR2 | 24 |  | N |
| 3 | `AP_CLNT_TRANS_CREATE_DATE` | Ap_Clnt_Trans_Createessorial Date | DATE | 7 |  | N |
| 4 | `AP_CLNT_TRANS_PROS_FLAG` | Ap_Clnt_Trans_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `AP_CLNT_TRANS_PROS_DATE` | Ap_Clnt_Trans_Prosessorial Date | DATE | 7 |  | Y |
| 6 | `AP_CLNT_TRANS_CONF_DATE` | Ap_Clnt_Trans_Confessorial Date | DATE | 7 |  | Y |
| 7 | `SEQ_NUM_CONF` | Seq_Numessorial Conf | NUMBER | 22 | 12 | Y |
| 8 | `AP_MES_CODE_CONF` | Ap_Mes_Codeessorial Conf | VARCHAR2 | 24 |  | Y |
| 9 | `AP_CLNT_CORRL_ID` | Ap_Clnt_Corrlessorial Id | VARCHAR2 | 24 |  | Y |
| 10 | `AP_CLNT_QUEUE_CORRL` | Ap_Clnt_Queueessorial Corrl | VARCHAR2 | 48 |  | Y |
| 11 | `AP_MES_CODE_CORRL` | Ap_Mes_Codeessorial Corrl | VARCHAR2 | 24 |  | Y |
| 12 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 13 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |

## `L_AP_COLOR`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COLOR_CODE` | Coloressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `COLOR_DES` | Coloressorial Des | VARCHAR2 | 40 |  | N |
| 4 | `COLOR_STAT` | Coloressorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `COLOR_SHORT_DES` | Color_Shortessorial Des | VARCHAR2 | 5 |  | Y |
| 6 | `COLOR_TOT_REC_CNT` | Color_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `COLOR_ENTRY_DATE` | Color_Entryessorial Date | DATE | 7 |  | N |
| 8 | `COLOR_PROS_FLAG` | Color_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `COLOR_PROS_DATE` | Color_Prosessorial Date | DATE | 7 |  | Y |
| 10 | `COLOR_ACT_FLAG` | Color_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_ERR`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AP_MES_CODE` | Ap_Mesessorial Code | VARCHAR2 | 24 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 3 | `ERR_DATE` | Error Code | DATE | 7 |  | N |
| 4 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 5 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |

## `L_AP_GDD_HIST`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AP_GDD_HIST_SEQ_NUM` | Ap_Gdd_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `AP_GDD_HIST_NUM_START` | Ap_Gdd_Hist_Numessorial Start | VARCHAR2 | 20 |  | N |
| 3 | `AP_GDD_HIST_NUM_END` | Ap_Gdd_Hist_Numessorial End | VARCHAR2 | 20 |  | N |

## `L_AP_GDD_PRT`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 2 | `AP_GDD_PRT_STAT` | Ap_Gdd_Prtessorial Stat | VARCHAR2 | 1 |  | N |
| 3 | `AP_GDD_PRT_NUM_START` | Ap_Gdd_Prt_Numessorial Start | VARCHAR2 | 20 |  | N |
| 4 | `AP_GDD_PRT_NUM_END` | Ap_Gdd_Prt_Numessorial End | VARCHAR2 | 20 |  | N |
| 5 | `AP_GDD_PRT_NUM_CRNT` | Ap_Gdd_Prt_Numessorial Crnt | VARCHAR2 | 20 |  | N |

## `L_AP_HD_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 3 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 4 | `HD_QTY` | Hdessorial Qty | NUMBER | 22 | 10 | N |
| 5 | `AP_WHSE_CODE_FROM` | Ap_Whse_Codeessorial From | NUMBER | 22 | 4 | N |
| 6 | `AP_WHSE_CODE_VIA` | Ap_Whse_Codeessorial Via | NUMBER | 22 | 4 | Y |

## `L_AP_HD_DEL`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `HD_REF_NUM` | Hd_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `HD_DEL_TOT_REC_CNT` | Hd_Del_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `HD_DEL_ENTRY_DATE` | Hd_Del_Entryessorial Date | DATE | 7 |  | N |
| 7 | `HD_DEL_PROS_FLAG` | Hd_Del_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `HD_DEL_PROS_DATE` | Hd_Del_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `HD_DEL_ACT_FLAG` | Hd_Del_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_HD_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 6 | `HD_REF_NUM` | Hd_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `HD_TO_SHIP_DATE` | Hd_To_Shipessorial Date | DATE | 7 |  | N |
| 8 | `HD_DEL_TIME_STAT` | Hd_Del_Timeessorial Stat | VARCHAR2 | 1 |  | Y |
| 9 | `HD_SECTOR` | Hdessorial Sector | VARCHAR2 | 20 |  | N |
| 10 | `HD_SHIPTO_NAME` | Hd_Shiptoessorial Name | VARCHAR2 | 30 |  | N |
| 11 | `HD_SHIPTO_ADD1` | Hd_Shiptoessorial Add1 | VARCHAR2 | 30 |  | Y |
| 12 | `HD_SHIPTO_ADD2` | Hd_Shiptoessorial Add2 | VARCHAR2 | 30 |  | Y |
| 13 | `HD_SHIPTO_ADD3` | Hd_Shiptoessorial Add3 | VARCHAR2 | 30 |  | Y |
| 14 | `HD_SHIPTO_ADD4` | Hd_Shiptoessorial Add4 | VARCHAR2 | 30 |  | Y |
| 15 | `HD_REMARK` | Hdessorial Remark | VARCHAR2 | 80 |  | Y |
| 16 | `HD_TOT_REC_CNT` | Hd_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 17 | `HD_ENTRY_DATE` | Hd_Entryessorial Date | DATE | 7 |  | N |
| 18 | `HD_PROS_FLAG` | Hd_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `HD_PROS_DATE` | Hd_Prosessorial Date | DATE | 7 |  | Y |
| 20 | `HD_ACT_FLAG` | Hd_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_HD_RCPT_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | Y |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | Y |
| 3 | `HD_RCPT_QTY` | Hd_Rcptessorial Qty | NUMBER | 22 | 12 | Y |

## `L_AP_HD_RCPT_DEL`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `HD_RCPT_REF_NUM` | Hd_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `HD_RCPT_DEL_TOT_REC_CNT` | Hd_Rcpt_Del_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `HD_RCPT_DEL_ENTRY_DATE` | Hd_Rcpt_Del_Entryessorial Date | DATE | 7 |  | N |
| 7 | `HD_RCPT_DEL_PROS_FLAG` | Hd_Rcpt_Del_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `HD_RCPT_DEL_PROS_DATE` | Hd_Rcpt_Del_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `HD_RCPT_DEL_ACT_FLAG` | Hd_Rcpt_Del_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_HD_RCPT_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `HD_RCPT_REF_NUM` | Hd_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `HD_RCPT_RES_FLAG` | Hd_Rcpt_Resessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 8 | `HD_RCPT_SHIP_DATE` | Hd_Rcpt_Shipessorial Date | DATE | 7 |  | N |
| 9 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | Y |
| 10 | `HD_RCPT_TOT_REC_CNT` | Hd_Rcpt_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 11 | `HD_RCPT_ENTRY_DATE` | Hd_Rcpt_Entryessorial Date | DATE | 7 |  | N |
| 12 | `HD_RCPT_PROS_FLAG` | Hd_Rcpt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `HD_RCPT_PROS_DATE` | Hd_Rcpt_Prosessorial Date | DATE | 7 |  | Y |
| 14 | `HD_RCPT_ACT_FLAG` | Hd_Rcpt_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_ITEM`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 45
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `JDA_ACTIVE_FLAG` | Jda_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `STYLE_CODE` | Styleessorial Code | NUMBER | 22 | 9 | N |
| 6 | `STYLE_DES` | Styleessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | Y |
| 8 | `SKU_DES` | Skuessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `SKU_DEP` | Skuessorial Dep | NUMBER | 22 | 3 | N |
| 10 | `SKU_SUB_DEP` | Sku_Subessorial Dep | NUMBER | 22 | 3 | N |
| 11 | `SKU_CLASS` | Skuessorial Class | NUMBER | 22 | 3 | N |
| 12 | `SKU_SUB_CLASS` | Sku_Subessorial Class | NUMBER | 22 | 3 | N |
| 13 | `COLOR_CODE` | Coloressorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `ITEM_REPL_TP` | Item_Replessorial Tp | VARCHAR2 | 1 |  | Y |
| 15 | `SIZE_CODE` | Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `DIM_CODE` | Dimessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `ITEM_UOM` | Itemessorial Uom | VARCHAR2 | 1 |  | Y |
| 18 | `ITEM_PACK_QTY` | Item_Packessorial Qty | NUMBER | 22 | 7 | Y |
| 19 | `ITEM_CASE_QTY` | Item_Caseessorial Qty | NUMBER | 22 | 7 | Y |
| 20 | `ITEM_PLT_QTY` | Item_Pltessorial Qty | NUMBER | 22 | 7 | Y |
| 21 | `ITEM_TIE_VENDOR` | Item_Tieessorial Vendor | NUMBER | 22 | 3 | Y |
| 22 | `ITEM_HIGH_VENDOR` | Item_Highessorial Vendor | NUMBER | 22 | 3 | Y |
| 23 | `ITEM_WGT` | Itemessorial Wgt | NUMBER | 22 | 7 | Y |
| 24 | `ITEM_LEN` | Itemessorial Len | NUMBER | 22 | 5 | Y |
| 25 | `ITEM_WID` | Itemessorial Wid | NUMBER | 22 | 5 | Y |
| 26 | `ITEM_HGT` | Itemessorial Hgt | NUMBER | 22 | 5 | Y |
| 27 | `ITEM_CUBE` | Itemessorial Cube | NUMBER | 22 | 7 | Y |
| 28 | `ITEM_VENDOR_CODE` | Item_Vendoressorial Code | VARCHAR2 | 10 |  | Y |
| 29 | `ITEM_VENDOR_ITEM_CODE` | Item_Vendor_Itemessorial Code | VARCHAR2 | 15 |  | Y |
| 30 | `ITEM_BRAND` | Itemessorial Brand | VARCHAR2 | 30 |  | Y |
| 31 | `ITEM_MODEL` | Itemessorial Model | VARCHAR2 | 30 |  | Y |
| 32 | `ITEM_HANDL_TP` | Item_Handlessorial Tp | VARCHAR2 | 1 |  | Y |
| 33 | `ITEM_COUNTRY_CODE` | Item_Countryessorial Code | VARCHAR2 | 3 |  | Y |
| 34 | `ITEM_BUYER_CODE` | Item_Buyeressorial Code | VARCHAR2 | 10 |  | Y |
| 35 | `ITEM_TICKET_TP` | Item_Ticketessorial Tp | VARCHAR2 | 2 |  | Y |
| 36 | `ITEM_DISC_TICKET_TP` | Item_Disc_Ticketessorial Tp | VARCHAR2 | 2 |  | Y |
| 37 | `ITEM_SECURITY_TAG_TP` | Item_Security_Tagessorial Tp | VARCHAR2 | 1 |  | Y |
| 38 | `ITEM_PRICE_CHGN_FLAG` | Item_Price_Chgnessorial Flag | VARCHAR2 | 1 |  | N |
| 39 | `ITEM_ID_TP` | Item_Idessorial Tp | VARCHAR2 | 1 |  | N |
| 40 | `ITEM_ORIGIN_FLAG` | Item_Originessorial Flag | VARCHAR2 | 1 |  | N |
| 41 | `ITEM_TOT_REC_CNT` | Item_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 42 | `ITEM_ENTRY_DATE` | Item_Entryessorial Date | DATE | 7 |  | N |
| 43 | `ITEM_PROS_FLAG` | Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 44 | `ITEM_PROS_DATE` | Item_Prosessorial Date | DATE | 7 |  | Y |
| 45 | `ITEM_ACT_FLAG` | Item_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_ITEM_CSD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE_MAST` | Item_Codeessorial Mast | VARCHAR2 | 20 |  | N |
| 4 | `AP_ITEM_CSD_NUM_LAST` | Ap_Item_Csd_Numessorial Last | NUMBER | 22 | 3 | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `COLOR_CODE` | Coloressorial Code | VARCHAR2 | 4 |  | N |
| 7 | `SIZE_CODE` | Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `DIM_CODE` | Dimessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `AP_ITEM_CSD_DATE` | Ap_Item_Csdessorial Date | DATE | 7 |  | N |

## `L_AP_ITEM_UPD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |

## `L_AP_LOAD_CTL`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `AP_LOAD_GDD_NUM` | Ap_Load_Gddessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `AP_LOAD_CTL_CART` | Ap_Load_Ctlessorial Cart | NUMBER | 22 | 10 | Y |
| 6 | `AP_LOAD_CTL_GOH` | Ap_Load_Ctlessorial Goh | NUMBER | 22 | 10 | Y |
| 7 | `AP_LOAD_CTL_PROS_DATE` | Ap_Load_Ctl_Prosessorial Date | DATE | 7 |  | N |

## `L_AP_LOAD_GDD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `AP_LOAD_GDD_NUM` | Ap_Load_Gddessorial Num | VARCHAR2 | 20 |  | N |
| 6 | `AP_LOAD_CART_ID_PRT` | Ap_Load_Cart_Idessorial Prt | VARCHAR2 | 20 |  | N |

## `L_AP_LOAD_NUM`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `AP_LOAD_NUM_START` | Ap_Load_Numessorial Start | NUMBER | 22 | 6 | N |
| 3 | `AP_LOAD_NUM_END` | Ap_Load_Numessorial End | NUMBER | 22 | 6 | N |
| 4 | `AP_LOAD_NUM_CRNT` | Ap_Load_Numessorial Crnt | NUMBER | 22 | 6 | N |

## `L_AP_LOAD_PACK`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |

## `L_AP_MAST_ITEM`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `SKU_DEP` | Skuessorial Dep | NUMBER | 22 | 3 | N |
| 5 | `SKU_SUB_DEP` | Sku_Subessorial Dep | NUMBER | 22 | 3 | Y |
| 6 | `SKU_CLASS` | Skuessorial Class | NUMBER | 22 | 3 | N |
| 7 | `SKU_SUB_CLASS` | Sku_Subessorial Class | NUMBER | 22 | 3 | N |
| 8 | `MAST_ITEM_ORIGIN_FLAG` | Mast_Item_Originessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `MAST_ITEM_TOT_REC_CNT` | Mast_Item_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 10 | `MAST_ITEM_ENTRY_DATE` | Mast_Item_Entryessorial Date | DATE | 7 |  | N |
| 11 | `MAST_ITEM_PROS_FLAG` | Mast_Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `MAST_ITEM_PROS_DATE` | Mast_Item_Prosessorial Date | DATE | 7 |  | Y |
| 13 | `MAST_ITEM_ACT_FLAG` | Mast_Item_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_MERGE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `MERGE_STYLE_CODE_FROM` | Merge_Style_Codeessorial From | NUMBER | 22 | 9 | Y |
| 5 | `MERGE_SKU_NUM_FROM` | Merge_Sku_Numessorial From | NUMBER | 22 | 9 | Y |
| 6 | `MERGE_STYLE_CODE_TO` | Merge_Style_Codeessorial To | NUMBER | 22 | 9 | Y |
| 7 | `MERGE_SKU_NUM_TO` | Merge_Sku_Numessorial To | NUMBER | 22 | 9 | Y |
| 8 | `MERGE_TOT_REC_CNT` | Merge_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 9 | `MERGE_ENTRY_DATE` | Merge_Entryessorial Date | DATE | 7 |  | N |
| 10 | `MERGE_PROS_FLAG` | Merge_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `MERGE_PROS_DATE` | Merge_Prosessorial Date | DATE | 7 |  | Y |
| 12 | `MERGE_ACT_FLAG` | Merge_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_MES`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 22

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AP_QUEUE_CODE` | Ap_Queueessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `AP_MES_CODE` | Ap_Mesessorial Code | VARCHAR2 | 24 |  | N |
| 3 | `AP_MES_DES` | Ap_Mesessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `AP_MES_STAT` | Ap_Mesessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `AP_MES_ACT_FLAG` | Ap_Mes_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `AP_MES_HIST_FLAG` | Ap_Mes_Histessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `AP_MES_INB_OUTB_FLAG` | Ap_Mes_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `AP_MES_PRTY_NUM` | Ap_Mes_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 9 | `AP_MES_DIR` | Ap_Mesessorial Dir | VARCHAR2 | 60 |  | Y |
| 10 | `AP_MES_ARCHIVE_DIR` | Ap_Mes_Archiveessorial Dir | VARCHAR2 | 60 |  | Y |
| 11 | `AP_MES_ERR_DIR` | Ap_Mes_Erressorial Dir | VARCHAR2 | 60 |  | Y |
| 12 | `AP_MES_FILE_PREX` | Ap_Mes_Fileessorial Prex | VARCHAR2 | 30 |  | Y |
| 13 | `AP_MES_FILE_SUFX` | Ap_Mes_Fileessorial Sufx | VARCHAR2 | 30 |  | Y |
| 14 | `AP_MES_FILE_LOCK_SUFX` | Ap_Mes_File_Lockessorial Sufx | VARCHAR2 | 30 |  | Y |
| 15 | `AP_MES_NUM_TRY` | Ap_Mes_Numessorial Try | NUMBER | 22 | 3 | Y |
| 16 | `AP_MES_FRQ_TIME` | Ap_Mes_Frqessorial Time | NUMBER | 22 | 6 | Y |
| 17 | `AP_MES_TIMEOUT` | Ap_Mesessorial Timeout | NUMBER | 22 | 6 | Y |
| 18 | `AP_MES_CONF_EXPY_TIME` | Ap_Mes_Conf_Expyessorial Time | NUMBER | 22 | 6 | Y |
| 19 | `AP_MES_REPLY_EXPY_TIME` | Ap_Mes_Reply_Expyessorial Time | NUMBER | 22 | 6 | Y |
| 20 | `AP_MES_CODE_REPLY_MES_CODE` | Ap_Mes_Code_Reply_Mesessorial Code | VARCHAR2 | 24 |  | Y |
| 21 | `AP_MES_EXE_JOB` | Ap_Mes_Exeessorial Job | VARCHAR2 | 60 |  | Y |
| 22 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | Y |

## `L_AP_MOD_RES`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RES_REF_NUM_ORIG` | Res_Ref_Numessorial Orig | VARCHAR2 | 20 |  | Y |
| 5 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 6 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | N |
| 7 | `MOD_RES_TOT_REC_CNT` | Mod_Res_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 8 | `MOD_RES_ENTRY_DATE` | Mod_Res_Entryessorial Date | DATE | 7 |  | N |
| 9 | `MOD_RES_PROS_FLAG` | Mod_Res_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `MOD_RES_PROS_DATE` | Mod_Res_Prosessorial Date | DATE | 7 |  | Y |
| 11 | `MOD_RES_ACT_FLAG` | Mod_Res_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_MOD_RES_QTY_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 3 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 4 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |
| 5 | `MOD_RES_QTY_QTY` | Mod_Res_Qtyessorial Qty | NUMBER | 22 | 10 | N |

## `L_AP_MOD_RES_QTY_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | N |
| 6 | `MOD_RES_QTY_TOT_REC_CNT` | Mod_Res_Qty_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `MOD_RES_QTY_ENTRY_DATE` | Mod_Res_Qty_Entryessorial Date | DATE | 7 |  | N |
| 8 | `MOD_RES_QTY_PROS_FLAG` | Mod_Res_Qty_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `MOD_RES_QTY_PROS_DATE` | Mod_Res_Qty_Prosessorial Date | DATE | 7 |  | Y |
| 10 | `MOD_RES_QTY_ACT_FLAG` | Mod_Res_Qty_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_ORD_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 3 | `ORD_QTY` | Ordessorial Qty | NUMBER | 22 | 12 | N |
| 4 | `SKU_COST_UNIT` | Sku_Costessorial Unit | NUMBER | 22 | 10 | Y |

## `L_AP_ORD_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `JDA_ACTIVE_FLAG` | Jda_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `ORD_TRANS_TP` | Ord_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `ORD_TRANS_REF_NUM` | Ord_Trans_Refessorial Num | VARCHAR2 | 20 |  | N |
| 7 | `ORD_TRANS_PRTY_NUM` | Ord_Trans_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 8 | `ORD_TRANS_DELV_DATE` | Ord_Trans_Delvessorial Date | DATE | 7 |  | N |
| 9 | `AP_CON_CODE` | Ap_Conessorial Code | NUMBER | 22 | 6 | N |
| 10 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_TOT_REC_CNT` | Ord_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 13 | `ORD_ENTRY_DATE` | Ord_Entryessorial Date | DATE | 7 |  | N |
| 14 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 16 | `ORD_ACT_FLAG` | Ord_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `VENDOR_NAME` | Vendoressorial Name | VARCHAR2 | 30 |  | Y |
| 18 | `VENDOR_ADD1` | Vendoressorial Add1 | VARCHAR2 | 30 |  | Y |
| 19 | `VENDOR_ADD2` | Vendoressorial Add2 | VARCHAR2 | 30 |  | Y |
| 20 | `VENDOR_ADD3` | Vendoressorial Add3 | VARCHAR2 | 30 |  | Y |
| 21 | `VENDOR_CITY` | Vendoressorial City | VARCHAR2 | 30 |  | Y |
| 22 | `VENDOR_STATE` | Vendoressorial State | VARCHAR2 | 4 |  | Y |
| 23 | `VENDOR_ZIP` | Vendoressorial Zip | VARCHAR2 | 10 |  | Y |
| 24 | `VENDOR_COUNTRY` | Vendoressorial Country | VARCHAR2 | 4 |  | Y |
| 25 | `VENDOR_RUT` | Vendoressorial Rut | VARCHAR2 | 10 |  | Y |

## `L_AP_POD_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 3 | `POD_QTY` | Podessorial Qty | NUMBER | 22 | 12 | N |
| 4 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | Y |

## `L_AP_POD_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `DELV_DATE` | Delvessorial Date | DATE | 7 |  | N |
| 6 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 6 | N |
| 7 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |
| 8 | `POD_TOT_C_REC_CNT` | Pod_Tot_C_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 9 | `POD_TOT_D_REC_CNT` | Pod_Tot_D_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 10 | `POD_TOT_REC_CNT` | Pod_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 11 | `POD_ENTRY_DATE` | Pod_Entryessorial Date | DATE | 7 |  | N |
| 12 | `POD_PROS_FLAG` | Pod_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `POD_PROS_DATE` | Pod_Prosessorial Date | DATE | 7 |  | Y |
| 14 | `POD_ACT_FLAG` | Pod_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_POS_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SKU_QTY` | Skuessorial Qty | NUMBER | 22 | 12 | N |
| 4 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |

## `L_AP_POS_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `POS_CRNT_DATE` | Pos_Crntessorial Date | DATE | 7 |  | N |
| 5 | `POS_TOT_REC_CNT` | Pos_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `POS_ENTRY_DATE` | Pos_Entryessorial Date | DATE | 7 |  | N |
| 7 | `POS_PROS_FLAG` | Pos_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `POS_PROS_DATE` | Pos_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `POS_ACT_FLAG` | Pos_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_POS_H_COPY`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `POS_CRNT_DATE` | Pos_Crntessorial Date | DATE | 7 |  | N |
| 5 | `POS_TOT_REC_CNT` | Pos_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `POS_ENTRY_DATE` | Pos_Entryessorial Date | DATE | 7 |  | N |
| 7 | `POS_PROS_FLAG` | Pos_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `POS_PROS_DATE` | Pos_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `POS_ACT_FLAG` | Pos_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_POS_STORE_SKU`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 3 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |
| 4 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 5 | `POS_STORE_SKU_SALE_DATE` | Pos_Store_Sku_Saleessorial Date | DATE | 7 |  | N |
| 6 | `POS_QTY` | Posessorial Qty | NUMBER | 22 | 12 | N |

## `L_AP_PO_D1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `PO_TEXT_LINE_NUM` | Po_Text_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `PO_REM_LINE_TEXT` | Po_Rem_Lineessorial Text | VARCHAR2 | 50 |  | Y |

## `L_AP_PO_D2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 6 | N |
| 3 | `STYLE_SKU_NUM` | Style_Skuessorial Num | NUMBER | 22 | 9 | N |
| 4 | `PO_LINE_QTY` | Po_Lineessorial Qty | NUMBER | 22 | 12 | N |
| 5 | `PO_UNIT_PRICE` | Po_Unitessorial Price | NUMBER | 22 | 10 | Y |
| 6 | `PO_DISC_PRICE` | Po_Discessorial Price | NUMBER | 22 | 10 | Y |
| 7 | `PO_TLR_OVER` | Po_Tlressorial Over | NUMBER | 22 | 12 | Y |
| 8 | `PO_TLR_OVER_TP_FLAG` | Po_Tlr_Over_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `PO_TLR_SHORT` | Po_Tlressorial Short | NUMBER | 22 | 12 | Y |
| 10 | `PO_TLR_SHORT_TP_FLAG` | Po_Tlr_Short_Tpessorial Flag | VARCHAR2 | 1 |  | Y |

## `L_AP_PO_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `JDA_ACTIVE_FLAG` | Jda_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | N |
| 6 | `VENDOR_NUM` | Vendoressorial Num | NUMBER | 22 | 6 | N |
| 7 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 6 | Y |
| 8 | `PO_DATE` | Poessorial Date | DATE | 7 |  | Y |
| 9 | `PO_TOT_QTY` | Po_Totessorial Qty | NUMBER | 22 | 10 | Y |
| 10 | `PO_DIST_TP` | Po_Distessorial Tp | VARCHAR2 | 4 |  | Y |
| 11 | `PO_IMP_FLAG` | Po_Impessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `PO_DATE_START` | Po_Dateessorial Start | DATE | 7 |  | N |
| 13 | `PO_DATE_END` | Po_Dateessorial End | DATE | 7 |  | N |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 15 | `PO_TOT_R_REC_CNT` | Po_Tot_R_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 16 | `PO_TOT_D_REC_CNT` | Po_Tot_D_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 17 | `PO_TOT_REC_CNT` | Po_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 18 | `PO_ENTRY_DATE` | Po_Entryessorial Date | DATE | 7 |  | N |
| 19 | `PO_PROS_FLAG` | Po_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `PO_PROS_DATE` | Po_Prosessorial Date | DATE | 7 |  | Y |
| 21 | `PO_ACT_FLAG` | Po_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |

## `L_AP_PRICE_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |
| 3 | `PRICE_RETAIL` | Priceessorial Retail | NUMBER | 22 | 10 | N |

## `L_AP_PRICE_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `STYLE_CODE` | Styleessorial Code | NUMBER | 22 | 9 | Y |
| 5 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | Y |
| 6 | `PRICE_RETAIL` | Priceessorial Retail | NUMBER | 22 | 10 | N |
| 7 | `PRICE_DISC` | Priceessorial Disc | NUMBER | 22 | 10 | Y |
| 8 | `PRICE_COST` | Priceessorial Cost | NUMBER | 22 | 10 | N |
| 9 | `PRICE_TOT_REC_CNT` | Price_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 10 | `PRICE_ENTRY_DATE` | Price_Entryessorial Date | DATE | 7 |  | N |
| 11 | `PRICE_PROS_FLAG` | Price_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `PRICE_PROS_DATE` | Price_Prosessorial Date | DATE | 7 |  | Y |
| 13 | `PRICE_ACT_FLAG` | Price_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_QUERY_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |

## `L_AP_QUERY_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `JDA_ACTIVE_FLAG` | Jda_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `QUERY_REF_NUM` | Query_Refessorial Num | VARCHAR2 | 20 |  | N |
| 6 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | Y |
| 7 | `QUERY_HOLD_INCL_FLAG` | Query_Hold_Inclessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `QUERY_TOT_REC_CNT` | Query_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 9 | `QUERY_ENTRY_DATE` | Query_Entryessorial Date | DATE | 7 |  | N |
| 10 | `QUERY_PROS_FLAG` | Query_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `QUERY_PROS_DATE` | Query_Prosessorial Date | DATE | 7 |  | Y |
| 12 | `QUERY_ACT_FLAG` | Query_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_QUERY_RES`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 5 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 6 | `QUERY_RES_TOT_REC_CNT` | Query_Res_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `QUERY_RES_ENTRY_DATE` | Query_Res_Entryessorial Date | DATE | 7 |  | N |
| 8 | `QUERY_RES_PROS_FLAG` | Query_Res_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `QUERY_RES_PROS_DATE` | Query_Res_Prosessorial Date | DATE | 7 |  | Y |
| 10 | `QUERY_RES_ACT_FLAG` | Query_Res_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_QUEUE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AP_QUEUE_CODE` | Ap_Queueessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `AP_QUEUE_DES` | Ap_Queueessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `AP_QUEUE_STAT` | Ap_Queueessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `AP_QUEUE_TP_CODE` | Ap_Queue_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `AP_QUEUE_PRTY_NUM` | Ap_Queue_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 6 | `AP_QUEUE_FRQ_TIME` | Ap_Queue_Frqessorial Time | NUMBER | 22 | 6 | N |
| 7 | `AP_QUEUE_NUM_TRY` | Ap_Queue_Numessorial Try | NUMBER | 22 | 3 | N |
| 8 | `AP_QUEUE_TIMEOUT` | Ap_Queueessorial Timeout | NUMBER | 22 | 6 | Y |
| 9 | `AP_QUEUE_CONF_EXPY_TIME` | Ap_Queue_Conf_Expyessorial Time | NUMBER | 22 | 6 | Y |
| 10 | `AP_QUEUE_REPLY_EXPY_TIME` | Ap_Queue_Reply_Expyessorial Time | NUMBER | 22 | 6 | Y |

## `L_AP_QUEUE_TP`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AP_QUEUE_TP_CODE` | Ap_Queue_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `AP_QUEUE_TP_DES` | Ap_Queue_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `AP_QUEUE_TP_STAT` | Ap_Queue_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `AP_QUEUE_TP_CONF_FLAG` | Ap_Queue_Tp_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `AP_QUEUE_TP_REPLY_FLAG` | Ap_Queue_Tp_Replyessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `AP_QUEUE_TP_FILE_FLAG` | Ap_Queue_Tp_Fileessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_RCPT_CART_D1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `GDD_NUM` | Gddessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | N |

## `L_AP_RCPT_CART_D2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `GDD_NUM` | Gddessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `CART_ID` | Cart ID | VARCHAR2 | 20 |  | N |
| 4 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 5 | `RCPT_CART_QTY` | Rcpt_Cartessorial Qty | NUMBER | 22 | 10 | N |

## `L_AP_RCPT_CART_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RCPT_CART_REF_NUM` | Rcpt_Cart_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `RCPT_CART_DATE` | Rcpt_Cartessorial Date | DATE | 7 |  | N |
| 6 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 8 | `CARR_NAME_MAN` | Carr_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 9 | `CARR_TRUCK_NUM` | Carr_Truckessorial Num | VARCHAR2 | 20 |  | Y |
| 10 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 20 |  | Y |
| 11 | `OP_NAME` | Opessorial Name | VARCHAR2 | 30 |  | Y |
| 12 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |
| 13 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 14 | `RCPT_CART_TOT_C_REC_CNT` | Rcpt_Cart_Tot_C_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 15 | `RCPT_CART_TOT_D_REC_CNT` | Rcpt_Cart_Tot_D_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 16 | `RCPT_CART_TOT_REC_CNT` | Rcpt_Cart_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 17 | `RCPT_CART_ENTRY_DATE` | Rcpt_Cart_Entryessorial Date | DATE | 7 |  | N |
| 18 | `RCPT_CART_PROS_FLAG` | Rcpt_Cart_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `RCPT_CART_PROS_DATE` | Rcpt_Cart_Prosessorial Date | DATE | 7 |  | Y |
| 20 | `RCPT_CART_ACT_FLAG` | Rcpt_Cart_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_RCPT_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | Y |
| 2 | `GDD_NUM` | Gddessorial Num | VARCHAR2 | 20 |  | Y |
| 3 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `RCPT_QTY` | Rcptessorial Qty | NUMBER | 22 | 10 | Y |

## `L_AP_RCPT_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |
| 6 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 8 | `CARR_NAME_MAN` | Carr_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 9 | `CARR_TRUCK_NUM` | Carr_Truckessorial Num | VARCHAR2 | 20 |  | Y |
| 10 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 20 |  | Y |
| 11 | `OP_NAME` | Opessorial Name | VARCHAR2 | 30 |  | Y |
| 12 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |
| 13 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 14 | `RCPT_TOT_REC_CNT` | Rcpt_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 15 | `RCPT_ENTRY_DATE` | Rcpt_Entryessorial Date | DATE | 7 |  | N |
| 16 | `RCPT_PROS_FLAG` | Rcpt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `RCPT_PROS_DATE` | Rcpt_Prosessorial Date | DATE | 7 |  | Y |
| 18 | `RCPT_ACT_FLAG` | Rcpt_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_RES_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 3 | `RES_QTY` | Resessorial Qty | NUMBER | 22 | 10 | N |
| 4 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 5 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |

## `L_AP_RES_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `RES_REF_NUM` | Res_Refessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `RES_HOLD_INCL_FLAG` | Res_Hold_Inclessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `RES_CUT_ROOM_FLAG` | Res_Cut_Roomessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 8 | `RES_TOT_REC_CNT` | Res_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 9 | `RES_ENTRY_DATE` | Res_Entryessorial Date | DATE | 7 |  | N |
| 10 | `RES_PROS_FLAG` | Res_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `RES_PROS_DATE` | Res_Prosessorial Date | DATE | 7 |  | Y |
| 12 | `RES_ACT_FLAG` | Res_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_RES_LOCK`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 3 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 4 | `AP_WHSE_CODE` | Ap_Whseessorial Code | NUMBER | 22 | 4 | N |

## `L_AP_SET_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SET_SKU_NUM_COMPN` | Set_Sku_Numessorial Compn | NUMBER | 22 | 9 | N |
| 3 | `SET_SKU_NUM_COMPN_QTY` | Set_Sku_Num_Compnessorial Qty | NUMBER | 22 | 6 | N |

## `L_AP_SET_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `SET_SKU_NUM` | Set_Skuessorial Num | NUMBER | 22 | 9 | Y |
| 5 | `SET_TOT_REC_CNT` | Set_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `SET_ENTRY_DATE` | Set_Entryessorial Date | DATE | 7 |  | N |
| 7 | `SET_PROS_FLAG` | Set_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `SET_PROS_DATE` | Set_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `SET_ACT_FLAG` | Set_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_SIZE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SIZE_CODE` | Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SIZE_DES` | Sizeessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `SIZE_STAT` | Sizeessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `SIZE_SHORT_DES` | Size_Shortessorial Des | VARCHAR2 | 5 |  | Y |
| 6 | `SIZE_TOT_REC_CNT` | Size_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `SIZE_ENTRY_DATE` | Size_Entryessorial Date | DATE | 7 |  | N |
| 8 | `SIZE_PROS_FLAG` | Size_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `SIZE_PROS_DATE` | Size_Prosessorial Date | DATE | 7 |  | Y |
| 10 | `SIZE_ACT_FLAG` | Size_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_SKU_CSD_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `AP_SKU_CSD_TOT_QTY` | Ap_Sku_Csd_Totessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_SKU_CSD_DD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | N |
| 4 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 5 | `COLOR_CODE` | Coloressorial Code | VARCHAR2 | 4 |  | N |
| 6 | `SIZE_CODE` | Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `DIM_CODE` | Dimessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `AP_SKU_CSD_QTY` | Ap_Sku_Csdessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_SKU_CSD_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `PO_REF_NUM` | Po_Refessorial Num | VARCHAR2 | 20 |  | N |
| 4 | `AP_PO_TP` | Ap_Poessorial Tp | VARCHAR2 | 1 |  | N |

## `L_AP_SRVR_TRANS_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_SRVR_TRANS_LINE_NUM` | Ap_Srvr_Trans_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `AP_SRVR_TRANS_TEXT` | Ap_Srvr_Transessorial Text | VARCHAR2 | 250 |  | Y |

## `L_AP_SRVR_TRANS_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `AP_MES_CODE` | Ap_Mesessorial Code | VARCHAR2 | 24 |  | N |
| 3 | `AP_SRVR_TRANS_CREATE_DATE` | Ap_Srvr_Trans_Createessorial Date | DATE | 7 |  | N |
| 4 | `AP_SRVR_CORRL_ID` | Ap_Srvr_Corrlessorial Id | VARCHAR2 | 24 |  | Y |
| 5 | `AP_SRVR_QUEUE_CORRL` | Ap_Srvr_Queueessorial Corrl | VARCHAR2 | 48 |  | Y |
| 6 | `AP_SRVR_TRANS_PROS_FLAG` | Ap_Srvr_Trans_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `AP_SRVR_TRANS_PROS_DATE` | Ap_Srvr_Trans_Prosessorial Date | DATE | 7 |  | Y |
| 8 | `AP_SRVR_TRANS_FULL_FILE_NAME` | Ap_Srvr_Trans_Full_Fileessorial Name | VARCHAR2 | 130 |  | Y |
| 9 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 10 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |

## `L_AP_STORE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | VARCHAR2 | 3 |  | N |
| 4 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |
| 5 | `STORE_NAME` | Storeessorial Name | VARCHAR2 | 30 |  | N |
| 6 | `STORE_ADD1` | Storeessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `STORE_ADD2` | Storeessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `STORE_ADD3` | Storeessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `STORE_ADD4` | Storeessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `STORE_CITY` | Storeessorial City | VARCHAR2 | 30 |  | N |
| 11 | `STORE_STATE` | Storeessorial State | VARCHAR2 | 4 |  | N |
| 12 | `STORE_ZIP` | Storeessorial Zip | VARCHAR2 | 10 |  | N |
| 13 | `STORE_COUNTRY` | Storeessorial Country | VARCHAR2 | 3 |  | N |
| 14 | `STORE_REGION` | Storeessorial Region | NUMBER | 22 | 3 | Y |
| 15 | `STORE_TP` | Storeessorial Tp | VARCHAR2 | 1 |  | N |
| 16 | `STORE_PHONE` | Storeessorial Phone | VARCHAR2 | 18 |  | Y |
| 17 | `STORE_FAX` | Storeessorial Fax | VARCHAR2 | 18 |  | Y |
| 18 | `STORE_MGR_NAME` | Store_Mgressorial Name | VARCHAR2 | 20 |  | Y |
| 19 | `STORE_TOT_REC_CNT` | Store_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 20 | `STORE_ENTRY_DATE` | Store_Entryessorial Date | DATE | 7 |  | N |
| 21 | `STORE_PROS_FLAG` | Store_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `STORE_PROS_DATE` | Store_Prosessorial Date | DATE | 7 |  | Y |
| 23 | `STORE_ACT_FLAG` | Store_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_SUPV_OP`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `L_AP_TMP_INVT_KIT`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `QTY_ON_HAND` | Qty_Onessorial Hand | NUMBER | 22 | 12 | N |
| 7 | `QTY_ON_HOLD_DAMAGE` | Qty_On_Holdessorial Damage | NUMBER | 22 | 12 | Y |
| 8 | `QTY_ON_HOLD_QUALITY` | Qty_On_Holdessorial Quality | NUMBER | 22 | 12 | Y |
| 9 | `QTY_ON_HOLD_RESERVE` | Qty_On_Holdessorial Reserve | NUMBER | 22 | 12 | Y |
| 10 | `QTY_ON_HOLD_HD` | Qty_On_Holdessorial Hd | NUMBER | 22 | 12 | Y |
| 11 | `QTY_ON_HOLD_AVAIL` | Qty_On_Holdessorial Avail | NUMBER | 22 | 12 | Y |
| 12 | `QTY_PHYS` | Qtyessorial Phys | NUMBER | 22 | 12 | Y |
| 13 | `ITEM_CODE_KIT` | Item_Codeessorial Kit | VARCHAR2 | 20 |  | Y |
| 14 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | NUMBER | 22 | 16 | Y |

## `L_AP_TMP_ITEM_BKD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |

## `L_AP_TMP_POD_REP`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 3 | `SHIP_QTY` | Shipessorial Qty | NUMBER | 22 | 10 | N |
| 4 | `POD_QTY` | Podessorial Qty | NUMBER | 22 | 10 | N |

## `L_AP_TMP_POS_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `SKU_NUM` | Skuessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SKU_QTY` | Skuessorial Qty | NUMBER | 22 | 12 | N |
| 4 | `STORE_NUM` | Storeessorial Num | NUMBER | 22 | 5 | N |

## `L_AP_TMP_POS_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | NUMBER | 22 | 3 | N |
| 4 | `POS_CRNT_DATE` | Pos_Crntessorial Date | DATE | 7 |  | N |
| 5 | `POS_TOT_REC_CNT` | Pos_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `POS_ENTRY_DATE` | Pos_Entryessorial Date | DATE | 7 |  | N |
| 7 | `POS_PROS_FLAG` | Pos_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `POS_PROS_DATE` | Pos_Prosessorial Date | DATE | 7 |  | Y |
| 9 | `POS_ACT_FLAG` | Pos_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_AP_TMP_SKU_POS`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `STYLE_CODE` | Styleessorial Code | NUMBER | 22 | 9 | Y |
| 3 | `STYLE_QTY` | Styleessorial Qty | NUMBER | 22 | 12 | Y |
| 4 | `STYLE_POS_QTY` | Style_Posessorial Qty | NUMBER | 22 | 15 | Y |
| 5 | `SKU_CODE` | SKU Code | NUMBER | 22 | 9 | Y |
| 6 | `SKU_QTY` | Skuessorial Qty | NUMBER | 22 | 12 | Y |
| 7 | `SKU_POS_QTY` | Sku_Posessorial Qty | NUMBER | 22 | 12 | Y |
| 8 | `SKU_COST_UNIT` | Sku_Costessorial Unit | NUMBER | 22 | 10 | Y |
| 9 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `L_AP_TRACK_REP_INB_BASE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | N |
| 6 | `TALLY_COMPL_FLAG` | Tally_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `TALLY_QTY` | Tallyessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | Y |
| 9 | `PO_NUM` | PO Number | NUMBER | 22 | 6 | N |

## `L_AP_TRACK_REP_INB_LEV_1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `TALLY_CNT` | Tallyessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `TALLY_TOT_QTY` | Tally_Totessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_TRACK_REP_INB_LEV_2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `TRACK_TALLY_FLOW_TP` | Track_Tally_Flowessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `TALLY_FLOW_QTY` | Tally_Flowessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_TRACK_REP_INB_LEV_3`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `TRACK_TALLY_FLOW_TP` | Track_Tally_Flowessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `TALLY_QTY` | Tallyessorial Qty | NUMBER | 22 | 9 | N |
| 7 | `TALLY_SEQ_NUM` | Tally_Seqessorial Num | NUMBER | 22 | 9 | N |
| 8 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | Y |
| 9 | `PO_NUM` | PO Number | NUMBER | 22 | 6 | N |

## `L_AP_TRACK_REP_OUTB_BASE`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | N |
| 7 | `ORD_TOT_QTY` | Ord_Totessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `ORD_TOT_REPI_QTY` | Ord_Tot_Repiessorial Qty | NUMBER | 22 | 9 | Y |

## `L_AP_TRACK_REP_OUTB_LEV_1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `ORD_NUM_CNT` | Ord_Numessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `ORD_TOT_QTY_SUM` | Ord_Tot_Qtyessorial Sum | NUMBER | 22 | 9 | N |

## `L_AP_TRACK_REP_OUTB_LEV_2A`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `LOC_CODE_AP_CODE` | Loc_Code_Apessorial Code | VARCHAR2 | 5 |  | N |
| 6 | `ORD_PICK_QTY` | Ord_Pickessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_TRACK_REP_OUTB_LEV_2B`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_NUM_CNT` | Ord_Numessorial Cnt | NUMBER | 22 | 6 | N |
| 7 | `ORD_TOT_QTY_SUM` | Ord_Tot_Qtyessorial Sum | NUMBER | 22 | 9 | N |
| 8 | `ORD_TOT_REPI_QTY_SUM` | Ord_Tot_Repi_Qtyessorial Sum | NUMBER | 22 | 9 | Y |

## `L_AP_TRACK_REP_OUTB_LEV_3`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `TRACK_ORD_FLOW_TP` | Track_Ord_Flowessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `TRACK_ORD_FLOW_QTY` | Track_Ord_Flowessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_TRACK_REP_OUTB_LEV_4`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DAYS_DELAY_NUM` | Days_Delayessorial Num | NUMBER | 22 | 6 | N |
| 5 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | N |
| 7 | `TRACK_ORD_FLOW_TP` | Track_Ord_Flowessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `TRACK_ORD_FLOW_QTY` | Track_Ord_Flowessorial Qty | NUMBER | 22 | 9 | N |

## `L_AP_VENDOR`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 12 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `AP_CUST_CODE` | AP Customer Code | VARCHAR2 | 3 |  | N |
| 4 | `VENDOR_NUM` | Vendoressorial Num | NUMBER | 22 | 5 | N |
| 5 | `VENDOR_NAME` | Vendoressorial Name | VARCHAR2 | 30 |  | N |
| 6 | `VENDOR_ADD1` | Vendoressorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `VENDOR_ADD2` | Vendoressorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `VENDOR_ADD3` | Vendoressorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `VENDOR_ADD4` | Vendoressorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `VENDOR_CITY` | Vendoressorial City | VARCHAR2 | 30 |  | N |
| 11 | `VENDOR_STATE` | Vendoressorial State | VARCHAR2 | 4 |  | N |
| 12 | `VENDOR_ZIP` | Vendoressorial Zip | VARCHAR2 | 10 |  | N |
| 13 | `VENDOR_COUNTRY` | Vendoressorial Country | VARCHAR2 | 3 |  | N |
| 14 | `VENDOR_REGION` | Vendoressorial Region | NUMBER | 22 | 3 | N |
| 15 | `VENDOR_RUT` | Vendoressorial Rut | VARCHAR2 | 10 |  | Y |
| 16 | `VENDOR_PHONE` | Vendoressorial Phone | VARCHAR2 | 18 |  | Y |
| 17 | `VENDOR_FAX` | Vendoressorial Fax | VARCHAR2 | 18 |  | Y |
| 18 | `VENDOR_MGR_NAME` | Vendor_Mgressorial Name | VARCHAR2 | 20 |  | Y |
| 19 | `VENDOR_TLR_OVER` | Vendor_Tlressorial Over | NUMBER | 22 | 9 | Y |
| 20 | `VENDOR_TLR_OVER_TP_FLAG` | Vendor_Tlr_Over_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `VENDOR_TLR_SHORT` | Vendor_Tlressorial Short | NUMBER | 22 | 9 | Y |
| 22 | `VENDOR_TLR_SHORT_TP_FLAG` | Vendor_Tlr_Short_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `VENDOR_RANK_CODE` | Vendor_Rankessorial Code | VARCHAR2 | 1 |  | Y |
| 24 | `VENDOR_TOT_REC_CNT` | Vendor_Tot_Recessorial Cnt | NUMBER | 22 | 6 | N |
| 25 | `VENDOR_ENTRY_DATE` | Vendor_Entryessorial Date | DATE | 7 |  | N |
| 26 | `VENDOR_PROS_FLAG` | Vendor_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `VENDOR_PROS_DATE` | Vendor_Prosessorial Date | DATE | 7 |  | Y |
| 28 | `VENDOR_ACT_FLAG` | Vendor_Actessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ITI_DATA`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 49
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ITI_DATA_SEQ_NUM` | Iti_Data_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `MANF_NUM` | Manfessorial Num | VARCHAR2 | 10 |  | Y |
| 3 | `MANF_NAME` | Manfessorial Name | VARCHAR2 | 30 |  | Y |
| 4 | `VEND_NAME` | Vendessorial Name | VARCHAR2 | 30 |  | Y |
| 5 | `VEND_NUM` | Vendessorial Num | VARCHAR2 | 10 |  | Y |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 10 |  | Y |
| 7 | `PACK_SIZE` | Packessorial Size | VARCHAR2 | 20 |  | Y |
| 8 | `ITEM_DES` | Itemessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `PACK_CODE` | Packessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `DC_NUM` | Dcessorial Num | VARCHAR2 | 10 |  | Y |
| 11 | `UOM` | Uomessorial Uom | VARCHAR2 | 10 |  | Y |
| 12 | `DC_NAME` | Dcessorial Name | VARCHAR2 | 30 |  | Y |
| 13 | `FOB_COST` | Fobessorial Cost | NUMBER | 22 | 9 | Y |
| 14 | `FRT_COST` | Frtessorial Cost | NUMBER | 22 | 9 | Y |
| 15 | `CURR_COST` | Curressorial Cost | NUMBER | 22 | 9 | Y |
| 16 | `CATCH_WGT` | Catchessorial Wgt | VARCHAR2 | 1 |  | Y |
| 17 | `CONCEPT` | Conceptessorial Concept | VARCHAR2 | 20 |  | Y |
| 18 | `JAN` | Janessorial Jan | VARCHAR2 | 5 |  | Y |
| 19 | `FEB` | Febessorial Feb | VARCHAR2 | 5 |  | Y |
| 20 | `MAR` | Maressorial Mar | VARCHAR2 | 5 |  | Y |
| 21 | `APR` | Apressorial Apr | VARCHAR2 | 5 |  | Y |
| 22 | `MAY` | Mayessorial May | VARCHAR2 | 5 |  | Y |
| 23 | `JUN` | Junessorial Jun | VARCHAR2 | 5 |  | Y |
| 24 | `JUL` | Julessorial Jul | VARCHAR2 | 5 |  | Y |
| 25 | `AUG` | Augessorial Aug | VARCHAR2 | 5 |  | Y |
| 26 | `SEP` | Sepessorial Sep | VARCHAR2 | 5 |  | Y |
| 27 | `OCT` | Octessorial Oct | VARCHAR2 | 5 |  | Y |
| 28 | `NOV` | Novessorial Nov | VARCHAR2 | 5 |  | Y |
| 29 | `DEC` | Decessorial Dec | VARCHAR2 | 5 |  | Y |
| 30 | `TOTAL_YTD_CASE` | Total_Ytdessorial Case | NUMBER | 22 | 16 | Y |
| 31 | `EST_MONTH_CASE` | Est_Monthessorial Case | NUMBER | 22 | 16 | Y |
| 32 | `EST_YEAR_CASE` | Est_Yearessorial Case | NUMBER | 22 | 16 | Y |
| 33 | `TOT_WGT_NET` | Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 34 | `SHIP_WGT` | Shipessorial Wgt | NUMBER | 22 | 16 | Y |
| 35 | `TOT_CUBE` | Totessorial Cube | NUMBER | 22 | 16 | Y |
| 36 | `ITEM_TI` | Itemessorial Ti | NUMBER | 22 | 5 | Y |
| 37 | `ITEM_HI` | Itemessorial Hi | NUMBER | 22 | 5 | Y |
| 38 | `SHIP_SECTION` | Shipessorial Section | VARCHAR2 | 20 |  | Y |
| 39 | `SHIP_CITY` | Shipessorial City | VARCHAR2 | 30 |  | Y |
| 40 | `SHIP_STATE` | Shipessorial State | VARCHAR2 | 4 |  | Y |
| 41 | `SHIP_ZIP` | Shipessorial Zip | VARCHAR2 | 10 |  | Y |
| 42 | `PAY_DISC` | Payessorial Disc | NUMBER | 22 | 5 | Y |
| 43 | `PAY_DAY` | Payessorial Day | NUMBER | 22 | 5 | Y |
| 44 | `PAY_NET` | Payessorial Net | NUMBER | 22 | 5 | Y |
| 45 | `EST_YEAR_PURCHASE` | Est_Yearessorial Purchase | NUMBER | 22 | 16 | Y |
| 46 | `EST_YEAR_DISC` | Est_Yearessorial Disc | NUMBER | 22 | 16 | Y |
| 47 | `DISC_PER_CASE` | Disc_Peressorial Case | NUMBER | 22 | 5 | Y |
| 48 | `BUYER_NUM` | Buyeressorial Num | VARCHAR2 | 10 |  | Y |
| 49 | `BUYER_NAME` | Buyeressorial Name | VARCHAR2 | 30 |  | Y |

## `L_ITI_DATE_DATA`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 29
- **Campos-chave prováveis:** ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ITI_DATA_SEQ_NUM` | Iti_Data_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `ITI_DATA_DATE` | Iti_Dataessorial Date | DATE | 7 |  | N |
| 3 | `DC_NUM` | Dcessorial Num | VARCHAR2 | 10 |  | Y |
| 4 | `BUYER_NUM` | Buyeressorial Num | VARCHAR2 | 10 |  | Y |
| 5 | `VEND_NUM` | Vendessorial Num | VARCHAR2 | 10 |  | Y |
| 6 | `VEND_NAME` | Vendessorial Name | VARCHAR2 | 30 |  | Y |
| 7 | `ITEM_CODE` | Item Code | VARCHAR2 | 10 |  | Y |
| 8 | `ITEM_DES` | Itemessorial Des | VARCHAR2 | 30 |  | Y |
| 9 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | Y |
| 10 | `ON_HOLD_QTY` | On_Holdessorial Qty | NUMBER | 22 | 9 | Y |
| 11 | `AVE_QTY` | Aveessorial Qty | NUMBER | 22 | 9 | Y |
| 12 | `LAST_WEEK_QTY` | Last_Weekessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `LAST_SEVEN_WEEK_QTY` | Last_Seven_Weekessorial Qty | NUMBER | 22 | 9 | Y |
| 14 | `FORECAST_QTY` | Forecastessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `SEASONAL_FORECAST_QTY` | Seasonal_Forecastessorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `ON_HAND_DAY` | On_Handessorial Day | NUMBER | 22 | 8 | Y |
| 17 | `ON_ORD_DAY` | On_Ordessorial Day | NUMBER | 22 | 8 | Y |
| 18 | `DUE_DATE` | Dueessorial Date | DATE | 7 |  | Y |
| 19 | `APPO_DATE` | Appointment Date | DATE | 7 |  | Y |
| 20 | `ORD_QTY_NEXT_PO` | Ord_Qty_Nextessorial Po | NUMBER | 22 | 9 | Y |
| 21 | `PO_NUM` | PO Number | VARCHAR2 | 20 |  | Y |
| 22 | `DEL_NUM` | Delessorial Num | VARCHAR2 | 20 |  | Y |
| 23 | `CONF_FLAG` | Confessorial Flag | VARCHAR2 | 10 |  | Y |
| 24 | `PRTY_CODE` | Prtyessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `ITEM_CODE_PROMO` | Item_Codeessorial Promo | VARCHAR2 | 10 |  | Y |
| 26 | `ON_HAND_DAY_DUE` | On_Hand_Dayessorial Due | NUMBER | 22 | 8 | Y |
| 27 | `PROD_MGR_NAME` | Prod_Mgressorial Name | VARCHAR2 | 30 |  | Y |
| 28 | `ARR_DATE` | Arressorial Date | DATE | 7 |  | Y |
| 29 | `ARR_TIME` | Arressorial Time | VARCHAR2 | 5 |  | Y |

## `L_METCAN_NEG`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `METCAN_NEG` | Metcanessorial Neg | NUMBER | 22 | 9 | N |
| 9 | `METCAN_TRANS_DATE` | Metcan_Transessorial Date | DATE | 7 |  | N |
| 10 | `METCAN_REF_DES` | Metcan_Refessorial Des | VARCHAR2 | 40 |  | N |

## `L_METCAN_ORD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | N |
| 5 | `BFIELD1` | Bfieldessorial Bfield1 | VARCHAR2 | 1 |  | Y |
| 6 | `BFIELD2` | Bfieldessorial Bfield2 | VARCHAR2 | 1 |  | Y |
| 7 | `BFIELD3` | Bfieldessorial Bfield3 | VARCHAR2 | 1 |  | Y |
| 8 | `DTFIELD1` | Dtfieldessorial Dtfield1 | DATE | 7 |  | Y |
| 9 | `DTFIELD2` | Dtfieldessorial Dtfield2 | DATE | 7 |  | Y |
| 10 | `DTFIELD3` | Dtfieldessorial Dtfield3 | DATE | 7 |  | Y |
| 11 | `DTFIELD4` | Dtfieldessorial Dtfield4 | DATE | 7 |  | Y |
| 12 | `VCFIELD1` | Vcfieldessorial Vcfield1 | VARCHAR2 | 40 |  | Y |
| 13 | `VCFIELD2` | Vcfieldessorial Vcfield2 | VARCHAR2 | 40 |  | Y |
| 14 | `VCFIELD3` | Vcfieldessorial Vcfield3 | VARCHAR2 | 40 |  | Y |
| 15 | `VCFIELD4` | Vcfieldessorial Vcfield4 | VARCHAR2 | 40 |  | Y |
| 16 | `VCFIELD5` | Vcfieldessorial Vcfield5 | VARCHAR2 | 40 |  | Y |
| 17 | `VCFIELD6` | Vcfieldessorial Vcfield6 | VARCHAR2 | 40 |  | Y |
| 18 | `VCFIELD7` | Vcfieldessorial Vcfield7 | VARCHAR2 | 40 |  | Y |
| 19 | `NUMFIELD1` | Numfieldessorial Numfield1 | NUMBER | 22 | 12 | Y |
| 20 | `NUMFIELD2` | Numfieldessorial Numfield2 | NUMBER | 22 | 12 | Y |
| 21 | `NUMFIELD3` | Numfieldessorial Numfield3 | NUMBER | 22 | 12 | Y |
| 22 | `NUMFIELD4` | Numfieldessorial Numfield4 | NUMBER | 22 | 12 | Y |
| 23 | `NUMFIELD5` | Numfieldessorial Numfield5 | NUMBER | 22 | 12 | Y |
| 24 | `NUMFIELD6` | Numfieldessorial Numfield6 | NUMBER | 22 | 12 | Y |

## `L_METCAN_RCPT`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |
| 5 | `BFIELD1` | Bfieldessorial Bfield1 | VARCHAR2 | 1 |  | Y |
| 6 | `BFIELD2` | Bfieldessorial Bfield2 | VARCHAR2 | 1 |  | Y |
| 7 | `BFIELD3` | Bfieldessorial Bfield3 | VARCHAR2 | 1 |  | Y |
| 8 | `DTFIELD1` | Dtfieldessorial Dtfield1 | DATE | 7 |  | Y |
| 9 | `DTFIELD2` | Dtfieldessorial Dtfield2 | DATE | 7 |  | Y |
| 10 | `DTFIELD3` | Dtfieldessorial Dtfield3 | DATE | 7 |  | Y |
| 11 | `DTFIELD4` | Dtfieldessorial Dtfield4 | DATE | 7 |  | Y |
| 12 | `VCFIELD1` | Vcfieldessorial Vcfield1 | VARCHAR2 | 40 |  | Y |
| 13 | `VCFIELD2` | Vcfieldessorial Vcfield2 | VARCHAR2 | 40 |  | Y |
| 14 | `VCFIELD3` | Vcfieldessorial Vcfield3 | VARCHAR2 | 40 |  | Y |
| 15 | `VCFIELD4` | Vcfieldessorial Vcfield4 | VARCHAR2 | 40 |  | Y |
| 16 | `VCFIELD5` | Vcfieldessorial Vcfield5 | VARCHAR2 | 40 |  | Y |
| 17 | `VCFIELD6` | Vcfieldessorial Vcfield6 | VARCHAR2 | 40 |  | Y |
| 18 | `VCFIELD7` | Vcfieldessorial Vcfield7 | VARCHAR2 | 40 |  | Y |
| 19 | `NUMFIELD1` | Numfieldessorial Numfield1 | NUMBER | 22 | 12 | Y |
| 20 | `NUMFIELD2` | Numfieldessorial Numfield2 | NUMBER | 22 | 12 | Y |
| 21 | `NUMFIELD3` | Numfieldessorial Numfield3 | NUMBER | 22 | 12 | Y |
| 22 | `NUMFIELD4` | Numfieldessorial Numfield4 | NUMBER | 22 | 12 | Y |
| 23 | `NUMFIELD5` | Numfieldessorial Numfield5 | NUMBER | 22 | 12 | Y |
| 24 | `NUMFIELD6` | Numfieldessorial Numfield6 | NUMBER | 22 | 12 | Y |

## `L_RY_LOC_SEQ_D1`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 20 |  | N |
| 2 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 5 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 7 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 9 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `L_RY_LOC_SEQ_D2`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 20 |  | N |
| 2 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 5 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 7 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 9 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `L_RY_PERF_REP`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FILE_NAME` | Fileessorial Name | VARCHAR2 | 60 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |

## `L_SL_EMP_YARD_LOCK_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |

## `L_SL_EMP_YARD_LOCK_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 6 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `L_SL_RF_INPUT_PROF_D`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RF_INPUT_PROF_CODE` | Rf_Input_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RF_INPUT_PROF_EFF_DATE` | Rf_Input_Prof_Effessorial Date | DATE | 7 |  | N |
| 4 | `RF_INPUT_PROF_STEP_NUM` | Rf_Input_Prof_Stepessorial Num | NUMBER | 22 | 2 | N |
| 5 | `RF_INPUT_PROF_STEP_DES` | Rf_Input_Prof_Stepessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `RF_INPUT_PROF_EXT_REF1` | Rf_Input_Prof_Extessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 7 | `RF_INPUT_PROF_EXT_REF2` | Rf_Input_Prof_Extessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 8 | `RF_INPUT_PROF_SCR_MESS1` | Rf_Input_Prof_Scressorial Mess1 | VARCHAR2 | 20 |  | N |
| 9 | `RF_INPUT_PROF_SCR_MESS2` | Rf_Input_Prof_Scressorial Mess2 | VARCHAR2 | 20 |  | Y |
| 10 | `RF_INPUT_PROF_ENTRY_MIN_LEN` | Rf_Input_Prof_Entry_Minessorial Len | NUMBER | 22 | 2 | N |
| 11 | `RF_INPUT_PROF_ENTRY_MAX_LEN` | Rf_Input_Prof_Entry_Maxessorial Len | NUMBER | 22 | 2 | N |
| 12 | `RF_INPUT_PROF_ENTRY_TP` | Rf_Input_Prof_Entryessorial Tp | VARCHAR2 | 1 |  | N |
| 13 | `RF_INPUT_PROF_ENTRY_VAL` | Rf_Input_Prof_Entryessorial Val | VARCHAR2 | 20 |  | Y |
| 14 | `RF_INPUT_PROF_ENTRY_DEF` | Rf_Input_Prof_Entryessorial Def | VARCHAR2 | 1 |  | Y |

## `L_SL_RF_INPUT_PROF_H`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RF_INPUT_PROF_CODE` | Rf_Input_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RF_INPUT_PROF_EFF_DATE` | Rf_Input_Prof_Effessorial Date | DATE | 7 |  | N |
| 4 | `RF_INPUT_PROF_DES` | Rf_Input_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `RF_INPUT_PROF_STAT` | Rf_Input_Professorial Stat | VARCHAR2 | 1 |  | N |

## `L_SL_RF_UNLOAD`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 6 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | N |
| 7 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 8 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 10 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 11 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |

## `L_TRANSLOGIX_JOB_DATA`

- **Tipo:** Custom
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 2 | `CUSTOMER_CODE` | Customeressorial Code | VARCHAR2 | 20 |  | Y |
| 3 | `JOB_DATA_DATE` | Job_Dataessorial Date | DATE | 7 |  | Y |
| 4 | `JOB_DATA_NUM` | Job_Dataessorial Num | VARCHAR2 | 20 |  | Y |
| 5 | `JOB_DATA_CONS_REF` | Job_Data_Consessorial Ref | VARCHAR2 | 20 |  | Y |
| 6 | `JOB_DATA_DAIRY_REF` | Job_Data_Dairyessorial Ref | VARCHAR2 | 20 |  | Y |
| 7 | `JOB_DATA_QTY` | Job_Dataessorial Qty | NUMBER | 22 | 16 | Y |
| 8 | `JOB_DATA_PALL` | Job_Dataessorial Pall | NUMBER | 22 | 16 | Y |
| 9 | `JOB_DATA_WGT` | Job_Dataessorial Wgt | NUMBER | 22 | 16 | Y |
| 10 | `JOB_DATA_CUBE` | Job_Dataessorial Cube | NUMBER | 22 | 16 | Y |
| 11 | `JOB_DATA_REVENUE` | Job_Dataessorial Revenue | NUMBER | 22 | 16 | Y |
| 12 | `JOB_DATA_EXPENSE` | Job_Dataessorial Expense | NUMBER | 22 | 16 | Y |
| 13 | `JOB_DATA_PROFIT` | Job_Dataessorial Profit | NUMBER | 22 | 16 | Y |

## `MAR`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 2 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | N |
| 3 | `ZIP_STAT` | Zarehouse Stat | VARCHAR2 | 1 |  | N |
| 4 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |

## `MAR1`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 107
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
| 65 | `COMP_DRMS_ACTIVE_FLAG` | Comp_Drms_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 66 | `COMP_PER_PROF_CODE` | Comp_Per_Professorial Code | VARCHAR2 | 4 |  | Y |
| 67 | `COMP_LAB_POST_DATE` | Comp_Lab_Postessorial Date | DATE | 7 |  | Y |
| 68 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 69 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 70 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 71 | `LAB_COST_CAT_CODE` | Lab_Cost_Catessorial Code | VARCHAR2 | 12 |  | Y |
| 72 | `COMP_LAB_STD_FLAG` | Comp_Lab_Stdessorial Flag | VARCHAR2 | 1 |  | Y |
| 73 | `LAB_STD_MEAS` | Lab_Stdessorial Meas | VARCHAR2 | 4 |  | Y |
| 74 | `MHE_COST_CAT_CODE` | Mhe_Cost_Catessorial Code | VARCHAR2 | 12 |  | Y |
| 75 | `COMP_ALLOW_ADJ_DATE_OVRR_FLAG` | Comp_Allow_Adj_Date_Ovrressorial Flag | VARCHAR2 | 1 |  | N |
| 76 | `COMP_PARA_LOC_SIZE_FLAG` | Comp_Para_Loc_Sizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 77 | `COMP_OUTB_SORT_CODE` | Comp_Outb_Sortessorial Code | VARCHAR2 | 4 |  | N |
| 78 | `COMP_PARA_EXT_INV_NUM_DES` | Comp_Para_Ext_Inv_Numessorial Des | VARCHAR2 | 12 |  | Y |
| 79 | `COMP_PARA_SALE_EXT_INV_FLAG` | Comp_Para_Sale_Ext_Invessorial Flag | VARCHAR2 | 1 |  | Y |
| 80 | `COMP_PARA_OP_PWORD_EXPY_NUM` | Comp_Para_Op_Pword_Expyessorial Num | NUMBER | 22 | 3 | Y |
| 81 | `COMP_DRMS_PHASE3_ACTIVE_FLAG` | Comp_Drms_Phase3_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 82 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 83 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 84 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 85 | `COMP_FLT_LOC_ACTIVE_FLAG` | Comp_Flt_Loc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 86 | `COMP_CAPC_WGT_ACTIVE_FLAG` | Comp_Capc_Wgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 87 | `COMP_DEXION_INTFACE_FLAG` | Comp_Dexion_Intfaceessorial Flag | VARCHAR2 | 1 |  | N |
| 88 | `COMP_LOOSE_WHSE_CODE_STATIC` | Comp_Loose_Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 89 | `COMP_LOOSE_LOC_CODE_STATIC` | Comp_Loose_Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 90 | `COMP_LOOSE_ISOL_CODE` | Comp_Loose_Isolessorial Code | VARCHAR2 | 4 |  | Y |
| 91 | `REG_PRT_CNT` | Reg_Prtessorial Cnt | NUMBER | 22 | 2 | Y |
| 92 | `COMP_PARA_REST_PALL_FLAG` | Comp_Para_Rest_Pallessorial Flag | VARCHAR2 | 1 |  | Y |
| 93 | `COMP_EXE_JAVA` | Comp_Exeessorial Java | VARCHAR2 | 20 |  | Y |
| 94 | `COMP_CAPC_CUBE_ACTIVE_FLAG` | Comp_Capc_Cube_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 95 | `COMP_CONSL_METH` | Comp_Conslessorial Meth | NUMBER | 22 | 1 | Y |
| 96 | `COMP_DRMS_AUTO_WAVE_FLAG` | Comp_Drms_Auto_Waveessorial Flag | VARCHAR2 | 1 |  | Y |
| 97 | `COMP_YARD_MGT_ACTIVE_FLAG` | Comp_Yard_Mgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 98 | `COMP_MAX_NUM_BAT_ORD` | Comp_Max_Num_Batessorial Ord | NUMBER | 22 | 4 | Y |
| 99 | `COMP_XDOCK_MGT_ACTIVE_FLAG` | Comp_Xdock_Mgt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 100 | `COMP_PARA_NUM_REC_INB` | Comp_Para_Num_Recessorial Inb | NUMBER | 22 | 6 | Y |
| 101 | `COMP_PARA_NUM_REC_OUTB` | Comp_Para_Num_Recessorial Outb | NUMBER | 22 | 6 | Y |
| 102 | `COMP_PARA_CART_ACTIVE_FLAG` | Comp_Para_Cart_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 103 | `COMP_VEND_SHIP_FLAG` | Comp_Vend_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 104 | `CARR_EQUAL_TRSPT_EQP_OWN_FLAG` | Carr_Equal_Trspt_Eqp_Ownessorial Flag | VARCHAR2 | 1 |  | N |
| 105 | `COMP_UPDOWNSTREAM_TP` | Comp_Updownstreamessorial Tp | VARCHAR2 | 1 |  | Y |
| 106 | `COMP_USE_EXT_LOAD_NUM_FLAG` | Comp_Use_Ext_Load_Numessorial Flag | VARCHAR2 | 1 |  | Y |
| 107 | `COMP_FRT_INTFACE_PROF_CODE` | Comp_Frt_Intface_Professorial Code | VARCHAR2 | 4 |  | Y |

## `MAR_TEST`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `COMP_NUM_YEAR_RET_SALE_DATA` | Comp_Num_Year_Ret_Saleessorial Data | VARCHAR2 | 1 |  | Y |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 4 | `COMP_MULT_CUR_FLAG` | Comp_Mult_Curessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `COMP_GL_ACTIVE_FLAG` | Comp_Gl_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `COMP_AP_ACTIVE_FLAG` | Comp_Ap_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `COMP_AP_GL_UPD_FLAG` | Comp_Ap_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `COMP_AR_ACTIVE_FLAG` | Comp_Ar_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `COMP_AR_GL_UPD_FLAG` | Comp_Ar_Gl_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `COMP_CC_ACTIVE_FLAG` | Comp_Cc_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `COMP_CC_AR_UPD_FLAG` | Comp_Cc_Ar_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `COMP_PO_ACTIVE_FLAG` | Comp_Po_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `COMP_PO_AP_INTFACE_FLAG` | Comp_Po_Ap_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `COMP_PW_ACTIVE_FLAG` | Comp_Pw_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `COMP_PUB_PRVT_FLAG` | Comp_Pub_Prvtessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `COMP_FRT_ACTIVE_FLAG` | Comp_Frt_Activeessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `COMP_TURN_ACTIVE_FLAG` | Comp_Turn_Activeessorial Flag | VARCHAR2 | 1 |  | Y |

## `MIKED`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 6 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | Y |
| 7 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |

## `MIKED_M_EXE_JOB_D2`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `EXE_JOB_LOCK_CODE` | Exe_Job_Lockessorial Code | VARCHAR2 | 10 |  | N |

## `MIKED_M_EXE_JOB_H`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `EXE_JOB_DES` | Exe_Jobessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `EXE_JOB_OP_REQ_FLAG` | Exe_Job_Op_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `EXE_JOB_PRT_JOB_FLAG` | Exe_Job_Prt_Jobessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `EXE_JOB_SEQ_SEL_FLAG` | Exe_Job_Seq_Selessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 30 |  | Y |
| 7 | `PRT_EXE_CODE` | Prt_Exeessorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `EXE_JOB_QU_JOB_FLAG` | Exe_Job_Qu_Jobessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EXE_JOB_CLASS_NAME` | Exe_Job_Classessorial Name | VARCHAR2 | 60 |  | Y |

## `MIKED_M_SEL`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_DES` | Selessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `SEL_SUBSYS_CODE` | Sel_Subsysessorial Code | VARCHAR2 | 6 |  | Y |
| 4 | `SEL_SORT_SEQ` | Sel_Sortessorial Seq | NUMBER | 22 | 2 | Y |
| 5 | `SEL_VIS_FLAG` | Sel_Visessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 8 | `SEL_REALIGN_FLAG` | Sel_Realignessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 10 | `ISO_REF_CODE` | Iso_Refessorial Code | VARCHAR2 | 20 |  | Y |

## `MIKE_STD`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STD_CODE_TP` | Std_Codeessorial Tp | VARCHAR2 | 4 |  | N |
| 2 | `STD_CODE` | Stdessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `STD_DES` | Stdessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `STD_STAT` | Stdessorial Stat | VARCHAR2 | 1 |  | N |

## `M_ACTN_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ACTN_PROF_CODE` | Actn_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ACTN_IN_OUT_FLAG` | Actn_In_Outessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 5 | `WHSE_LOC_ATTR_NUM` | Warehouse Loc Attr Num | NUMBER | 22 | 2 | Y |

## `M_ACTN_DD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ACTN_PROF_CODE` | Actn_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ACTN_IN_OUT_FLAG` | Actn_In_Outessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `ACTN_CONSL_FLAG` | Actn_Conslessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ACTN_LINE_TP` | Actn_Lineessorial Tp | VARCHAR2 | 1 |  | Y |
| 7 | `ITEM_CODE_MAST_REST_FLAG` | Item_Code_Mast_Restessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_ACTN_DDD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ACTN_PROF_CODE` | Actn_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ACTN_IN_OUT_FLAG` | Actn_In_Outessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |

## `M_ACTN_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ACTN_PROF_CODE` | Actn_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ACTN_DES` | Actnessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `ACTN_STAT` | Actnessorial Stat | VARCHAR2 | 1 |  | N |

## `M_ACT_BLOCK_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ACT_BLOCK_CODE` | Act_Blockessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `ACT_FIELD_CODE` | Act_Fieldessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `ACT_FIELD_DES` | Act_Fieldessorial Des | VARCHAR2 | 50 |  | Y |
| 5 | `ACT_FIELD_SEQ_NUM` | Act_Field_Seqessorial Num | NUMBER | 22 | 4 | Y |
| 6 | `ACT_FIELD_LEN` | Act_Fieldessorial Len | NUMBER | 22 | 3 | N |
| 7 | `ACT_FIELD_TP_CODE` | Act_Field_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 8 | `ACT_FIELD_MAND_FLAG` | Act_Field_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ACT_FIELD_DEF_FLAG` | Act_Field_Defessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ACT_BLOCK_DD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ACT_BLOCK_CODE` | Act_Blockessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `ACT_FIELD_CODE` | Act_Fieldessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `ACT_COMP_CODE` | Act_Compessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ACT_CUST_CODE` | Act_Custessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ACT_FIELD_DEF` | Act_Fieldessorial Def | VARCHAR2 | 40 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ACT_BLOCK_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ACT_BLOCK_CODE` | Act_Blockessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `ACT_BLOCK_DES` | Act_Blockessorial Des | VARCHAR2 | 50 |  | N |
| 4 | `ACT_BLOCK_STAT` | Act_Blockessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_AGE_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `AGE_TP_CODE` | Age_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `AGE_TP_DES` | Age_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `AGE_BK_DES1` | Age_Bkessorial Des1 | VARCHAR2 | 12 |  | N |
| 5 | `AGE_BK_FORUL1` | Age_Bkessorial Forul1 | VARCHAR2 | 20 |  | N |
| 6 | `AGE_BK_DES2` | Age_Bkessorial Des2 | VARCHAR2 | 12 |  | Y |
| 7 | `AGE_BK_FORUL2` | Age_Bkessorial Forul2 | VARCHAR2 | 20 |  | Y |
| 8 | `AGE_BK_DES3` | Age_Bkessorial Des3 | VARCHAR2 | 12 |  | Y |
| 9 | `AGE_BK_FORUL3` | Age_Bkessorial Forul3 | VARCHAR2 | 20 |  | Y |
| 10 | `AGE_BK_DES4` | Age_Bkessorial Des4 | VARCHAR2 | 12 |  | Y |
| 11 | `AGE_BK_FORUL4` | Age_Bkessorial Forul4 | VARCHAR2 | 20 |  | Y |
| 12 | `AGE_BK_DES5` | Age_Bkessorial Des5 | VARCHAR2 | 12 |  | Y |
| 13 | `AGE_BK_FORUL5` | Age_Bkessorial Forul5 | VARCHAR2 | 20 |  | Y |
| 14 | `AGE_BK_DES6` | Age_Bkessorial Des6 | VARCHAR2 | 12 |  | Y |
| 15 | `AGE_BK_FORUL6` | Age_Bkessorial Forul6 | VARCHAR2 | 20 |  | Y |

## `M_ALIAS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `ALIAS_CODE` | Aliasessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ALIAS_DES` | Aliasessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 5 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |

## `M_BUD_TMPL`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BUD_TMPL_CODE` | Bud_Tmplessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `BUD_TMPL_DES` | Bud_Tmplessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `BUD_TMPL_STAT` | Bud_Tmplessorial Stat | VARCHAR2 | 1 |  | N |

## `M_CALL_SYS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CALL_SYS_CODE` | Call_Sysessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `CALL_SYS_DIAL_NUM` | Call_Sys_Dialessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `CALL_SYS_DEV` | Call_Sysessorial Dev | VARCHAR2 | 20 |  | N |
| 4 | `CALL_SYS_SPEED` | Call_Sysessorial Speed | VARCHAR2 | 6 |  | N |

## `M_CHECKIN_CUST_PARA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `CHECKIN_CUST_PARA_REP_LEV` | Checkin_Cust_Para_Repessorial Lev | NUMBER | 22 | 1 | Y |
| 6 | `CHECKIN_CUST_PARA_BAL_LEV` | Checkin_Cust_Para_Balessorial Lev | NUMBER | 22 | 1 | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHECK_LIST_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_CODE` | Check_Listessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHECK_LIST_SEQ_NUM` | Check_List_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHECK_LIST_QUEST` | Check_Listessorial Quest | VARCHAR2 | 250 |  | N |
| 6 | `CHECK_LIST_INFO_FLAG` | Check_List_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHECK_LIST_DD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_CODE` | Check_Listessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHECK_LIST_SEQ_NUM` | Check_List_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CHECK_LIST_ANSW_SEQ_NUM` | Check_List_Answ_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `CHECK_LIST_ANSW` | Check_Listessorial Answ | VARCHAR2 | 250 |  | N |
| 7 | `CHECK_LIST_FAIL_FLAG` | Check_List_Failessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHECK_LIST_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_CODE` | Check_Listessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHECK_LIST_DES` | Check_Listessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CHECK_LIST_STAT` | Check_Listessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CHECK_LIST_MHE_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CHECK_LIST_CODE` | Check_Listessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COST_CAT`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COST_CAT_CODE` | Cost_Catessorial Code | VARCHAR2 | 12 |  | N |
| 3 | `COST_CAT_DES` | Cost_Catessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `COST_CAT_GROUP1_CODE` | Cost_Cat_Group1essorial Code | VARCHAR2 | 4 |  | N |
| 5 | `COST_CAT_GROUP2_CODE` | Cost_Cat_Group2essorial Code | VARCHAR2 | 4 |  | N |
| 6 | `COST_CAT_GL_CODE` | Cost_Cat_Glessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `COST_CAT_CALC_METHOD` | Cost_Cat_Calcessorial Method | VARCHAR2 | 4 |  | N |
| 8 | `COST_CAT_STAT` | Cost_Catessorial Stat | VARCHAR2 | 1 |  | N |

## `M_COST_CAT_GROUP_1`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COST_CAT_GROUP1_CODE` | Cost_Cat_Group1essorial Code | VARCHAR2 | 4 |  | N |
| 3 | `COST_CAT_GROUP1_DES` | Cost_Cat_Group1essorial Des | VARCHAR2 | 30 |  | N |
| 4 | `COST_CAT_GROUP1_STAT` | Cost_Cat_Group1essorial Stat | VARCHAR2 | 1 |  | N |

## `M_COST_CAT_GROUP_2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COST_CAT_GROUP2_CODE` | Cost_Cat_Group2essorial Code | VARCHAR2 | 4 |  | N |
| 3 | `COST_CAT_GROUP2_DES` | Cost_Cat_Group2essorial Des | VARCHAR2 | 30 |  | N |
| 4 | `COST_CAT_GROUP2_STAT` | Cost_Cat_Group2essorial Stat | VARCHAR2 | 1 |  | N |

## `M_DISC_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DISC_PROF_CODE` | Disc_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DISC_PROF_DATE` | Disc_Professorial Date | DATE | 7 |  | N |
| 5 | `DISC_PCT` | Discessorial Pct | NUMBER | 22 | 4 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DISC_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DISC_PROF_CODE` | Disc_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DISC_PROF_DES` | Disc_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DISC_PROF_STAT` | Disc_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DIST_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DIST_TP_DES` | Dist_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DIST_TP_INB_OUTB_FLAG` | Dist_Tp_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DIST_TP_COMPL_ORD_FLAG` | Dist_Tp_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `DIST_TP_STAT` | Dist_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DRMS_CHILD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_CHILD_ID` | Drms_Childessorial Id | NUMBER | 22 | 6 | N |
| 3 | `DRMS_ROLE_ID` | Drms_Roleessorial Id | NUMBER | 22 | 6 | N |
| 4 | `DRMS_CHILD_SHORT` | Drms_Childessorial Short | VARCHAR2 | 20 |  | N |
| 5 | `DRMS_CHILD_DES` | Drms_Childessorial Des | VARCHAR2 | 40 |  | Y |
| 6 | `DRMS_SEL` | Drmsessorial Sel | VARCHAR2 | 2000 |  | Y |
| 7 | `DRMS_WHERE` | Drmsessorial Where | VARCHAR2 | 2000 |  | Y |
| 8 | `DRMS_ORD` | Drmsessorial Ord | VARCHAR2 | 2000 |  | Y |
| 9 | `DRMS_GRP_BY_FLAG` | Drms_Grp_Byessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_DRMS_OP_DEFAULTS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_OP_CODE` | Drms_Opessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `DRMS_COMP_CODE` | Drms_Compessorial Code | VARCHAR2 | 2 |  | Y |
| 3 | `DRMS_ROLE_ID` | Drms_Roleessorial Id | NUMBER | 22 | 6 | Y |
| 4 | `DRMS_TEMPL_VIEW_ACCESS_FLAG` | Drms_Templ_View_Accessessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `DRMS_TEMPL_ALTER_FLAG` | Drms_Templ_Alteressorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `DRMS_VIEW_ALTER_FLAG` | Drms_View_Alteressorial Flag | VARCHAR2 | 1 |  | Y |

## `M_DRMS_PARENT_D1`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_SKEL` | Drmsessorial Skel | VARCHAR2 | 2000 |  | Y |
| 3 | `DRMS_PROP_STR` | Drms_Propessorial Str | LONG | 0 |  | Y |

## `M_DRMS_PARENT_D2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_SEQ_NUM` | Drms_Seqessorial Num | NUMBER | 22 | 1 | N |
| 3 | `DRMS_TABLE_NAME` | Drms_Tableessorial Name | VARCHAR2 | 40 |  | N |

## `M_DRMS_PARENT_D3`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_FIELD_NAME` | Drms_Fieldessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `DRMS_PROP_CODE` | Drms_Propessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DRMS_PROP_VALUE` | Drms_Propessorial Value | VARCHAR2 | 512 |  | Y |
| 5 | `DRMS_PROP_USER_INP_FLAG` | Drms_Prop_User_Inpessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `LAST_UPD_OP_CODE` | Last_Upd_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `LAST_UPD_DATE` | Last_Updessorial Date | DATE | 7 |  | Y |

## `M_DRMS_PARENT_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 2 | `DRMS_PARENT_SHORT` | Drms_Parentessorial Short | VARCHAR2 | 20 |  | N |
| 3 | `DRMS_PARENT_DES` | Drms_Parentessorial Des | VARCHAR2 | 40 |  | Y |
| 4 | `DRMS_PARENT_ID_MENU` | Drms_Parent_Idessorial Menu | NUMBER | 22 | 6 | Y |

## `M_DRMS_SECU_OP_CHILD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `DRMS_PARENT_ID` | Drms_Parentessorial Id | NUMBER | 22 | 6 | N |
| 3 | `DRMS_CHILD_ID` | Drms_Childessorial Id | NUMBER | 22 | 6 | N |

## `M_DRV`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | N |
| 4 | `DRV_NAME` | Drvessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `DRV_STAT` | Drvessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DRV_PCENT` | Drvessorial Pcent | NUMBER | 22 | 3 | N |
| 7 | `DRV_HOUR_RATE` | Drv_Houressorial Rate | NUMBER | 22 | 6 | N |
| 8 | `DRV_LIC` | Drvessorial Lic | VARCHAR2 | 20 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DSHB_FLOW_PROS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DSHB_FLOW_PROS_CODE` | Dshb_Flow_Prosessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `DSHB_FLOW_PROS_DES` | Dshb_Flow_Prosessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `DSHB_FLOW_PROS_STAT` | Dshb_Flow_Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `DSHB_FLOW_PROS_INB_SEQ_NUM` | Dshb_Flow_Pros_Inb_Seqessorial Num | NUMBER | 22 | 3 | Y |
| 6 | `DSHB_FLOW_PROS_OUTB_SEQ_NUM` | Dshb_Flow_Pros_Outb_Seqessorial Num | NUMBER | 22 | 3 | Y |
| 7 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 9 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |

## `M_DSHB_QUERY`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `QUERY_CODE` | Queryessorial Code | VARCHAR2 | 20 |  | N |
| 3 | `QUERY_DES` | Queryessorial Des | VARCHAR2 | 200 |  | N |
| 4 | `QUERY_XML` | Queryessorial Xml | VARCHAR2 | 4000 |  | N |
| 5 | `QUERY_DATE` | Queryessorial Date | DATE | 7 |  | N |
| 6 | `QUERY_AUTO_FLAG` | Query_Autoessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_DSHB_SEARCH_TEMPL_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_SEARCH_TEMPL_SEQ_NUM` | Dshb_Search_Templ_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INPUT_FIELD_SEQ_NUM` | Input_Field_Seqessorial Num | NUMBER | 22 | 6 | N |
| 3 | `INPUT_FIELD_NAME` | Input_Fieldessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `INPUT_FIELD_VALUE` | Input_Fieldessorial Value | VARCHAR2 | 250 |  | Y |

## `M_DSHB_SEARCH_TEMPL_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_SEARCH_TEMPL_SEQ_NUM` | Dshb_Search_Templ_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `DSHB_SEARCH_TEMPL_DES` | Dshb_Search_Templessorial Des | VARCHAR2 | 30 |  | N |

## `M_DSHB_SEARCH_TEMPL_OP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_SEARCH_TEMPL_SEQ_NUM` | Dshb_Search_Templ_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `M_ERR_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ERR_TP_CODE` | Err_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ERR_TP_DES` | Err_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `ERR_TP_STAT` | Err_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_EV_ACC_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_ACC_SEQ_NUM` | Ev_Acc_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `M_EV_ACC_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_ACC_SEQ_NUM` | Ev_Acc_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `EV_ACC_DES` | Ev_Accessorial Des | VARCHAR2 | 50 |  | N |
| 3 | `EV_ACC_STAT` | Ev_Accessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `EV_ACC_TP` | Ev_Accessorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `EV_ACC_SESS_DUR_MIN` | Ev_Acc_Sess_Duressorial Min | NUMBER | 22 | 6 | Y |
| 6 | `EV_ACC_CLIENT_LOGO` | Ev_Acc_Clientessorial Logo | VARCHAR2 | 30 |  | Y |
| 7 | `EV_ACC_MAX_ACTIVE_USERS` | Ev_Acc_Max_Activeessorial Users | NUMBER | 22 | 6 | Y |
| 8 | `EV_ACC_ROWS_PER_PAGE` | Ev_Acc_Rows_Peressorial Page | NUMBER | 22 | 9 | Y |
| 9 | `EV_ACC_ROWS_PER_QU` | Ev_Acc_Rows_Peressorial Qu | NUMBER | 22 | 9 | Y |
| 10 | `EV_ACC_START_DATE` | Ev_Acc_Startessorial Date | DATE | 7 |  | Y |
| 11 | `EV_ACC_EXPY_DATE` | Ev_Acc_Expyessorial Date | DATE | 7 |  | Y |
| 12 | `EV_ACC_DBA_FLAG` | Ev_Acc_Dbaessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `EV_ACC_ORD_RCPT_TP` | Ev_Acc_Ord_Rcptessorial Tp | VARCHAR2 | 1 |  | Y |
| 14 | `EV_ACC_JOB_SCH_ADMIN_FLAG` | Ev_Acc_Job_Sch_Adminessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `EV_ACC_HOLD_PROS_FLAG` | Ev_Acc_Hold_Prosessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_EV_CRON_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_CRON_SEQ_NUM` | Ev_Cron_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EV_CRON_JOB_START_DATE` | Ev_Cron_Job_Startessorial Date | DATE | 7 |  | N |
| 3 | `EV_CRON_JOB_END_DATE` | Ev_Cron_Job_Endessorial Date | DATE | 7 |  | N |
| 4 | `EV_CRON_JOB_REF` | Ev_Cron_Jobessorial Ref | VARCHAR2 | 200 |  | N |
| 5 | `EV_CRON_ERR_NUM` | Ev_Cron_Erressorial Num | NUMBER | 22 | 6 | N |
| 6 | `EV_CRON_ERR_TEXT` | Ev_Cron_Erressorial Text | VARCHAR2 | 200 |  | N |
| 7 | `EV_CRON_JOB_TIME_SLOT` | Ev_Cron_Job_Timeessorial Slot | NUMBER | 22 | 2 | Y |

## `M_EV_CRON_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_CRON_SEQ_NUM` | Ev_Cron_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `EV_CRON_STAT` | Ev_Cronessorial Stat | VARCHAR2 | 1 |  | N |
| 3 | `EV_USER_CODE` | Ev_Useressorial Code | VARCHAR2 | 20 |  | N |
| 4 | `EV_USER_LIST` | Ev_Useressorial List | VARCHAR2 | 2000 |  | N |
| 5 | `EV_CRON_CREATE_DATE` | Ev_Cron_Createessorial Date | DATE | 7 |  | N |
| 6 | `EV_CRON_LAST_JOB_DATE` | Ev_Cron_Last_Jobessorial Date | DATE | 7 |  | N |
| 7 | `EV_CRON_START_DATE` | Ev_Cron_Startessorial Date | DATE | 7 |  | Y |
| 8 | `EV_CRON_EXPY_DATE` | Ev_Cron_Expyessorial Date | DATE | 7 |  | Y |
| 9 | `EV_CRON_NAME` | Ev_Cronessorial Name | VARCHAR2 | 20 |  | N |
| 10 | `EV_CRON_PARMS` | Ev_Cronessorial Parms | VARCHAR2 | 2000 |  | N |
| 11 | `EV_CRON_OUT_FMT` | Ev_Cron_Outessorial Fmt | VARCHAR2 | 20 |  | N |
| 12 | `EV_CRON_DES` | Ev_Cronessorial Des | VARCHAR2 | 100 |  | N |
| 13 | `EV_CRON_MASK` | Ev_Cronessorial Mask | VARCHAR2 | 2000 |  | N |

## `M_EV_USER`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_USER_CODE` | Ev_Useressorial Code | VARCHAR2 | 20 |  | N |
| 2 | `EV_USER_NAME` | Ev_Useressorial Name | VARCHAR2 | 50 |  | N |
| 3 | `EV_USER_STAT` | Ev_Useressorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `EV_USER_PWORD` | Ev_Useressorial Pword | VARCHAR2 | 20 |  | N |
| 5 | `EV_USER_DBA_FLAG` | Ev_User_Dbaessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EV_USER_EMAIL_ADD` | Ev_User_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 7 | `EV_ACC_SEQ_NUM` | Ev_Acc_Seqessorial Num | NUMBER | 22 | 6 | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `EV_USER_LAST_LOGIN_DATE` | Ev_User_Last_Loginessorial Date | DATE | 7 |  | Y |
| 10 | `EV_USER_EXPY_DATE` | Ev_User_Expyessorial Date | DATE | 7 |  | Y |
| 11 | `EV_USER_START_DATE` | Ev_User_Startessorial Date | DATE | 7 |  | Y |
| 12 | `EV_USER_ROWS_PER_PAGE` | Ev_User_Rows_Peressorial Page | NUMBER | 22 | 6 | Y |
| 13 | `EV_USER_SESS_MONITOR_REFR_TIME` | Ev_User_Sess_Monitor_Refressorial Time | NUMBER | 22 | 6 | Y |
| 14 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 15 | `EV_USER_HOLD_PROS_FLAG` | Ev_User_Hold_Prosessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_EV_USER_DEL_AUDIT`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 17

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EV_USER_CODE` | Ev_Useressorial Code | VARCHAR2 | 20 |  | N |
| 2 | `EV_USER_NAME` | Ev_Useressorial Name | VARCHAR2 | 50 |  | N |
| 3 | `EV_USER_STAT` | Ev_Useressorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `EV_USER_PWORD` | Ev_Useressorial Pword | VARCHAR2 | 20 |  | N |
| 5 | `EV_USER_DBA_FLAG` | Ev_User_Dbaessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EV_USER_EMAIL_ADD` | Ev_User_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 7 | `EV_ACC_SEQ_NUM` | Ev_Acc_Seqessorial Num | NUMBER | 22 | 6 | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `EV_USER_LAST_LOGIN_DATE` | Ev_User_Last_Loginessorial Date | DATE | 7 |  | Y |
| 10 | `EV_USER_EXPY_DATE` | Ev_User_Expyessorial Date | DATE | 7 |  | Y |
| 11 | `EV_USER_START_DATE` | Ev_User_Startessorial Date | DATE | 7 |  | Y |
| 12 | `EV_USER_ROWS_PER_PAGE` | Ev_User_Rows_Peressorial Page | NUMBER | 22 | 6 | Y |
| 13 | `EV_USER_SESS_MONITOR_REFR_TIME` | Ev_User_Sess_Monitor_Refressorial Time | NUMBER | 22 | 6 | Y |
| 14 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 15 | `EV_USER_HOLD_PROS_FLAG` | Ev_User_Hold_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `EV_USER_DEL_DATE` | Ev_User_Delessorial Date | DATE | 7 |  | N |
| 17 | `EV_USER_DEL_OP_CODE` | Ev_User_Del_Opessorial Code | VARCHAR2 | 20 |  | N |

## `M_EXE_JOB_D2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `EXE_JOB_LOCK_CODE` | Exe_Job_Lockessorial Code | VARCHAR2 | 10 |  | N |

## `M_EXE_JOB_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `EXE_JOB_DES` | Exe_Jobessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `EXE_JOB_OP_REQ_FLAG` | Exe_Job_Op_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `EXE_JOB_PRT_JOB_FLAG` | Exe_Job_Prt_Jobessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `EXE_JOB_SEQ_SEL_FLAG` | Exe_Job_Seq_Selessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 30 |  | Y |
| 7 | `PRT_EXE_CODE` | Prt_Exeessorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `EXE_JOB_QU_JOB_FLAG` | Exe_Job_Qu_Jobessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EXE_JOB_CLASS_NAME` | Exe_Job_Classessorial Name | VARCHAR2 | 60 |  | Y |
| 10 | `EXE_JOB_TP` | Exe_Jobessorial Tp | VARCHAR2 | 4 |  | Y |
| 11 | `AUTO_QU_FLAG` | Auto_Quessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_EXPD_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `EXPD_TP_CODE` | Expd_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EXPD_TP_DES` | Expd_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `EXPD_TP_STAT` | Expd_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_EXT_LAB_SWARE_CONFIG`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INB_FLOW_SEQ_NUM` | Inb_Flow_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 4 | `INB_SUM_ENRE_FLAG` | Inb_Sum_Enreessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `INB_INCL_NUM_DAY` | Inb_Incl_Numessorial Day | NUMBER | 22 | 3 | Y |
| 6 | `OUTB_FLOW_SEQ_NUM` | Outb_Flow_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 7 | `OUTB_SUM_ENOR_FLAG` | Outb_Sum_Enoressorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `OUTB_INCL_NUM_DAY` | Outb_Incl_Numessorial Day | NUMBER | 22 | 3 | Y |
| 9 | `OUTB_NOT_ASSIGN_LOAD_FLAG` | Outb_Not_Assign_Loadessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `MHE_MOVE_STAMP_TIME` | Mhe_Move_Stampessorial Time | NUMBER | 22 | 3 | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FIELD_DEF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 30 |  | Y |
| 2 | `FIELD_SEQ_NUM` | Field_Seqessorial Num | NUMBER | 22 | 4 | Y |
| 3 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 30 |  | Y |
| 4 | `FIELD_DES` | Fieldessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `FIELD_REQ_FLAG` | Field_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `FIELD_DISP_FLAG` | Field_Dispessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `FIELD_INP_FLAG` | Field_Inpessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `FIELD_DEF` | Fieldessorial Def | VARCHAR2 | 30 |  | Y |
| 9 | `FIELD_SHOW_FLAG` | Field_Showessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_FIN_INTFACE_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FIN_INTFACE_CODE` | Fin_Intfaceessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FIN_INTFACE_BKD_NUM` | Fin_Intface_Bkdessorial Num | NUMBER | 22 | 1 | N |
| 4 | `FIN_INTFACE_BKD_DES` | Fin_Intface_Bkdessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FIN_INTFACE_BKD_START_POS` | Fin_Intface_Bkd_Startessorial Pos | NUMBER | 22 | 2 | N |
| 6 | `FIN_INTFACE_BKD_END_POS` | Fin_Intface_Bkd_Endessorial Pos | NUMBER | 22 | 2 | Y |

## `M_FIN_INTFACE_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FIN_INTFACE_CODE` | Fin_Intfaceessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FIN_INTFACE_DES` | Fin_Intfaceessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FIN_INTFACE_STAT` | Fin_Intfaceessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `FIN_INTFACE_TP` | Fin_Intfaceessorial Tp | VARCHAR2 | 4 |  | N |
| 6 | `FIN_INTFACE_NUM_BKD` | Fin_Intface_Numessorial Bkd | NUMBER | 22 | 1 | N |

## `M_FIS_DATE`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FIS_YEAR` | Fisessorial Year | NUMBER | 22 | 1 | N |
| 3 | `FIS_PER_END_DATE1` | Fis_Per_Endessorial Date1 | DATE | 7 |  | N |
| 4 | `FIS_PER_END_DATE2` | Fis_Per_Endessorial Date2 | DATE | 7 |  | N |
| 5 | `FIS_PER_END_DATE3` | Fis_Per_Endessorial Date3 | DATE | 7 |  | N |
| 6 | `FIS_PER_END_DATE4` | Fis_Per_Endessorial Date4 | DATE | 7 |  | N |
| 7 | `FIS_PER_END_DATE5` | Fis_Per_Endessorial Date5 | DATE | 7 |  | N |
| 8 | `FIS_PER_END_DATE6` | Fis_Per_Endessorial Date6 | DATE | 7 |  | N |
| 9 | `FIS_PER_END_DATE7` | Fis_Per_Endessorial Date7 | DATE | 7 |  | N |
| 10 | `FIS_PER_END_DATE8` | Fis_Per_Endessorial Date8 | DATE | 7 |  | N |
| 11 | `FIS_PER_END_DATE9` | Fis_Per_Endessorial Date9 | DATE | 7 |  | N |
| 12 | `FIS_PER_END_DATE10` | Fis_Per_Endessorial Date10 | DATE | 7 |  | N |
| 13 | `FIS_PER_END_DATE11` | Fis_Per_Endessorial Date11 | DATE | 7 |  | N |
| 14 | `FIS_PER_END_DATE12` | Fis_Per_Endessorial Date12 | DATE | 7 |  | N |
| 15 | `FIS_PER_END_DATE13` | Fis_Per_Endessorial Date13 | DATE | 7 |  | Y |

## `M_FLOW_PROS_D1`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 4 | `FLOW_PROS_STEP_NUM` | Flow_Pros_Stepessorial Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_STEP_DES` | Flow_Pros_Stepessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `FLOW_PROS_SCR_MESS1` | Flow_Pros_Scressorial Mess1 | VARCHAR2 | 20 |  | N |
| 7 | `FLOW_PROS_SCR_MESS2` | Flow_Pros_Scressorial Mess2 | VARCHAR2 | 20 |  | Y |
| 8 | `FLOW_PROS_SCR_VAL` | Flow_Pros_Scressorial Val | VARCHAR2 | 20 |  | N |
| 9 | `FLOW_PROS_SCR_DEF_VAL` | Flow_Pros_Scr_Defessorial Val | VARCHAR2 | 1 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FLOW_PROS_D2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FLOW_PROS_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 4 | `FLOW_PROS_DES` | Flow_Prosessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `FLOW_PROS_STAT` | Flow_Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `FLOW_PROS_PRTY_NUM` | Flow_Pros_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 7 | `DSHB_FLOW_PROS_CODE` | Dshb_Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `DSHB_FLOW_PROS_INB_SEQ_NUM` | Dshb_Flow_Pros_Inb_Seqessorial Num | NUMBER | 22 | 3 | Y |
| 9 | `DSHB_FLOW_PROS_OUTB_SEQ_NUM` | Dshb_Flow_Pros_Outb_Seqessorial Num | NUMBER | 22 | 3 | Y |
| 10 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 12 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `FLOW_PROS_WHSE_ACT_FLAG` | Flow_Pros_Whse_Actessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 15 | `FLOW_PROS_ALERT_TIME` | Flow_Pros_Alertessorial Time | VARCHAR2 | 6 |  | Y |
| 16 | `EV_FLOW_SUPPRESS_TP` | Ev_Flow_Suppressessorial Tp | VARCHAR2 | 1 |  | Y |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_FLOW_PROS_LAB`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | N |
| 5 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | N |

## `M_FORM`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 3 | `FORM_DES` | Formessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `FORM_STAT` | Formessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `FORM_VERT_LINE` | Form_Vertessorial Line | NUMBER | 22 | 3 | N |
| 6 | `FORM_ORIENTATION_TP` | Form_Orientationessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_GENR_INFO_PROF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `GENR_INFO_PROF_CODE` | Genr_Info_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `GENR_INFO_PROF_DES` | Genr_Info_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `GENR_INFO_PROF_STAT` | Genr_Info_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `GENR_INFO_PROF_INB_HAND_PCENT` | Genr_Info_Prof_Inb_Handessorial Pcent | NUMBER | 22 | 3 | N |
| 7 | `GENR_INFO_PROF_OUTB_HAND_PCENT` | Genr_Info_Prof_Outb_Handessorial Pcent | NUMBER | 22 | 3 | N |
| 8 | `GENR_INFO_PROF_CAL_TURN_FLAG` | Genr_Info_Prof_Cal_Turnessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `GENR_INFO_PROF_CAL_TONN_FLAG` | Genr_Info_Prof_Cal_Tonnessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 11 | `CUBE_MEAS_CODE` | Cube_Measessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `GENR_INFO_PROF_ASSEM_FLAG` | Genr_Info_Prof_Assemessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `GENR_INFO_PROF_SHIP_ALONE_FLAG` | Genr_Info_Prof_Ship_Aloneessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_GEN_NUM_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `GEN_NUM_PROF_CODE` | Gen_Num_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `GEN_NUM_PROF_SEQ_NUM` | Gen_Num_Prof_Seqessorial Num | NUMBER | 22 | 1 | N |
| 4 | `SEG_TP_CODE` | Seg_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `GEN_NUM_PROF_SEQ_LEN` | Gen_Num_Prof_Seqessorial Len | NUMBER | 22 | 2 | N |
| 6 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CHK_DIG_CODE` | Chk_Digessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `GEN_NUM_PROF_SEQ_VAL` | Gen_Num_Prof_Seqessorial Val | VARCHAR2 | 10 |  | Y |
| 9 | `GEN_NUM_PROF_SEQ_START` | Gen_Num_Prof_Seqessorial Start | NUMBER | 22 | 9 | Y |

## `M_GEN_NUM_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `GEN_NUM_PROF_CODE` | Gen_Num_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `GEN_NUM_PROF_DES` | Gen_Num_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `GEN_NUM_PROF_STAT` | Gen_Num_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_HAND_PROF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HAND_PROF_CODE` | Hand_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `HAND_PROF_DES` | Hand_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `HAND_PROF_STAT` | Hand_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CHG_CODE_INB` | Chg_Codeessorial Inb | VARCHAR2 | 6 |  | Y |
| 7 | `CHG_CODE_OUTB` | Chg_Codeessorial Outb | VARCHAR2 | 6 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INIT_STOR_PROF_D1`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INIT_STOR_PROF_CODE` | Init_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INIT_STOR_PROF_D2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INIT_STOR_PROF_CODE` | Init_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INIT_STOR_PROF_DISC_DAY` | Init_Stor_Prof_Discessorial Day | NUMBER | 22 | 2 | N |
| 5 | `INIT_STOR_PROF_DISC_PCENT` | Init_Stor_Prof_Discessorial Pcent | NUMBER | 22 | 5 | N |
| 6 | `INIT_STOR_PROF_PRO_RATE_FLAG` | Init_Stor_Prof_Pro_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INIT_STOR_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INIT_STOR_PROF_CODE` | Init_Stor_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INIT_STOR_PROF_DES` | Init_Stor_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INIT_STOR_PROF_STAT` | Init_Stor_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INSTALL`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 30

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INSTALL_NAME` | Installessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `INSTALL_ADD1` | Installessorial Add1 | VARCHAR2 | 30 |  | N |
| 4 | `INSTALL_ADD2` | Installessorial Add2 | VARCHAR2 | 30 |  | Y |
| 5 | `INSTALL_ADD3` | Installessorial Add3 | VARCHAR2 | 30 |  | Y |
| 6 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 7 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 8 | `INSTALL_DATE_DELIM` | Install_Dateessorial Delim | VARCHAR2 | 1 |  | N |
| 9 | `INSTALL_DATE_FMT` | Install_Dateessorial Fmt | VARCHAR2 | 9 |  | N |
| 10 | `INSTALL_MAST_DATE` | Install_Mastessorial Date | DATE | 7 |  | N |
| 11 | `INSTALL_SEL_ERR_NUM` | Install_Sel_Erressorial Num | NUMBER | 22 | 2 | N |
| 12 | `INSTALL_SYS_LOCK` | Install_Sysessorial Lock | VARCHAR2 | 1 |  | N |
| 13 | `INSTALL_PRT_REST_FLAG` | Install_Prt_Restessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `INSTALL_ADD4` | Installessorial Add4 | VARCHAR2 | 30 |  | Y |
| 15 | `INSTALL_DEF_PWORD` | Install_Defessorial Pword | VARCHAR2 | 20 |  | N |
| 16 | `INSTALL_PWORD_EXPY_DAY_NUM` | Install_Pword_Expy_Dayessorial Num | NUMBER | 22 | 3 | Y |
| 17 | `INSTALL_DEL4_HOME_DIR` | Install_Del4_Homeessorial Dir | VARCHAR2 | 50 |  | Y |
| 18 | `DAMIGO_SECU_ENBLD_FLAG` | Damigo_Secu_Enbldessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 20 | `VIEW_DOCU_ARCH_DIR` | View_Docu_Archessorial Dir | VARCHAR2 | 80 |  | Y |
| 21 | `INSTALL_RETAIN_DOCU_NUM_MONTH` | Install_Retain_Docu_Numessorial Month | NUMBER | 22 | 2 | Y |
| 22 | `INSTALL_LAB_TIME_ALLOC_RULE_TP` | Install_Lab_Time_Alloc_Ruleessorial Tp | VARCHAR2 | 3 |  | Y |
| 23 | `INSTALL_PWORD_MIN_LEN` | Install_Pword_Minessorial Len | NUMBER | 22 | 1 | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 29 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |
| 30 | `INSTALL_TZ_NAME` | Install_Tzessorial Name | VARCHAR2 | 64 |  | N |

## `M_INSTALL_TZNAME_CHANGE`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INSTALL_TZ_NAME_PRV` | Install_Tz_Nameessorial Prv | VARCHAR2 | 64 |  | N |
| 3 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 4 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 5 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 6 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LEV_VER_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LEV_VER_PROF_CODE` | Lev_Ver_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LEV_VER_PROF_LEV_CODE` | Lev_Ver_Prof_Levessorial Code | VARCHAR2 | 40 |  | N |
| 5 | `LEV_VER_PROF_LEV_DES` | Lev_Ver_Prof_Levessorial Des | VARCHAR2 | 60 |  | N |
| 6 | `LEV_VER_PROF_REST_ITEM_FLAG` | Lev_Ver_Prof_Rest_Itemessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LEV_VER_PROF_DD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LEV_VER_PROF_CODE` | Lev_Ver_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LEV_VER_PROF_LEV_CODE` | Lev_Ver_Prof_Levessorial Code | VARCHAR2 | 40 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LEV_VER_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LEV_VER_PROF_CODE` | Lev_Ver_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LEV_VER_PROF_DES` | Lev_Ver_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LEV_VER_PROF_STAT` | Lev_Ver_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LINE_TP_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LINE_TP_CODE` | Line_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |

## `M_LINE_TP_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LINE_TP_CODE` | Line_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LINE_TP_DES` | Line_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `LINE_TP_SHT_DES` | Line_Tp_Shtessorial Des | VARCHAR2 | 10 |  | N |
| 5 | `LINE_TP_TRANS_TP` | Line_Tp_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `LINE_TP_DATE_ENTRY` | Line_Tp_Dateessorial Entry | VARCHAR2 | 1 |  | N |
| 7 | `LINE_TP_PRT_CUST_FLAG` | Line_Tp_Prt_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LINE_TP_CHG_ACCESS_FLAG` | Line_Tp_Chg_Accessessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `LINE_TP_CHG_QTY_MINIMUM` | Line_Tp_Chg_Qtyessorial Minimum | NUMBER | 22 | 3 | N |
| 10 | `LINE_TP_CHG_CODE_FLAG` | Line_Tp_Chg_Codeessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `LINE_TP_CHG_FLAG_FLAG` | Line_Tp_Chg_Flagessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `LINE_TP_CHG_VALUE_FLAG` | Line_Tp_Chg_Valueessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `LINE_TP_COST_ACCESS_FLAG` | Line_Tp_Cost_Accessessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `LINE_TP_COST_QTY_MINIMUM` | Line_Tp_Cost_Qtyessorial Minimum | NUMBER | 22 | 3 | N |
| 15 | `LINE_TP_COST_CODE_FLAG` | Line_Tp_Cost_Codeessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `LINE_TP_COST_FLAG_FLAG` | Line_Tp_Cost_Flagessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `LINE_TP_COST_VALUE_FLAG` | Line_Tp_Cost_Valueessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `LINE_TP_STAT` | Line_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_MANF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MANF_CODE` | Manfessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `MANF_NAME` | Manfessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `MANF_STAT` | Manfessorial Stat | VARCHAR2 | 1 |  | N |

## `M_MAN_NUM`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `MAN_NUM_DES` | Man_Numessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MAN_NUM_STAT` | Man_Numessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MAN_NUM_NUM_START` | Man_Num_Numessorial Start | NUMBER | 22 | 10 | N |
| 7 | `MAN_NUM_NUM_END` | Man_Num_Numessorial End | NUMBER | 22 | 10 | N |
| 8 | `MAN_NUM_NUM_CRNT` | Man_Num_Numessorial Crnt | NUMBER | 22 | 10 | N |
| 9 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 10 | `MAN_NUM_LAST_DATE` | Man_Num_Lastessorial Date | DATE | 7 |  | N |
| 11 | `MAN_NUM_LAST_NUM` | Man_Num_Lastessorial Num | NUMBER | 22 | 10 | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_MNT_ACT`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_ACT_CODE` | Mnt_Actessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_ACT_DES` | Mnt_Actessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `MNT_ACT_STAT` | Mnt_Actessorial Stat | VARCHAR2 | 1 |  | N |

## `M_MNT_ACT_GRP_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_ACT_GRP_CODE` | Mnt_Act_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_ACT_CODE` | Mnt_Actessorial Code | VARCHAR2 | 4 |  | N |

## `M_MNT_ACT_GRP_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_ACT_GRP_CODE` | Mnt_Act_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_ACT_GRP_DES` | Mnt_Act_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `MNT_ACT_GRP_STAT` | Mnt_Act_Grpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_MNT_SCH_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_SCH_CODE` | Mnt_Schessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_SCH_BK_NUM` | Mnt_Sch_Bkessorial Num | NUMBER | 22 | 4 | N |
| 4 | `MNT_SCH_DATE_FRQ` | Mnt_Sch_Dateessorial Frq | VARCHAR2 | 10 |  | Y |
| 5 | `MNT_SCH_ODO` | Mnt_Schessorial Odo | NUMBER | 22 | 9 | Y |
| 6 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |

## `M_MNT_SCH_DD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_SCH_CODE` | Mnt_Schessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_SCH_BK_NUM` | Mnt_Sch_Bkessorial Num | NUMBER | 22 | 4 | N |
| 4 | `MNT_ACT_GRP_CODE` | Mnt_Act_Grpessorial Code | VARCHAR2 | 4 |  | N |

## `M_MNT_SCH_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MNT_SCH_CODE` | Mnt_Schessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MNT_SCH_DES` | Mnt_Schessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `MNT_SCH_STAT` | Mnt_Schessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `BAS_EQP_CODE` | Bas_Eqpessorial Code | VARCHAR2 | 4 |  | N |

## `M_MODEL`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MANF_CODE` | Manfessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `MODEL_CODE` | Modelessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `MODEL_DES` | Modelessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MODEL_STAT` | Modelessorial Stat | VARCHAR2 | 1 |  | N |

## `M_NEWS_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `NEWS_SEQ_NUM` | News_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `NEWS_LINE_NUM` | News_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `NEWS_TEXT` | Newsessorial Text | VARCHAR2 | 2000 |  | N |

## `M_NEWS_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `NEWS_SEQ_NUM` | News_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `NEWS_DATE` | Newsessorial Date | DATE | 7 |  | N |
| 4 | `NEWS_TITLE` | Newsessorial Title | VARCHAR2 | 30 |  | N |
| 5 | `NEWS_HEADER` | Newsessorial Header | VARCHAR2 | 160 |  | N |
| 6 | `NEWS_POST_FROM_DATE` | News_Post_Fromessorial Date | DATE | 7 |  | Y |
| 7 | `NEWS_POST_TO_DATE` | News_Post_Toessorial Date | DATE | 7 |  | Y |

## `M_NON_STD_EDI_PROS_AREA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRANS_TP_CODE` | Trans_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `TRANS_TP_INB_OUTB_FLAG` | Trans_Tp_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |

## `M_NON_STD_EDI_TRANS_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRANS_TP_CODE` | Trans_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TRANS_TP_DES` | Trans_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TRANS_TP_STAT` | Trans_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `TRANS_TP_INB_OUTB_FLAG` | Trans_Tp_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TRANS_TP_COMPL_ORD_FLAG` | Trans_Tp_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `TRANS_TP_INB_CONSOL_FLAG` | Trans_Tp_Inb_Consolessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `TRANS_TP_SHIP_CONF_FLAG` | Trans_Tp_Ship_Confessorial Flag | VARCHAR2 | 1 |  | N |

## `M_NUM`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `NUM_TP_CODE` | Num_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 5 | `PREX` | Prexessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `SUFX` | Sufxessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `NUM_START` | Numessorial Start | NUMBER | 22 | 9 | N |
| 8 | `NUM_END` | Numessorial End | NUMBER | 22 | 9 | N |
| 9 | `NUM_CRNT` | Numessorial Crnt | NUMBER | 22 | 9 | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ORG_DEST`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORG_DEST_CODE` | Org_Destessorial Code | VARCHAR2 | 20 |  | N |
| 3 | `ORG_DEST_DES` | Org_Destessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `ORG_DEST_STAT` | Org_Destessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `ORG_DEST_GRP_CODE` | Org_Dest_Grpessorial Code | VARCHAR2 | 4 |  | N |

## `M_ORG_DEST_GRP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORG_DEST_GRP_CODE` | Org_Dest_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORG_DEST_GRP_DES` | Org_Dest_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `ORG_DEST_GRP_STAT` | Org_Dest_Grpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_ORG_FWD`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORG_FWD_CODE` | Org_Fwdessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `ORG_FWD_NAME` | Org_Fwdessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `ORG_FWD_STAT` | Org_Fwdessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ORG_FWD_ADD1` | Org_Fwdessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `ORG_FWD_ADD2` | Org_Fwdessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `ORG_FWD_ADD3` | Org_Fwdessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ORG_FWD_ADD4` | Org_Fwdessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_PACK_STN_D1`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PACK_STN_D2`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PACK_STN_D3`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 5 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PACK_STN_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PACK_STN_DES` | Pack_Stnessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PACK_STN_STAT` | Pack_Stnessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `PACK_STN_WAVE_DUR_MINT_NUM` | Pack_Stn_Wave_Dur_Mintessorial Num | NUMBER | 22 | 3 | N |
| 8 | `PACK_STN_WAVE_MARG_MINT_NUM` | Pack_Stn_Wave_Marg_Mintessorial Num | NUMBER | 22 | 3 | N |
| 9 | `PACK_STN_WAVE_REL_SEQ_NUM` | Pack_Stn_Wave_Rel_Seqessorial Num | NUMBER | 22 | 3 | N |
| 10 | `PACK_STN_START_TIME` | Pack_Stn_Startessorial Time | NUMBER | 22 | 4 | N |
| 11 | `PACK_STN_END_TIME` | Pack_Stn_Endessorial Time | NUMBER | 22 | 4 | N |
| 12 | `PACK_STN_OVFL_SHIFT_FLAG` | Pack_Stn_Ovfl_Shiftessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `PACK_STN_OVFL_DAY_FLAG` | Pack_Stn_Ovfl_Dayessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `PACK_STN_LAST_WAVE_DATE` | Pack_Stn_Last_Waveessorial Date | DATE | 7 |  | Y |
| 15 | `PACK_STN_SECD_WAVE_DATE` | Pack_Stn_Secd_Waveessorial Date | DATE | 7 |  | Y |
| 16 | `PACK_STN_ORD_CAPC_QTY` | Pack_Stn_Ord_Capcessorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `PACK_STN_ORD_SING_LINE_FLAG` | Pack_Stn_Ord_Sing_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `PACK_STN_AUTO_WGT_ENTRY_FLAG` | Pack_Stn_Auto_Wgt_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `PACK_STN_DEV_NAME` | Pack_Stn_Devessorial Name | VARCHAR2 | 40 |  | Y |
| 20 | `PACK_STN_EXE_JOB_CODE` | Pack_Stn_Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 21 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 22 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 23 | `PACK_STN_PROF_CODE` | Pack_Stn_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PERIOD_DEF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PER_PROF_CODE` | Per_Professorial Code | VARCHAR2 | 4 |  | N |
| 2 | `PER_PROF_FIS_YEAR` | Per_Prof_Fisessorial Year | VARCHAR2 | 4 |  | N |
| 3 | `PER_SEQ_NUM` | Per_Seqessorial Num | NUMBER | 22 | 3 | N |
| 4 | `PER_START_DATE` | Per_Startessorial Date | DATE | 7 |  | N |

## `M_PERIOD_DEF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PER_PROF_CODE` | Per_Professorial Code | VARCHAR2 | 4 |  | N |
| 2 | `PER_PROF_FIS_YEAR` | Per_Prof_Fisessorial Year | VARCHAR2 | 4 |  | N |
| 3 | `PER_PROF_DES` | Per_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PER_PROF_NUM` | Per_Professorial Num | NUMBER | 22 | 3 | N |
| 5 | `PER_PROF_SET` | Per_Professorial Set | VARCHAR2 | 1 |  | N |
| 6 | `PER_PROF_STAT` | Per_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_PER_DIEUM`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 4 | `PER_DIEUM_AMT` | Per_Dieumessorial Amt | VARCHAR2 | 4 |  | N |

## `M_PER_PROF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PER_PROF_CODE` | Per_Professorial Code | VARCHAR2 | 4 |  | N |
| 2 | `PER_PROF_DES` | Per_Professorial Des | VARCHAR2 | 30 |  | N |
| 3 | `PER_PROF_STAT` | Per_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_PROS_AREA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_AREA_DES` | Pros_Areaessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PROS_AREA_STAT` | Pros_Areaessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WHSE_CODE_INB` | Whse_Codeessorial Inb | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_INB` | Loc_Codeessorial Inb | VARCHAR2 | 12 |  | N |
| 8 | `WHSE_CODE_OUTB` | Whse_Codeessorial Outb | VARCHAR2 | 4 |  | N |
| 9 | `LOC_CODE_OUTB` | Loc_Codeessorial Outb | VARCHAR2 | 12 |  | N |
| 10 | `WHSE_CODE_SORT` | Whse_Codeessorial Sort | VARCHAR2 | 4 |  | N |
| 11 | `LOC_CODE_SORT` | Loc_Codeessorial Sort | VARCHAR2 | 12 |  | N |
| 12 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `WHSE_CODE_RETICK` | Whse_Codeessorial Retick | VARCHAR2 | 4 |  | Y |
| 14 | `LOC_CODE_RETICK` | Loc_Codeessorial Retick | VARCHAR2 | 12 |  | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROS_AREA_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_AREA_TP_CODE` | Pros_Area_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_AREA_TP_DES` | Pros_Area_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PROS_AREA_TP_STAT` | Pros_Area_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROS_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 5 | `PROS_MESS` | Prosessorial Mess | VARCHAR2 | 45 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROS_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PROS_STAT` | Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `PROS_ENTRY_FLAG` | Pros_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `PROS_INB_OUTB_FLAG` | Pros_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | Y |
| 10 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 12 | `PROS_AUTO_REC_FLAG` | Pros_Auto_Recessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `PROS_ENTRY_VAL_FLAG` | Pros_Entry_Valessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `PROS_DUP_REC_FLAG` | Pros_Dup_Recessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `PROS_DEL_CONF_FLAG` | Pros_Del_Confessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `PROS_TRF_INVT_FLAG` | Pros_Trf_Invtessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `PROS_MAND_ENTRY_FLAG` | Pros_Mand_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `PROS_DISCOVERY_FLAG` | Pros_Discoveryessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `PROS_QTY_CLASS_FLAG` | Pros_Qty_Classessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `PROS_USER_WGT_ENT_FLAG` | Pros_User_Wgt_Entessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `PROS_WGT_MODY` | Pros_Wgtessorial Mody | NUMBER | 22 | 16 | Y |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROS_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `PROS_DEP_FLAG` | Pros_Depessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROS_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_PROF_DES` | Pros_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PROS_PROF_STAT` | Pros_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PT_PT_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORG_DEST_CODE_ORG` | Org_Dest_Codeessorial Org | VARCHAR2 | 20 |  | N |
| 3 | `ORG_DEST_CODE_DEST` | Org_Dest_Codeessorial Dest | VARCHAR2 | 20 |  | N |
| 4 | `PT_PT_BILL_COST_TP` | Pt_Pt_Bill_Costessorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 7 | `TABLE_CODE` | Tableessorial Code | VARCHAR2 | 20 |  | N |

## `M_PT_PT_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORG_DEST_CODE_ORG` | Org_Dest_Codeessorial Org | VARCHAR2 | 20 |  | N |
| 3 | `ORG_DEST_CODE_DEST` | Org_Dest_Codeessorial Dest | VARCHAR2 | 20 |  | N |
| 4 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 5 | `PT_PT_DISTA` | Pt_Ptessorial Dista | NUMBER | 22 | 11 | Y |

## `M_PUT_PROF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PUT_PROF_CODE` | Put_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PUT_PROF_DES` | Put_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PUT_PROF_STAT` | Put_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `PUT_PROF_PICKL_FLAG` | Put_Prof_Picklessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `ITEM_RCPT_HOLD_PROF_CODE` | Item_Rcpt_Hold_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `ITEM_RCPT_HOLD_OVRR_FLAG` | Item_Rcpt_Hold_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 10 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 16 | `PUT_PROF_RGE_DATE_CODE` | Put_Prof_Rge_Dateessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `PUT_PROF_RGE_DAY_FROM_NUM` | Put_Prof_Rge_Day_Fromessorial Num | NUMBER | 22 | 4 | Y |

## `M_QRS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `QRS_PREX` | Qrsessorial Prex | VARCHAR2 | 2 |  | N |
| 6 | `QRS_MEMB_NUM` | Qrs_Membessorial Num | VARCHAR2 | 7 |  | N |
| 7 | `QRS_NUM_START` | Qrs_Numessorial Start | NUMBER | 22 | 9 | N |
| 8 | `QRS_NUM_END` | Qrs_Numessorial End | NUMBER | 22 | 9 | N |
| 9 | `QRS_NUM_CRNT` | Qrs_Numessorial Crnt | NUMBER | 22 | 9 | N |
| 10 | `DOC_CODE_QRS` | Doc_Codeessorial Qrs | VARCHAR2 | 4 |  | Y |
| 11 | `DOC_CODE_LABEL` | Doc_Codeessorial Label | VARCHAR2 | 4 |  | Y |
| 12 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 13 | `QRS_SKU_FLAG` | Qrs_Skuessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `QRS_LEV_ENT_NUM` | Qrs_Lev_Entessorial Num | NUMBER | 22 | 1 | N |
| 15 | `QRS_ALLOW_CONTAIN_FLAG` | Qrs_Allow_Containessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `QRS_MAND_PROS_FLAG` | Qrs_Mand_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `QRS_TP_DEF` | Qrs_Tpessorial Def | NUMBER | 22 | 1 | Y |
| 18 | `QRS_UPC_FLAG` | Qrs_Upcessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_REAS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `REAS_DES` | Reasessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `REAS_STAT` | Reasessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `REAS_INTERNAL_EXT_TP` | Reas_Internal_Extessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `REAS_EXT_TP_CODE` | Reas_Ext_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `REAS_EXT_REF` | Reas_Extessorial Ref | VARCHAR2 | 4 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_REGION_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_TP` | Regionessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `REGION_FILTER_COL_NAME` | Region_Filter_Colessorial Name | VARCHAR2 | 30 |  | N |
| 7 | `REGION_FILTER_COL_VAL` | Region_Filter_Colessorial Val | VARCHAR2 | 255 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_REGION_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_DES` | Regionessorial Des | VARCHAR2 | 100 |  | N |
| 6 | `GLOBAL_COMP` | Globalessorial Comp | VARCHAR2 | 2 |  | N |
| 7 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | N |
| 8 | `STAG_WHSE_CODE` | Stag_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `STAG_LOC_CODE` | Stag_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 10 | `REGION_STAT` | Regionessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `OPID_PREX` | Opidessorial Prex | VARCHAR2 | 30 |  | Y |
| 12 | `OPID_SPOKEN_LEN` | Opid_Spokenessorial Len | NUMBER | 22 | 2 | Y |
| 13 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 14 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 15 | `MAX_PALL_WGT` | Max_Pallessorial Wgt | NUMBER | 22 | 14 | Y |
| 16 | `MAX_PALL_CUBE` | Max_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 17 | `MAX_HALF_PALL_CUBE` | Max_Half_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 18 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `OPID_SPOKEN_NUM_FLAG` | Opid_Spoken_Numessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `UI_LOC_CHECK_DIGIT_LEN` | Ui_Loc_Check_Digitessorial Len | NUMBER | 22 | 2 | Y |
| 21 | `PICK_PATH_MODE_CODE` | Pick_Path_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `MAX_NUM_OF_CART` | Max_Num_Ofessorial Cart | NUMBER | 22 | 9 | Y |
| 23 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 24 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 26 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 27 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 28 | `MAX_PALL_HGT` | Max_Pallessorial Hgt | NUMBER | 22 | 7 | Y |
| 29 | `MAX_OP_NUM_AISLE` | Max_Op_Numessorial Aisle | NUMBER | 22 | 2 | Y |
| 30 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 31 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 32 | `CUST_VOICE_PROF_CODE` | Cust_Voice_Professorial Code | VARCHAR2 | 4 |  | Y |

## `M_REGION_WHSE_ACT_TP_NUM`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 3 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |

## `M_REP_RUN_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `REP_COL_SEQ_NUM` | Rep_Col_Seqessorial Num | NUMBER | 22 | 6 | N |
| 4 | `REP_TABLE_NAME` | Rep_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `REP_COL_NAME` | Rep_Colessorial Name | VARCHAR2 | 30 |  | N |
| 6 | `REP_COL_VALUE` | Rep_Colessorial Value | VARCHAR2 | 60 |  | Y |

## `M_REP_RUN_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `REP_DES` | Repessorial Des | VARCHAR2 | 60 |  | N |
| 4 | `D4_JOB_NUM` | D4_Jobessorial Num | NUMBER | 22 | 6 | N |
| 5 | `REP_START_EXE_DATE` | Rep_Start_Exeessorial Date | DATE | 7 |  | N |
| 6 | `REP_PER_CODE` | Rep_Peressorial Code | VARCHAR2 | 5 |  | Y |
| 7 | `REP_FRQ_NUM` | Rep_Frqessorial Num | NUMBER | 22 | 3 | Y |
| 8 | `REP_MON_CODE` | Rep_Monessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `REP_END_EXE_DATE` | Rep_End_Exeessorial Date | DATE | 7 |  | N |
| 10 | `REP_LAST_EXE_DATE` | Rep_Last_Exeessorial Date | DATE | 7 |  | Y |
| 11 | `REP_COMPL_FLAG` | Rep_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 13 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |

## `M_RETAIL_PARA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE_CUT_ROOM` | Whse_Code_Cutessorial Room | VARCHAR2 | 4 |  | Y |
| 3 | `LOC_CODE_CUT_ROOM` | Loc_Code_Cutessorial Room | VARCHAR2 | 12 |  | Y |
| 4 | `WHSE_CODE_SECURE_AREA` | Whse_Code_Secureessorial Area | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE_SECURE_AREA` | Loc_Code_Secureessorial Area | VARCHAR2 | 12 |  | Y |
| 6 | `HOLD_CODE_RES` | Hold_Codeessorial Res | VARCHAR2 | 4 |  | Y |
| 7 | `RETICK_FLOW_PROF_CODE` | Retick_Flow_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `WHSE_CODE_TAKEOFF` | Whse_Codeessorial Takeoff | VARCHAR2 | 4 |  | Y |
| 9 | `LOC_CODE_TAKEOFF` | Loc_Codeessorial Takeoff | VARCHAR2 | 12 |  | Y |
| 10 | `WHSE_CODE_CONVEYOR` | Whse_Codeessorial Conveyor | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE_CONVEYOR` | Loc_Codeessorial Conveyor | VARCHAR2 | 12 |  | Y |
| 12 | `HOLD_CODE_INTERNET` | Hold_Codeessorial Internet | VARCHAR2 | 4 |  | Y |
| 13 | `PICK_PACK_OPT_TP` | Pick_Pack_Optessorial Tp | VARCHAR2 | 1 |  | Y |

## `M_SCH_COMP_PARA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ALT_CUST_REP_TP_CODE` | Alt_Cust_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `VES_TRSPT_MODE_CODE` | Ves_Trspt_Modeessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SHIP_LINE_TRSPT_MODE_CODE` | Ship_Line_Trspt_Modeessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `PIER_TRSPT_MODE_CODE` | Pier_Trspt_Modeessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `LOAD_TP_CODE_SPC` | Load_Tp_Codeessorial Spc | VARCHAR2 | 4 |  | Y |
| 7 | `CON_CODE_SPC` | Con_Codeessorial Spc | VARCHAR2 | 10 |  | Y |
| 8 | `SCH_CRS_REF_PERMIT_WGT` | Sch_Crs_Ref_Permitessorial Wgt | NUMBER | 22 | 16 | Y |
| 9 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 10 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 11 | `LOAD_TP_CODE_20` | Load_Tp_Codeessorial 20 | VARCHAR2 | 4 |  | Y |
| 12 | `LOAD_TP_CODE_40` | Load_Tp_Codeessorial 40 | VARCHAR2 | 4 |  | Y |
| 13 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 14 | `CRM_CODE` | Crmessorial Code | VARCHAR2 | 4 |  | N |

## `M_SCH_CUST_PARA`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `FLOW_PROS_CODE_SPC` | Flow_Pros_Codeessorial Spc | VARCHAR2 | 4 |  | N |
| 4 | `SCH_CRS_REF_CUST_REF_INVT_LEV` | Sch_Crs_Ref_Cust_Ref_Invtessorial Lev | VARCHAR2 | 4 |  | Y |
| 5 | `SCH_CRS_REF_SHIP_MARK_INVT_LEV` | Sch_Crs_Ref_Ship_Mark_Invtessorial Lev | VARCHAR2 | 4 |  | Y |
| 6 | `SCH_CRS_REF_LOT_INVT_LEV` | Sch_Crs_Ref_Lot_Invtessorial Lev | VARCHAR2 | 4 |  | Y |

## `M_SEL`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_DES` | Selessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `SEL_SUBSYS_CODE` | Sel_Subsysessorial Code | VARCHAR2 | 6 |  | Y |
| 4 | `SEL_SORT_SEQ` | Sel_Sortessorial Seq | NUMBER | 22 | 3 | N |
| 5 | `SEL_VIS_FLAG` | Sel_Visessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 8 | `SEL_REALIGN_FLAG` | Sel_Realignessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ISO_REF_CODE` | Iso_Refessorial Code | VARCHAR2 | 20 |  | Y |
| 10 | `FIRST_MENU` | Firstessorial Menu | VARCHAR2 | 4 |  | N |
| 11 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | Y |
| 12 | `SEL_HELP_FILE_CODE` | Sel_Help_Fileessorial Code | VARCHAR2 | 4 |  | Y |

## `M_SELL_BKD_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SELL_BKD_PROF_CODE` | Sell_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SELL_BKD_PROF_LEV_NUM` | Sell_Bkd_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 4 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 5 | `UPC_CODE_REQ_FLAG` | Upc_Code_Reqessorial Flag | VARCHAR2 | 1 |  | N |

## `M_SELL_BKD_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SELL_BKD_PROF_CODE` | Sell_Bkd_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SELL_BKD_PROF_DES` | Sell_Bkd_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `SELL_BKD_PROF_STAT` | Sell_Bkd_Professorial Stat | VARCHAR2 | 1 |  | N |

## `M_SMAN`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SMAN_CODE` | Smanessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SMAN_NAME` | Smanessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `SMAN_STAT` | Smanessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SOLDTO`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SOLDTO_CODE` | Soldtoessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `SOLDTO_NAME` | Soldtoessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `SOLDTO_STAT` | Soldtoessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `SOLDTO_ADD1` | Soldtoessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `SOLDTO_ADD2` | Soldtoessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `SOLDTO_ADD3` | Soldtoessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `SOLDTO_LAST_ACT_DATE` | Soldto_Last_Actessorial Date | DATE | 7 |  | Y |
| 11 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 12 | `SOLDTO_REF1` | Soldtoessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 13 | `SOLDTO_REF2` | Soldtoessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 14 | `SOLDTO_ADD4` | Soldtoessorial Add4 | VARCHAR2 | 30 |  | Y |
| 15 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 16 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |
| 17 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 23 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_SORT_SEQ`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SORT_SEQ_DES` | Sort_Seqessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SORT_SEQ_STAT` | Sort_Seqessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `SORT_SEQ_ORD_BY_CLAUSE` | Sort_Seq_Ord_Byessorial Clause | VARCHAR2 | 4000 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SPC_VER`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 14

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SPC_VER_CODE` | Spc_Veressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SPC_VER_DES` | Spc_Veressorial Des | VARCHAR2 | 40 |  | N |
| 4 | `SPC_VER_STAT` | Spc_Veressorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `SPC_VER_INB_OUTB_FLAG` | Spc_Ver_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `SPC_VER_TP_FLAG` | Spc_Ver_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `SPC_VER_TP_CODE` | Spc_Ver_Tpessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `SPC_VER_TRACE_FLAG` | Spc_Ver_Traceessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SPC_VER_SQL_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SPC_VER_CODE` | Spc_Veressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SPC_VER_SEQ_NUM` | Spc_Ver_Seqessorial Num | NUMBER | 22 | 4 | N |
| 4 | `SPC_VER_SEQ_DES` | Spc_Ver_Seqessorial Des | VARCHAR2 | 40 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 6 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 8 | `SPC_VER_SQL` | Spc_Veressorial Sql | VARCHAR2 | 2000 |  | N |
| 9 | `SPC_VER_FAIL_FLAG` | Spc_Ver_Failessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `SPC_VER_FAIL_MES` | Spc_Ver_Failessorial Mes | VARCHAR2 | 250 |  | N |
| 11 | `SPC_VER_SQL_RETURN_DATA_FLAG` | Spc_Ver_Sql_Return_Dataessorial Flag | VARCHAR2 | 1 |  | N |

## `M_SPC_VER_SQL_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SPC_VER_CODE` | Spc_Veressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SPC_VER_DES` | Spc_Veressorial Des | VARCHAR2 | 40 |  | N |
| 4 | `SPC_VER_INB_OUTB_FLAG` | Spc_Ver_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |

## `M_SPOOL_PARA_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 5 | `SPOOL_PARA_RETEN_PER` | Spool_Para_Retenessorial Per | NUMBER | 22 | 3 | N |

## `M_SPOOL_PARA_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SPOOL_PARA_AUTO_PURGE_FLAG` | Spool_Para_Auto_Purgeessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `SPOOL_PARA_RETEN_PER` | Spool_Para_Retenessorial Per | NUMBER | 22 | 3 | Y |

## `M_SQL_SCRIPT`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SQL_SCRIPT_CODE` | Sql_Scriptessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SQL_SCRIPT_DES` | Sql_Scriptessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `SQL_SCRIPT_EXEC_FILE` | Sql_Script_Execessorial File | VARCHAR2 | 60 |  | N |
| 5 | `SQL_SCRIPT_CLEAN_CODE` | Sql_Script_Cleanessorial Code | VARCHAR2 | 4 |  | N |

## `M_STN`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STN_CODE` | Stnessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `STN_DES` | Stnessorial Des | VARCHAR2 | 10 |  | N |
| 3 | `STN_STAT` | Stnessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `PSS_ACCNT_NUM` | Pss_Accntessorial Num | VARCHAR2 | 30 |  | N |
| 5 | `PSS_MAST_METER_NUM` | Pss_Mast_Meteressorial Num | VARCHAR2 | 30 |  | N |
| 6 | `PSS_METER_NUM` | Pss_Meteressorial Num | VARCHAR2 | 30 |  | N |
| 7 | `PSS_TCPIP_ADD` | Pss_Tcpipessorial Add | VARCHAR2 | 30 |  | N |
| 8 | `PSS_PORT_NUM` | Pss_Portessorial Num | VARCHAR2 | 30 |  | N |
| 9 | `LABEL_PRT_TCPIP_ADD` | Label_Prt_Tcpipessorial Add | VARCHAR2 | 30 |  | Y |
| 10 | `PRT_CODE_LABEL` | Prt_Codeessorial Label | VARCHAR2 | 4 |  | Y |
| 11 | `PRT_CODE_PACK` | Prt_Codeessorial Pack | VARCHAR2 | 4 |  | Y |
| 12 | `PRT_CODE_SOE` | Prt_Codeessorial Soe | VARCHAR2 | 4 |  | Y |
| 13 | `PACK_THIRD_PARTY_ACC_NUM` | Pack_Third_Party_Accessorial Num | VARCHAR2 | 20 |  | Y |

## `M_STN_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STN_CODE` | Stnessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 3 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `PSS_ACC_NUM` | Pss_Accessorial Num | VARCHAR2 | 30 |  | N |
| 5 | `PSS_THIRD_PARTY_ACC_NUM` | Pss_Third_Party_Accessorial Num | VARCHAR2 | 30 |  | Y |

## `M_STN_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STN_CODE` | Stnessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `STN_DES` | Stnessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `STN_STAT` | Stnessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `PSS_ACC_NUM` | Pss_Accessorial Num | VARCHAR2 | 30 |  | N |
| 5 | `PSS_MAST_METER_NUM` | Pss_Mast_Meteressorial Num | VARCHAR2 | 30 |  | N |
| 6 | `PSS_METER_NUM` | Pss_Meteressorial Num | VARCHAR2 | 30 |  | N |
| 7 | `PSS_TCPIP_ADD` | Pss_Tcpipessorial Add | VARCHAR2 | 30 |  | N |
| 8 | `PSS_PORT_NUM` | Pss_Portessorial Num | VARCHAR2 | 30 |  | N |
| 9 | `LABEL_PRT_TCPIP_ADD` | Label_Prt_Tcpipessorial Add | VARCHAR2 | 30 |  | Y |
| 10 | `PRT_CODE_LABEL` | Prt_Codeessorial Label | VARCHAR2 | 4 |  | Y |
| 11 | `PRT_CODE_PACK` | Prt_Codeessorial Pack | VARCHAR2 | 4 |  | Y |
| 12 | `PRT_CODE_SOE` | Prt_Codeessorial Soe | VARCHAR2 | 4 |  | Y |
| 13 | `PSS_THIRD_PARTY_ACC_NUM` | Pss_Third_Party_Accessorial Num | VARCHAR2 | 30 |  | Y |

## `M_SUMM_LEV`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SUMM_LEV_CODE` | Summ_Levessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `SUMM_LEV_DES` | Summ_Levessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `SUMM_LEV_STAT` | Summ_Levessorial Stat | VARCHAR2 | 1 |  | N |

## `M_SYVOX_WORK_CLASS`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SYVOX_WORK_CLASS_CODE` | Syvox_Work_Classessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `SYVOX_WORK_CLASS_DES` | Syvox_Work_Classessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `SYVOX_WORK_CLASS_STAT` | Syvox_Work_Classessorial Stat | VARCHAR2 | 1 |  | N |

## `M_TABLE_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TABLE_CODE` | Tableessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TABLE_EFF_DATE` | Table_Effessorial Date | DATE | 7 |  | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `TABLE_CLASS_NUM_BK` | Table_Class_Numessorial Bk | NUMBER | 22 | 2 | N |
| 6 | `TABLE_CLASS_BK_FACT` | Table_Class_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 7 | `TABLE_CLASS_BK_VALUE_FACT` | Table_Class_Bk_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `TABLE_CLASS_RATE_FACT` | Table_Class_Rateessorial Fact | VARCHAR2 | 220 |  | N |
| 9 | `TABLE_CLASS_FLAT_FACT` | Table_Class_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 10 | `TABLE_CLASS_MIN_FACT` | Table_Class_Minessorial Fact | VARCHAR2 | 240 |  | N |
| 11 | `TABLE_CLASS_MAX_FACT` | Table_Class_Maxessorial Fact | VARCHAR2 | 240 |  | N |

## `M_TABLE_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TABLE_CODE` | Tableessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TABLE_DES` | Tableessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TABLE_EFF_DATE` | Table_Effessorial Date | DATE | 7 |  | N |
| 5 | `TABLE_STAT` | Tableessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 8 | `TABLE_MIN_AMT` | Table_Minessorial Amt | NUMBER | 22 | 10 | Y |
| 9 | `TABLE_MAX_AMT` | Table_Maxessorial Amt | NUMBER | 22 | 10 | Y |

## `M_TER`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_NUM` | Teressorial Num | NUMBER | 22 | 6 | N |
| 2 | `TER_USAGE_DATE` | Ter_Usageessorial Date | DATE | 7 |  | Y |
| 3 | `TER_USAGE_FLAG` | Ter_Usageessorial Flag | VARCHAR2 | 1 |  | N |

## `M_TERM_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TERM_CODE` | Termessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TERM_INSTMNT_NUM` | Term_Instmntessorial Num | NUMBER | 22 | 3 | N |
| 5 | `TERM_PCENT_INV` | Term_Pcentessorial Inv | NUMBER | 22 | 6 | N |
| 6 | `TERM_NUM_DAY` | Term_Numessorial Day | NUMBER | 22 | 3 | N |
| 7 | `TERM_DISC_PCENT` | Term_Discessorial Pcent | NUMBER | 22 | 6 | N |
| 8 | `TERM_DISC_NUM_DAY` | Term_Disc_Numessorial Day | NUMBER | 22 | 3 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_TERM_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TERM_CODE` | Termessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TERM_DES` | Termessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `TERM_STAT` | Termessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `TERM_USE_FLAG` | Term_Useessorial Flag | VARCHAR2 | 11 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_TEST`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TEST_NAME` | Testessorial Name | VARCHAR2 | 10 |  | N |
| 2 | `TEST_NUM` | Testessorial Num | NUMBER | 22 | 5 | N |

## `M_TRACK_LEV`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRACK_LEV_CODE` | Track_Levessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TRACK_LEV_DES` | Track_Levessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TRACK_LEV_STAT` | Track_Levessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `TRACK_LEV_NUM` | Track_Levessorial Num | NUMBER | 22 | 1 | N |
| 6 | `MAST_TRACK_LEV_CODE` | Mast_Track_Levessorial Code | NUMBER | 22 | 1 | N |

## `M_TRSPT_EQP_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 4 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |

## `M_TRSPT_EQP_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_EQP_DES` | Trspt_Eqpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TRSPT_EQP_STAT` | Trspt_Eqpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_TRSPT_EQP_OWN`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_EQP_OWN_NAME` | Trspt_Eqp_Ownessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `TRSPT_EQP_OWN_STAT` | Trspt_Eqp_Ownessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `TRSPT_EQP_OWN_ADD1` | Trspt_Eqp_Ownessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `TRSPT_EQP_OWN_ADD2` | Trspt_Eqp_Ownessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `TRSPT_EQP_OWN_ADD3` | Trspt_Eqp_Ownessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `TRSPT_EQP_OWN_ADD4` | Trspt_Eqp_Ownessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `TRSPT_EQP_OWN_STD_ALPHA_CODE` | Trspt_Eqp_Own_Std_Alphaessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `TRSPT_UNIT_VAL_HIST_FLAG` | Trspt_Unit_Val_Histessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 19 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_TRSPT_EQP_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_TP_CODE` | Trspt_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TRSPT_EQP_TP_DES` | Trspt_Eqp_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TRSPT_EQP_TP_STAT` | Trspt_Eqp_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `TRSPT_EQP_TP_USE_FLAG` | Trspt_Eqp_Tp_Useessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TRSPT_EQP_TP_TRACK_DIARY_FLAG` | Trspt_Eqp_Tp_Track_Diaryessorial Flag | VARCHAR2 | 1 |  | N |

## `M_TRSPT_MODE`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_MODE_CODE` | Trspt_Modeessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TRSPT_MODE_DES` | Trspt_Modeessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `TRSPT_MODE_STAT` | Trspt_Modeessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `TRSPT_MODE_EXT_REF` | Trspt_Mode_Extessorial Ref | VARCHAR2 | 10 |  | Y |
| 7 | `TRSPT_MODE_TP` | Trspt_Modeessorial Tp | VARCHAR2 | 4 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_TRSPT_PRTY`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_PRTY_CODE` | Trspt_Prtyessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TRSPT_PRTY_DES` | Trspt_Prtyessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TRSPT_PRTY_STAT` | Trspt_Prtyessorial Stat | VARCHAR2 | 1 |  | N |

## `M_UI_PROFILE_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | NVARCHAR2 | 100 |  | N |
| 2 | `PROFILE_ID` | Profileessorial Id | NVARCHAR2 | 100 |  | N |
| 3 | `APPLICATION_ID` | Applicationessorial Id | NVARCHAR2 | 100 |  | N |
| 4 | `SCREEN_ID` | Screenessorial Id | NVARCHAR2 | 100 |  | N |
| 5 | `CONFIGURATION` | Configurationessorial Configuration | CLOB | 4000 |  | N |

## `M_UI_PROFILE_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | NVARCHAR2 | 100 |  | N |
| 2 | `NAME` | Nameessorial Name | NVARCHAR2 | 100 |  | N |

## `M_UPDOWNSTREAM_ASN_CRS_REF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE_UPDOWNSTREAM` | Comp_Codeessorial Updownstream | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE_UPDOWNSTREAM` | Cust_Codeessorial Updownstream | VARCHAR2 | 10 |  | N |
| 5 | `SHIP_CODE_UPDOWNSTREAM` | Ship_Codeessorial Updownstream | VARCHAR2 | 10 |  | N |
| 6 | `WHSE_CODE_UPDOWNSTREAM` | Warehouse Code Updownstream | VARCHAR2 | 10 |  | N |
| 7 | `EDI_PARTNER_CODE` | Edi_Partneressorial Code | VARCHAR2 | 10 |  | N |

## `M_UPDOWNSTREAM_CRS_REF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 29

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE_UPSTREAM` | Comp_Codeessorial Upstream | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE_UPSTREAM` | Cust_Codeessorial Upstream | VARCHAR2 | 10 |  | N |
| 4 | `WHSE_CODE_UPSTREAM` | Warehouse Code Upstream | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE_UPSTREAM` | Loc_Codeessorial Upstream | VARCHAR2 | 12 |  | N |
| 6 | `COMP_CODE_DOWNSTREAM` | Comp_Codeessorial Downstream | VARCHAR2 | 2 |  | N |
| 7 | `CUST_CODE_DOWNSTREAM` | Cust_Codeessorial Downstream | VARCHAR2 | 10 |  | N |
| 8 | `SAME_DB_FLAG` | Same_Dbessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `SAME_SRVR_FLAG` | Same_Srvressorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `DOWNSTREAM_IP_ADD` | Downstream_Ipessorial Add | VARCHAR2 | 30 |  | Y |
| 11 | `DOWNSTREAM_LOGIN` | Downstreamessorial Login | VARCHAR2 | 30 |  | Y |
| 12 | `DOWNSTREAM_PWORD` | Downstreamessorial Pword | VARCHAR2 | 30 |  | Y |
| 13 | `UPSTREAM_INB_DIR` | Upstream_Inbessorial Dir | VARCHAR2 | 60 |  | Y |
| 14 | `UPSTREAM_OUTB_DIR` | Upstream_Outbessorial Dir | VARCHAR2 | 60 |  | Y |
| 15 | `UPSTREAM_ARCH_DIR` | Upstream_Archessorial Dir | VARCHAR2 | 60 |  | Y |
| 16 | `UPSTREAM_ERR_DIR` | Upstream_Erressorial Dir | VARCHAR2 | 60 |  | Y |
| 17 | `DOWNSTREAM_INB_DIR` | Downstream_Inbessorial Dir | VARCHAR2 | 60 |  | Y |
| 18 | `DOWNSTREAM_OUTB_DIR` | Downstream_Outbessorial Dir | VARCHAR2 | 60 |  | Y |
| 19 | `DOWNSTREAM_ARCH_DIR` | Downstream_Archessorial Dir | VARCHAR2 | 60 |  | Y |
| 20 | `DOWNSTREAM_ERR_DIR` | Downstream_Erressorial Dir | VARCHAR2 | 60 |  | Y |
| 21 | `EMAIL_ADD` | Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 22 | `ALERT_TP` | Alertessorial Tp | VARCHAR2 | 1 |  | Y |
| 23 | `SEND_ID` | Sendessorial Id | VARCHAR2 | 20 |  | Y |
| 24 | `RECV_ID` | Recvessorial Id | VARCHAR2 | 20 |  | Y |
| 25 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 26 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 27 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 28 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 29 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_UPDOWNSTREAM_MES`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MES_CODE_INTFACE` | Mes_Codeessorial Intface | VARCHAR2 | 10 |  | N |
| 4 | `MES_DES` | Mesessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MES_STAT` | Mesessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MES_TP` | Mesessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `MES_PRTY_NUM` | Mes_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 8 | `MES_INB_OUTB_TP` | Mes_Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `MES_DIR` | Mesessorial Dir | VARCHAR2 | 60 |  | Y |
| 10 | `MES_PREX` | Mesessorial Prex | VARCHAR2 | 4 |  | Y |
| 11 | `MES_ARCH_DIR` | Mes_Archessorial Dir | VARCHAR2 | 60 |  | Y |
| 12 | `MES_SLEEP_TIME` | Mes_Sleepessorial Time | NUMBER | 22 | 4 | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_VALUE_INX`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `VALUE_INX_CODE` | Value_Inxessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `VALUE_INX_DES` | Value_Inxessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `VALUE_INX_STAT` | Value_Inxessorial Stat | VARCHAR2 | 1 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_VEH_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `VEH_TP_CODE` | Veh_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `VEH_TP_DES` | Veh_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `VEH_TP_STAT` | Veh_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WARR`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WARR_CODE` | Warressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WARR_DES` | Warressorial Des | VARCHAR2 | 30 |  | N |
| 4 | `WARR_STAT` | Warressorial Stat | VARCHAR2 | 1 |  | N |

## `M_WARR_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WARR_CODE` | Warressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TRACK_LEV1_CODE` | Track_Lev1essorial Code | VARCHAR2 | 4 |  | N |
| 4 | `TRACK_LEV2_CODE` | Track_Lev2essorial Code | VARCHAR2 | 4 |  | N |
| 5 | `TRACK_LEV3_CODE` | Track_Lev3essorial Code | VARCHAR2 | 4 |  | N |
| 6 | `TRACK_LEV4_CODE` | Track_Lev4essorial Code | VARCHAR2 | 4 |  | N |
| 7 | `TRACK_LEV5_CODE` | Track_Lev5essorial Code | VARCHAR2 | 4 |  | N |

## `M_WARR_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WARR_CODE` | Warressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WARR_DES` | Warressorial Des | VARCHAR2 | 30 |  | N |
| 4 | `WARR_STAT` | Warressorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `WARR_START_DAY` | Warr_Startessorial Day | DATE | 7 |  | N |
| 6 | `WARR_END_DAY` | Warr_Endessorial Day | DATE | 7 |  | N |
| 7 | `WARR_TIME_CODE` | Warr_Timeessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |

## `M_WARR_TIME`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WARR_TIME_CODE` | Warr_Timeessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WARR_TIME_DES` | Warr_Timeessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `WARR_TIME_STAT` | Warr_Timeessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `WARR_TIME_DAY` | Warr_Timeessorial Day | VARCHAR2 | 1 |  | N |
| 6 | `WARR_TIME_START_TIME` | Warr_Time_Startessorial Time | NUMBER | 22 | 4 | N |
| 7 | `WARR_TIME_END_TIME` | Warr_Time_Endessorial Time | NUMBER | 22 | 4 | N |

## `M_WDR_PROF`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WDR_PROF_CODE` | Wdr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WDR_PROF_DES` | Wdr_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `WDR_PROF_STAT` | Wdr_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |

## `M_WORK_GRP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WORK_GRP_CODE` | Warehouse Grp Code | VARCHAR2 | 4 |  | N |
| 4 | `WORK_GRP_DES` | Warehouse Grp Des | VARCHAR2 | 30 |  | N |
| 5 | `WORK_GRP_STAT` | Warehouse Grp Stat | VARCHAR2 | 1 |  | N |
| 6 | `WORK_GRP_BILL_PCENT` | Warehouse Grp Bill Pcent | NUMBER | 22 | 5 | N |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WORK_UNIT_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WORK_UNIT_CODE` | Warehouse Unit Code | VARCHAR2 | 4 |  | N |
| 3 | `WORK_UNIT_DES` | Warehouse Unit Des | VARCHAR2 | 30 |  | N |
| 4 | `WORK_UNIT_STAT` | Warehouse Unit Stat | VARCHAR2 | 1 |  | N |

## `M_WO_JOB_FUN_TMPL_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_JOB_FUN_TMPL_CODE` | Warehouse Job Fun Tmpl Code | VARCHAR2 | 4 |  | N |
| 3 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WO_JUB_FUN_TMPL_PCENT_TOT_HOUR` | Warehouse Jub Fun Tmpl Pcent Tot Hour | NUMBER | 22 | 10 | N |
| 5 | `WO_JOB_FUN_TMPL_PCENT_TOTA_AMT` | Warehouse Job Fun Tmpl Pcent Tota Amt | NUMBER | 22 | 10 | N |

## `M_WO_JOB_FUN_TMPL_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_JOB_FUN_TMPL_CODE` | Warehouse Job Fun Tmpl Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_JOB_FUN_TMPL_DES` | Warehouse Job Fun Tmpl Des | VARCHAR2 | 30 |  | N |
| 4 | `WO_JOB_FUN_TMPL_STAT` | Warehouse Job Fun Tmpl Stat | VARCHAR2 | 1 |  | N |

## `M_WO_LINE_TP_TMPL_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_LINE_TP_TMPL_CODE` | Warehouse Line Tp Tmpl Code | VARCHAR2 | 4 |  | N |
| 3 | `LINE_TP_CODE` | Line_Tpessorial Code | VARCHAR2 | 4 |  | N |

## `M_WO_LINE_TP_TMPL_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_LINE_TP_TMPL_CODE` | Warehouse Line Tp Tmpl Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_LINE_TP_TMPL_DES` | Warehouse Line Tp Tmpl Des | VARCHAR2 | 30 |  | N |
| 4 | `WO_LINE_TP_TMPL_STAT` | Warehouse Line Tp Tmpl Stat | VARCHAR2 | 1 |  | N |

## `M_WO_PRTY`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_PRTY_CODE` | Warehouse Prty Code | VARCHAR2 | 4 |  | N |
| 3 | `WP_PRTY_DESC` | Warehouse Prty Desc | VARCHAR2 | 30 |  | N |
| 4 | `WO_PRTY_STAT` | Warehouse Prty Stat | VARCHAR2 | 1 |  | N |
| 5 | `WO_PRTY_RSP_DAY` | Warehouse Prty Rsp Day | NUMBER | 22 | 3 | N |

## `M_WO_SER_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_TP_CODE` | Warehouse Tp Code | VARCHAR2 | 4 |  | N |

## `M_WO_SER_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_SER_DESC` | Warehouse Ser Desc | VARCHAR2 | 30 |  | N |
| 4 | `WO_SER_MAST_WO_OPT_FLAG` | Warehouse Ser Mast Wo Opt Flag | VARCHAR2 | 1 |  | N |
| 5 | `WO_SER_REQ_MAST_WO_FLAG` | Warehouse Ser Req Mast Wo Flag | VARCHAR2 | 1 |  | N |
| 6 | `WO_SER_ALLOW_LOCK_FLAG` | Warehouse Ser Allow Lock Flag | VARCHAR2 | 1 |  | N |
| 7 | `WO_SER_ERR_ENTRY_FLAG` | Warehouse Ser Err Entry Flag | VARCHAR2 | 1 |  | N |
| 8 | `WO_SER_QUOTE_ENTRY_FLAG` | Warehouse Ser Quote Entry Flag | VARCHAR2 | 1 |  | N |
| 9 | `WO_SER_PROGR_BILL_ENTRY_FLAG` | Warehouse Ser Progr Bill Entry Flag | VARCHAR2 | 1 |  | N |
| 10 | `WO_SER_REQ_BAL_EST_TIME` | Warehouse Ser Req Bal Est Time | VARCHAR2 | 1 |  | N |
| 11 | `WO_SER_REQ_BAL_EST_VALUE` | Warehouse Ser Req Bal Est Value | VARCHAR2 | 1 |  | N |
| 12 | `WO_SER_REQ_BAL_CHG_TIME` | Warehouse Ser Req Bal Chg Time | VARCHAR2 | 1 |  | N |
| 13 | `WO_SER_REQ_BAL_CHG_VALUE` | Warehouse Ser Req Bal Chg Value | VARCHAR2 | 1 |  | N |
| 14 | `WO_SER_T_AND_M_FLAG` | Warehouse Ser T And M Flag | VARCHAR2 | 1 |  | N |
| 15 | `WO_SER_PCENT_COMPL_TIME_ALERT` | Warehouse Ser Pcent Compl Time Alert | NUMBER | 22 | 3 | Y |
| 16 | `WO_SER_ON_LINE_ALERT_TIME_FLAG` | Warehouse Ser On Line Alert Time Flag | VARCHAR2 | 1 |  | N |
| 17 | `WO_SER_PCENT_COMPL_VALUE_ALERT` | Warehouse Ser Pcent Compl Value Alert | NUMBER | 22 | 3 | Y |
| 18 | `WO_SER_ON_LINE_ALERT_VALUE_FLA` | Warehouse Ser On Line Alert Value Fla | VARCHAR2 | 1 |  | N |
| 19 | `WO_SER_MIN_CHG_TIME` | Warehouse Ser Min Chg Time | NUMBER | 22 | 3 | N |
| 20 | `WORDING_PROF_CODE` | Warehouse Prof Code | VARCHAR2 | 4 |  | N |

## `M_WO_STD_WORDING`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WORDING_SEGM_CODE` | Warehouse Segm Code | VARCHAR2 | 4 |  | N |
| 3 | `WORDING_TITLE` | Warehouse Title | VARCHAR2 | 30 |  | N |
| 4 | `WORDING_TEXT` | Warehouse Text | LONG | 0 |  | N |
| 5 | `WORDING_STAT` | Warehouse Stat | VARCHAR2 | 1 |  | N |

## `M_WO_STD_WORDING_PROF_D`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WORDING_PROF_CODE` | Warehouse Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `WORDING_SEGM_CODE` | Warehouse Segm Code | VARCHAR2 | 4 |  | N |
| 4 | `WORDING_SEGM_SEQ` | Warehouse Segm Seq | NUMBER | 22 | 3 | N |

## `M_WO_STD_WORDING_PROF_H`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WORDING_PROF_CODE` | Warehouse Prof Code | VARCHAR2 | 4 |  | N |
| 3 | `WORDING_PROF_DES` | Warehouse Prof Des | VARCHAR2 | 30 |  | N |
| 4 | `WORDING_PROF_STAT` | Warehouse Prof Stat | VARCHAR2 | 1 |  | N |

## `M_WO_TMPL`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_TMPL_CODE` | Warehouse Tmpl Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_TMPL_DES` | Warehouse Tmpl Des | VARCHAR2 | 30 |  | N |
| 4 | `WO_TMPL_STAT` | Warehouse Tmpl Stat | VARCHAR2 | 1 |  | N |
| 5 | `PROGR_BILL_CODE` | Progr_Billessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `WO_PRTY_CODE` | Warehouse Prty Code | VARCHAR2 | 4 |  | N |
| 7 | `WO_TP_CODE` | Warehouse Tp Code | VARCHAR2 | 4 |  | N |
| 8 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |
| 9 | `WO_TMPL_EST_HOUR` | Warehouse Tmpl Est Hour | NUMBER | 22 | 10 | N |
| 10 | `WO_TMPL_EST_VALUE` | Warehouse Tmpl Est Value | NUMBER | 22 | 10 | N |
| 11 | `WO_TMPL_REM_FLAG` | Warehouse Tmpl Rem Flag | VARCHAR2 | 1 |  | N |

## `M_WO_TP`

- **Tipo:** Master
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WO_TP_CODE` | Warehouse Tp Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_TP_DESC` | Warehouse Tp Desc | VARCHAR2 | 30 |  | N |
| 4 | `WO_TP_EXPY_DATE_MODY` | Warehouse Tp Expy Date Mody | NUMBER | 22 | 3 | N |
| 5 | `WO_TP_REM` | Warehouse Tp Rem | VARCHAR2 | 2000 |  | Y |
| 6 | `WO_TP_STAT` | Warehouse Tp Stat | VARCHAR2 | 1 |  | N |

## `PICK1`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CODE1` | Codeessorial Code1 | VARCHAR2 | 40 |  | Y |
| 2 | `CODE2` | Codeessorial Code2 | VARCHAR2 | 40 |  | Y |
| 3 | `CODE3` | Codeessorial Code3 | VARCHAR2 | 40 |  | Y |
| 4 | `CODE4` | Codeessorial Code4 | VARCHAR2 | 40 |  | Y |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 20 |  | Y |

## `PLAN_TABLE`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 16

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STATEMENT_ID` | Statementessorial Id | VARCHAR2 | 30 |  | Y |
| 2 | `TIMESTAMP` | Timestampessorial Timestamp | DATE | 7 |  | Y |
| 3 | `REMARKS` | Remarksessorial Remarks | VARCHAR2 | 80 |  | Y |
| 4 | `OPERATION` | Operationessorial Operation | VARCHAR2 | 30 |  | Y |
| 5 | `OPTIONS` | Optionsessorial Options | VARCHAR2 | 30 |  | Y |
| 6 | `OBJECT_NODE` | Objectessorial Node | VARCHAR2 | 128 |  | Y |
| 7 | `OBJECT_OWNER` | Objectessorial Owner | VARCHAR2 | 30 |  | Y |
| 8 | `OBJECT_NAME` | Objectessorial Name | VARCHAR2 | 30 |  | Y |
| 9 | `OBJECT_INSTANCE` | Objectessorial Instance | NUMBER | 22 |  | Y |
| 10 | `OBJECT_TYPE` | Objectessorial Type | VARCHAR2 | 30 |  | Y |
| 11 | `OPTIMIZER` | Optimizeressorial Optimizer | VARCHAR2 | 255 |  | Y |
| 12 | `SEARCH_COLUMNS` | Searchessorial Columns | NUMBER | 22 |  | Y |
| 13 | `ID` | ID | NUMBER | 22 |  | Y |
| 14 | `PARENT_ID` | Parentessorial Id | NUMBER | 22 |  | Y |
| 15 | `POSITION` | Positionessorial Position | NUMBER | 22 |  | Y |
| 16 | `OTHER` | Otheressorial Other | LONG | 0 |  | Y |

## `PRODUCT_PROFILE`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRODUCT` | Productessorial Product | VARCHAR2 | 30 |  | N |
| 2 | `USERID` | Useridessorial Userid | VARCHAR2 | 30 |  | Y |
| 3 | `ATTRIBUTE` | Attributeessorial Attribute | VARCHAR2 | 240 |  | Y |
| 4 | `SCOPE` | Scopeessorial Scope | VARCHAR2 | 240 |  | Y |
| 5 | `NUMERIC_VALUE` | Numericessorial Value | NUMBER | 22 | 15 | Y |
| 6 | `CHAR_VALUE` | Charessorial Value | VARCHAR2 | 240 |  | Y |
| 7 | `DATE_VALUE` | Dateessorial Value | DATE | 7 |  | Y |
| 8 | `LONG_VALUE` | Longessorial Value | LONG | 0 |  | Y |

## `QIN_TMP`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_VALUE` | Labelessorial Value | VARCHAR2 | 20 |  | N |
| 4 | `LABEL_ROW` | Labelessorial Row | NUMBER | 22 | 4 | N |
| 5 | `LABEL_COL` | Labelessorial Col | NUMBER | 22 | 4 | N |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `RM2`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 10 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `LOC_DES` | Locessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `LOC_STAT` | Locessorial Stat | VARCHAR2 | 10 |  | N |
| 6 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 7 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_HGT` | Locessorial Hgt | NUMBER | 22 | 7 | N |
| 9 | `LOC_WID` | Locessorial Wid | NUMBER | 22 | 7 | N |
| 10 | `LOC_LEN` | Locessorial Len | NUMBER | 22 | 7 | N |
| 11 | `LOC_CUBE` | Locessorial Cube | NUMBER | 22 | 10 | Y |
| 12 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 15 | `LOC_MAX_SKU_CAPC` | Loc_Max_Skuessorial Capc | VARCHAR2 | 4 |  | N |
| 16 | `SKU_CAPC_PCENT` | Sku_Capcessorial Pcent | NUMBER | 22 |  | Y |
| 17 | `SPACE_CAPC_PCENT` | Space_Capcessorial Pcent | NUMBER | 22 |  | Y |
| 18 | `LOC_PRT_PROF_CODE` | Loc_Prt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `LOC_NUM` | Locessorial Num | NUMBER | 22 | 6 | Y |
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
| 30 | `LOC_USE_LAST_PUT_FLAG` | Loc_Use_Last_Putessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `LOC_VERT_HGT_FACT_CODE` | Loc_Vert_Hgt_Factessorial Code | VARCHAR2 | 4 |  | Y |

## `RMC_BAL`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 26

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `A` | A | VARCHAR2 | 30 |  | Y |
| 2 | `B` | Bessorial B | VARCHAR2 | 30 |  | Y |
| 3 | `C` | Cessorial C | VARCHAR2 | 30 |  | Y |
| 4 | `D` | Dessorial D | VARCHAR2 | 30 |  | Y |
| 5 | `E` | Eessorial E | VARCHAR2 | 30 |  | Y |
| 6 | `F` | F | VARCHAR2 | 30 |  | Y |
| 7 | `G` | Gessorial G | VARCHAR2 | 30 |  | Y |
| 8 | `H` | Hessorial H | VARCHAR2 | 30 |  | Y |
| 9 | `I` | I | VARCHAR2 | 30 |  | Y |
| 10 | `J` | Jessorial J | VARCHAR2 | 30 |  | Y |
| 11 | `K` | Kessorial K | VARCHAR2 | 30 |  | Y |
| 12 | `L` | Lessorial L | VARCHAR2 | 30 |  | Y |
| 13 | `M` | Messorial M | VARCHAR2 | 30 |  | Y |
| 14 | `N` | Nessorial N | VARCHAR2 | 30 |  | Y |
| 15 | `O` | Oessorial O | VARCHAR2 | 30 |  | Y |
| 16 | `P` | Pessorial P | VARCHAR2 | 30 |  | Y |
| 17 | `Q` | Qessorial Q | VARCHAR2 | 30 |  | Y |
| 18 | `R` | Ressorial R | VARCHAR2 | 30 |  | Y |
| 19 | `S` | Sessorial S | VARCHAR2 | 30 |  | Y |
| 20 | `T` | Tessorial T | VARCHAR2 | 30 |  | Y |
| 21 | `U` | Uessorial U | VARCHAR2 | 30 |  | Y |
| 22 | `V` | Vessorial V | VARCHAR2 | 30 |  | Y |
| 23 | `W` | Wessorial W | VARCHAR2 | 30 |  | Y |
| 24 | `X` | X | VARCHAR2 | 30 |  | Y |
| 25 | `Y` | Y | VARCHAR2 | 30 |  | Y |
| 26 | `Z` | Z | VARCHAR2 | 1 |  | Y |

## `SS`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_ATTR_TP_NUM` | Whse_Attr_Tpessorial Num | NUMBER | 22 | 3 | N |
| 4 | `WHSE_ATTR_TP_OPT_NUM` | Whse_Attr_Tp_Optessorial Num | NUMBER | 22 | 3 | N |

## `S_ACCSS_AUDIT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ACCSS_AUD_DATE` | Accss_Audessorial Date | DATE | 7 |  | N |
| 3 | `ACCSS_AUD_OP_CODE` | Accss_Aud_Opessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `ACCSS_AUD_ACTN` | Accss_Audessorial Actn | VARCHAR2 | 3 |  | N |
| 5 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 6 | `ACCSS_AUD_COL_NAME` | Accss_Aud_Colessorial Name | VARCHAR2 | 30 |  | N |
| 7 | `ACCSS_AUD_ORG_VALUE` | Accss_Aud_Orgessorial Value | VARCHAR2 | 30 |  | Y |
| 8 | `ACCSS_AUD_CUR_VALUE` | Accss_Aud_Curessorial Value | VARCHAR2 | 30 |  | Y |
| 9 | `ACCSS_AUD_NUM` | Accss_Audessorial Num | NUMBER | 22 | 6 | Y |
| 10 | `ACCSS_AUD_PGM_NAME` | Accss_Aud_Pgmessorial Name | VARCHAR2 | 4 |  | N |
| 11 | `ACCSS_AUD_INV_NUM` | Accss_Aud_Invessorial Num | NUMBER | 22 | 9 | Y |
| 12 | `ACCSS_AUD_INV_LINE_NUM` | Accss_Aud_Inv_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 13 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | N |

## `S_ADJ_AUDIT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | N |
| 3 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 4 | `ADJ_AUDIT_NUM` | Adj_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 5 | `ADJ_EDI_PROS_FLAG` | Adj_Edi_Prosessorial Flag | VARCHAR2 | 1 |  | N |

## `S_AUD_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AUD_SEQ_NUM` | Aud_Seqessorial Num | NUMBER | 22 | 10 | N |
| 2 | `COL_NAME` | Column Name | VARCHAR2 | 40 |  | N |
| 3 | `AUD_OLD_VAL` | Aud_Oldessorial Val | VARCHAR2 | 60 |  | Y |
| 4 | `AUD_NEW_VAL` | Aud_Newessorial Val | VARCHAR2 | 60 |  | Y |

## `S_AUD_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 17

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AUD_SEQ_NUM` | Aud_Seqessorial Num | NUMBER | 22 | 10 | N |
| 2 | `AUD_REP_NUM` | Aud_Repessorial Num | NUMBER | 22 | 10 | Y |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 5 | `AUD_GRP_TP` | Aud_Grpessorial Tp | VARCHAR2 | 15 |  | N |
| 6 | `AUD_LOG_DATE` | Aud_Logessorial Date | DATE | 7 |  | N |
| 7 | `AUD_ACTN` | Audessorial Actn | VARCHAR2 | 10 |  | N |
| 8 | `IND_COL1` | Indessorial Col1 | VARCHAR2 | 40 |  | Y |
| 9 | `IND_COL2` | Indessorial Col2 | VARCHAR2 | 40 |  | Y |
| 10 | `IND_COL3` | Indessorial Col3 | VARCHAR2 | 40 |  | Y |
| 11 | `IND_COL4` | Indessorial Col4 | VARCHAR2 | 40 |  | Y |
| 12 | `IND_COL5` | Indessorial Col5 | VARCHAR2 | 40 |  | Y |
| 13 | `IND_COL6` | Indessorial Col6 | VARCHAR2 | 40 |  | Y |
| 14 | `IND_COL7` | Indessorial Col7 | VARCHAR2 | 40 |  | Y |
| 15 | `IND_COL8` | Indessorial Col8 | VARCHAR2 | 40 |  | Y |
| 16 | `IND_COL9` | Indessorial Col9 | VARCHAR2 | 40 |  | Y |
| 17 | `IND_COL10` | Indessorial Col10 | VARCHAR2 | 40 |  | Y |

## `S_BACKGRND`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `BACKGRND_ACT` | Backgrndessorial Act | VARCHAR2 | 30 |  | N |

## `S_BARCODE_AI`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `BARCODE_TP` | Barcodeessorial Tp | VARCHAR2 | 10 |  | N |
| 2 | `BARCODE_SEQ_NUM` | Barcode_Seqessorial Num | NUMBER | 22 | 3 | N |
| 3 | `BARCODE_DES` | Barcodeessorial Des | VARCHAR2 | 80 |  | N |
| 4 | `BARCODE_AI_LEN` | Barcode_Aiessorial Len | VARCHAR2 | 10 |  | Y |
| 5 | `BARCODE_AI_DATA_STRUCT` | Barcode_Ai_Dataessorial Struct | VARCHAR2 | 30 |  | Y |
| 6 | `BARCODE_AI` | Barcodeessorial Ai | VARCHAR2 | 10 |  | N |

## `S_CUBE_MEAS_FACT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CUBE_MEAS_CODE` | Cube_Measessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `CUBE_MEAS_DES` | Cube_Measessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `CUBE_MEAS_FACT` | Cube_Measessorial Fact | NUMBER | 22 | 9 | N |
| 4 | `CUBE_MEAS_FORMAT` | Cube_Measessorial Format | VARCHAR2 | 20 |  | N |

## `S_DAY_ACT_REG`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DAY_ACT_REG_NUM` | Day_Act_Regessorial Num | NUMBER | 22 | 6 | N |
| 3 | `DAY_ACT_REG_STAT` | Day_Act_Regessorial Stat | NUMBER | 22 | 2 | N |
| 4 | `DAY_ACT_REG_STAT_PREX` | Day_Act_Reg_Statessorial Prex | VARCHAR2 | 4 |  | Y |
| 5 | `DAY_ACT_REG_STAT_NUM` | Day_Act_Reg_Statessorial Num | NUMBER | 22 | 2 | N |
| 6 | `DAY_ACT_REG_STAT_CODE` | Day_Act_Reg_Statessorial Code | VARCHAR2 | 40 |  | Y |

## `S_DOC_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 5 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | Y |
| 8 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `BAT_NUM` | Batch Number | NUMBER | 22 | 6 | Y |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |

## `S_DOC_VIEW`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_TP_CODE` | Doc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `DOC_VIEW_DATE` | Doc_Viewessorial Date | DATE | 7 |  | N |
| 8 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 9 | `SYS_PRT_CODE` | Sys_Prtessorial Code | VARCHAR2 | 30 |  | N |
| 10 | `SPOOL_FILE_ARCH_ID` | Spool_File_Archessorial Id | VARCHAR2 | 80 |  | N |
| 11 | `FRONT_FAX_OVRL_ARCH_ID` | Front_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 12 | `BACK_FAX_OVRL_ARCH_ID` | Back_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 13 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_EXE_PROG_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_PROG_CODE` | Exe_Progessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `EXE_PROG_REM_LINE_NUM` | Exe_Prog_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `EXE_PROG_REM_LINE_TEXT` | Exe_Prog_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `S_EXE_PROG_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_PROG_CODE` | Exe_Progessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `EXE_PROG_DES` | Exe_Progessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `EXE_PROG_STAT` | Exe_Progessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `MODU_CODE` | Moduessorial Code | VARCHAR2 | 20 |  | N |

## `S_INB_OUTB_PARA`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INB_OUTB_CODE` | Inb_Outbessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `INB_OUTB_PARA_NUM` | Inb_Outb_Paraessorial Num | NUMBER | 22 | 2 | N |
| 4 | `INB_OUTB_PARA_OPT_NUM` | Inb_Outb_Para_Optessorial Num | NUMBER | 22 | 2 | N |
| 5 | `INB_OUTB_PARA_OPT_DES` | Inb_Outb_Para_Optessorial Des | VARCHAR2 | 75 |  | N |
| 6 | `MIN_INVT_LEV` | Min_Invtessorial Lev | NUMBER | 22 | 1 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_INFO_FLOW`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INFO_FLOW_CODE` | Info_Flowessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `INFO_FLOW_DES` | Info_Flowessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `INFO_FLOW_STAT` | Info_Flowessorial Stat | VARCHAR2 | 1 |  | N |

## `S_INSTALL_SWITCH`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 20

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SYS_PW_ACTIVE_FLAG` | Sys_Pw_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 2 | `SYS_GL_ACTIVE_FLAG` | Sys_Gl_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `SYS_AP_ACTIVE_FLAG` | Sys_Ap_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `SYS_AR_ACTIVE_FLAG` | Sys_Ar_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SYS_CC_ACTIVE_FLAG` | Sys_Cc_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `SYS_PO_ACTIVE_FLAG` | Sys_Po_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `SYS_FRT_ACTIVE_FLAG` | Sys_Frt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `SYS_DYN_LOC_RCPT_ACTIVE_FLAG` | Sys_Dyn_Loc_Rcpt_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `SYS_DYN_LOC_SHIP_ACTIVE_FLAG` | Sys_Dyn_Loc_Ship_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `SYS_TURN_ACTIVE_FLAG` | Sys_Turn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `SYS_TONN_ACTIVE_FLAG` | Sys_Tonn_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `SYS_BORD_ACTIVE_FLAG` | Sys_Bord_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `SYS_FORD_ACTIVE_FLAG` | Sys_Ford_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `SYS_INTRANS_ACTIVE_FLAG` | Sys_Intrans_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `SYS_SET_ASSEM_ACTIVE_FLAG` | Sys_Set_Assem_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `SYS_MULT_CUR_ACTIVE_FLAG` | Sys_Mult_Cur_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `SYS_ITEM_PRI_ACTIVE_FLAG` | Sys_Item_Pri_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `SYS_MAX_INVT_LEV_NUM` | Sys_Max_Invt_Levessorial Num | NUMBER | 22 | 1 | N |
| 19 | `SYS_DRMS_ACTIVE_FLAG` | Sys_Drms_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `SYS_OP_SEL_AUD_FLAG` | Sys_Op_Sel_Audessorial Flag | VARCHAR2 | 1 |  | N |

## `S_INTERNAL_OP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `OP_NAME` | Opessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `OP_DES` | Opessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_JAVA_REPORT_ATTRIBUTES_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `TAG_ID` | Tagessorial Id | NUMBER | 22 | 6 | N |
| 3 | `ATTRIBUTE_NAME` | Attribute Name | VARCHAR2 | 60 |  | N |
| 4 | `ATTRIBUTE_VALUE` | Attribute Name | VARCHAR2 | 60 |  | N |

## `S_JAVA_REPORT_ATTRIBUTES_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `TAG_ID` | Tagessorial Id | NUMBER | 22 | 6 | N |
| 3 | `PARENT_TAG_ID` | Parent_Tagessorial Id | NUMBER | 22 | 6 | N |
| 4 | `TAG_NAME` | Tagessorial Name | VARCHAR2 | 60 |  | N |

## `S_JAVA_SCREEN_ATTRIBUTES_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `TAG_ID` | Tagessorial Id | NUMBER | 22 | 6 | N |
| 3 | `ATTRIBUTE_NAME` | Attribute Name | VARCHAR2 | 60 |  | N |
| 4 | `ATTRIBUTE_VALUE` | Attribute Name | VARCHAR2 | 60 |  | N |

## `S_JAVA_SCREEN_ATTRIBUTES_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `TAG_ID` | Tagessorial Id | NUMBER | 22 | 6 | N |
| 3 | `PARENT_TAG_ID` | Parent_Tagessorial Id | NUMBER | 22 | 6 | N |
| 4 | `TAG_NAME` | Tagessorial Name | VARCHAR2 | 60 |  | N |

## `S_JAVA_SCREEN_COMPONENT_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `COMPONENT_ID` | Componentessorial Id | NUMBER | 22 | 6 | N |
| 3 | `ATTRIBUTE_NAME` | Attribute Name | VARCHAR2 | 60 |  | N |
| 4 | `ATTRIBUTE_VALUE` | Attribute Name | VARCHAR2 | 60 |  | N |

## `S_JAVA_SCREEN_COMPONENT_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `COMPONENT_ID` | Componentessorial Id | NUMBER | 22 | 6 | N |
| 3 | `PARENT_COMPONENT_ID` | Parent_Componentessorial Id | NUMBER | 22 | 6 | N |

## `S_JAVA_TRANSL_LABEL`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `COL_CODE` | Colessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 60 |  | Y |

## `S_JAVA_TRANSL_MENU`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `MENU_CODE` | Menuessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `MENU_TEXT` | Menuessorial Text | VARCHAR2 | 60 |  | N |
| 6 | `MENU_LET` | Menuessorial Let | VARCHAR2 | 30 |  | Y |

## `S_JAVA_TRANSL_MES`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `TRANSL_MES_CODE` | Transl_Mesessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `TRANSL_MES_TEXT` | Transl_Mesessorial Text | VARCHAR2 | 60 |  | Y |

## `S_JAVA_TRANSL_PANEL`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `PANEL_CODE` | Panelessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `PANEL_TEXT` | Panelessorial Text | VARCHAR2 | 60 |  | Y |

## `S_JAVA_TRANSL_TITLE`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 4 | `TITLE_TEXT` | Titleessorial Text | VARCHAR2 | 60 |  | Y |

## `S_JOB_ACCESS`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_ACCESS` | Jobessorial Access | VARCHAR2 | 5 |  | N |
| 2 | `JOB_ACCESS_LAST_DATE` | Job_Access_Lastessorial Date | DATE | 7 |  | Y |

## `S_LANG_REP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `LANG_REP_SEARCH_TEXT` | Lang_Rep_Searchessorial Text | VARCHAR2 | 60 |  | N |
| 4 | `LANG_REP_MAX_COL_WID` | Lang_Rep_Max_Colessorial Wid | NUMBER | 22 | 3 | N |
| 5 | `LANG_REP_REPLACE_TEXT` | Lang_Rep_Replaceessorial Text | VARCHAR2 | 60 |  | Y |

## `S_LINEAR_MEAS_FACT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 2 | `LINEAR_MEAS_DES` | Linear_Measessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `LINEAR_MEAS_FACT` | Linear_Measessorial Fact | NUMBER | 22 | 8 | N |
| 4 | `LINEAR_MEAS_FORMAT` | Linear_Measessorial Format | VARCHAR2 | 20 |  | N |

## `S_MODU_D1`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MODU_CODE` | Moduessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `MODU_REM_LINE_NUM` | Modu_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `MODU_REM_LINE_TEXT` | Modu_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `S_MODU_D2`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MODU_CODE` | Moduessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `STRUCT_CODE` | Structessorial Code | VARCHAR2 | 20 |  | N |

## `S_MODU_D3`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MODU_CODE` | Moduessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `MODU_CODE_CALL` | Modu_Codeessorial Call | VARCHAR2 | 20 |  | N |

## `S_MODU_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MODU_CODE` | Moduessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `MODU_DES` | Moduessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `MODU_STAT` | Moduessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `PROG_FILE_CODE` | Prog_Fileessorial Code | VARCHAR2 | 20 |  | Y |
| 5 | `MODU_DIR` | Moduessorial Dir | VARCHAR2 | 100 |  | Y |

## `S_MS_U_NUM`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MS_SPC_CODE` | Ms_Spcessorial Code | VARCHAR2 | 30 |  | N |
| 2 | `MS_NXT_U_NUM` | Ms_Nxt_Uessorial Num | NUMBER | 22 | 6 | N |
| 3 | `MS_LAST_DATE` | Ms_Lastessorial Date | DATE | 7 |  | Y |

## `S_OP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `S_PROG_FILE`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PROG_FILE_CODE` | Prog_Fileessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `PROG_FILE_DES` | Prog_Fileessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `PROG_FILE_STAT` | Prog_Fileessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |

## `S_PROS_ID`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PROS_ID_NAME` | Pros_Idessorial Name | VARCHAR2 | 30 |  | N |
| 2 | `PROS_ID_NUM` | Pros_Idessorial Num | NUMBER | 22 | 9 | N |

## `S_PRT_COL`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COL_CODE` | Colessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `COL_SEQ_NUM` | Col_Seqessorial Num | NUMBER | 22 | 3 | N |
| 4 | `BASE_TABLE_CODE` | Base_Tableessorial Code | VARCHAR2 | 30 |  | N |
| 5 | `JOIN_TABLE_CODE` | Join_Tableessorial Code | VARCHAR2 | 30 |  | Y |
| 6 | `COL_DEPTH_NUM` | Col_Depthessorial Num | NUMBER | 22 | 3 | N |
| 7 | `COL_JOIN_CODE` | Col_Joinessorial Code | VARCHAR2 | 30 |  | Y |

## `S_PRT_EXE`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_EXE_CODE` | Prt_Exeessorial Code | VARCHAR2 | 10 |  | N |

## `S_REP_D1`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `SUB_REP_NAME` | Sub_Repessorial Name | VARCHAR2 | 30 |  | N |

## `S_REP_D2`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `REP_PROMPT_PROF_CODE` | Rep_Prompt_Professorial Code | VARCHAR2 | 20 |  | N |
| 3 | `REP_PROMPT_SEQ_NUM` | Rep_Prompt_Seqessorial Num | NUMBER | 22 | 4 | N |
| 4 | `REP_PROMPT_SQL_FLAG` | Rep_Prompt_Sqlessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `REP_PROMPT_DEP_TP` | Rep_Prompt_Depessorial Tp | VARCHAR2 | 20 |  | Y |

## `S_REP_D2D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `REP_PROMPT_PROF_CODE` | Rep_Prompt_Professorial Code | VARCHAR2 | 20 |  | N |
| 3 | `REP_PROMPT_PROF_CODE_DEP` | Rep_Prompt_Prof_Codeessorial Dep | VARCHAR2 | 20 |  | N |

## `S_REP_D3`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `REP_PARA_NAME` | Rep_Paraessorial Name | VARCHAR2 | 250 |  | N |
| 3 | `REP_PARA_VAL` | Rep_Paraessorial Val | VARCHAR2 | 250 |  | N |

## `S_REP_D4`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `SQL_NAME` | Sqlessorial Name | VARCHAR2 | 100 |  | N |

## `S_REP_D4D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `SQL_NAME` | Sqlessorial Name | VARCHAR2 | 100 |  | N |
| 3 | `COL_NAME` | Column Name | VARCHAR2 | 40 |  | N |
| 4 | `COL_TP_FLAG` | Col_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `COL_SEQ_NUM` | Col_Seqessorial Num | NUMBER | 22 | 4 | N |

## `S_REP_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `REP_DES` | Repessorial Des | VARCHAR2 | 60 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 4 | `SCH_PROF_CODE` | Sch_Professorial Code | VARCHAR2 | 10 |  | N |
| 5 | `REP_VIRTUAL_DIR` | Rep_Virtualessorial Dir | VARCHAR2 | 40 |  | N |
| 6 | `REP_TP_FLAG` | Rep_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `S_REP_PARA_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_PARA_SEQ_NUM` | Rep_Para_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `REP_PARA_LINE_NUM` | Rep_Para_Lineessorial Num | NUMBER | 22 | 2 | N |
| 3 | `REP_PARA_NAME` | Rep_Paraessorial Name | VARCHAR2 | 50 |  | N |
| 4 | `REP_PARA_VAL` | Rep_Paraessorial Val | VARCHAR2 | 50 |  | Y |

## `S_REP_PARA_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_PARA_SEQ_NUM` | Rep_Para_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `D4_JOB_NUM` | D4_Jobessorial Num | NUMBER | 22 | 6 | N |
| 4 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |

## `S_REP_PROMPT_DEP_TP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_PROMPT_DEP_TP` | Rep_Prompt_Depessorial Tp | VARCHAR2 | 20 |  | N |
| 2 | `REP_PROMPT_TP_DES` | Rep_Prompt_Tpessorial Des | VARCHAR2 | 60 |  | N |

## `S_REP_PROMPT_PROF`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_PROMPT_PROF_CODE` | Rep_Prompt_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `REP_PROMPT_PROF_DES` | Rep_Prompt_Professorial Des | VARCHAR2 | 60 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 4 | `REP_PROMPT_LABEL_DEFAULT` | Rep_Prompt_Labelessorial Default | VARCHAR2 | 60 |  | N |
| 5 | `REP_PROMPT_TP_CODE` | Rep_Prompt_Tpessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 7 | `REP_PROMPT_LABEL_OVERRIDE` | Rep_Prompt_Labelessorial Override | VARCHAR2 | 40 |  | Y |
| 8 | `REP_PROMPT_VAL_DEFAULT` | Rep_Prompt_Valessorial Default | VARCHAR2 | 60 |  | Y |
| 9 | `REP_PROMPT_NAME` | Rep_Promptessorial Name | VARCHAR2 | 60 |  | Y |
| 10 | `ENTRY_MES_NUM` | Entry_Mesessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `ERR_MES_NUM` | Err_Mesessorial Num | NUMBER | 22 | 9 | Y |

## `S_REP_PROMPT_TP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `REP_PROMPT_TP_CODE` | Rep_Prompt_Tpessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `REP_PROMPT_TP_DES` | Rep_Prompt_Tpessorial Des | VARCHAR2 | 60 |  | N |
| 3 | `REP_PROMPT_TP_FLAG` | Rep_Prompt_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `S_SCH_PROF_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SCH_PROF_CODE` | Sch_Professorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |

## `S_SCH_PROF_DD`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SCH_PROF_CODE` | Sch_Professorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 3 | `SCH_PROF_PARA_NAME` | Sch_Prof_Paraessorial Name | VARCHAR2 | 20 |  | N |
| 4 | `SCH_PROF_PARA_VAL` | Sch_Prof_Paraessorial Val | VARCHAR2 | 250 |  | Y |

## `S_SCH_PROF_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SCH_PROF_CODE` | Sch_Professorial Code | VARCHAR2 | 10 |  | N |
| 2 | `SCH_PROF_DES` | Sch_Professorial Des | VARCHAR2 | 30 |  | N |

## `S_SCR_CLIENT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLIENT_CODE` | Clientessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `CLIENT_DES` | Clientessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `SCR_SIZE` | Scressorial Size | NUMBER | 22 | 4 | N |
| 4 | `CLIENT_WHSE_MAND_FLAG` | Client_Whse_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SCAN_ENT_CODE` | Scan_Entessorial Code | VARCHAR2 | 20 |  | Y |
| 6 | `RF_TER_MAND_FLAG` | Rf_Ter_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `MAX_ALLOW_CART_CNT` | Max_Allow_Cartessorial Cnt | NUMBER | 22 | 4 | Y |
| 8 | `ALLOW_OVAGE_FLAG` | Allow_Ovageessorial Flag | VARCHAR2 | 1 |  | N |

## `S_SCR_FIELD_PARA`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 45 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `FIELD_SEQ_NUM` | Field_Seqessorial Num | NUMBER | 22 | 4 | N |
| 4 | `FIELD_ROW` | Fieldessorial Row | NUMBER | 22 | 4 | N |
| 5 | `FIELD_COL` | Fieldessorial Col | NUMBER | 22 | 4 | N |
| 6 | `DISPLAY_LEN` | Displayessorial Len | NUMBER | 22 | 4 | N |
| 7 | `DEFAULT_VALUE` | Defaultessorial Value | VARCHAR2 | 60 |  | Y |
| 8 | `ECHO_FLAG` | Echoessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `UPPERCASE_FLAG` | Uppercaseessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `ENTERABLE_FLAG` | Enterableessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `UPDATEABLE_FLAG` | Updateableessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `NULLABLE_FLAG` | Nullableessorial Flag | VARCHAR2 | 1 |  | N |

## `S_SCR_FIELD_PARAM_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `MENU_CODE` | Menuessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `FIELD_SEQ_NUM` | Field_Seqessorial Num | NUMBER | 22 | 4 | N |
| 4 | `FIELD_ROW` | Fieldessorial Row | NUMBER | 22 | 4 | Y |
| 5 | `FIELD_COL` | Fieldessorial Col | NUMBER | 22 | 4 | Y |
| 6 | `DISPLAY_LEN` | Displayessorial Len | NUMBER | 22 | 4 | Y |
| 7 | `DEFAULT_VALUE` | Defaultessorial Value | VARCHAR2 | 60 |  | Y |
| 8 | `ECHO_FLAG` | Echoessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `UPPERCASE_FLAG` | Uppercaseessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `ENTERABLE_FLAG` | Enterableessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `NULLABLE_FLAG` | Nullableessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |

## `S_SCR_FIELD_PARAM_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `FIELD_ROW` | Fieldessorial Row | NUMBER | 22 | 4 | N |
| 3 | `FIELD_COL` | Fieldessorial Col | NUMBER | 22 | 4 | N |
| 4 | `FIELD_LEN` | Fieldessorial Len | NUMBER | 22 | 4 | N |
| 5 | `FIELD_TP` | Fieldessorial Tp | VARCHAR2 | 9 |  | N |
| 6 | `FIELD_PRECISION` | Fieldessorial Precision | NUMBER | 22 | 4 | Y |
| 7 | `DISPLAY_LEN` | Displayessorial Len | NUMBER | 22 | 4 | N |
| 8 | `DEFAULT_VALUE` | Defaultessorial Value | VARCHAR2 | 60 |  | N |
| 9 | `ECHO_FLAG` | Echoessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `UPPERCASE_FLAG` | Uppercaseessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `ENTERABLE_FLAG` | Enterableessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `NULLABLE_FLAG` | Nullableessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_SCR_FIELD_PROMPT_DES`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 30 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 4 | N |
| 3 | `FIELD_PROMPT_DES` | Field_Promptessorial Des | VARCHAR2 | 60 |  | N |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_SCR_FLOW`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SCR_CODE` | Scressorial Code | VARCHAR2 | 4 |  | Y |
| 3 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 4 | `FLOW_PROS_CODE_NXT` | Flow_Pros_Codeessorial Nxt | VARCHAR2 | 4 |  | N |
| 5 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |

## `S_SCR_LABEL_PARA`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_VALUE` | Labelessorial Value | VARCHAR2 | 20 |  | N |
| 4 | `LABEL_ROW` | Labelessorial Row | NUMBER | 22 | 4 | N |
| 5 | `LABEL_COL` | Labelessorial Col | NUMBER | 22 | 4 | N |

## `S_SCR_LABEL_PARAM_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `MENU_CODE` | Menuessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_VALUE` | Labelessorial Value | VARCHAR2 | 20 |  | Y |
| 4 | `LABEL_ROW` | Labelessorial Row | NUMBER | 22 | 4 | Y |
| 5 | `LABEL_COL` | Labelessorial Col | NUMBER | 22 | 4 | Y |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |

## `S_SCR_LABEL_PARAM_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `LABEL_VALUE` | Labelessorial Value | VARCHAR2 | 20 |  | N |
| 3 | `LABEL_ROW` | Labelessorial Row | NUMBER | 22 | 4 | N |
| 4 | `LABEL_COL` | Labelessorial Col | NUMBER | 22 | 4 | N |
| 5 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_SCR_MENU`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MENU_CODE` | Menuessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `MENU_TP` | Menuessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_SCR_MES`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MES_CODE` | Message Code | VARCHAR2 | 30 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 512 |  | N |

## `S_SCR_MES_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MES_CODE` | Message Code | NUMBER | 22 | 9 | N |
| 2 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 20 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `S_SCR_SEL`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_CODE_SUBSYSTEM` | Sel_Codeessorial Subsystem | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 10 |  | Y |
| 4 | `SCR_CODE` | Scressorial Code | VARCHAR2 | 4 |  | Y |

## `S_SEL_ALTER`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ALTER_NUM` | Alteressorial Num | NUMBER | 22 | 6 | N |
| 2 | `ALTER_TP` | Alteressorial Tp | VARCHAR2 | 3 |  | N |
| 3 | `ALTER_DATE` | Alteressorial Date | DATE | 7 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 6 | `SEL_DES` | Selessorial Des | VARCHAR2 | 40 |  | N |
| 7 | `SEL_SUBSYS_CODE` | Sel_Subsysessorial Code | VARCHAR2 | 6 |  | Y |
| 8 | `SEL_SORT_SEQ` | Sel_Sortessorial Seq | NUMBER | 22 | 3 | Y |
| 9 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 11 | `SEL_REALIGN_FLAG` | Sel_Realignessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_SEL_COPY_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_COPY_TABLE_NAME` | Sel_Copy_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `SEL_COPY_PK2` | Sel_Copyessorial Pk2 | VARCHAR2 | 30 |  | Y |
| 4 | `SEL_COPY_PK3` | Sel_Copyessorial Pk3 | VARCHAR2 | 30 |  | Y |
| 5 | `SEL_COPY_PK4` | Sel_Copyessorial Pk4 | VARCHAR2 | 30 |  | Y |
| 6 | `SEL_COPY_PK5` | Sel_Copyessorial Pk5 | VARCHAR2 | 30 |  | Y |
| 7 | `SEL_COPY_PK6` | Sel_Copyessorial Pk6 | VARCHAR2 | 30 |  | Y |

## `S_SEL_COPY_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_COPY_TABLE_NAME` | Sel_Copy_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 3 | `SEL_COPY_STAT_COL` | Sel_Copy_Statessorial Col | VARCHAR2 | 40 |  | Y |
| 4 | `SEL_COPY_GLOBAL_FLAG` | Sel_Copy_Globalessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `SEL_COPY_PK1` | Sel_Copyessorial Pk1 | VARCHAR2 | 30 |  | Y |
| 6 | `SEL_COPY_PK2` | Sel_Copyessorial Pk2 | VARCHAR2 | 30 |  | Y |
| 7 | `SEL_COPY_PK3` | Sel_Copyessorial Pk3 | VARCHAR2 | 30 |  | Y |
| 8 | `SEL_COPY_SQL_ADD` | Sel_Copy_Sqlessorial Add | VARCHAR2 | 200 |  | Y |

## `S_SEL_COPY_LIST`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_CODE_CHILD` | Sel_Codeessorial Child | VARCHAR2 | 6 |  | Y |
| 3 | `SEL_COPY_PARTIAL_FLAG` | Sel_Copy_Partialessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_SRCE_PATCH`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SRCE_PATCH_NUM` | Srce_Patchessorial Num | VARCHAR2 | 20 |  | N |
| 2 | `SRCE_PATCH_DATE` | Srce_Patchessorial Date | DATE | 7 |  | N |

## `S_SRCE_VERS_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SRCE_VERS_NUM` | Srce_Versessorial Num | VARCHAR2 | 30 |  | N |
| 2 | `SRCE_VERS_REL_NUM` | Srce_Vers_Relessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `SRCE_VERS_REL_DATE` | Srce_Vers_Relessorial Date | DATE | 7 |  | N |
| 4 | `SRCE_VERS_REL_STAMP` | Srce_Vers_Relessorial Stamp | VARCHAR2 | 30 |  | Y |
| 5 | `SRCE_VERS_REL_ID` | Srce_Vers_Relessorial Id | NUMBER | 22 | 4 | Y |
| 6 | `SRCE_VERS_REL_SHORT` | Srce_Vers_Relessorial Short | VARCHAR2 | 8 |  | Y |

## `S_SRCE_VERS_DD`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SRCE_VERS_NUM` | Srce_Versessorial Num | VARCHAR2 | 30 |  | N |
| 2 | `SRCE_VERS_REL_NUM` | Srce_Vers_Relessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `SRCE_VERS_APP_CODE` | Srce_Vers_Appessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `SRCE_VERS_APP_SEQ_NUM` | Srce_Vers_App_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `SRCE_VERS_APP_REL_NUM` | Srce_Vers_App_Relessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `SRCE_VERS_APP_REL_DATE` | Srce_Vers_App_Relessorial Date | DATE | 7 |  | N |

## `S_SRCE_VERS_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SRCE_VERS_NUM` | Srce_Versessorial Num | VARCHAR2 | 30 |  | N |
| 2 | `SRCE_VERS_DATE` | Srce_Versessorial Date | DATE | 7 |  | N |

## `S_STRUCT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STRUCT_CODE` | Structessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `STRUCT_DES` | Structessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `STRUCT_STAT` | Structessorial Stat | VARCHAR2 | 1 |  | N |

## `S_T0`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ASS_PARA_OPT_CODE_UNQ` | Ass_Para_Opt_Codeessorial Unq | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 20 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 20 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 20 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 20 |  | Y |
| 9 | `START_VALUE` | Startessorial Value | VARCHAR2 | 20 |  | N |
| 10 | `END_VALUE` | Endessorial Value | VARCHAR2 | 20 |  | N |
| 11 | `NXT_VALUE` | Nxtessorial Value | VARCHAR2 | 20 |  | N |

## `S_T1`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ASS_PARA_OPT_CODE_WHEN` | Ass_Para_Opt_Codeessorial When | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 20 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 20 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 20 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 20 |  | Y |
| 9 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 10 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 11 | `CURRENT_DATE` | Currentessorial Date | DATE | 7 |  | Y |
| 12 | `EXPY_DATE` | Expyessorial Date | DATE | 7 |  | Y |
| 13 | `CRNT_VALUE` | Crntessorial Value | VARCHAR2 | 20 |  | N |

## `S_TAB_DOC_D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TABLE_CODE` | Tableessorial Code | VARCHAR2 | 30 |  | N |
| 2 | `TABLE_CODE_DEPENDANT` | Table_Codeessorial Dependant | VARCHAR2 | 30 |  | N |
| 3 | `TABLE_DEPEND_GLOBAL_COMP_FLAG` | Table_Depend_Global_Compessorial Flag | VARCHAR2 | 1 |  | N |

## `S_TAB_DOC_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TABLE_CODE` | Tableessorial Code | VARCHAR2 | 30 |  | N |
| 2 | `TABLE_GLOBAL_COMP_FLAG` | Table_Global_Compessorial Flag | VARCHAR2 | 1 |  | N |

## `S_TAX`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | N |
| 3 | `TAX_DES` | Taxessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TAX_STAT` | Taxessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CHG_CODE1` | Chgessorial Code1 | VARCHAR2 | 6 |  | Y |
| 6 | `TAX_DES1` | Taxessorial Des1 | VARCHAR2 | 10 |  | Y |
| 7 | `CHG_CODE2` | Chgessorial Code2 | VARCHAR2 | 6 |  | Y |
| 8 | `TAX_DES2` | Taxessorial Des2 | VARCHAR2 | 10 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_TER`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 5 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | Y |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 7 | `TER_LOG_FLAG` | Ter_Logessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `TER_REP_INFO` | Ter_Repessorial Info | VARCHAR2 | 255 |  | Y |
| 9 | `TER_REP_FILE_NAME` | Ter_Rep_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 10 | `TER_EXT_RESULT_VAL_NUM1` | Ter_Ext_Result_Valessorial Num1 | NUMBER | 22 |  | Y |
| 11 | `TER_EXT_RESULT_VAL_NUM2` | Ter_Ext_Result_Valessorial Num2 | NUMBER | 22 |  | Y |
| 12 | `TER_EXT_RESULT_VAL_NUM3` | Ter_Ext_Result_Valessorial Num3 | NUMBER | 22 |  | Y |
| 13 | `TER_EXT_RESULT_VAL_NUM4` | Ter_Ext_Result_Valessorial Num4 | NUMBER | 22 |  | Y |
| 14 | `TER_EXT_RESULT_VAL_NUM5` | Ter_Ext_Result_Valessorial Num5 | NUMBER | 22 |  | Y |
| 15 | `TER_EXT_RESULT_VAL_CHAR1` | Ter_Ext_Result_Valessorial Char1 | VARCHAR2 | 60 |  | Y |
| 16 | `TER_EXT_RESULT_VAL_CHAR2` | Ter_Ext_Result_Valessorial Char2 | VARCHAR2 | 60 |  | Y |
| 17 | `TER_EXT_RESULT_VAL_CHAR3` | Ter_Ext_Result_Valessorial Char3 | VARCHAR2 | 60 |  | Y |
| 18 | `TER_EXT_RESULT_VAL_CHAR4` | Ter_Ext_Result_Valessorial Char4 | VARCHAR2 | 60 |  | Y |
| 19 | `TER_EXT_RESULT_VAL_CHAR5` | Ter_Ext_Result_Valessorial Char5 | VARCHAR2 | 60 |  | Y |
| 20 | `TER_REP_INFO_LONG` | Ter_Rep_Infoessorial Long | VARCHAR2 | 2000 |  | Y |
| 21 | `D4_JOB_NUM` | D4_Jobessorial Num | NUMBER | 22 | 6 | Y |
| 22 | `MENU_SEL_CODE` | Menu_Selessorial Code | VARCHAR2 | 10 |  | Y |
| 23 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_TER_ADJ`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 17
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 5 | `INVT_AVAIL_OUT` | Invt_Availessorial Out | NUMBER | 22 | 9 | N |
| 6 | `NET_QTY_OUT` | Net_Qtyessorial Out | NUMBER | 22 | 9 | N |
| 7 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 8 | `INVT_AVAIL_IN` | Invt_Availessorial In | NUMBER | 22 | 9 | N |
| 9 | `NET_QTY_IN` | Net_Qtyessorial In | NUMBER | 22 | 9 | N |
| 10 | `NET_ENT_QTY_OUT` | Net_Ent_Qtyessorial Out | VARCHAR2 | 20 |  | Y |
| 11 | `NET_ENT_QTY_IN` | Net_Ent_Qtyessorial In | VARCHAR2 | 20 |  | Y |
| 12 | `NET_CNVC_QTY_IN` | Net_Cnvc_Qtyessorial In | NUMBER | 22 | 6 | Y |
| 13 | `NET_CNVC_QTY_OUT` | Net_Cnvc_Qtyessorial Out | NUMBER | 22 | 6 | Y |
| 14 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 16 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |

## `S_TER_ADJ_PROS`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 4 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 6 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 8 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 9 | `PROCESS_FLAG` | Processessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_TER_ADJ_PROS_TRF`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 7 | `PROCESS_FLAG` | Processessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_TER_EXT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_EXT_DATE` | Ter_Extessorial Date | DATE | 7 |  | N |
| 4 | `TER_EXT_LINE_NUM` | Ter_Ext_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `TER_EXT_LINE_TEXT` | Ter_Ext_Lineessorial Text | VARCHAR2 | 500 |  | Y |
| 6 | `TER_EXT_LINE_PROS_FLAG` | Ter_Ext_Line_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `TER_EXT_SORT_TEXT` | Ter_Ext_Sortessorial Text | VARCHAR2 | 40 |  | Y |

## `S_TER_FRT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `ORD_TO_SHIP_DATE_SCH` | Ord_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 8 | `ORD_TO_ARR_DATE_SCH` | Ord_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |
| 9 | `ORD_TOT_UNIT` | Ord_Totessorial Unit | NUMBER | 22 | 11 | Y |
| 10 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 12 | Y |
| 11 | `CON_NAME_MAN` | Con_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 12 | `ORD_ASSIGN_FLAG` | Ord_Assignessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_TER_LOC`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 19
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 7 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 8 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 9 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 11 | `NET_ADJ_QTY` | Net_Adjessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `NET_CNVC_QTY` | Net_Cnvcessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `ON_HAND_CNVC_QTY` | On_Hand_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 14 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 16 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 18 | `LOC_DEL_FLAG` | Loc_Delessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `HOLD_CODE_ORG` | Hold_Codeessorial Org | VARCHAR2 | 4 |  | Y |

## `S_TER_LOC_AUDIT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `NET_ADJ_QTY` | Net_Adjessorial Qty | NUMBER | 22 | 9 | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | N |
| 9 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |

## `S_TER_NUM`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_NUM` | Teressorial Num | NUMBER | 22 | 9 | N |
| 2 | `TER_NUM_DATE` | Ter_Numessorial Date | DATE | 7 |  | Y |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `S_TER_PALL`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PALL_ACC_TP` | Pall_Accessorial Tp | VARCHAR2 | 4 |  | N |
| 4 | `PALL_ACC_CODE` | Pall_Accessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `PALL_TRANS_TP` | Pall_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `PALL_TRANS_DATE` | Pall_Transessorial Date | DATE | 7 |  | N |
| 7 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `PALL_QTY` | Pallessorial Qty | NUMBER | 22 | 4 | N |
| 9 | `PALL_REF_DES` | Pall_Refessorial Des | VARCHAR2 | 60 |  | Y |

## `S_TER_REM`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `TER_REM_LINE_NUM` | Ter_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `TER_REM_LINE_TEXT` | Ter_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `S_TER_REP`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `TER_REP_FLAG` | Ter_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `TER_REP_PAGE_NUM` | Ter_Rep_Pageessorial Num | NUMBER | 22 | 4 | N |
| 4 | `TER_REP_LINE_NUM` | Ter_Rep_Lineessorial Num | NUMBER | 22 | 2 | N |
| 5 | `TER_REP_LINE_DATA` | Ter_Rep_Lineessorial Data | VARCHAR2 | 132 |  | Y |

## `S_TER_TRF_AUDIT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `TER_TRF_INS_UPD_FLAG` | Ter_Trf_Ins_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `INVT_AVAIL_OUT` | Invt_Availessorial Out | NUMBER | 22 | 9 | N |
| 8 | `NET_QTY_OUT` | Net_Qtyessorial Out | NUMBER | 22 | 9 | N |
| 9 | `NET_WGT_OUT` | Net_Wgtessorial Out | NUMBER | 22 | 11 | N |
| 10 | `NET_CUBE_OUT` | Net_Cubeessorial Out | NUMBER | 22 | 12 | N |
| 11 | `INVT_RECD_DATE` | Invt_Recdessorial Date | DATE | 7 |  | Y |
| 12 | `INVT_AVAIL_IN` | Invt_Availessorial In | NUMBER | 22 | 9 | N |
| 13 | `NET_QTY_IN` | Net_Qtyessorial In | NUMBER | 22 | 9 | N |
| 14 | `NET_WGT_IN` | Net_Wgtessorial In | NUMBER | 22 | 11 | N |
| 15 | `NET_CUBE_IN` | Net_Cubeessorial In | NUMBER | 22 | 12 | N |
| 16 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |

## `S_TIME_ZONE`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TIME_ZONE_CODE` | Time_Zoneessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `TIME_ZONE_DES` | Time_Zoneessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `TIME_ZONE_STAT` | Time_Zoneessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `TIME_ZONE_FACT` | Time_Zoneessorial Fact | VARCHAR2 | 4 |  | N |

## `S_TRAP_DIR`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRAP_DIR` | Trapessorial Dir | VARCHAR2 | 30 |  | N |

## `S_U_NUM`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `U_SPC_CODE` | U_Spcessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `U_SPC_NUM` | U_Spcessorial Num | NUMBER | 22 | 6 | N |
| 4 | `U_SPC_LAST_DATE` | U_Spc_Lastessorial Date | DATE | 7 |  | N |

## `S_U_NUM_FRT`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `U_SPC_CODE` | U_Spcessorial Code | VARCHAR2 | 30 |  | N |
| 4 | `U_SPC_NUM` | U_Spcessorial Num | NUMBER | 22 | 6 | N |
| 5 | `U_SPC_LAST_DATE` | U_Spc_Lastessorial Date | DATE | 7 |  | N |

## `S_VAL_PROF_D1`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 4 | `PROMPT_COL_NAME` | Prompt_Colessorial Name | VARCHAR2 | 40 |  | N |
| 5 | `PICK_LIST_PROF_CODE` | Pick_List_Professorial Code | VARCHAR2 | 20 |  | Y |

## `S_VAL_PROF_D1D`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `TAB_NAME` | Tabessorial Name | VARCHAR2 | 40 |  | N |
| 4 | `COL_NAME` | Column Name | VARCHAR2 | 40 |  | N |
| 5 | `COL_DEFAULT_VAL` | Col_Defaultessorial Val | VARCHAR2 | 100 |  | Y |

## `S_VAL_PROF_D2`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `VAL_PROF_STR` | Val_Professorial Str | VARCHAR2 | 250 |  | Y |
| 4 | `INTERNAL_GRP_CODE` | Internal_Grpessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `INTERNAL_GRP_DATA_TYPE` | Internal_Grp_Dataessorial Type | VARCHAR2 | 20 |  | Y |

## `S_VAL_PROF_D3`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `VAL_PROF_DATE_STR` | Val_Prof_Dateessorial Str | VARCHAR2 | 100 |  | Y |

## `S_VAL_PROF_D4`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `VAL_PROF_START_NUM` | Val_Prof_Startessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `VAL_PROF_END_NUM` | Val_Prof_Endessorial Num | NUMBER | 22 | 9 | Y |

## `S_VAL_PROF_D5`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `VAL_PROF_CHAR_EXPR` | Val_Prof_Charessorial Expr | VARCHAR2 | 40 |  | Y |
| 4 | `VAL_PROF_CHAR_VAL` | Val_Prof_Charessorial Val | VARCHAR2 | 40 |  | Y |

## `S_VAL_PROF_H`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VAL_PROF_CODE` | Val_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `VAL_PROF_DES` | Val_Professorial Des | VARCHAR2 | 30 |  | N |
| 3 | `VAL_PROF_TP` | Val_Professorial Tp | VARCHAR2 | 1 |  | N |

## `S_VAR_DOC`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `VAR_CODE` | Varessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `VAR_LINE_NUM` | Var_Lineessorial Num | NUMBER | 22 | 5 | N |
| 4 | `VAR_LINE_TEXT` | Var_Lineessorial Text | VARCHAR2 | 60 |  | N |
| 5 | `VAR_LINE_CONN_NUM` | Var_Line_Connessorial Num | NUMBER | 22 | 5 | N |
| 6 | `VAR_LINE_ROOT_FLAG` | Var_Line_Rootessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_VERS`

- **Tipo:** System Setup Related
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VERS_NUM` | Versessorial Num | VARCHAR2 | 20 |  | N |
| 2 | `VERS_DATE` | Versessorial Date | DATE | 7 |  | N |

## `T1`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `F1` | F1 | VARCHAR2 | 10 |  | Y |
| 2 | `F2` | F2 | VARCHAR2 | 10 |  | Y |

## `T2`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `F1` | F1 | CHAR | 10 |  | Y |
| 2 | `F2` | F2 | CHAR | 20 |  | Y |

## `TC_MVT_H`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 50
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, MVT_TRANS_TP, SKU_CODE, RCPT_NUM, ORD_NUM, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `MVT_TRANS_DATE` | Mvt_Transessorial Date | DATE | 7 |  | N |
| 3 | `MVT_CNT` | Mvtessorial Cnt | NUMBER | 22 | 6 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `MVT_LEV1` | Mvtessorial Lev1 | VARCHAR2 | 20 |  | N |
| 7 | `MVT_LEV2` | Mvtessorial Lev2 | VARCHAR2 | 20 |  | N |
| 8 | `MVT_LEV3` | Mvtessorial Lev3 | VARCHAR2 | 20 |  | N |
| 9 | `INVT_LEV_DES` | Invt_Levessorial Des | VARCHAR2 | 40 |  | Y |
| 10 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 11 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 12 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 13 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 15 | `TRANS_UNIT` | Transessorial Unit | NUMBER | 22 | 9 | N |
| 16 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 17 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 18 | `TRANS_WGT` | Transessorial Wgt | NUMBER | 22 | 11 | N |
| 19 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 11 | N |
| 20 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 21 | `TRANS_CUBE` | Transessorial Cube | NUMBER | 22 | 12 | N |
| 22 | `MVT_CUBE` | Mvtessorial Cube | NUMBER | 22 | 12 | N |
| 23 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 24 | `CARR_NAME_MAN` | Carr_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 25 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 26 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 27 | `SHIP_NAME_MAN` | Ship_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 28 | `RCPT_PREX` | Rcptessorial Prex | VARCHAR2 | 4 |  | Y |
| 29 | `RCPT_SUFX` | Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 30 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | Y |
| 31 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 32 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | Y |
| 33 | `RCPT_PRO_BILL_NUM` | Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 34 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 35 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 36 | `CON_NAME_MAN` | Con_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 37 | `SOLDTO_CODE` | Soldtoessorial Code | VARCHAR2 | 10 |  | Y |
| 38 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | Y |
| 39 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 40 | `ORD_NUM` | Order Number | NUMBER | 22 | 6 | Y |
| 41 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 42 | `ORD_TP` | Ordessorial Tp | VARCHAR2 | 1 |  | Y |
| 43 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 44 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 45 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 46 | `ADJ_CODE` | Adjessorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `ADJ_DES_MVT` | Adj_Desessorial Mvt | VARCHAR2 | 30 |  | Y |
| 48 | `MON_END_PROS_FLAG` | Mon_End_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `MVT_REP_FLAG` | Mvt_Repessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `TEMP_CONV_ITEM`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 54
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 4 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | Y |
| 5 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 6 | `CLASS_CODE` | Class Code | VARCHAR2 | 3 |  | Y |
| 7 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | VARCHAR2 | 3 |  | Y |
| 8 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | VARCHAR2 | 3 |  | Y |
| 9 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | VARCHAR2 | 3 |  | Y |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 11 | `ITEM_QTY_BKD_WGT_GROSS` | Item_Qty_Bkd_Wgtessorial Gross | VARCHAR2 | 15 |  | Y |
| 12 | `ITEM_QTY_BKD_LEN` | Item_Qty_Bkdessorial Len | VARCHAR2 | 8 |  | Y |
| 13 | `ITEM_QTY_BKD_WID` | Item_Qty_Bkdessorial Wid | VARCHAR2 | 8 |  | Y |
| 14 | `ITEM_QTY_BKD_HGT` | Item_Qty_Bkdessorial Hgt | VARCHAR2 | 8 |  | Y |
| 15 | `ITEM_QTY_BKD_WGT_NET` | Item_Qty_Bkd_Wgtessorial Net | VARCHAR2 | 15 |  | Y |
| 16 | `PALL_QTY` | Pallessorial Qty | VARCHAR2 | 6 |  | Y |
| 17 | `GENR_INFO_PROF_CODE` | Genr_Info_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `ITEM_BILL_PROF_CODE1` | Item_Bill_Professorial Code1 | VARCHAR2 | 4 |  | Y |
| 19 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | Y |
| 21 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | Y |
| 22 | `ITEM_QTY_BKD_CUBE` | Item_Qty_Bkdessorial Cube | VARCHAR2 | 10 |  | Y |
| 23 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 24 | `ITEM_VAR_QTY_BKD_FLAG` | Item_Var_Qty_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `ITEM_WGT_TP_CODE` | Item_Wgt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | Y |
| 27 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 28 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `ITEM_VALUE` | Itemessorial Value | VARCHAR2 | 11 |  | Y |
| 30 | `ITEM_QTY_BKD_BASE_NUM` | Item_Qty_Bkd_Baseessorial Num | VARCHAR2 | 13 |  | Y |
| 31 | `VAR_QTY_BKD_QTY1` | Var_Qty_Bkdessorial Qty1 | VARCHAR2 | 4 |  | Y |
| 32 | `VAR_QTY_BKD_QTY2` | Var_Qty_Bkdessorial Qty2 | VARCHAR2 | 4 |  | Y |
| 33 | `VAR_QTY_BKD_QTY3` | Var_Qty_Bkdessorial Qty3 | VARCHAR2 | 4 |  | Y |
| 34 | `VAR_QTY_BKD_QTY4` | Var_Qty_Bkdessorial Qty4 | VARCHAR2 | 4 |  | Y |
| 35 | `VAR_QTY_BKD_QTY5` | Var_Qty_Bkdessorial Qty5 | VARCHAR2 | 4 |  | Y |
| 36 | `PROS_PROF_CODE` | Pros_Professorial Code | VARCHAR2 | 4 |  | Y |
| 37 | `SHIP_PROF_CODE` | Ship_Professorial Code | VARCHAR2 | 4 |  | Y |
| 38 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 39 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 40 | `ALT_INVT_REP_UPC_CODE` | Alt_Invt_Rep_Upcessorial Code | VARCHAR2 | 20 |  | Y |
| 41 | `CONV_UPD_FLAG` | Conv_Updessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `NUM_OPEN_DAY` | Num_Openessorial Day | VARCHAR2 | 3 |  | Y |
| 43 | `ITEM_BILL_PROF_CODE2` | Item_Bill_Professorial Code2 | VARCHAR2 | 4 |  | Y |
| 44 | `ITEM_BILL_PROF_CODE3` | Item_Bill_Professorial Code3 | VARCHAR2 | 4 |  | Y |
| 45 | `ITEM_VAL_PROF_CODE` | Item_Val_Professorial Code | VARCHAR2 | 4 |  | Y |
| 46 | `VOL_MEAS_CODE` | Vol_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `ITEM_QTY_BKD_VOL` | Item_Qty_Bkdessorial Vol | VARCHAR2 | 15 |  | Y |
| 48 | `ALLOW_ENTRY_LEV_NUM` | Allow_Entry_Levessorial Num | VARCHAR2 | 1 |  | Y |
| 49 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 50 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | Y |
| 51 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 52 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 4 |  | Y |
| 53 | `ITEM_CRS_DOCK_FLAG` | Item_Crs_Dockessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `ITEM_KIT_FLAG` | Item_Kitessorial Flag | VARCHAR2 | 1 |  | Y |

## `TEST`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TEST_TXT` | Testessorial Txt | VARCHAR2 | 100 |  | Y |

## `TEST_C_LAB`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LAB_DATE` | Labessorial Date | DATE | 7 |  | N |
| 6 | `LAB_TP_FLAG` | Lab_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `DOC_NUM` | Document Number | NUMBER | 22 | 6 | Y |
| 8 | `LAB_HOUR` | Labessorial Hour | NUMBER | 22 | 3 | Y |
| 9 | `LAB_MIN` | Labessorial Min | NUMBER | 22 | 4 | Y |
| 10 | `LAB_SYS_FLAG` | Lab_Sysessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `LAB_DES` | Labessorial Des | VARCHAR2 | 40 |  | Y |
| 12 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 13 | `LAB_UNIT` | Labessorial Unit | NUMBER | 22 | 9 | Y |
| 14 | `LAB_WGT` | Labessorial Wgt | NUMBER | 22 | 9 | Y |

## `TEST_E_SHIP_H`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_NUM` | Shipessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_ROUTE_ID` | Ship_Routeessorial Id | VARCHAR2 | 10 |  | N |
| 5 | `SHIP_LANE_ID` | Ship_Laneessorial Id | VARCHAR2 | 10 |  | N |
| 6 | `SHIP_TRUCK_NUM` | Ship_Truckessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `SHIP_EQP_NUM` | Ship_Eqpessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `SHIP_DRV_NUM` | Ship_Drvessorial Num | VARCHAR2 | 10 |  | Y |
| 9 | `SHIP_DRV_NAME` | Ship_Drvessorial Name | VARCHAR2 | 30 |  | Y |
| 10 | `SHIP_START_DATE` | Ship_Startessorial Date | DATE | 7 |  | N |
| 11 | `SHIP_END_DATE` | Ship_Endessorial Date | DATE | 7 |  | Y |
| 12 | `SHIP_TOT_CART` | Ship_Totessorial Cart | NUMBER | 22 | 9 | Y |
| 13 | `SHIP_PRT_DATE` | Ship_Prtessorial Date | DATE | 7 |  | Y |
| 14 | `SHIP_PRT_CNT` | Ship_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 15 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 16 | `SHIP_EDI_PRT_DATE` | Ship_Edi_Prtessorial Date | DATE | 7 |  | Y |
| 17 | `SHIP_EDI_PRT_CNT` | Ship_Edi_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 18 | `SHIP_NUM_BOL_NUM` | Ship_Num_Bolessorial Num | NUMBER | 22 | 6 | Y |
| 19 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |

## `TEST_RF_PROF`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RF_PROF_CODE` | Rf_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RF_PROF_DES` | Rf_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `RF_PROF_STAT` | Rf_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `RF_PROF_CALC_VARI_TP` | Rf_Prof_Calc_Variessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `RF_PROF_ALLOW_LOAD_PICK_FLAG` | Rf_Prof_Allow_Load_Pickessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `RF_PROF_VAL_LEV_NUM` | Rf_Prof_Val_Levessorial Num | NUMBER | 22 | 1 | Y |
| 8 | `RF_PROF_DEF_QTY_FLAG` | Rf_Prof_Def_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `RF_PROF_VAL_PICK_RELO_FLAG` | Rf_Prof_Val_Pick_Reloessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `RF_PROF_VAL_PICK_PUT_FLAG` | Rf_Prof_Val_Pick_Putessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `RF_PROF_QU_RESULT_FLAG` | Rf_Prof_Qu_Resultessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `RF_PROF_RCPT_FLAG` | Rf_Prof_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `RF_PROF_RCPT_LINE_FLAG` | Rf_Prof_Rcpt_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `RF_PROF_CUST_FLAG` | Rf_Prof_Custessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `RF_PROF_INVT_LEV1_FLAG` | Rf_Prof_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `RF_PROF_INVT_LEV2_FLAG` | Rf_Prof_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `RF_PROF_INVT_LEV3_FLAG` | Rf_Prof_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `RF_PROF_INVT_LEV4_FLAG` | Rf_Prof_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `RF_PROF_WHSE_FLAG` | Rf_Prof_Whseessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `RF_PROF_QTY_FLAG` | Rf_Prof_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `RF_PROF_HOLD_FLAG` | Rf_Prof_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `RF_PROF_DISP_ORD_LINE_FLAG` | Rf_Prof_Disp_Ord_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `SCAN_PROF_CODE` | Scan_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `RF_PROF_SCAN_PROF_FLAG` | Rf_Prof_Scan_Professorial Flag | VARCHAR2 | 1 |  | N |

## `TMP_MVT_H`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, MVT_TRANS_TP, INVT_LEV1, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 7 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 11 | `START_DATE` | Startessorial Date | VARCHAR2 | 9 |  | Y |
| 12 | `END_DATE` | Endessorial Date | VARCHAR2 | 9 |  | Y |
| 13 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 14 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 15 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |
| 16 | `DOC_NUM` | Document Number | NUMBER | 22 | 6 | N |
| 17 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 18 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 19 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 20 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |

## `TMP_UPD`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_CODE` | Document Code | CHAR | 4 |  | Y |
| 5 | `CYC_CNT_INCL_EMPTY_LOC_FLAG` | Cyc_Cnt_Incl_Empty_Locessorial Flag | CHAR | 1 |  | Y |
| 6 | `CYC_CNT_ALLOW_DUP_PER_LOC_FLAG` | Cyc_Cnt_Allow_Dup_Per_Locessorial Flag | CHAR | 1 |  | Y |
| 7 | `CYC_CNT_SHOW_INVT_LEV1_FLAG` | Cyc_Cnt_Show_Invt_Lev1essorial Flag | CHAR | 1 |  | Y |
| 8 | `CYC_CNT_SHOW_INVT_LEV2_FLAG` | Cyc_Cnt_Show_Invt_Lev2essorial Flag | CHAR | 1 |  | Y |
| 9 | `CYC_CNT_SHOW_INVT_LEV3_FLAG` | Cyc_Cnt_Show_Invt_Lev3essorial Flag | CHAR | 1 |  | Y |
| 10 | `CYC_CNT_SHOW_INVT_LEV4_FLAG` | Cyc_Cnt_Show_Invt_Lev4essorial Flag | CHAR | 1 |  | Y |

## `TRAN10`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 20
- **Campos-chave prováveis:** CUST_CODE, MVT_TRANS_TP, INVT_LEV1, INVT_LEV2, COMP_CODE, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |
| 6 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 7 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 8 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 13 | `COMP_NAME` | Compessorial Name | VARCHAR2 | 30 |  | N |
| 14 | `MVT_WGT_NET` | Mvt_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `REF` | Refessorial Ref | VARCHAR2 | 4000 |  | Y |
| 16 | `DES1` | Desessorial Des1 | VARCHAR2 | 4000 |  | Y |
| 17 | `TERM2` | Termessorial Term2 | VARCHAR2 | 4000 |  | Y |
| 18 | `TERM3` | Termessorial Term3 | VARCHAR2 | 4000 |  | Y |
| 19 | `TERM4` | Termessorial Term4 | VARCHAR2 | 4000 |  | Y |
| 20 | `TERM1` | Termessorial Term1 | VARCHAR2 | 4000 |  | Y |

## `T_ACT_BLIND_PROS`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_BLIND_PROS_SEQ_NUM` | Act_Blind_Pros_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | N |
| 3 | `ACT_TP_CODE` | Act_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `ACT_BLIND_PROS_SCAN_DATE` | Act_Blind_Pros_Scanessorial Date | DATE | 7 |  | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 14 | `ACT_BLIND_PROS_QTY` | Act_Blind_Prosessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `ACT_BLIND_PROS_WGT` | Act_Blind_Prosessorial Wgt | NUMBER | 22 | 16 | Y |
| 16 | `ACT_BLIND_PROS_WGT_NET` | Act_Blind_Pros_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 17 | `ACT_BLIND_PROS_CUBE` | Act_Blind_Prosessorial Cube | NUMBER | 22 | 16 | Y |
| 18 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 19 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 20 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 21 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 22 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 23 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 24 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 26 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 27 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | Y |
| 28 | `DOC_TP_CODE` | Doc_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `T_ASS_GRP`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE, INVT_LEV1, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ASS_GRP_SEQ_NUM` | Ass_Grp_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 10 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 12 | `ASS_GRP_CODE` | Ass_Grpessorial Code | VARCHAR2 | 2000 |  | Y |
| 13 | `ASS_GRP_CODE_NEXT` | Ass_Grp_Codeessorial Next | VARCHAR2 | 2000 |  | Y |
| 14 | `ASS_GRP_CODE_LAST` | Ass_Grp_Codeessorial Last | VARCHAR2 | 2000 |  | Y |
| 15 | `ASS_GRP_CODE_ORD_CNT` | Ass_Grp_Code_Ordessorial Cnt | NUMBER | 22 | 9 | Y |
| 16 | `ASS_GRP_NUM` | Ass_Grpessorial Num | NUMBER | 22 | 9 | Y |
| 17 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 18 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | N |
| 19 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 20 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 21 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 22 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |

## `T_ASS_TASK`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 27
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | N |
| 7 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 8 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 12 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 13 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 14 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 15 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 16 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 17 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 18 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 19 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 20 | `ASS_SKIP_FLAG` | Ass_Skipessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 22 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 23 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 24 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | Y |
| 25 | `AUDIT_MESSAGE` | Auditessorial Message | VARCHAR2 | 500 |  | Y |
| 26 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 27 | `ASS_TASK_SRCE_TP_CODE` | Ass_Task_Srce_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `T_AUDIT_DATA`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `AUD_FIELD1` | Audessorial Field1 | VARCHAR2 | 100 |  | Y |
| 2 | `AUD_FIELD2` | Audessorial Field2 | VARCHAR2 | 100 |  | Y |
| 3 | `AUD_FIELD3` | Audessorial Field3 | VARCHAR2 | 100 |  | Y |
| 4 | `AUD_FIELD4` | Audessorial Field4 | VARCHAR2 | 100 |  | Y |
| 5 | `AUD_FIELD5` | Audessorial Field5 | VARCHAR2 | 100 |  | Y |
| 6 | `AUD_FIELD6` | Audessorial Field6 | VARCHAR2 | 100 |  | Y |
| 7 | `AUD_FIELD7` | Audessorial Field7 | VARCHAR2 | 100 |  | Y |
| 8 | `AUD_FIELD8` | Audessorial Field8 | VARCHAR2 | 100 |  | Y |
| 9 | `AUD_FIELD9` | Audessorial Field9 | VARCHAR2 | 100 |  | Y |
| 10 | `AUD_FIELD10` | Audessorial Field10 | VARCHAR2 | 100 |  | Y |

## `T_DSHB_REPORT`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 27
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `RUN_TIME_TER_CODE` | Run_Time_Teressorial Code | VARCHAR2 | 10 |  | Y |
| 5 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 6 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 8 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 9 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 10 | `LAB_TP_FLAG` | Lab_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 12 | `LAB_START_DATE` | Lab_Startessorial Date | DATE | 7 |  | Y |
| 13 | `LAB_END_DATE` | Lab_Endessorial Date | DATE | 7 |  | Y |
| 14 | `DIRECT_TIME` | Directessorial Time | NUMBER | 22 | 16 | Y |
| 15 | `INDIRECT_TIME` | Indirectessorial Time | NUMBER | 22 | 16 | Y |
| 16 | `CLASS_QTY` | Classessorial Qty | NUMBER | 22 | 12 | Y |
| 17 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | Y |
| 18 | `SESSION_ID` | Sessionessorial Id | VARCHAR2 | 16 |  | Y |
| 19 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 20 | `LOW_QTY` | Lowessorial Qty | NUMBER | 22 | 12 | Y |
| 21 | `MVT_WGT_NET` | Mvt_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 22 | `ACTUAL_TIME` | Actualessorial Time | NUMBER | 22 | 16 | Y |
| 23 | `IDLE_TIME` | Idleessorial Time | NUMBER | 22 | 16 | Y |
| 24 | `CUST_TIME` | Custessorial Time | NUMBER | 22 | 16 | Y |
| 25 | `ADJACENT_CUST_TIME` | Adjacent_Custessorial Time | NUMBER | 22 | 16 | Y |
| 26 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 27 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |

## `T_EXE_JOB_D1`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE_DEL4` | Exe_Job_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 2 | `EXE_JOB_TRIG_SEQ_NUM_DEL4` | Exe_Job_Trig_Seq_Numessorial Del4 | VARCHAR2 | 2 |  | Y |
| 3 | `EXE_JOB_TRIG_NAME_DEL4` | Exe_Job_Trig_Nameessorial Del4 | VARCHAR2 | 30 |  | Y |
| 4 | `EXE_JOB_TRIG_DES_DEL4` | Exe_Job_Trig_Desessorial Del4 | VARCHAR2 | 30 |  | Y |

## `T_EXE_JOB_D2`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE_DEL4` | Exe_Job_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 2 | `EXE_JOB_LOCK_CODE_DEL4` | Exe_Job_Lock_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |

## `T_EXE_JOB_D3`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE_DEL4` | Exe_Job_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 2 | `EXE_JOB_FMT_CODE_DEL4` | Exe_Job_Fmt_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 3 | `EXE_JOB_FMT_DES_DEL4` | Exe_Job_Fmt_Desessorial Del4 | VARCHAR2 | 30 |  | Y |
| 4 | `EXE_JOB_FMT_EXE_JOB_DEL4` | Exe_Job_Fmt_Exe_Jobessorial Del4 | VARCHAR2 | 10 |  | Y |

## `T_EXE_JOB_H`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EXE_JOB_CODE_DEL4` | Exe_Job_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 2 | `EXE_JOB_DES_DEL4` | Exe_Job_Desessorial Del4 | VARCHAR2 | 30 |  | Y |
| 3 | `EXE_JOB_OP_REQ_FLAG_DEL4` | Exe_Job_Op_Req_Flagessorial Del4 | VARCHAR2 | 1 |  | Y |
| 4 | `EXE_JOB_PRT_JOB_FLAG_DEL4` | Exe_Job_Prt_Job_Flagessorial Del4 | VARCHAR2 | 1 |  | Y |
| 5 | `EXE_JOB_SEQ_SEL_FLAG_DEL4` | Exe_Job_Seq_Sel_Flagessorial Del4 | VARCHAR2 | 1 |  | Y |
| 6 | `TABLE_NAME_DEL4` | Table_Nameessorial Del4 | VARCHAR2 | 30 |  | Y |
| 7 | `PRT_EXE_CODE_DEL4` | Prt_Exe_Codeessorial Del4 | VARCHAR2 | 10 |  | Y |
| 8 | `EXE_JOB_QU_JOB_FLAG_DEL4` | Exe_Job_Qu_Job_Flagessorial Del4 | VARCHAR2 | 1 |  | Y |
| 9 | `EXE_JOB_CLASS_NAME_DEL4` | Exe_Job_Class_Nameessorial Del4 | VARCHAR2 | 60 |  | Y |

## `T_L_PO_103`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_KIT_LINE_NUM` | Ord_Kit_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ORD_KIT_INVT_LEV1` | Ord_Kit_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 6 | `ORD_KIT_ORD_QTY` | Ord_Kit_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 7 | `ORD_KIT_SHIP_QTY` | Ord_Kit_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `ORD_COMPN_LINE_NUM` | Ord_Compn_Lineessorial Num | NUMBER | 22 | 4 | N |
| 9 | `ORD_COMPN_INVT_LEV1` | Ord_Compn_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 10 | `ORD_COMPN_ORD_QTY` | Ord_Compn_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_COMPN_SHIP_QTY` | Ord_Compn_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `ORD_KIT_PROS_FLAG` | Ord_Kit_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `ORD_COMPN_WILL_SHIP_QTY` | Ord_Compn_Will_Shipessorial Qty | NUMBER | 22 | 9 | Y |

## `T_L_TRANSLOGIX_JOB_DATA`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CUSTOMER_CODE` | Customeressorial Code | VARCHAR2 | 20 |  | Y |
| 2 | `JOB_DATA_DATE` | Job_Dataessorial Date | DATE | 7 |  | Y |
| 3 | `JOB_DATA_NUM` | Job_Dataessorial Num | VARCHAR2 | 20 |  | Y |
| 4 | `JOB_DATA_CONS_REF` | Job_Data_Consessorial Ref | VARCHAR2 | 20 |  | Y |
| 5 | `JOB_DATA_DAIRY_REF` | Job_Data_Dairyessorial Ref | VARCHAR2 | 20 |  | Y |
| 6 | `JOB_DATA_QTY` | Job_Dataessorial Qty | NUMBER | 22 | 16 | Y |
| 7 | `JOB_DATA_PALL` | Job_Dataessorial Pall | NUMBER | 22 | 16 | Y |
| 8 | `JOB_DATA_WGT` | Job_Dataessorial Wgt | NUMBER | 22 | 16 | Y |
| 9 | `JOB_DATA_CUBE` | Job_Dataessorial Cube | NUMBER | 22 | 16 | Y |
| 10 | `JOB_DATA_REVENUE` | Job_Dataessorial Revenue | NUMBER | 22 | 16 | Y |
| 11 | `JOB_DATA_EXPENSE` | Job_Dataessorial Expense | NUMBER | 22 | 16 | Y |
| 12 | `JOB_DATA_PROFIT` | Job_Dataessorial Profit | NUMBER | 22 | 16 | Y |

## `T_MENU_UPD_AUD`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TABLE_NAME` | Tableessorial Name | VARCHAR2 | 30 |  | Y |
| 2 | `VALUE` | Valueessorial Value | VARCHAR2 | 30 |  | Y |
| 3 | `ACTION` | Actionessorial Action | VARCHAR2 | 4 |  | Y |
| 4 | `ACTION_DATE` | Actionessorial Date | DATE | 7 |  | Y |

## `T_MOVE_LOC_LIST`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_OP_223`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 7 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | N |

## `T_QD130`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 7
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 2 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 3 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 4 | `ROW_TOT` | Rowessorial Tot | NUMBER | 22 | 9 | N |
| 5 | `ROW_CAPC` | Rowessorial Capc | NUMBER | 22 | 9 | N |
| 6 | `ROW_USED` | Rowessorial Used | NUMBER | 22 | 9 | N |
| 7 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |

## `T_QD138`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 2 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 4 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 5 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |

## `T_SAMC_DOC`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 16 | N |
| 2 | `WORKSPACE_USER_ID` | Warehouse User Id | VARCHAR2 | 100 |  | N |
| 3 | `SAMC_DOC_TP_FLAG` | Samc_Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 7 | `DOC_SHIP_CON_CODE` | Doc_Ship_Conessorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `DOC_SHIP_CON_NAME` | Doc_Ship_Conessorial Name | VARCHAR2 | 30 |  | Y |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 11 | `FLOW_PROS_CODE_MAX` | Flow_Pros_Codeessorial Max | VARCHAR2 | 4 |  | Y |
| 12 | `FLOW_DATE` | Flow Date | DATE | 7 |  | Y |
| 13 | `FLOW_DATE_OP_CODE` | Flow_Date_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 14 | `DOC_DATE` | Docessorial Date | DATE | 7 |  | Y |
| 15 | `DOC_REF_NUM` | Doc_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 16 | `DOC_PRTY_NUM` | Doc_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 17 | `SAMC_DOC_LATE_FLAG` | Samc_Doc_Lateessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `SAMC_DOC_VARI_FLAG` | Samc_Doc_Variessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `SAMC_DOC_TOT_UNIT` | Samc_Doc_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 20 | `SAMC_DOC_TOT_PALL` | Samc_Doc_Totessorial Pall | NUMBER | 22 | 9 | Y |
| 21 | `SAMC_DOC_TOT_OPID` | Samc_Doc_Totessorial Opid | NUMBER | 22 | 9 | Y |
| 22 | `SAMC_DOC_TOT_WGT` | Samc_Doc_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 23 | `SAMC_DOC_TOT_WGT_NET` | Samc_Doc_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 24 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 25 | `SAMC_DOC_EST_LAB_TIME` | Samc_Doc_Est_Labessorial Time | NUMBER | 22 | 9 | Y |
| 26 | `SAMC_DOC_ACTUAL_LAB_TIME` | Samc_Doc_Actual_Labessorial Time | NUMBER | 22 | 9 | Y |
| 27 | `WHSE_CODE_STAG` | Whse_Codeessorial Stag | VARCHAR2 | 4 |  | Y |
| 28 | `LOC_CODE_STAG` | Loc_Codeessorial Stag | VARCHAR2 | 12 |  | Y |
| 29 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 30 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 31 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | Y |
| 32 | `APP_A1SCHEDULE_NUM` | App_A1Scheduleessorial Num | VARCHAR2 | 100 |  | Y |
| 33 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | N |
| 34 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SAMC_SUMM`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 28

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 16 | N |
| 2 | `WORKSPACE_USER_ID` | Warehouse User Id | VARCHAR2 | 100 |  | N |
| 3 | `SAMC_SUMM_ORD_CNT` | Samc_Summ_Ordessorial Cnt | NUMBER | 22 | 9 | Y |
| 4 | `SAMC_SUMM_ORD_LINE_CNT` | Samc_Summ_Ord_Lineessorial Cnt | NUMBER | 22 | 9 | Y |
| 5 | `SAMC_SUMM_ORD_ITEM_CNT` | Samc_Summ_Ord_Itemessorial Cnt | NUMBER | 22 | 9 | Y |
| 6 | `SAMC_SUMM_ORD_TOT_WGT` | Samc_Summ_Ord_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 7 | `SAMC_SUMM_ORD_TOT_WGT_NET` | Samc_Summ_Ord_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 8 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 9 | `SAMC_SUMM_ORD_TOT_UNIT` | Samc_Summ_Ord_Totessorial Unit | NUMBER | 22 | 16 | Y |
| 10 | `SAMC_SUMM_ORD_TOT_PALL` | Samc_Summ_Ord_Totessorial Pall | NUMBER | 22 | 16 | Y |
| 11 | `SAMC_SUMM_RCPT_CNT` | Samc_Summ_Rcptessorial Cnt | NUMBER | 22 | 9 | Y |
| 12 | `SAMC_SUMM_RCPT_LINE_CNT` | Samc_Summ_Rcpt_Lineessorial Cnt | NUMBER | 22 | 9 | Y |
| 13 | `SAMC_SUMM_RCPT_ITEM_CNT` | Samc_Summ_Rcpt_Itemessorial Cnt | NUMBER | 22 | 9 | Y |
| 14 | `SAMC_SUMM_RCPT_TOT_WGT` | Samc_Summ_Rcpt_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 15 | `SAMC_SUMM_RCPT_TOT_WGT_NET` | Samc_Summ_Rcpt_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 16 | `SAMC_SUMM_RCPT_TOT_UNIT` | Samc_Summ_Rcpt_Totessorial Unit | NUMBER | 22 | 16 | Y |
| 17 | `SAMC_SUMM_RCPT_TOT_PALL` | Samc_Summ_Rcpt_Totessorial Pall | NUMBER | 22 | 16 | Y |
| 18 | `SAMC_SUMM_RELO_CNT` | Samc_Summ_Reloessorial Cnt | NUMBER | 22 | 9 | Y |
| 19 | `SAMC_SUMM_RELO_TOT_WGT` | Samc_Summ_Relo_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 20 | `SAMC_SUMM_RELO_TOT_WGT_NET` | Samc_Summ_Relo_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 21 | `SAMC_SUMM_RELO_TOT_UNIT` | Samc_Summ_Relo_Totessorial Unit | NUMBER | 22 | 16 | Y |
| 22 | `SAMC_SUMM_REPI_CNT` | Samc_Summ_Repiessorial Cnt | NUMBER | 22 | 9 | Y |
| 23 | `SAMC_SUMM_REPI_TOT_WGT` | Samc_Summ_Repi_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 24 | `SAMC_SUMM_REPI_TOT_WGT_NET` | Samc_Summ_Repi_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 25 | `SAMC_SUMM_REPI_TOT_UNIT` | Samc_Summ_Repi_Totessorial Unit | NUMBER | 22 | 16 | Y |
| 26 | `SAMC_SUMM_CRM_CNT` | Samc_Summ_Crmessorial Cnt | NUMBER | 22 | 9 | Y |
| 27 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | N |
| 28 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SAMC_TASK`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 49
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 16 | N |
| 2 | `WORKSPACE_USER_ID` | Warehouse User Id | VARCHAR2 | 100 |  | N |
| 3 | `SAMC_TASK_TP_FLAG` | Samc_Task_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `DOC_TASK_SEQ_NUM` | Doc_Task_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 6 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 7 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 8 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 9 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 11 | `DOC_SHIP_CON_CODE` | Doc_Ship_Conessorial Code | VARCHAR2 | 10 |  | Y |
| 12 | `DOC_SHIP_CON_NAME` | Doc_Ship_Conessorial Name | VARCHAR2 | 30 |  | Y |
| 13 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 14 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 15 | `FLOW_PROS_CODE_MAX` | Flow_Pros_Codeessorial Max | VARCHAR2 | 4 |  | Y |
| 16 | `FLOW_DATE` | Flow Date | DATE | 7 |  | Y |
| 17 | `FLOW_DATE_OP_CODE` | Flow_Date_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 18 | `DOC_DATE` | Docessorial Date | DATE | 7 |  | Y |
| 19 | `DOC_REF_NUM` | Doc_Refessorial Num | VARCHAR2 | 100 |  | Y |
| 20 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 21 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 23 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 24 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 25 | `SAMC_TASK_TOT_UNIT` | Samc_Task_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 26 | `SAMC_TASK_TOT_PALL` | Samc_Task_Totessorial Pall | NUMBER | 22 | 9 | Y |
| 27 | `SAMC_TASK_TOT_WGT` | Samc_Task_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 28 | `SAMC_TASK_TOT_WGT_NET` | Samc_Task_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 29 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 30 | `SAMC_TASK_EST_LAB_TIME` | Samc_Task_Est_Labessorial Time | NUMBER | 22 | 9 | Y |
| 31 | `SAMC_TASK_ACTUAL_LAB_TIME` | Samc_Task_Actual_Labessorial Time | NUMBER | 22 | 9 | Y |
| 32 | `ISOL_CODE_FROM` | Isol_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 33 | `LOC_TP_CODE_FROM` | Loc_Tp_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 34 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 35 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 36 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 37 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 38 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 39 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 40 | `SAMC_TASK_STAT_CODE` | Samc_Task_Statessorial Code | VARCHAR2 | 4 |  | Y |
| 41 | `CRM_SRCE_REF_FLAG` | Crm_Srce_Refessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `CRM_CODE` | Crmessorial Code | VARCHAR2 | 4 |  | Y |
| 43 | `CRM_PCENT_COMPL` | Crm_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 44 | `OP_CODE_ASS` | Op_Codeessorial Ass | VARCHAR2 | 20 |  | Y |
| 45 | `SAMC_TASK_COMPL_FLAG` | Samc_Task_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 46 | `SAMC_TASK_LATE_FLAG` | Samc_Task_Lateessorial Flag | VARCHAR2 | 1 |  | Y |
| 47 | `SAMC_TASK_VARI_FLAG` | Samc_Task_Variessorial Flag | VARCHAR2 | 1 |  | Y |
| 48 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | N |
| 49 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SAMC_TASK_OP_ASS`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 16 | N |
| 2 | `SEQ_NUM_SAMC_TASK` | Seq_Num_Samcessorial Task | NUMBER | 22 | 16 | N |
| 3 | `OP_CODE_ASS` | Op_Codeessorial Ass | VARCHAR2 | 20 |  | Y |
| 4 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SAMC_TIME_BAR`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 17

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 16 | N |
| 2 | `WORKSPACE_USER_ID` | Warehouse User Id | VARCHAR2 | 100 |  | N |
| 3 | `SAMC_DATE` | Samcessorial Date | DATE | 7 |  | N |
| 4 | `SAMC_OPEN_ORD_UNIT_ASS` | Samc_Open_Ord_Unitessorial Ass | NUMBER | 22 | 9 | Y |
| 5 | `SAMC_OPEN_ORD_UNIT_NOT_ASS` | Samc_Open_Ord_Unit_Notessorial Ass | NUMBER | 22 | 9 | Y |
| 6 | `SAMC_CLOSE_ORD_UNIT` | Samc_Close_Ordessorial Unit | NUMBER | 22 | 9 | Y |
| 7 | `SAMC_OPEN_RCPT_UNIT_ASS` | Samc_Open_Rcpt_Unitessorial Ass | NUMBER | 22 | 9 | Y |
| 8 | `SAMC_OPEN_RCPT_UNIT_NOT_ASS` | Samc_Open_Rcpt_Unit_Notessorial Ass | NUMBER | 22 | 9 | Y |
| 9 | `SAMC_CLOSE_RCPT_UNIT` | Samc_Close_Rcptessorial Unit | NUMBER | 22 | 9 | Y |
| 10 | `SAMC_OPEN_REPI_UNIT_ASS` | Samc_Open_Repi_Unitessorial Ass | NUMBER | 22 | 9 | Y |
| 11 | `SAMC_OPEN_REPI_UNIT_NOT_ASS` | Samc_Open_Repi_Unit_Notessorial Ass | NUMBER | 22 | 9 | Y |
| 12 | `SAMC_CLOSE_REPI_UNIT` | Samc_Close_Repiessorial Unit | NUMBER | 22 | 9 | Y |
| 13 | `SAMC_OPEN_RELO_UNIT_ASS` | Samc_Open_Relo_Unitessorial Ass | NUMBER | 22 | 9 | Y |
| 14 | `SAMC_OPEN_RELO_UNIT_NOT_ASS` | Samc_Open_Relo_Unit_Notessorial Ass | NUMBER | 22 | 9 | Y |
| 15 | `SAMC_CLOSE_RELO_UNIT` | Samc_Close_Reloessorial Unit | NUMBER | 22 | 9 | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | N |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SCR_FIELD_PARA`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `FIELD_NAME` | Fieldessorial Name | VARCHAR2 | 45 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 4 | `FIELD_SEQ_NUM` | Field_Seqessorial Num | NUMBER | 22 | 4 | N |
| 5 | `FIELD_ROW` | Fieldessorial Row | NUMBER | 22 | 4 | N |
| 6 | `FIELD_COL` | Fieldessorial Col | NUMBER | 22 | 4 | N |
| 7 | `DISPLAY_LEN` | Displayessorial Len | NUMBER | 22 | 4 | N |
| 8 | `DEFAULT_VALUE` | Defaultessorial Value | VARCHAR2 | 60 |  | Y |
| 9 | `ECHO_FLAG` | Echoessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `UPPERCASE_FLAG` | Uppercaseessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `ENTERABLE_FLAG` | Enterableessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `UPDATEABLE_FLAG` | Updateableessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `NULLABLE_FLAG` | Nullableessorial Flag | VARCHAR2 | 1 |  | N |

## `T_SCR_LABEL_PARA`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 20 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_VALUE` | Labelessorial Value | VARCHAR2 | 20 |  | N |
| 4 | `LABEL_ROW` | Labelessorial Row | NUMBER | 22 | 4 | N |
| 5 | `LABEL_COL` | Labelessorial Col | NUMBER | 22 | 4 | N |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |

## `T_SCR_SEL`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_CODE_SUBSYSTEM` | Sel_Codeessorial Subsystem | VARCHAR2 | 6 |  | N |
| 3 | `LABEL_NAME` | Labelessorial Name | VARCHAR2 | 10 |  | Y |
| 4 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 5 | `SCR_CODE` | Scressorial Code | VARCHAR2 | 4 |  | Y |

## `T_SEL`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `SEL_DES` | Selessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `SEL_SUBSYS_CODE` | Sel_Subsysessorial Code | VARCHAR2 | 6 |  | Y |
| 4 | `SEL_SORT_SEQ` | Sel_Sortessorial Seq | NUMBER | 22 | 2 | Y |
| 5 | `SEL_VIS_FLAG` | Sel_Visessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 8 | `SEL_REALIGN_FLAG` | Sel_Realignessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 10 | `ISO_REF_CODE` | Iso_Refessorial Code | VARCHAR2 | 20 |  | Y |
| 11 | `FIRST_MENU` | Firstessorial Menu | VARCHAR2 | 4 |  | N |
| 12 | `REP_CODE` | Repessorial Code | VARCHAR2 | 20 |  | Y |

## `T_SKIP_TASK_LIST`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `ID` | ID | RAW | 32 |  | N |
| 3 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `T_SYNC_LOAD`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `LOAD_NUM_ORIG` | Load_Numessorial Orig | NUMBER | 22 | 6 | Y |
| 3 | `LOAD_NUM_NEW` | Load_Numessorial New | NUMBER | 22 | 6 | Y |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |

## `T_TASK_ENG_QUERY`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 5 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 8 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 10 | `RFOT_TEXT_QUERY_1_010` | Rfot_Text_Query_1essorial 010 | VARCHAR2 | 4000 |  | Y |
| 11 | `RFOT_TEXT_QUERY_2_010` | Rfot_Text_Query_2essorial 010 | VARCHAR2 | 4000 |  | Y |
| 12 | `RFOT_SAME_LOC_QUERY_1_020` | Rfot_Same_Loc_Query_1essorial 020 | VARCHAR2 | 4000 |  | Y |
| 13 | `RFOT_SAME_LOC_QUERY_2_020` | Rfot_Same_Loc_Query_2essorial 020 | VARCHAR2 | 4000 |  | Y |
| 14 | `RFOT_SAME_AISLE_QUERY_1_030` | Rfot_Same_Aisle_Query_1essorial 030 | VARCHAR2 | 4000 |  | Y |
| 15 | `RFOT_SAME_AISLE_QUERY_2_030` | Rfot_Same_Aisle_Query_2essorial 030 | VARCHAR2 | 4000 |  | Y |
| 16 | `RFOT_SAME_ZONE_QUERY_1_040` | Rfot_Same_Zone_Query_1essorial 040 | VARCHAR2 | 4000 |  | Y |
| 17 | `RFOT_SAME_ZONE_QUERY_2_040` | Rfot_Same_Zone_Query_2essorial 040 | VARCHAR2 | 4000 |  | Y |
| 18 | `RFOT_ALL_LOC_QUERY_1_050` | Rfot_All_Loc_Query_1essorial 050 | VARCHAR2 | 4000 |  | Y |
| 19 | `RFOT_ALL_LOC_QUERY_2_050` | Rfot_All_Loc_Query_2essorial 050 | VARCHAR2 | 4000 |  | Y |
| 20 | `ALL_TEXT_QUERY_1_060` | All_Text_Query_1essorial 060 | VARCHAR2 | 4000 |  | Y |
| 21 | `ALL_TEXT_QUERY_2_060` | All_Text_Query_2essorial 060 | VARCHAR2 | 4000 |  | Y |
| 22 | `ALL_SAME_LOC_QUERY_1_070` | All_Same_Loc_Query_1essorial 070 | VARCHAR2 | 4000 |  | Y |
| 23 | `ALL_SAME_LOC_QUERY_2_070` | All_Same_Loc_Query_2essorial 070 | VARCHAR2 | 4000 |  | Y |
| 24 | `ALL_SAME_AISLE_QUERY_1_080` | All_Same_Aisle_Query_1essorial 080 | VARCHAR2 | 4000 |  | Y |
| 25 | `ALL_SAME_AISLE_QUERY_2_080` | All_Same_Aisle_Query_2essorial 080 | VARCHAR2 | 4000 |  | Y |
| 26 | `ALL_SAME_ZONE_QUERY_1_090` | All_Same_Zone_Query_1essorial 090 | VARCHAR2 | 4000 |  | Y |
| 27 | `ALL_SAME_ZONE_QUERY_2_090` | All_Same_Zone_Query_2essorial 090 | VARCHAR2 | 4000 |  | Y |
| 28 | `ALL_ALL_LOC_QUERY_1_100` | All_All_Loc_Query_1essorial 100 | VARCHAR2 | 4000 |  | Y |
| 29 | `ALL_ALL_LOC_QUERY_2_100` | All_All_Loc_Query_2essorial 100 | VARCHAR2 | 4000 |  | Y |

## `T_TASK_LIST`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `ID` | ID | RAW | 32 |  | N |
| 4 | `TASK_PEND_ID` | Task_Pendessorial Id | RAW | 32 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 7 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 9 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 10 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 11 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 12 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 13 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 14 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 15 | `OP_REGION_CODE` | Op_Regionessorial Code | VARCHAR2 | 20 |  | N |
| 16 | `OP_MHE_CODE` | Op_Mheessorial Code | VARCHAR2 | 10 |  | N |
| 17 | `OP_WHSE_CODE` | Op_Whseessorial Code | VARCHAR2 | 4 |  | N |
| 18 | `OP_LOC_CODE` | Op_Locessorial Code | VARCHAR2 | 12 |  | N |
| 19 | `OP_WHSE_ACT_TP_NUM` | Op_Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 20 | `TASK_PROS_FLAG` | Task_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `TASK_LIST_REM` | Task_Listessorial Rem | VARCHAR2 | 80 |  | Y |

## `T_TASK_MGR`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TASK_RQST_SEQ_NUM` | Task_Rqst_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `TASK_TP_CODE` | Task_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `TASK_NUM` | Taskessorial Num | NUMBER | 22 | 9 | N |
| 5 | `TASK_LINE_NUM` | Task_Lineessorial Num | NUMBER | 22 | 6 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 7 | `TASK_RQST_CODE` | Task_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `TASK_RQST_DATE` | Task_Rqstessorial Date | DATE | 7 |  | N |
| 9 | `TASK_START_DATE` | Task_Startessorial Date | DATE | 7 |  | Y |
| 10 | `TASK_END_DATE` | Task_Endessorial Date | DATE | 7 |  | Y |
| 11 | `TASK_ERR_DATE` | Task_Erressorial Date | DATE | 7 |  | Y |
| 12 | `TASK_ERR_NUM` | Task_Erressorial Num | NUMBER | 22 | 3 | Y |
| 13 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 14 | `TASK_RQST_PRTY_NUM` | Task_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 15 | `TASK_TP_PRTY_NUM` | Task_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 16 | `TASK_LOC_LINE_NUM` | Task_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |

## `T_TER_FILE`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 2 | `FILE_NAME` | Fileessorial Name | VARCHAR2 | 60 |  | Y |

## `T_UPD`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CYC_CNT_NUM` | Cycle Count Number | NUMBER | 22 | 6 | N |
| 3 | `CYC_CNT_PROF_CODE` | Cyc_Cnt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 5 | `CYC_CNT_INCL_EMPTY_LOC_FLAG` | Cyc_Cnt_Incl_Empty_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `CYC_CNT_ALLOW_DUP_PER_LOC_FLAG` | Cyc_Cnt_Allow_Dup_Per_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `CYC_CNT_SHOW_INVT_LEV1_FLAG` | Cyc_Cnt_Show_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `CYC_CNT_SHOW_INVT_LEV2_FLAG` | Cyc_Cnt_Show_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `CYC_CNT_SHOW_INVT_LEV3_FLAG` | Cyc_Cnt_Show_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `CYC_CNT_SHOW_INVT_LEV4_FLAG` | Cyc_Cnt_Show_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | Y |

## `T_UPDOWNSTREAM_ADJ_HOLD`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 4 | `SEND_ID` | Sendessorial Id | VARCHAR2 | 20 |  | Y |
| 5 | `RECV_ID` | Recvessorial Id | VARCHAR2 | 20 |  | Y |

## `T_WHSE_CODE_LOC_CODE`

- **Tipo:** Temporary
- **Categoria:** Misc
- **Campos:** 2
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 2 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |

## `USER_PROFILE`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRODUCT` | Productessorial Product | VARCHAR2 | 30 |  | Y |
| 2 | `USERID` | Useridessorial Userid | VARCHAR2 | 30 |  | Y |
| 3 | `PROFILE` | Profileessorial Profile | VARCHAR2 | 240 |  | Y |
| 4 | `ATTRIBUTE` | Attributeessorial Attribute | VARCHAR2 | 240 |  | Y |
| 5 | `NUMERIC_VALUE` | Numericessorial Value | NUMBER | 22 | 15 | Y |
| 6 | `CHAR_VALUE` | Charessorial Value | VARCHAR2 | 240 |  | Y |
| 7 | `DATE_VALUE` | Dateessorial Value | DATE | 7 |  | Y |
| 8 | `LONG_VALUE` | Longessorial Value | LONG | 0 |  | Y |

## `X1`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_ATTR_PROF_DES` | Whse_Attr_Professorial Des | VARCHAR2 | 40 |  | N |
| 4 | `WHSE_ATTR_PROF_STAT` | Whse_Attr_Professorial Stat | VARCHAR2 | 1 |  | N |

## `X2`

- **Tipo:** Misc
- **Categoria:** Misc
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_ATTR_PROF_CODE` | Whse_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_ATTR_TP_NUM` | Whse_Attr_Tpessorial Num | NUMBER | 22 | 3 | N |
| 4 | `WHSE_ATTR_TP_OPT_NUM` | Whse_Attr_Tp_Optessorial Num | NUMBER | 22 | 3 | N |

