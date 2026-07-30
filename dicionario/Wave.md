# Tabelas — Wave

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **32**.

## `C_DSHB_WAVE_D`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `WHSE_CODE_OVRR` | Whse_Codeessorial Ovrr | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE_OVRR` | Loc_Codeessorial Ovrr | VARCHAR2 | 12 |  | Y |
| 6 | `ORD_TO_DEALLOC_FLAG` | Ord_To_Deallocessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `DSHB_WAVE_SUSP_TASK_FLAG` | Dshb_Wave_Susp_Taskessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_DSHB_WAVE_DD`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |

## `C_DSHB_WAVE_H`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `WAVE_TP` | Waveessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `WAVE_CREATE_DATE` | Wave_Createessorial Date | DATE | 7 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 7 | `DSHB_WAVE_QU_SEQ_NUM` | Dshb_Wave_Qu_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 8 | `DSHB_WAVE_ADV_FLOW_FLAG` | Dshb_Wave_Adv_Flowessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `DSHB_WAVE_BANDING_FLAG` | Dshb_Wave_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 11 | `PRT_LAB_CODE` | Prt_Labessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 13 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 14 | `WAVE_PROS_STAT_MES` | Wave_Pros_Statessorial Mes | VARCHAR2 | 1500 |  | Y |
| 15 | `DSHB_WAVE_DEALLOC_RULE_TP` | Dshb_Wave_Dealloc_Ruleessorial Tp | VARCHAR2 | 1 |  | Y |
| 16 | `DSHB_WAVE_SUSP_TASK_FLAG` | Dshb_Wave_Susp_Taskessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_DSHB_WAVE_MES`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `WAVE_MES_SEQ_NUM` | Wave_Mes_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `WAVE_MES` | Waveessorial Mes | VARCHAR2 | 1500 |  | N |
| 4 | `WAVE_MES_DATE` | Wave_Mesessorial Date | DATE | 7 |  | N |

