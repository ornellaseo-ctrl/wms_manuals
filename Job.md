# Tabelas — Job

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **20**.

## `C_JOB`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 70
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 7 | `JOB_TP` | Jobessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 11 | `JOB_DATE` | Jobessorial Date | DATE | 7 |  | N |
| 12 | `JOB_CONF_DATE` | Job_Confessorial Date | DATE | 7 |  | Y |
| 13 | `JOB_TOT_WGT` | Job_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `JOB_TOT_WGT_NET` | Job_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `JOB_NUM_LINE` | Job_Numessorial Line | NUMBER | 22 | 4 | N |
| 21 | `JOB_NUM_LOC_LINE` | Job_Num_Locessorial Line | NUMBER | 22 | 4 | N |
| 22 | `JOB_TOT_CUBE` | Job_Totessorial Cube | NUMBER | 22 | 16 | N |
| 23 | `JOB_LAB_STD_ERR_FLAG` | Job_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `JOB_EST_METH_FLAG` | Job_Est_Methessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `JOB_EST_TIME_HIST` | Job_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 26 | `JOB_EST_TIME_MAN` | Job_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 27 | `JOB_EST_TIME` | Job_Estessorial Time | NUMBER | 22 | 6 | Y |
| 28 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 29 | `JOB_PRTY_NUM` | Job_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 30 | `JOB_PRTY_CODE_INIT_DATE` | Job_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 31 | `JOB_PRTY_OVRR_FLAG` | Job_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `JOB_PRTY_MAN_FLAG` | Job_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `JOB_CREATE_DATE` | Job_Createessorial Date | DATE | 7 |  | Y |
| 34 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 35 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 36 | `JOB_DLINE_DATE` | Job_Dlineessorial Date | DATE | 7 |  | Y |
| 37 | `JOB_EST_START_DATE` | Job_Est_Startessorial Date | DATE | 7 |  | Y |
| 38 | `JOB_EST_START_MAN_FLAG` | Job_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `JOB_EST_START_OVRR_FLAG` | Job_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `JOB_EST_END_DATE` | Job_Est_Endessorial Date | DATE | 7 |  | Y |
| 41 | `JOB_EST_END_MAN_FLAG` | Job_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `JOB_EST_END_OVRR_FLAG` | Job_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `JOB_PCENT_COMPL` | Job_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 44 | `JOB_PCENT_MAN_FLAG` | Job_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `JOB_PCENT_OVRR_FLAG` | Job_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 46 | `JOB_PURGE_DATE` | Job_Purgeessorial Date | DATE | 7 |  | Y |
| 47 | `JOB_EST_TIME_REMA_HIST` | Job_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 48 | `JOB_EST_TIME_REMA` | Job_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 49 | `JOB_EST_TIME_REMA_MAN` | Job_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 50 | `JOB_TO_PROS_DATE` | Job_To_Prosessorial Date | DATE | 7 |  | Y |
| 51 | `JOB_TO_ARR_DATE` | Job_To_Arressorial Date | DATE | 7 |  | Y |
| 52 | `JOB_APPO_DATE` | Job_Appoessorial Date | DATE | 7 |  | Y |
| 53 | `JOB_CNVC_QTY` | Job_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 54 | `JOB_MODSKU` | Jobessorial Modsku | NUMBER | 22 | 9 | N |
| 55 | `JOB_ASS_DATE` | Job_Assessorial Date | DATE | 7 |  | Y |
| 56 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 57 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 58 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 59 | `JOB_HOLD_DATE` | Job_Holdessorial Date | DATE | 7 |  | Y |
| 60 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `JOB_WAVE_ALLOC_INIT_FLAG` | Job_Wave_Alloc_Initessorial Flag | VARCHAR2 | 1 |  | Y |
| 62 | `JOB_WAVE_ALLOC_COMPL_FLAG` | Job_Wave_Alloc_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `HOST_JOB_NUM` | Host_Jobessorial Num | NUMBER | 22 | 9 | Y |
| 64 | `JOB_CANCEL_DATE` | Job_Cancelessorial Date | DATE | 7 |  | Y |
| 65 | `JOB_PCENT_COMPL_ADJ` | Job_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 66 | `JOB_EST_TIME_REMA_ADJ` | Job_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 67 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | Y |
| 68 | `CARR_STD_ALPHA_CODE` | Carr_Std_Alphaessorial Code | VARCHAR2 | 4 |  | Y |
| 69 | `CON_PRTY_NUM` | Con_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 70 | `JOB_PROS_FLAG` | Job_Prosessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_JOB_HIST`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 67
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `JOB_NUM` | Job Number | NUMBER | 22 | 6 | N |
| 7 | `JOB_TP` | Jobessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 11 | `JOB_DATE` | Jobessorial Date | DATE | 7 |  | N |
| 12 | `JOB_CONF_DATE` | Job_Confessorial Date | DATE | 7 |  | Y |
| 13 | `JOB_TOT_WGT` | Job_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `JOB_TOT_WGT_NET` | Job_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `JOB_NUM_LINE` | Job_Numessorial Line | NUMBER | 22 | 4 | N |
| 21 | `JOB_NUM_LOC_LINE` | Job_Num_Locessorial Line | NUMBER | 22 | 4 | N |
| 22 | `JOB_TOT_CUBE` | Job_Totessorial Cube | NUMBER | 22 | 16 | N |
| 23 | `JOB_LAB_STD_ERR_FLAG` | Job_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `JOB_EST_METH_FLAG` | Job_Est_Methessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `JOB_EST_TIME_HIST` | Job_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 26 | `JOB_EST_TIME_MAN` | Job_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 27 | `JOB_EST_TIME` | Job_Estessorial Time | NUMBER | 22 | 6 | Y |
| 28 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 29 | `JOB_PRTY_NUM` | Job_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 30 | `JOB_PRTY_CODE_INIT_DATE` | Job_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 31 | `JOB_PRTY_OVRR_FLAG` | Job_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `JOB_PRTY_MAN_FLAG` | Job_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `JOB_CREATE_DATE` | Job_Createessorial Date | DATE | 7 |  | Y |
| 34 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 35 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 36 | `JOB_DLINE_DATE` | Job_Dlineessorial Date | DATE | 7 |  | Y |
| 37 | `JOB_EST_START_DATE` | Job_Est_Startessorial Date | DATE | 7 |  | Y |
| 38 | `JOB_EST_START_MAN_FLAG` | Job_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `JOB_EST_START_OVRR_FLAG` | Job_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `JOB_EST_END_DATE` | Job_Est_Endessorial Date | DATE | 7 |  | Y |
| 41 | `JOB_EST_END_MAN_FLAG` | Job_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `JOB_EST_END_OVRR_FLAG` | Job_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `JOB_PCENT_COMPL` | Job_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 44 | `JOB_PCENT_MAN_FLAG` | Job_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `JOB_PCENT_OVRR_FLAG` | Job_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 46 | `JOB_PURGE_DATE` | Job_Purgeessorial Date | DATE | 7 |  | Y |
| 47 | `JOB_EST_TIME_REMA_HIST` | Job_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 48 | `JOB_EST_TIME_REMA` | Job_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 49 | `JOB_EST_TIME_REMA_MAN` | Job_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 50 | `JOB_TO_PROS_DATE` | Job_To_Prosessorial Date | DATE | 7 |  | Y |
| 51 | `JOB_TO_ARR_DATE` | Job_To_Arressorial Date | DATE | 7 |  | Y |
| 52 | `JOB_APPO_DATE` | Job_Appoessorial Date | DATE | 7 |  | Y |
| 53 | `JOB_CNVC_QTY` | Job_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 54 | `JOB_MODSKU` | Jobessorial Modsku | NUMBER | 22 | 9 | N |
| 55 | `JOB_ASS_DATE` | Job_Assessorial Date | DATE | 7 |  | Y |
| 56 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 57 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 58 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 59 | `JOB_HOLD_DATE` | Job_Holdessorial Date | DATE | 7 |  | Y |
| 60 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `JOB_WAVE_ALLOC_INIT_FLAG` | Job_Wave_Alloc_Initessorial Flag | VARCHAR2 | 1 |  | Y |
| 62 | `JOB_WAVE_ALLOC_COMPL_FLAG` | Job_Wave_Alloc_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `HOST_JOB_NUM` | Host_Jobessorial Num | NUMBER | 22 | 10 | Y |
| 64 | `JOB_CANCEL_DATE` | Job_Cancelessorial Date | DATE | 7 |  | Y |
| 65 | `JOB_PCENT_COMPL_ADJ` | Job_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 66 | `JOB_EST_TIME_REMA_ADJ` | Job_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 67 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | Y |

## `C_JOB_H_HIST`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_ACCESS` | Jobessorial Access | VARCHAR2 | 10 |  | Y |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 6 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 7 | `JOB_TYPE_TP` | Job_Typeessorial Tp | VARCHAR2 | 1 |  | Y |
| 8 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 11 | `JOB_DATE` | Jobessorial Date | DATE | 7 |  | Y |
| 12 | `JOB_CONF_DATE` | Job_Confessorial Date | DATE | 7 |  | Y |
| 13 | `JOB_TOT_WGT` | Job_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 14 | `JOB_TOT_WGT_NET` | Job_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 15 | `JOB_SHIP_QTY` | Job_Shipessorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `JOB_SKU_CLASS_NUM1_QTY` | Job_Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `JOB_SKU_CLASS_NUM2_QTY` | Job_Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `JOB_SKU_CLASS_NUM3_QTY` | Job_Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `JOB_SKU_CLASS_NUM4_QTY` | Job_Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `JOB_SKU_CLASS_NUM5_QTY` | Job_Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 21 | `JOB_NUM_OF_LINES` | Job_Num_Ofessorial Lines | NUMBER | 22 | 4 | Y |
| 22 | `JOB_NUM_OF_LOC_LINES` | Job_Num_Of_Locessorial Lines | NUMBER | 22 | 4 | Y |
| 23 | `JOB_TOT_CUBE` | Job_Totessorial Cube | NUMBER | 22 | 16 | Y |