## `C_WAVE`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 65
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_TP_CODE` | Wave_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `WAVE_TP` | Waveessorial Tp | VARCHAR2 | 1 |  | Y |
| 7 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 8 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 9 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_DATE` | Waveessorial Date | DATE | 7 |  | N |
| 11 | `WAVE_CONF_DATE` | Wave_Confessorial Date | DATE | 7 |  | Y |
| 12 | `WAVE_TOT_WGT` | Wave_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 13 | `WAVE_TOT_WGT_NET` | Wave_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 14 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `WAVE_NUM_LINES` | Wave_Numessorial Lines | NUMBER | 22 | 4 | N |
| 20 | `WAVE_NUM_LOC_LINES` | Wave_Num_Locessorial Lines | NUMBER | 22 | 4 | N |
| 21 | `WAVE_TOT_CUBE` | Wave_Totessorial Cube | NUMBER | 22 | 16 | N |
| 22 | `WAVE_LAB_STD_ERR_FLAG` | Wave_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `WAVE_EST_METH` | Wave_Estessorial Meth | VARCHAR2 | 1 |  | Y |
| 24 | `WAVE_EST_TIME_HIST` | Wave_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `WAVE_EST_TIME_MAN` | Wave_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `WAVE_EST_TIME` | Wave_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PRTY_NUM` | Wave_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 29 | `WAVE_PRTY_CODE_INIT_DATE` | Wave_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 30 | `WAVE_PRTY_OVRR_FLAG` | Wave_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `WAVE_PRTY_MAN_FLAG` | Wave_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `WAVE_CREATE_DATE` | Wave_Createessorial Date | DATE | 7 |  | Y |
| 33 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 34 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 35 | `WAVE_DLINE_DATE` | Wave_Dlineessorial Date | DATE | 7 |  | Y |
| 36 | `WAVE_EST_START_DATE` | Wave_Est_Startessorial Date | DATE | 7 |  | Y |
| 37 | `WAVE_EST_START_MAN_FLAG` | Wave_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `WAVE_EST_START_OVRR_FLAG` | Wave_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `WAVE_EST_END_DATE` | Wave_Est_Endessorial Date | DATE | 7 |  | Y |
| 40 | `WAVE_EST_END_MAN_FLAG` | Wave_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `WAVE_EST_END_OVRR_FLAG` | Wave_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `WAVE_PCENT_COMPL` | Wave_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 43 | `WAVE_PCENT_MAN_FLAG` | Wave_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `WAVE_PCENT_OVRR_FLAG` | Wave_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `WAVE_PURGE_DATE` | Wave_Purgeessorial Date | DATE | 7 |  | Y |
| 46 | `WAVE_EST_TIME_REMA_HIST` | Wave_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 47 | `WAVE_EST_TIME_REMA` | Wave_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 48 | `WAVE_EST_TIME_REMA_MAN` | Wave_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 49 | `WAVE_TO_PROCESS_DATE` | Wave_To_Processessorial Date | DATE | 7 |  | Y |
| 50 | `WAVE_TO_ARR_DATE` | Wave_To_Arressorial Date | DATE | 7 |  | Y |
| 51 | `WAVE_APPO_DATE` | Wave_Appoessorial Date | DATE | 7 |  | Y |
| 52 | `WAVE_CNVC_QTY` | Wave_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 53 | `WAVE_MODSKU` | Waveessorial Modsku | NUMBER | 22 | 9 | N |
| 54 | `WAVE_ASS_DATE` | Wave_Assessorial Date | DATE | 7 |  | N |
| 55 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 56 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 57 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 58 | `WAVE_HOLD_DATE` | Wave_Holdessorial Date | DATE | 7 |  | Y |
| 59 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 60 | `WAVE_CANCEL_DATE` | Wave_Cancelessorial Date | DATE | 7 |  | Y |
| 61 | `WAVE_PCENT_COMPL_ADJ` | Wave_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 62 | `WAVE_EST_TIME_REMA_ADJ` | Wave_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 63 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 64 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |
| 65 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `C_WAVE_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 64
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_TP_CODE` | Wave_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `WAVE_TP` | Waveessorial Tp | VARCHAR2 | 1 |  | Y |
| 7 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 8 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 9 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_DATE` | Waveessorial Date | DATE | 7 |  | N |
| 11 | `WAVE_CONF_DATE` | Wave_Confessorial Date | DATE | 7 |  | Y |
| 12 | `WAVE_TOT_WGT` | Wave_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 13 | `WAVE_TOT_WGT_NET` | Wave_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 14 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `WAVE_NUM_LINES` | Wave_Numessorial Lines | NUMBER | 22 | 4 | N |
| 20 | `WAVE_NUM_LOC_LINES` | Wave_Num_Locessorial Lines | NUMBER | 22 | 4 | N |
| 21 | `WAVE_TOT_CUBE` | Wave_Totessorial Cube | NUMBER | 22 | 16 | N |
| 22 | `WAVE_LAB_STD_ERR_FLAG` | Wave_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `WAVE_EST_METH` | Wave_Estessorial Meth | VARCHAR2 | 1 |  | Y |
| 24 | `WAVE_EST_TIME_HIST` | Wave_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `WAVE_EST_TIME_MAN` | Wave_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `WAVE_EST_TIME` | Wave_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PRTY_NUM` | Wave_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 29 | `WAVE_PRTY_CODE_INIT_DATE` | Wave_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 30 | `WAVE_PRTY_OVRR_FLAG` | Wave_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `WAVE_PRTY_MAN_FLAG` | Wave_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `WAVE_CREATE_DATE` | Wave_Createessorial Date | DATE | 7 |  | Y |
| 33 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 34 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 35 | `WAVE_DLINE_DATE` | Wave_Dlineessorial Date | DATE | 7 |  | Y |
| 36 | `WAVE_EST_START_DATE` | Wave_Est_Startessorial Date | DATE | 7 |  | Y |
| 37 | `WAVE_EST_START_MAN_FLAG` | Wave_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `WAVE_EST_START_OVRR_FLAG` | Wave_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `WAVE_EST_END_DATE` | Wave_Est_Endessorial Date | DATE | 7 |  | Y |
| 40 | `WAVE_EST_END_MAN_FLAG` | Wave_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `WAVE_EST_END_OVRR_FLAG` | Wave_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `WAVE_PCENT_COMPL` | Wave_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 43 | `WAVE_PCENT_MAN_FLAG` | Wave_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `WAVE_PCENT_OVRR_FLAG` | Wave_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `WAVE_PURGE_DATE` | Wave_Purgeessorial Date | DATE | 7 |  | Y |
| 46 | `WAVE_EST_TIME_REMA_HIST` | Wave_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 47 | `WAVE_EST_TIME_REMA` | Wave_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 48 | `WAVE_EST_TIME_REMA_MAN` | Wave_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 49 | `WAVE_TO_PROCESS_DATE` | Wave_To_Processessorial Date | DATE | 7 |  | Y |
| 50 | `WAVE_TO_ARR_DATE` | Wave_To_Arressorial Date | DATE | 7 |  | Y |
| 51 | `WAVE_APPO_DATE` | Wave_Appoessorial Date | DATE | 7 |  | Y |
| 52 | `WAVE_CNVC_QTY` | Wave_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 53 | `WAVE_MODSKU` | Waveessorial Modsku | NUMBER | 22 | 9 | N |
| 54 | `WAVE_ASS_DATE` | Wave_Assessorial Date | DATE | 7 |  | N |
| 55 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 56 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 57 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 58 | `WAVE_HOLD_DATE` | Wave_Holdessorial Date | DATE | 7 |  | Y |
| 59 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 60 | `WAVE_CANCEL_DATE` | Wave_Cancelessorial Date | DATE | 7 |  | Y |
| 61 | `WAVE_PCENT_COMPL_ADJ` | Wave_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 62 | `WAVE_EST_TIME_REMA_ADJ` | Wave_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 63 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 64 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |

## `C_WAVE_MGR_D1`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_STEP` | Wave_Rqstessorial Step | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_STEP_START_DATE` | Wave_Rqst_Step_Startessorial Date | DATE | 7 |  | Y |
| 6 | `WAVE_RQST_STEP_END_DATE` | Wave_Rqst_Step_Endessorial Date | DATE | 7 |  | Y |
| 7 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 8 | `SEL_CNT` | Selessorial Cnt | NUMBER | 22 | 4 | Y |

## `C_WAVE_MGR_D1_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_STEP` | Wave_Rqstessorial Step | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_STEP_START_DATE` | Wave_Rqst_Step_Startessorial Date | DATE | 7 |  | Y |
| 6 | `WAVE_RQST_STEP_END_DATE` | Wave_Rqst_Step_Endessorial Date | DATE | 7 |  | Y |

## `C_WAVE_MGR_D2`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `WAVE_JOB_DATE` | Wave_Jobessorial Date | DATE | 7 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 5 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_EST_TIME_STD` | Pros_Est_Timeessorial Std | NUMBER | 22 | 6 | Y |
| 7 | `JOB_PACK_FLAG` | Job_Packessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_WAVE_MGR_D2_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `WAVE_JOB_DATE` | Wave_Jobessorial Date | DATE | 7 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 6 | N |
| 5 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_EST_TIME_STD` | Pros_Est_Timeessorial Std | NUMBER | 22 | 6 | Y |

## `C_WAVE_MGR_H`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_CODE` | Wave_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_DATE` | Wave_Rqstessorial Date | DATE | 7 |  | N |
| 6 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_ERR_DATE` | Wave_Erressorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_ERR_NUM` | Wave_Erressorial Num | NUMBER | 22 | 3 | Y |
| 10 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `WAVE_ABORT_DATE` | Wave_Abortessorial Date | DATE | 7 |  | Y |
| 14 | `ORG_WAVE_RQST_SEQ_NUM` | Org_Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | Y |

## `C_WAVE_MGR_H_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_CODE` | Wave_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_DATE` | Wave_Rqstessorial Date | DATE | 7 |  | N |
| 6 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_ERR_DATE` | Wave_Erressorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_ERR_NUM` | Wave_Erressorial Num | NUMBER | 22 | 3 | Y |
| 10 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `C_WAVE_MGR_JOB`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_DATE` | Waveessorial Date | DATE | 7 |  | N |
| 3 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 4 | `JOB_ERR_NUM` | Job_Erressorial Num | NUMBER | 22 | 6 | Y |
| 5 | `JOB_ERR_DATE` | Job_Erressorial Date | DATE | 7 |  | Y |

## `C_WAVE_MGR_JOB_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_DATE` | Waveessorial Date | DATE | 7 |  | N |
| 3 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 4 | `JOB_ERR_NUM` | Job_Erressorial Num | NUMBER | 22 | 6 | Y |
| 5 | `JOB_ERR_DATE` | Job_Erressorial Date | DATE | 7 |  | Y |

## `C_WAVE_PROS`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WAVE_PROS_START_DATE` | Wave_Pros_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_PROS_END_DATE` | Wave_Pros_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_PROS_DLINE_DATE` | Wave_Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_PROS_EST_START_DATE` | Wave_Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 10 | `WAVE_PROS_EST_START_MAN_FLAG` | Wave_Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `WAVE_PROS_EST_START_OVRR_FLAG` | Wave_Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `WAVE_PROS_EST_END_DATE` | Wave_Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 13 | `WAVE_PROS_EST_END_MAN_FLAG` | Wave_Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_PROS_EST_END_OVRR_FLAG` | Wave_Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `WAVE_PROS_PCENT_COMPL` | Wave_Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 16 | `WAVE_PROS_PCENT_MAN_FLAG` | Wave_Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WAVE_PROS_PCENT_OVRR_FLAG` | Wave_Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `WAVE_PROS_EST_TIME_HIST` | Wave_Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 19 | `WAVE_PROS_EST_TIME_MAN` | Wave_Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 20 | `WAVE_PROS_EST_TIME` | Wave_Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 21 | `WAVE_PROS_EST_TIME_REMA_HIST` | Wave_Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 22 | `WAVE_PROS_EST_TIME_REMA` | Wave_Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 23 | `WAVE_PROS_EST_TIME_REMA_MAN` | Wave_Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 24 | `WAVE_PROS_WAVE_ALLOC_FLAG` | Wave_Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `WAVE_PROS_PCENT_COMPL_ADJ` | Wave_Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 26 | `WAVE_PROS_EST_TIME_REMA_ADJ` | Wave_Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 27 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PROS_HOLD_DATE` | Wave_Pros_Holdessorial Date | DATE | 7 |  | Y |