## `C_JOB_MGR`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 6 | `JOB_RQST_CODE` | Job_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `JOB_RQST_DATE` | Job_Rqstessorial Date | DATE | 7 |  | N |
| 8 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 9 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 10 | `JOB_ERR_DATE` | Job_Erressorial Date | DATE | 7 |  | Y |
| 11 | `JOB_ERR_NUM` | Job_Erressorial Num | NUMBER | 22 | 3 | Y |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `JOB_RQST_PRTY_NUM` | Job_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 14 | `JOB_TP_PRTY_NUM` | Job_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |

## `C_JOB_MGR_HIST`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 6 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 6 | `JOB_RQST_CODE` | Job_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `JOB_RQST_DATE` | Job_Rqstessorial Date | DATE | 7 |  | N |
| 8 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 9 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 10 | `JOB_ERR_DATE` | Job_Erressorial Date | DATE | 7 |  | Y |
| 11 | `JOB_ERR_NUM` | Job_Erressorial Num | NUMBER | 22 | 3 | Y |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `JOB_RQST_PRTY_NUM` | Job_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 14 | `JOB_TP_PRTY_NUM` | Job_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |

## `C_JOB_PROS`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WHSE_LAB_STD_MODY_NUM` | Warehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 7 | `CUST_LAB_STD_MODY_NUM` | Cust_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `CARR_LAB_STD_MODY_NUM` | Carr_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `CON_LAB_STD_MODY_NUM` | Con_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 10 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 11 | `LOAD_TP_LAB_STD_MODY_NUM` | Load_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 12 | `PROS_START_DATE` | Pros_Startessorial Date | DATE | 7 |  | Y |
| 13 | `PROS_END_DATE` | Pros_Endessorial Date | DATE | 7 |  | Y |
| 14 | `PROS_DLINE_DATE` | Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 15 | `PROS_EST_START_DATE` | Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 16 | `PROS_EST_START_MAN_FLAG` | Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `PROS_EST_START_OVRR_FLAG` | Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `PROS_EST_END_DATE` | Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 19 | `PROS_EST_END_MAN_FLAG` | Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `PROS_EST_END_OVRR_FLAG` | Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `PROS_PCENT_COMPL` | Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 22 | `PROS_PCENT_MAN_FLAG` | Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `PROS_PCENT_OVRR_FLAG` | Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `PROS_EST_TIME_HIST` | Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `PROS_EST_TIME_MAN` | Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `PROS_EST_TIME` | Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `PROS_EST_TIME_REMA_HIST` | Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 28 | `PROS_EST_TIME_REMA` | Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 29 | `PROS_EST_TIME_REMA_MAN` | Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 30 | `PROS_WAVE_ALLOC_FLAG` | Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `PROS_PCENT_COMPL_ADJ` | Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 32 | `PROS_EST_TIME_REMA_ADJ` | Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |

## `C_JOB_PROS_HIST`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WHSE_LAB_STD_MODY_NUM` | Warehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 7 | `CUST_LAB_STD_MODY_NUM` | Cust_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `CARR_LAB_STD_MODY_NUM` | Carr_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `CON_LAB_STD_MODY_NUM` | Con_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 10 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 11 | `LOAD_TP_LAB_STD_MODY_NUM` | Load_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 12 | `PROS_START_DATE` | Pros_Startessorial Date | DATE | 7 |  | Y |
| 13 | `PROS_END_DATE` | Pros_Endessorial Date | DATE | 7 |  | Y |
| 14 | `PROS_DLINE_DATE` | Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 15 | `PROS_EST_START_DATE` | Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 16 | `PROS_EST_START_MAN_FLAG` | Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `PROS_EST_START_OVRR_FLAG` | Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `PROS_EST_END_DATE` | Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 19 | `PROS_EST_END_MAN_FLAG` | Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `PROS_EST_END_OVRR_FLAG` | Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `PROS_PCENT_COMPL` | Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 22 | `PROS_PCENT_MAN_FLAG` | Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `PROS_PCENT_OVRR_FLAG` | Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `PROS_EST_TIME_HIST` | Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `PROS_EST_TIME_MAN` | Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `PROS_EST_TIME` | Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `PROS_EST_TIME_REMA_HIST` | Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 28 | `PROS_EST_TIME_REMA` | Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 29 | `PROS_EST_TIME_REMA_MAN` | Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 30 | `PROS_WAVE_ALLOC_FLAG` | Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `PROS_PCENT_COMPL_ADJ` | Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 32 | `PROS_EST_TIME_REMA_ADJ` | Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |

## `C_JOB_PURGE`

- **Tipo:** Transactional
- **Categoria:** Job
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 4 | `PURGE_MV_FLAG` | Purge_Mvessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `PURGE_CREATE_DATE` | Purge_Createessorial Date | DATE | 7 |  | N |
| 6 | `PURGE_TO_PROS_DATE` | Purge_To_Prosessorial Date | DATE | 7 |  | N |

## `H_JOB`

- **Tipo:** Historical
- **Categoria:** Job
- **Campos:** 70
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 7 | `JOB_TP` | Jobessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 9 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 10 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 11 | `JOB_DATE` | Jobessorial Date | DATE | 7 |  | N |
| 12 | `JOB_CONF_DATE` | Job_Confessorial Date | DATE | 7 |  | Y |
| 13 | `JOB_TOT_WGT` | Job_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `JOB_TOT_WGT_NET` | Job_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `SKU_CLASS_NUM1_QTY` | Sku_Class_Num1essorial Qty | NUMBER | 22 | 9 | Y |
| 16 | `SKU_CLASS_NUM2_QTY` | Sku_Class_Num2essorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `SKU_CLASS_NUM3_QTY` | Sku_Class_Num3essorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `SKU_CLASS_NUM4_QTY` | Sku_Class_Num4essorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `SKU_CLASS_NUM5_QTY` | Sku_Class_Num5essorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `JOB_NUM_LINE` | Job_Numessorial Line | NUMBER | 22 | 4 | N |
| 21 | `JOB_NUM_LOC_LINE` | Job_Num_Locessorial Line | NUMBER | 22 | 4 | N |
| 22 | `JOB_TOT_CUBE` | Job_Totessorial Cube | NUMBER | 22 | 16 | N |
| 23 | `JOB_LAB_STD_ERR_FLAG` | Job_Lab_Std_Erressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `JOB_EST_METH_FLAG` | Job_Est_Methessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `JOB_EST_TIME_HIST` | Job_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 26 | `JOB_EST_TIME_MAN` | Job_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 27 | `JOB_EST_TIME` | Job_Estessorial Time | NUMBER | 22 | 6 | Y |
| 28 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 29 | `JOB_PRTY_NUM` | Job_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 30 | `JOB_PRTY_CODE_INIT_DATE` | Job_Prty_Code_Initessorial Date | DATE | 7 |  | Y |
| 31 | `JOB_PRTY_OVRR_FLAG` | Job_Prty_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `JOB_PRTY_MAN_FLAG` | Job_Prty_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `JOB_CREATE_DATE` | Job_Createessorial Date | DATE | 7 |  | Y |
| 34 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 35 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 36 | `JOB_DLINE_DATE` | Job_Dlineessorial Date | DATE | 7 |  | Y |
| 37 | `JOB_EST_START_DATE` | Job_Est_Startessorial Date | DATE | 7 |  | Y |
| 38 | `JOB_EST_START_MAN_FLAG` | Job_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `JOB_EST_START_OVRR_FLAG` | Job_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `JOB_EST_END_DATE` | Job_Est_Endessorial Date | DATE | 7 |  | Y |
| 41 | `JOB_EST_END_MAN_FLAG` | Job_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `JOB_EST_END_OVRR_FLAG` | Job_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `JOB_PCENT_COMPL` | Job_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 44 | `JOB_PCENT_MAN_FLAG` | Job_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `JOB_PCENT_OVRR_FLAG` | Job_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 46 | `JOB_PURGE_DATE` | Job_Purgeessorial Date | DATE | 7 |  | Y |
| 47 | `JOB_EST_TIME_REMA_HIST` | Job_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 48 | `JOB_EST_TIME_REMA` | Job_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 49 | `JOB_EST_TIME_REMA_MAN` | Job_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 50 | `JOB_TO_PROS_DATE` | Job_To_Prosessorial Date | DATE | 7 |  | Y |
| 51 | `JOB_TO_ARR_DATE` | Job_To_Arressorial Date | DATE | 7 |  | Y |
| 52 | `JOB_APPO_DATE` | Job_Appoessorial Date | DATE | 7 |  | Y |
| 53 | `JOB_CNVC_QTY` | Job_Cnvcessorial Qty | NUMBER | 22 | 9 | N |
| 54 | `JOB_MODSKU` | Jobessorial Modsku | NUMBER | 22 | 9 | N |
| 55 | `JOB_ASS_DATE` | Job_Assessorial Date | DATE | 7 |  | Y |
| 56 | `LAST_RECALC_DATE` | Last_Recalcessorial Date | DATE | 7 |  | N |
| 57 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 58 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 59 | `JOB_HOLD_DATE` | Job_Holdessorial Date | DATE | 7 |  | Y |
| 60 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `JOB_WAVE_ALLOC_INIT_FLAG` | Job_Wave_Alloc_Initessorial Flag | VARCHAR2 | 1 |  | Y |
| 62 | `JOB_WAVE_ALLOC_COMPL_FLAG` | Job_Wave_Alloc_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `HOST_JOB_NUM` | Host_Jobessorial Num | NUMBER | 22 | 9 | Y |
| 64 | `JOB_CANCEL_DATE` | Job_Cancelessorial Date | DATE | 7 |  | Y |
| 65 | `JOB_PCENT_COMPL_ADJ` | Job_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 66 | `JOB_EST_TIME_REMA_ADJ` | Job_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |
| 67 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | Y |
| 68 | `CARR_STD_ALPHA_CODE` | Carr_Std_Alphaessorial Code | VARCHAR2 | 4 |  | Y |
| 69 | `CON_PRTY_NUM` | Con_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 70 | `JOB_PROS_FLAG` | Job_Prosessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_JOB_MGR`

- **Tipo:** Historical
- **Categoria:** Job
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_RQST_SEQ_NUM` | Job_Rqst_Seqessorial Num | NUMBER | 22 | 7 | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 6 | `JOB_RQST_CODE` | Job_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `JOB_RQST_DATE` | Job_Rqstessorial Date | DATE | 7 |  | N |
| 8 | `JOB_START_DATE` | Job_Startessorial Date | DATE | 7 |  | Y |
| 9 | `JOB_END_DATE` | Job_Endessorial Date | DATE | 7 |  | Y |
| 10 | `JOB_ERR_DATE` | Job_Erressorial Date | DATE | 7 |  | Y |
| 11 | `JOB_ERR_NUM` | Job_Erressorial Num | NUMBER | 22 | 3 | Y |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `JOB_RQST_PRTY_NUM` | Job_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 14 | `JOB_TP_PRTY_NUM` | Job_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |

## `H_JOB_PROS`

- **Tipo:** Historical
- **Categoria:** Job
- **Campos:** 32
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 6 | `WHSE_LAB_STD_MODY_NUM` | Warehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 7 | `CUST_LAB_STD_MODY_NUM` | Cust_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `CARR_LAB_STD_MODY_NUM` | Carr_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `CON_LAB_STD_MODY_NUM` | Con_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 10 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 11 | `LOAD_TP_LAB_STD_MODY_NUM` | Load_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 12 | `PROS_START_DATE` | Pros_Startessorial Date | DATE | 7 |  | Y |
| 13 | `PROS_END_DATE` | Pros_Endessorial Date | DATE | 7 |  | Y |
| 14 | `PROS_DLINE_DATE` | Pros_Dlineessorial Date | DATE | 7 |  | Y |
| 15 | `PROS_EST_START_DATE` | Pros_Est_Startessorial Date | DATE | 7 |  | Y |
| 16 | `PROS_EST_START_MAN_FLAG` | Pros_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `PROS_EST_START_OVRR_FLAG` | Pros_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `PROS_EST_END_DATE` | Pros_Est_Endessorial Date | DATE | 7 |  | Y |
| 19 | `PROS_EST_END_MAN_FLAG` | Pros_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `PROS_EST_END_OVRR_FLAG` | Pros_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `PROS_PCENT_COMPL` | Pros_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 22 | `PROS_PCENT_MAN_FLAG` | Pros_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `PROS_PCENT_OVRR_FLAG` | Pros_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `PROS_EST_TIME_HIST` | Pros_Est_Timeessorial Hist | VARCHAR2 | 6 |  | Y |
| 25 | `PROS_EST_TIME_MAN` | Pros_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 26 | `PROS_EST_TIME` | Pros_Estessorial Time | NUMBER | 22 | 6 | Y |
| 27 | `PROS_EST_TIME_REMA_HIST` | Pros_Est_Time_Remaessorial Hist | NUMBER | 22 | 6 | Y |
| 28 | `PROS_EST_TIME_REMA` | Pros_Est_Timeessorial Rema | NUMBER | 22 | 6 | Y |
| 29 | `PROS_EST_TIME_REMA_MAN` | Pros_Est_Time_Remaessorial Man | NUMBER | 22 | 6 | Y |
| 30 | `PROS_WAVE_ALLOC_FLAG` | Pros_Wave_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `PROS_PCENT_COMPL_ADJ` | Pros_Pcent_Complessorial Adj | NUMBER | 22 | 4 | Y |
| 32 | `PROS_EST_TIME_REMA_ADJ` | Pros_Est_Time_Remaessorial Adj | NUMBER | 22 | 6 | Y |

## `M_JOB_CLASS`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `JOB_CLASS_CODE` | Job_Classessorial Code | VARCHAR2 | 6 |  | N |
| 2 | `JOB_CLASS_DES` | Job_Classessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `JOB_CLASS_STAT` | Job_Classessorial Stat | VARCHAR2 | 1 |  | N |

## `M_JOB_FUN_D`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WO_SER_CODE` | Warehouse Ser Code | VARCHAR2 | 4 |  | N |

## `M_JOB_FUN_H`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `JOB_FUN_DES` | Job_Funessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 5 | `JOB_FUN_STAT` | Job_Funessorial Stat | VARCHAR2 | 1 |  | N |

## `M_JOB_FUN_H_`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `JOB_FUN_DES` | Job_Funessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `REVN_ANAL_CODE` | Revenue Analysis Code | VARCHAR2 | 4 |  | N |
| 5 | `JOB_FUN_STAT` | Job_Funessorial Stat | VARCHAR2 | 1 |  | N |

## `M_JOB_MGR_PARA_D1`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_RQST_CODE` | Job_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `JOB_RQST_PRTY_NUM` | Job_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |

## `M_JOB_MGR_PARA_D2`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `JOB_TP_PRTY_NUM` | Job_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 4 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `M_JOB_MGR_PARA_H`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DEF_JOB_RQST_PRTY_NUM` | Def_Job_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 3 | `DEF_JOB_TP_PRTY_NUM` | Def_Job_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 4 | `JOB_MGR_SLEEP_MINT_NUM` | Job_Mgr_Sleep_Mintessorial Num | NUMBER | 22 | 4 | N |
| 5 | `JOB_MGR_SLEEP_SECD_NUM` | Job_Mgr_Sleep_Secdessorial Num | NUMBER | 22 | 4 | N |
| 6 | `TRSFR_HIST_JOB_COMPL_FLAG` | Trsfr_Hist_Job_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `TRSFR_HIST_DAY_NUM` | Trsfr_Hist_Dayessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `INCL_PASSV_TASK_MGR_REP_FLAG` | Incl_Passv_Task_Mgr_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `PURGE_DAY_NUM` | Purge_Dayessorial Num | NUMBER | 22 | 4 | Y |
| 10 | `PURGE_HIST_DAY_NUM` | Purge_Hist_Dayessorial Num | NUMBER | 22 | 4 | Y |
| 11 | `NUM_OF_REC_TO_COMMIT` | Num_Of_Rec_Toessorial Commit | NUMBER | 22 | 6 | Y |

## `M_JOB_TP_D`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_JOB_TP_H`

- **Tipo:** Master
- **Categoria:** Job
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `JOB_TP_DES` | Job_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `JOB_TP_STAT` | Job_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 8 | `CRM_CODE` | Crmessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 15 | `JOB_TP_DIR_LAB_TP_FLAG` | Job_Tp_Dir_Lab_Tpessorial Flag | VARCHAR2 | 1 |  | Y |