## `C_WAVE_PROS_HIST`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WAVE_PROS_START_DATE` | Wave_Pros_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_PROS_END_DATE` | Wave_Pros_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_PROS_DLINE_DATE` | Wave_Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_PROS_EST_START_DATE` | Wave_Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 10 | `WAVE_PROS_EST_START_MAN_FLAG` | Wave_Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `WAVE_PROS_EST_START_OVRR_FLAG` | Wave_Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `WAVE_PROS_EST_END_DATE` | Wave_Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 13 | `WAVE_PROS_EST_END_MAN_FLAG` | Wave_Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_PROS_EST_END_OVRR_FLAG` | Wave_Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `WAVE_PROS_PCENT_COMPL` | Wave_Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 16 | `WAVE_PROS_PCENT_MAN_FLAG` | Wave_Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WAVE_PROS_PCENT_OVRR_FLAG` | Wave_Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `WAVE_PROS_EST_TIME_HIST` | Wave_Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 19 | `WAVE_PROS_EST_TIME_MAN` | Wave_Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 20 | `WAVE_PROS_EST_TIME` | Wave_Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 21 | `WAVE_PROS_EST_TIME_REMA_HIST` | Wave_Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 22 | `WAVE_PROS_EST_TIME_REMA` | Wave_Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 23 | `WAVE_PROS_EST_TIME_REMA_MAN` | Wave_Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 24 | `WAVE_PROS_WAVE_ALLOC_FLAG` | Wave_Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `WAVE_PROS_PCENT_COMPL_ADJ` | Wave_Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 26 | `WAVE_PROS_EST_TIME_REMA_ADJ` | Wave_Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 27 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PROS_HOLD_DATE` | Wave_Pros_Holdessorial Date | DATE | 7 |  | Y |

## `C_WAVE_PURGE`

- **Tipo:** Transactional
- **Categoria:** Wave
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 4 | `WAVE_PURGE_PROS_FLAG` | Wave_Purge_Prosessorial Flag | VARCHAR2 | 1 |  | N |

## `H_WAVE`

- **Tipo:** Historical
- **Categoria:** Wave
- **Campos:** 65
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_TP_CODE` | Wave_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `WAVE_TP` | Waveessorial Tp | VARCHAR2 | 1 |  | Y |
| 7 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 8 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 9 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_DATE` | Waveessorial Date | DATE | 7 |  | N |
| 11 | `WAVE_CONF_DATE` | Wave_Confessorial Date | DATE | 7 |  | Y |
| 12 | `WAVE_TOT_WGT` | Wave_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 13 | `WAVE_TOT_WGT_NET` | Wave_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 14 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `WAVE_NUM_LINES` | Wave_Numessorial Lines | NUMBER | 22 | 4 | N |
| 20 | `WAVE_NUM_LOC_LINES` | Wave_Num_Locessorial Lines | NUMBER | 22 | 4 | N |
| 21 | `WAVE_TOT_CUBE` | Wave_Totessorial Cube | NUMBER | 22 | 16 | N |
| 22 | `WAVE_LAB_STD_ERR_FLAG` | Wave_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `WAVE_EST_METH` | Wave_Estessorial Meth | VARCHAR2 | 1 |  | Y |
| 24 | `WAVE_EST_TIME_HIST` | Wave_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `WAVE_EST_TIME_MAN` | Wave_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `WAVE_EST_TIME` | Wave_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PRTY_NUM` | Wave_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 29 | `WAVE_PRTY_CODE_INIT_DATE` | Wave_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 30 | `WAVE_PRTY_OVRR_FLAG` | Wave_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `WAVE_PRTY_MAN_FLAG` | Wave_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `WAVE_CREATE_DATE` | Wave_Createessorial Date | DATE | 7 |  | Y |
| 33 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 34 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 35 | `WAVE_DLINE_DATE` | Wave_Dlineessorial Date | DATE | 7 |  | Y |
| 36 | `WAVE_EST_START_DATE` | Wave_Est_Startessorial Date | DATE | 7 |  | Y |
| 37 | `WAVE_EST_START_MAN_FLAG` | Wave_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `WAVE_EST_START_OVRR_FLAG` | Wave_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `WAVE_EST_END_DATE` | Wave_Est_Endessorial Date | DATE | 7 |  | Y |
| 40 | `WAVE_EST_END_MAN_FLAG` | Wave_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `WAVE_EST_END_OVRR_FLAG` | Wave_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `WAVE_PCENT_COMPL` | Wave_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 43 | `WAVE_PCENT_MAN_FLAG` | Wave_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `WAVE_PCENT_OVRR_FLAG` | Wave_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `WAVE_PURGE_DATE` | Wave_Purgeessorial Date | DATE | 7 |  | Y |
| 46 | `WAVE_EST_TIME_REMA_HIST` | Wave_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 47 | `WAVE_EST_TIME_REMA` | Wave_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 48 | `WAVE_EST_TIME_REMA_MAN` | Wave_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 49 | `WAVE_TO_PROCESS_DATE` | Wave_To_Processessorial Date | DATE | 7 |  | Y |
| 50 | `WAVE_TO_ARR_DATE` | Wave_To_Arressorial Date | DATE | 7 |  | Y |
| 51 | `WAVE_APPO_DATE` | Wave_Appoessorial Date | DATE | 7 |  | Y |
| 52 | `WAVE_CNVC_QTY` | Wave_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 53 | `WAVE_MODSKU` | Waveessorial Modsku | NUMBER | 22 | 9 | N |
| 54 | `WAVE_ASS_DATE` | Wave_Assessorial Date | DATE | 7 |  | N |
| 55 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 56 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 57 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 58 | `WAVE_HOLD_DATE` | Wave_Holdessorial Date | DATE | 7 |  | Y |
| 59 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 60 | `WAVE_CANCEL_DATE` | Wave_Cancelessorial Date | DATE | 7 |  | Y |
| 61 | `WAVE_PCENT_COMPL_ADJ` | Wave_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 62 | `WAVE_EST_TIME_REMA_ADJ` | Wave_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 63 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 64 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |
| 65 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `H_WAVE_MGR_D1`

- **Tipo:** Historical
- **Categoria:** Wave
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_STEP` | Wave_Rqstessorial Step | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_STEP_START_DATE` | Wave_Rqst_Step_Startessorial Date | DATE | 7 |  | Y |
| 6 | `WAVE_RQST_STEP_END_DATE` | Wave_Rqst_Step_Endessorial Date | DATE | 7 |  | Y |
| 7 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 8 | `SEL_CNT` | Selessorial Cnt | NUMBER | 22 | 4 | Y |

## `H_WAVE_MGR_D2`

- **Tipo:** Historical
- **Categoria:** Wave
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `WAVE_JOB_DATE` | Wave_Jobessorial Date | DATE | 7 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 5 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_EST_TIME_STD` | Pros_Est_Timeessorial Std | NUMBER | 22 | 6 | Y |
| 7 | `JOB_PACK_FLAG` | Job_Packessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_WAVE_MGR_H`

- **Tipo:** Historical
- **Categoria:** Wave
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WAVE_RQST_SEQ_NUM` | Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `WAVE_RQST_CODE` | Wave_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `WAVE_RQST_DATE` | Wave_Rqstessorial Date | DATE | 7 |  | N |
| 6 | `WAVE_START_DATE` | Wave_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_END_DATE` | Wave_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_ERR_DATE` | Wave_Erressorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_ERR_NUM` | Wave_Erressorial Num | NUMBER | 22 | 3 | Y |
| 10 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `WAVE_METH` | Waveessorial Meth | NUMBER | 22 | 1 | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `WAVE_ABORT_DATE` | Wave_Abortessorial Date | DATE | 7 |  | Y |
| 14 | `ORG_WAVE_RQST_SEQ_NUM` | Org_Wave_Rqst_Seqessorial Num | NUMBER | 22 | 7 | Y |

## `H_WAVE_PROS`

- **Tipo:** Historical
- **Categoria:** Wave
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WAVE_PROS_START_DATE` | Wave_Pros_Startessorial Date | DATE | 7 |  | Y |
| 7 | `WAVE_PROS_END_DATE` | Wave_Pros_Endessorial Date | DATE | 7 |  | Y |
| 8 | `WAVE_PROS_DLINE_DATE` | Wave_Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 9 | `WAVE_PROS_EST_START_DATE` | Wave_Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 10 | `WAVE_PROS_EST_START_MAN_FLAG` | Wave_Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `WAVE_PROS_EST_START_OVRR_FLAG` | Wave_Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `WAVE_PROS_EST_END_DATE` | Wave_Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 13 | `WAVE_PROS_EST_END_MAN_FLAG` | Wave_Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_PROS_EST_END_OVRR_FLAG` | Wave_Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `WAVE_PROS_PCENT_COMPL` | Wave_Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 16 | `WAVE_PROS_PCENT_MAN_FLAG` | Wave_Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WAVE_PROS_PCENT_OVRR_FLAG` | Wave_Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `WAVE_PROS_EST_TIME_HIST` | Wave_Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 19 | `WAVE_PROS_EST_TIME_MAN` | Wave_Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 20 | `WAVE_PROS_EST_TIME` | Wave_Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 21 | `WAVE_PROS_EST_TIME_REMA_HIST` | Wave_Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 22 | `WAVE_PROS_EST_TIME_REMA` | Wave_Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 23 | `WAVE_PROS_EST_TIME_REMA_MAN` | Wave_Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 24 | `WAVE_PROS_WAVE_ALLOC_FLAG` | Wave_Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `WAVE_PROS_PCENT_COMPL_ADJ` | Wave_Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 26 | `WAVE_PROS_EST_TIME_REMA_ADJ` | Wave_Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 27 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 28 | `WAVE_PROS_HOLD_DATE` | Wave_Pros_Holdessorial Date | DATE | 7 |  | Y |

## `M_DSHB_WAVE_OP_QU`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `DSHB_WAVE_QU_SEQ_NUM` | Dshb_Wave_Qu_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `DSHB_WAVE_QU_DES` | Dshb_Wave_Quessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `DSHB_WAVE_QU_AUTO_FLAG` | Dshb_Wave_Qu_Autoessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `DSHB_WAVE_QU_SAVE_FLAG` | Dshb_Wave_Qu_Saveessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DSHB_WAVE_QU_STR` | Dshb_Wave_Quessorial Str | CLOB | 4000 |  | N |
| 7 | `DSHB_WAVE_QU_FIL_SEQ_NUM` | Dshb_Wave_Qu_Fil_Seqessorial Num | NUMBER | 22 | 9 | N |
| 8 | `DSHB_WAVE_QU_CREATE_DATE` | Dshb_Wave_Qu_Createessorial Date | DATE | 7 |  | N |
| 9 | `DSHB_WAVE_QU_MOD_DATE` | Dshb_Wave_Qu_Modessorial Date | DATE | 7 |  | Y |
| 10 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 11 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 12 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 13 | `DSHB_WAVE_ADV_FLOW_FLAG` | Dshb_Wave_Adv_Flowessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `DSHB_WAVE_BANDING_FLAG` | Dshb_Wave_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 16 | `PRT_LAB_CODE` | Prt_Labessorial Code | VARCHAR2 | 4 |  | Y |

## `M_DSHB_WAVE_OP_QU_FIL`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_WAVE_QU_FIL_SEQ_NUM` | Dshb_Wave_Qu_Fil_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `DSHB_WAVE_QU_FIL_SEQ_NUM_CNT` | Dshb_Wave_Qu_Fil_Seq_Numessorial Cnt | NUMBER | 22 | 9 | N |
| 3 | `DSHB_WAVE_QU_PARA_CODE` | Dshb_Wave_Qu_Paraessorial Code | VARCHAR2 | 80 |  | N |
| 4 | `DSHB_WAVE_QU_PARA_VAL` | Dshb_Wave_Qu_Paraessorial Val | VARCHAR2 | 1500 |  | Y |

## `M_DSHB_WAVE_SCH_D`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_WAVE_QU_SEQ_NUM` | Dshb_Wave_Qu_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `DSHB_WAVE_QU_PROS_DATE` | Dshb_Wave_Qu_Prosessorial Date | DATE | 7 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DSHB_WAVE_QU_PROS_STAT` | Dshb_Wave_Qu_Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `DSHB_WAVE_QU_PROS_ERR_NUM` | Dshb_Wave_Qu_Pros_Erressorial Num | NUMBER | 22 | 6 | Y |
| 6 | `DSHB_WAVE_QU_PROS_ERR_MES` | Dshb_Wave_Qu_Pros_Erressorial Mes | CLOB | 4000 |  | Y |

## `M_DSHB_WAVE_SCH_H`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `DSHB_WAVE_QU_SEQ_NUM` | Dshb_Wave_Qu_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `DSHB_WAVE_QU_START_DATE` | Dshb_Wave_Qu_Startessorial Date | DATE | 7 |  | N |
| 3 | `DSHB_WAVE_QU_EXPY_DATE` | Dshb_Wave_Qu_Expyessorial Date | DATE | 7 |  | Y |
| 4 | `DSHB_WAVE_SCH_PARA` | Dshb_Wave_Schessorial Para | VARCHAR2 | 250 |  | N |

## `M_WAVE_INSTANCE_PARA_D`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INSTANCE_MODE_NUM` | Instance_Modeessorial Num | NUMBER | 22 | 2 | N |
| 4 | `INSTANCE_NUM` | Instanceessorial Num | NUMBER | 22 | 2 | N |
| 5 | `QUALIFY_CHAR` | Qualifyessorial Char | VARCHAR2 | 100 |  | N |

## `M_WAVE_INSTANCE_PARA_H`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INSTANCE_MODE_NUM` | Instance_Modeessorial Num | NUMBER | 22 | 2 | N |
| 4 | `ITEM_CODE_CHAR_POS` | Item_Code_Charessorial Pos | NUMBER | 22 | 2 | N |

## `M_WAVE_PARA`

- **Tipo:** Master
- **Categoria:** Wave
- **Campos:** 18

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_DUR_MINT_NUM` | Wave_Dur_Mintessorial Num | NUMBER | 22 | 3 | N |
| 2 | `WAVE_MARG_MINT_NUM` | Wave_Marg_Mintessorial Num | NUMBER | 22 | 3 | N |
| 3 | `WAVE_MAX_MINT_NUM` | Wave_Max_Mintessorial Num | NUMBER | 22 | 6 | N |
| 4 | `WAVE_MAX_MINT_PER_PACK_STN` | Wave_Max_Mint_Per_Packessorial Stn | NUMBER | 22 | 6 | N |
| 5 | `SGL_PACK_STN_MINT_LMT` | Sgl_Pack_Stn_Mintessorial Lmt | NUMBER | 22 | 6 | N |
| 6 | `WAVE_MGR_SLEEP_MINT_NUM` | Wave_Mgr_Sleep_Mintessorial Num | NUMBER | 22 | 4 | N |
| 7 | `WAVE_MGR_SLEEP_SECD_NUM` | Wave_Mgr_Sleep_Secdessorial Num | NUMBER | 22 | 4 | N |
| 8 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 9 | `CUST_MIX_FLAG` | Cust_Mixessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CARR_MIX_FLAG` | Carr_Mixessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CON_MIX_FLAG` | Con_Mixessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `LOAD_TP_MIX_FLAG` | Load_Tp_Mixessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `WAVE_PRTY_TP` | Wave_Prtyessorial Tp | VARCHAR2 | 1 |  | N |
| 14 | `WAVE_MAX_ORD_LINE_NUM` | Wave_Max_Ord_Lineessorial Num | NUMBER | 22 | 6 | Y |
| 15 | `WAVE_IGNORE_PRTY_FLAG` | Wave_Ignore_Prtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `WAVE_USE_ITEM_PROS_FLAG` | Wave_Use_Item_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WAVE_TASKENGN_MHE_TP_CALC_FLAG` | Wave_Taskengn_Mhe_Tp_Calcessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `WAVE_REL_TASK_PER_WAVE_FLAG` | Wave_Rel_Task_Per_Waveessorial Flag | VARCHAR2 | 1 |  | N |

## `T_DSHB_WAVE`

- **Tipo:** Temporary
- **Categoria:** Wave
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WEB_SESS_ID` | Web_Sessessorial Id | VARCHAR2 | 20 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 5 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `ORD_ALT_REF1` | Ord_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_ALT_REF2` | Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 11 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 12 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 13 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 14 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | N |
| 15 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | N |
| 16 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | N |
| 17 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 18 | `TOTAL_STR` | Totalessorial Str | VARCHAR2 | 1500 |  | Y |

## `T_DSHB_WAVE_D`

- **Tipo:** Temporary
- **Categoria:** Wave
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `WHSE_CODE_OVRR` | Whse_Codeessorial Ovrr | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE_OVRR` | Loc_Codeessorial Ovrr | VARCHAR2 | 12 |  | Y |

## `T_JOB_NUM_WAVE`

- **Tipo:** Temporary
- **Categoria:** Wave
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_WAVE_SEQ_NUM` | Job_Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |

