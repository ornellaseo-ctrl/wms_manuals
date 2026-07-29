# Tabelas — Employee

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **15**.

## `C_EMP_TASK_D1`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 11
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TIME_STAMP_DATE` | Time_Stampessorial Date | DATE | 7 |  | N |
| 3 | `TIME_STAMP_TP_CODE` | Time_Stamp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 6 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | N |
| 7 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 8 | `EMP_HOUR_COST` | Emp_Houressorial Cost | NUMBER | 22 | 8 | Y |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 11 | `EMP_TOT_TIME_FLAG` | Emp_Tot_Timeessorial Flag | VARCHAR2 | 1 |  | N |

## `C_EMP_TASK_D1_HIST`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 11
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TIME_STAMP_DATE` | Time_Stampessorial Date | DATE | 7 |  | N |
| 3 | `TIME_STAMP_TP_CODE` | Time_Stamp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 6 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | N |
| 7 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 8 | `EMP_HOUR_COST` | Emp_Houressorial Cost | NUMBER | 22 | 8 | Y |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 11 | `EMP_TOT_TIME_FLAG` | Emp_Tot_Timeessorial Flag | VARCHAR2 | 1 |  | N |

## `C_EMP_TASK_D2`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `REM_TEXT` | Remessorial Text | VARCHAR2 | 45 |  | N |

## `C_EMP_TASK_D2_HIST`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `REM_TEXT` | Remessorial Text | VARCHAR2 | 45 |  | N |

## `C_EMP_TASK_D3`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `FLOW_PROS_STEP_NUM` | Flow_Pros_Stepessorial Num | NUMBER | 22 | 2 | N |
| 3 | `FLOW_PROS_SCR_ENTRY` | Flow_Pros_Scressorial Entry | VARCHAR2 | 40 |  | N |

## `C_EMP_TASK_H`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 105
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | Y |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 7 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 8 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `EMP_TASK_CREATE_DATE` | Emp_Task_Createessorial Date | DATE | 7 |  | N |
| 12 | `EMP_TASK_START_DATE` | Emp_Task_Startessorial Date | DATE | 7 |  | Y |
| 13 | `EMP_TASK_END_DATE` | Emp_Task_Endessorial Date | DATE | 7 |  | Y |
| 14 | `EMP_TASK_TOT_TIME` | Emp_Task_Totessorial Time | NUMBER | 22 | 6 | Y |
| 15 | `EMP_TASK_TRANS_LEV_FLAG` | Emp_Task_Trans_Levessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `EMP_TASK_TRANS_TP_FLAG` | Emp_Task_Trans_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `EMP_TASK_PARENT_PROG` | Emp_Task_Parentessorial Prog | VARCHAR2 | 14 |  | N |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 19 | `EMP_TASK_MARK_FOR_DEL_FLAG` | Emp_Task_Mark_For_Delessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `EMP_TASK_OK_FLAG` | Emp_Task_Okessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `JOB_LINE_NUM` | Job_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 22 | `JOB_LOC_LINE_NUM` | Job_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 23 | `WHSE_CODE_CRNT` | Whse_Codeessorial Crnt | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_CRNT` | Loc_Codeessorial Crnt | VARCHAR2 | 12 |  | Y |
| 25 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 26 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 27 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | Y |
| 28 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | Y |
| 29 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 30 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 31 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 32 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 33 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 34 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 35 | `SKU_CODE1` | Skuessorial Code1 | VARCHAR2 | 4 |  | Y |
| 36 | `INVT_QTY_BKD_NUM1` | Invt_Qty_Bkdessorial Num1 | NUMBER | 22 | 9 | Y |
| 37 | `EMP_TASK_QTY1` | Emp_Taskessorial Qty1 | NUMBER | 22 | 9 | Y |
| 38 | `SKU_CODE2` | Skuessorial Code2 | VARCHAR2 | 4 |  | Y |
| 39 | `INVT_QTY_BKD_NUM2` | Invt_Qty_Bkdessorial Num2 | NUMBER | 22 | 9 | Y |
| 40 | `EMP_TASK_QTY2` | Emp_Taskessorial Qty2 | NUMBER | 22 | 9 | Y |
| 41 | `SKU_CODE3` | Skuessorial Code3 | VARCHAR2 | 4 |  | Y |
| 42 | `INVT_QTY_BKD_NUM3` | Invt_Qty_Bkdessorial Num3 | NUMBER | 22 | 9 | Y |
| 43 | `EMP_TASK_QTY3` | Emp_Taskessorial Qty3 | NUMBER | 22 | 9 | Y |
| 44 | `SKU_CODE4` | Skuessorial Code4 | VARCHAR2 | 4 |  | Y |
| 45 | `INVT_QTY_BKD_NUM4` | Invt_Qty_Bkdessorial Num4 | NUMBER | 22 | 9 | Y |
| 46 | `EMP_TASK_QTY4` | Emp_Taskessorial Qty4 | NUMBER | 22 | 9 | Y |
| 47 | `SKU_CODE5` | Skuessorial Code5 | VARCHAR2 | 4 |  | Y |
| 48 | `INVT_QTY_BKD_NUM5` | Invt_Qty_Bkdessorial Num5 | NUMBER | 22 | 9 | Y |
| 49 | `EMP_TASK_QTY5` | Emp_Taskessorial Qty5 | NUMBER | 22 | 9 | Y |
| 50 | `EMP_TASK_TOT_WGT` | Emp_Task_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 51 | `EMP_TASK_TOT_WGT_NET` | Emp_Task_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 52 | `EMP_TASK_TOT_CUBE` | Emp_Task_Totessorial Cube | NUMBER | 22 | 16 | Y |
| 53 | `EMP_TASK_REM_FLAG` | Emp_Task_Remessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `EMP_TASK_PAY` | Emp_Taskessorial Pay | NUMBER | 22 | 6 | Y |
| 55 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 56 | `EMP_HOUR_PAY` | Emp_Houressorial Pay | NUMBER | 22 | 8 | Y |
| 57 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 58 | `MHE_CODE_TASK_COST` | Mhe_Code_Taskessorial Cost | NUMBER | 22 | 6 | Y |
| 59 | `EMP_TASK_LINK_SEQ_NUM` | Emp_Task_Link_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 60 | `EMP_TASK_DLINE_DATE` | Emp_Task_Dlineessorial Date | DATE | 7 |  | Y |
| 61 | `EMP_TASK_EST_START_DATE` | Emp_Task_Est_Startessorial Date | DATE | 7 |  | Y |
| 62 | `EMP_TASK_EST_START_MAN_FLAG` | Emp_Task_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `EMP_TASK_EST_START_OVRR_FLAG` | Emp_Task_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 64 | `EMP_TASK_EST_END_DATE` | Emp_Task_Est_Endessorial Date | DATE | 7 |  | Y |
| 65 | `EMP_TASK_EST_END_MAN_FLAG` | Emp_Task_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 66 | `EMP_TASK_EST_END_OVRR_FLAG` | Emp_Task_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 67 | `EMP_TASK_EST_TIME_HIST` | Emp_Task_Est_Timeessorial Hist | NUMBER | 22 | 6 | Y |
| 68 | `EMP_TASK_EST_TIME` | Emp_Task_Estessorial Time | NUMBER | 22 | 6 | Y |
| 69 | `EMP_TASK_EST_TIME_MAN` | Emp_Task_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 70 | `EMP_TASK_PCENT_COMPL` | Emp_Task_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 71 | `EMP_TASK_PCENT_MAN_FLAG` | Emp_Task_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 72 | `EMP_TASK_PCENT_OVRR_FLAG` | Emp_Task_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 73 | `EMP_TASK_PRTY_NUM` | Emp_Task_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 74 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 75 | `EMP_TASK_HOLD_FLAG` | Emp_Task_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `EMP_TASK_QTY` | Emp_Taskessorial Qty | NUMBER | 22 | 9 | Y |
| 77 | `WHSE_CODE_FLT` | Whse_Codeessorial Flt | VARCHAR2 | 4 |  | Y |
| 78 | `LOC_CODE_FLT` | Loc_Codeessorial Flt | VARCHAR2 | 12 |  | Y |
| 79 | `EMP_TASK_EMPTY_TOTE_FLAG` | Emp_Task_Empty_Toteessorial Flag | VARCHAR2 | 1 |  | Y |
| 80 | `EMP_TASK_TOTE_DUMMY_FLAG` | Emp_Task_Tote_Dummyessorial Flag | VARCHAR2 | 1 |  | Y |
| 81 | `EMP_TASK_EST_TIME_WAVE` | Emp_Task_Est_Timeessorial Wave | NUMBER | 22 | 6 | Y |
| 82 | `CONV_ID` | Convessorial Id | VARCHAR2 | 12 |  | Y |
| 83 | `ITEM_SET_CODE` | Item_Setessorial Code | VARCHAR2 | 20 |  | Y |
| 84 | `EMP_TASK_ITEM_SET_QTY` | Emp_Task_Item_Setessorial Qty | NUMBER | 22 | 9 | Y |
| 85 | `FLOW_PROS_PRTY_NUM` | Flow_Pros_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 86 | `ZONE_LAB_STD_MODY_NUM` | Zarehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 87 | `ITEM_LAB_STD_MODY_NUM` | Item_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 88 | `MHE_TP_LAB_STD_MODY_NUM` | Mhe_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 89 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 90 | `LOC_TP_LAB_STD_MODY_NUM` | Loc_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 91 | `EMP_TASK_LINE_TP` | Emp_Task_Lineessorial Tp | VARCHAR2 | 1 |  | Y |
| 92 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 93 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 94 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 95 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 96 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 97 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 98 | `UNIT_RETAIL_PRICE` | Unit_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 99 | `UNIT_DISC_PRICE` | Unit_Discessorial Price | NUMBER | 22 | 12 | Y |
| 100 | `UNIT_COST` | Unitessorial Cost | NUMBER | 22 | 12 | Y |
| 101 | `ACC_CODE` | Accessorial Code | VARCHAR2 | 10 |  | Y |
| 102 | `ACC_TP_CODE` | Acc_Tpessorial Code | VARCHAR2 | 1 |  | Y |
| 103 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 104 | `ITEM_CODE_MAST` | Item_Codeessorial Mast | VARCHAR2 | 20 |  | Y |
| 105 | `EMP_TASK_OVPI_FLAG` | Emp_Task_Ovpiessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_EMP_TASK_H_HIST`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 93
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | Y |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 7 | `JOB_NUM` | Job Number | NUMBER | 22 | 6 | Y |
| 8 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `EMP_TASK_CREATE_DATE` | Emp_Task_Createessorial Date | DATE | 7 |  | N |
| 12 | `EMP_TASK_START_DATE` | Emp_Task_Startessorial Date | DATE | 7 |  | Y |
| 13 | `EMP_TASK_END_DATE` | Emp_Task_Endessorial Date | DATE | 7 |  | Y |
| 14 | `EMP_TASK_TOT_TIME` | Emp_Task_Totessorial Time | NUMBER | 22 | 6 | Y |
| 15 | `EMP_TASK_TRANS_LEV_FLAG` | Emp_Task_Trans_Levessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `EMP_TASK_TRANS_TP_FLAG` | Emp_Task_Trans_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `EMP_TASK_PARENT_PROG` | Emp_Task_Parentessorial Prog | VARCHAR2 | 14 |  | N |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 19 | `EMP_TASK_MARK_FOR_DEL_FLAG` | Emp_Task_Mark_For_Delessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `EMP_TASK_OK_FLAG` | Emp_Task_Okessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `JOB_LINE_NUM` | Job_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 22 | `JOB_LOC_LINE_NUM` | Job_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 23 | `WHSE_CODE_CRNT` | Whse_Codeessorial Crnt | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_CRNT` | Loc_Codeessorial Crnt | VARCHAR2 | 12 |  | Y |
| 25 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 26 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 27 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | Y |
| 28 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | Y |
| 29 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 30 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 31 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 32 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 33 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 34 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 35 | `SKU_CODE1` | Skuessorial Code1 | VARCHAR2 | 4 |  | Y |
| 36 | `INVT_QTY_BKD_NUM1` | Invt_Qty_Bkdessorial Num1 | NUMBER | 22 | 9 | Y |
| 37 | `EMP_TASK_QTY1` | Emp_Taskessorial Qty1 | NUMBER | 22 | 9 | Y |
| 38 | `SKU_CODE2` | Skuessorial Code2 | VARCHAR2 | 4 |  | Y |
| 39 | `INVT_QTY_BKD_NUM2` | Invt_Qty_Bkdessorial Num2 | NUMBER | 22 | 9 | Y |
| 40 | `EMP_TASK_QTY2` | Emp_Taskessorial Qty2 | NUMBER | 22 | 9 | Y |
| 41 | `SKU_CODE3` | Skuessorial Code3 | VARCHAR2 | 4 |  | Y |
| 42 | `INVT_QTY_BKD_NUM3` | Invt_Qty_Bkdessorial Num3 | NUMBER | 22 | 9 | Y |
| 43 | `EMP_TASK_QTY3` | Emp_Taskessorial Qty3 | NUMBER | 22 | 9 | Y |
| 44 | `SKU_CODE4` | Skuessorial Code4 | VARCHAR2 | 4 |  | Y |
| 45 | `INVT_QTY_BKD_NUM4` | Invt_Qty_Bkdessorial Num4 | NUMBER | 22 | 9 | Y |
| 46 | `EMP_TASK_QTY4` | Emp_Taskessorial Qty4 | NUMBER | 22 | 9 | Y |
| 47 | `SKU_CODE5` | Skuessorial Code5 | VARCHAR2 | 4 |  | Y |
| 48 | `INVT_QTY_BKD_NUM5` | Invt_Qty_Bkdessorial Num5 | NUMBER | 22 | 9 | Y |
| 49 | `EMP_TASK_QTY5` | Emp_Taskessorial Qty5 | NUMBER | 22 | 9 | Y |
| 50 | `EMP_TASK_TOT_WGT` | Emp_Task_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 51 | `EMP_TASK_TOT_WGT_NET` | Emp_Task_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 52 | `EMP_TASK_TOT_CUBE` | Emp_Task_Totessorial Cube | NUMBER | 22 | 16 | Y |
| 53 | `EMP_TASK_REM_FLAG` | Emp_Task_Remessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `EMP_TASK_PAY` | Emp_Taskessorial Pay | NUMBER | 22 | 6 | Y |
| 55 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 56 | `EMP_HOUR_PAY` | Emp_Houressorial Pay | NUMBER | 22 | 8 | Y |
| 57 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 58 | `MHE_CODE_TASK_COST` | Mhe_Code_Taskessorial Cost | NUMBER | 22 | 6 | Y |
| 59 | `EMP_TASK_LINK_SEQ_NUM` | Emp_Task_Link_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 60 | `EMP_TASK_DLINE_DATE` | Emp_Task_Dlineessorial Date | DATE | 7 |  | Y |
| 61 | `EMP_TASK_EST_START_DATE` | Emp_Task_Est_Startessorial Date | DATE | 7 |  | Y |
| 62 | `EMP_TASK_EST_START_MAN_FLAG` | Emp_Task_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `EMP_TASK_EST_START_OVRR_FLAG` | Emp_Task_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 64 | `EMP_TASK_EST_END_DATE` | Emp_Task_Est_Endessorial Date | DATE | 7 |  | Y |
| 65 | `EMP_TASK_EST_END_MAN_FLAG` | Emp_Task_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 66 | `EMP_TASK_EST_END_OVRR_FLAG` | Emp_Task_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 67 | `EMP_TASK_EST_TIME_HIST` | Emp_Task_Est_Timeessorial Hist | NUMBER | 22 | 6 | Y |
| 68 | `EMP_TASK_EST_TIME` | Emp_Task_Estessorial Time | NUMBER | 22 | 6 | Y |
| 69 | `EMP_TASK_EST_TIME_MAN` | Emp_Task_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 70 | `EMP_TASK_PCENT_COMPL` | Emp_Task_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 71 | `EMP_TASK_PCENT_MAN_FLAG` | Emp_Task_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 72 | `EMP_TASK_PCENT_OVRR_FLAG` | Emp_Task_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 73 | `EMP_TASK_PRTY_NUM` | Emp_Task_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 74 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 75 | `EMP_TASK_HOLD_FLAG` | Emp_Task_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `EMP_TASK_QTY` | Emp_Taskessorial Qty | NUMBER | 22 | 9 | Y |
| 77 | `WHSE_CODE_FLT` | Whse_Codeessorial Flt | VARCHAR2 | 4 |  | Y |
| 78 | `LOC_CODE_FLT` | Loc_Codeessorial Flt | VARCHAR2 | 12 |  | Y |
| 79 | `EMP_TASK_EMPTY_TOTE_FLAG` | Emp_Task_Empty_Toteessorial Flag | VARCHAR2 | 1 |  | Y |
| 80 | `EMP_TASK_TOTE_DUMMY_FLAG` | Emp_Task_Tote_Dummyessorial Flag | VARCHAR2 | 1 |  | Y |
| 81 | `EMP_TASK_EST_TIME_WAVE` | Emp_Task_Est_Timeessorial Wave | NUMBER | 22 | 6 | Y |
| 82 | `CONV_ID` | Convessorial Id | VARCHAR2 | 12 |  | Y |
| 83 | `ITEM_SET_CODE` | Item_Setessorial Code | VARCHAR2 | 20 |  | Y |
| 84 | `EMP_TASK_ITEM_SET_QTY` | Emp_Task_Item_Setessorial Qty | NUMBER | 22 | 9 | Y |
| 85 | `FLOW_PROS_PRTY_NUM` | Flow_Pros_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 86 | `ZONE_LAB_STD_MODY_NUM` | Zarehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 87 | `ITEM_LAB_STD_MODY_NUM` | Item_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 88 | `MHE_TP_LAB_STD_MODY_NUM` | Mhe_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 89 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 90 | `LOC_TP_LAB_STD_MODY_NUM` | Loc_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 91 | `EMP_TASK_LINE_TP` | Emp_Task_Lineessorial Tp | VARCHAR2 | 1 |  | Y |
| 92 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 93 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `C_EMP_TASK_STEP`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | Y |
| 5 | `START_DATE` | Startessorial Date | DATE | 7 |  | Y |
| 6 | `END_DATE` | Endessorial Date | DATE | 7 |  | Y |
| 7 | `TIME_STAMP_TP_CODE` | Time_Stamp_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `STEP_SECD` | Stepessorial Secd | NUMBER | 22 | 6 | Y |
| 9 | `NUM_OPEN_TASK` | Num_Openessorial Task | NUMBER | 22 | 4 | Y |
| 10 | `WGTED_SECD` | Wgtedessorial Secd | NUMBER | 22 | 9 | Y |
| 11 | `EMP_TOT_TIME_FLAG` | Emp_Tot_Timeessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `TASK_QTY` | Taskessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `TASK_SET_QTY` | Task_Setessorial Qty | NUMBER | 22 | 1 | Y |
| 14 | `TASK_TOTE_QTY` | Task_Toteessorial Qty | NUMBER | 22 | 1 | Y |
| 15 | `TASK_GIFT_QTY` | Task_Giftessorial Qty | NUMBER | 22 | 1 | Y |
| 16 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 17 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 18 | `TASK_LOOSE_QTY` | Task_Looseessorial Qty | NUMBER | 22 | 9 | Y |
| 19 | `TASK_PLT_QTY` | Task_Pltessorial Qty | NUMBER | 22 | 1 | Y |
| 20 | `TASK_CART_QTY` | Task_Cartessorial Qty | NUMBER | 22 | 1 | Y |

## `C_EMP_TASK_SUMM`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | Y |
| 3 | `TASK_DATE` | Taskessorial Date | DATE | 7 |  | Y |
| 4 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | Y |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 6 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 7 | `TOT_TIME` | Totessorial Time | NUMBER | 22 | 9 | Y |
| 8 | `TASK_QTY` | Taskessorial Qty | NUMBER | 22 | 6 | Y |
| 9 | `TASK_SET_QTY` | Task_Setessorial Qty | NUMBER | 22 | 6 | Y |
| 10 | `TASK_BOX_QTY` | Task_Boxessorial Qty | NUMBER | 22 | 6 | Y |
| 11 | `TASK_PLT_QTY` | Task_Pltessorial Qty | NUMBER | 22 | 6 | Y |
| 12 | `TASK_CART_QTY` | Task_Cartessorial Qty | NUMBER | 22 | 6 | Y |
| 13 | `TASK_ACCESS_QTY` | Task_Accessessorial Qty | NUMBER | 22 | 6 | Y |
| 14 | `TASK_TOTE_QTY` | Task_Toteessorial Qty | NUMBER | 22 | 6 | Y |
| 15 | `TASK_GIFT_QTY` | Task_Giftessorial Qty | NUMBER | 22 | 6 | Y |
| 16 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 17 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 18 | `TASK_LOOSE_QTY` | Task_Looseessorial Qty | NUMBER | 22 | 9 | Y |

## `EMP`

- **Tipo:** Misc
- **Categoria:** Employee
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMPNO` | Empnoessorial Empno | NUMBER | 22 | 4 | N |
| 2 | `ENAME` | Enameessorial Ename | VARCHAR2 | 10 |  | Y |
| 3 | `JOB` | Jobessorial Job | VARCHAR2 | 9 |  | Y |
| 4 | `MGR` | Mgressorial Mgr | NUMBER | 22 | 4 | Y |
| 5 | `HIREDATE` | Hiredateessorial Hiredate | DATE | 7 |  | Y |
| 6 | `SAL` | Salessorial Sal | NUMBER | 22 | 7 | Y |
| 7 | `COMM` | Commessorial Comm | NUMBER | 22 | 7 | Y |
| 8 | `DEPTNO` | Deptnoessorial Deptno | NUMBER | 22 | 2 | Y |

## `E_EMP_LOG_D`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 5
- **Campos-chave prováveis:** ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 3 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |

## `E_EMP_LOG_H`

- **Tipo:** Transactional
- **Categoria:** Employee
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `EMP_LOG_START_DATE` | Emp_Log_Startessorial Date | DATE | 7 |  | N |
| 3 | `EMP_LOG_END_DATE` | Emp_Log_Endessorial Date | DATE | 7 |  | Y |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 5 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 10 | `REL_OP_CODE` | Rel_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 11 | `RF_TER_CODE` | Rf_Teressorial Code | VARCHAR2 | 20 |  | Y |

## `H_EMP_TASK_D1`

- **Tipo:** Historical
- **Categoria:** Employee
- **Campos:** 11
- **Campos-chave prováveis:** LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TIME_STAMP_DATE` | Time_Stampessorial Date | DATE | 7 |  | N |
| 3 | `TIME_STAMP_TP_CODE` | Time_Stamp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 6 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | N |
| 7 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 8 | `EMP_HOUR_COST` | Emp_Houressorial Cost | NUMBER | 22 | 8 | Y |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 11 | `EMP_TOT_TIME_FLAG` | Emp_Tot_Timeessorial Flag | VARCHAR2 | 1 |  | N |

## `H_EMP_TASK_D2`

- **Tipo:** Historical
- **Categoria:** Employee
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `REM_LINE_NUM` | Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 3 | `REM_TEXT` | Remessorial Text | VARCHAR2 | 45 |  | N |

## `H_EMP_TASK_H`

- **Tipo:** Historical
- **Categoria:** Employee
- **Campos:** 105
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | Y |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 7 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 8 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `EMP_TASK_CREATE_DATE` | Emp_Task_Createessorial Date | DATE | 7 |  | N |
| 12 | `EMP_TASK_START_DATE` | Emp_Task_Startessorial Date | DATE | 7 |  | Y |
| 13 | `EMP_TASK_END_DATE` | Emp_Task_Endessorial Date | DATE | 7 |  | Y |
| 14 | `EMP_TASK_TOT_TIME` | Emp_Task_Totessorial Time | NUMBER | 22 | 6 | Y |
| 15 | `EMP_TASK_TRANS_LEV_FLAG` | Emp_Task_Trans_Levessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `EMP_TASK_TRANS_TP_FLAG` | Emp_Task_Trans_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `EMP_TASK_PARENT_PROG` | Emp_Task_Parentessorial Prog | VARCHAR2 | 14 |  | N |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 19 | `EMP_TASK_MARK_FOR_DEL_FLAG` | Emp_Task_Mark_For_Delessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `EMP_TASK_OK_FLAG` | Emp_Task_Okessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `JOB_LINE_NUM` | Job_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 22 | `JOB_LOC_LINE_NUM` | Job_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 23 | `WHSE_CODE_CRNT` | Whse_Codeessorial Crnt | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_CRNT` | Loc_Codeessorial Crnt | VARCHAR2 | 12 |  | Y |
| 25 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 26 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 27 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | Y |
| 28 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | Y |
| 29 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 30 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 31 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 32 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 33 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 34 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 35 | `SKU_CODE1` | Skuessorial Code1 | VARCHAR2 | 4 |  | Y |
| 36 | `INVT_QTY_BKD_NUM1` | Invt_Qty_Bkdessorial Num1 | NUMBER | 22 | 9 | Y |
| 37 | `EMP_TASK_QTY1` | Emp_Taskessorial Qty1 | NUMBER | 22 | 9 | Y |
| 38 | `SKU_CODE2` | Skuessorial Code2 | VARCHAR2 | 4 |  | Y |
| 39 | `INVT_QTY_BKD_NUM2` | Invt_Qty_Bkdessorial Num2 | NUMBER | 22 | 9 | Y |
| 40 | `EMP_TASK_QTY2` | Emp_Taskessorial Qty2 | NUMBER | 22 | 9 | Y |
| 41 | `SKU_CODE3` | Skuessorial Code3 | VARCHAR2 | 4 |  | Y |
| 42 | `INVT_QTY_BKD_NUM3` | Invt_Qty_Bkdessorial Num3 | NUMBER | 22 | 9 | Y |
| 43 | `EMP_TASK_QTY3` | Emp_Taskessorial Qty3 | NUMBER | 22 | 9 | Y |
| 44 | `SKU_CODE4` | Skuessorial Code4 | VARCHAR2 | 4 |  | Y |
| 45 | `INVT_QTY_BKD_NUM4` | Invt_Qty_Bkdessorial Num4 | NUMBER | 22 | 9 | Y |
| 46 | `EMP_TASK_QTY4` | Emp_Taskessorial Qty4 | NUMBER | 22 | 9 | Y |
| 47 | `SKU_CODE5` | Skuessorial Code5 | VARCHAR2 | 4 |  | Y |
| 48 | `INVT_QTY_BKD_NUM5` | Invt_Qty_Bkdessorial Num5 | NUMBER | 22 | 9 | Y |
| 49 | `EMP_TASK_QTY5` | Emp_Taskessorial Qty5 | NUMBER | 22 | 9 | Y |
| 50 | `EMP_TASK_TOT_WGT` | Emp_Task_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 51 | `EMP_TASK_TOT_WGT_NET` | Emp_Task_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 52 | `EMP_TASK_TOT_CUBE` | Emp_Task_Totessorial Cube | NUMBER | 22 | 16 | Y |
| 53 | `EMP_TASK_REM_FLAG` | Emp_Task_Remessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `EMP_TASK_PAY` | Emp_Taskessorial Pay | NUMBER | 22 | 6 | Y |
| 55 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | Y |
| 56 | `EMP_HOUR_PAY` | Emp_Houressorial Pay | NUMBER | 22 | 8 | Y |
| 57 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | Y |
| 58 | `MHE_CODE_TASK_COST` | Mhe_Code_Taskessorial Cost | NUMBER | 22 | 6 | Y |
| 59 | `EMP_TASK_LINK_SEQ_NUM` | Emp_Task_Link_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 60 | `EMP_TASK_DLINE_DATE` | Emp_Task_Dlineessorial Date | DATE | 7 |  | Y |
| 61 | `EMP_TASK_EST_START_DATE` | Emp_Task_Est_Startessorial Date | DATE | 7 |  | Y |
| 62 | `EMP_TASK_EST_START_MAN_FLAG` | Emp_Task_Est_Start_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 63 | `EMP_TASK_EST_START_OVRR_FLAG` | Emp_Task_Est_Start_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 64 | `EMP_TASK_EST_END_DATE` | Emp_Task_Est_Endessorial Date | DATE | 7 |  | Y |
| 65 | `EMP_TASK_EST_END_MAN_FLAG` | Emp_Task_Est_End_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 66 | `EMP_TASK_EST_END_OVRR_FLAG` | Emp_Task_Est_End_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 67 | `EMP_TASK_EST_TIME_HIST` | Emp_Task_Est_Timeessorial Hist | NUMBER | 22 | 6 | Y |
| 68 | `EMP_TASK_EST_TIME` | Emp_Task_Estessorial Time | NUMBER | 22 | 6 | Y |
| 69 | `EMP_TASK_EST_TIME_MAN` | Emp_Task_Est_Timeessorial Man | NUMBER | 22 | 6 | Y |
| 70 | `EMP_TASK_PCENT_COMPL` | Emp_Task_Pcentessorial Compl | NUMBER | 22 | 4 | Y |
| 71 | `EMP_TASK_PCENT_MAN_FLAG` | Emp_Task_Pcent_Manessorial Flag | VARCHAR2 | 1 |  | Y |
| 72 | `EMP_TASK_PCENT_OVRR_FLAG` | Emp_Task_Pcent_Ovrressorial Flag | VARCHAR2 | 1 |  | Y |
| 73 | `EMP_TASK_PRTY_NUM` | Emp_Task_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 74 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 75 | `EMP_TASK_HOLD_FLAG` | Emp_Task_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `EMP_TASK_QTY` | Emp_Taskessorial Qty | NUMBER | 22 | 9 | Y |
| 77 | `WHSE_CODE_FLT` | Whse_Codeessorial Flt | VARCHAR2 | 4 |  | Y |
| 78 | `LOC_CODE_FLT` | Loc_Codeessorial Flt | VARCHAR2 | 12 |  | Y |
| 79 | `EMP_TASK_EMPTY_TOTE_FLAG` | Emp_Task_Empty_Toteessorial Flag | VARCHAR2 | 1 |  | Y |
| 80 | `EMP_TASK_TOTE_DUMMY_FLAG` | Emp_Task_Tote_Dummyessorial Flag | VARCHAR2 | 1 |  | Y |
| 81 | `EMP_TASK_EST_TIME_WAVE` | Emp_Task_Est_Timeessorial Wave | NUMBER | 22 | 6 | Y |
| 82 | `CONV_ID` | Convessorial Id | VARCHAR2 | 12 |  | Y |
| 83 | `ITEM_SET_CODE` | Item_Setessorial Code | VARCHAR2 | 20 |  | Y |
| 84 | `EMP_TASK_ITEM_SET_QTY` | Emp_Task_Item_Setessorial Qty | NUMBER | 22 | 9 | Y |
| 85 | `FLOW_PROS_PRTY_NUM` | Flow_Pros_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 86 | `ZONE_LAB_STD_MODY_NUM` | Zarehouse Lab Std Mody Num | NUMBER | 22 | 4 | Y |
| 87 | `ITEM_LAB_STD_MODY_NUM` | Item_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 88 | `MHE_TP_LAB_STD_MODY_NUM` | Mhe_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 89 | `LOC_LAB_STD_MODY_NUM` | Loc_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 90 | `LOC_TP_LAB_STD_MODY_NUM` | Loc_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 91 | `EMP_TASK_LINE_TP` | Emp_Task_Lineessorial Tp | VARCHAR2 | 1 |  | Y |
| 92 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 93 | `JOB_SEQ_NUM` | Job_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 94 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 95 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 96 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 97 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 98 | `UNIT_RETAIL_PRICE` | Unit_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 99 | `UNIT_DISC_PRICE` | Unit_Discessorial Price | NUMBER | 22 | 12 | Y |
| 100 | `UNIT_COST` | Unitessorial Cost | NUMBER | 22 | 12 | Y |
| 101 | `ACC_CODE` | Accessorial Code | VARCHAR2 | 10 |  | Y |
| 102 | `ACC_TP_CODE` | Acc_Tpessorial Code | VARCHAR2 | 1 |  | Y |
| 103 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | Y |
| 104 | `ITEM_CODE_MAST` | Item_Codeessorial Mast | VARCHAR2 | 20 |  | Y |
| 105 | `EMP_TASK_OVPI_FLAG` | Emp_Task_Ovpiessorial Flag | VARCHAR2 | 1 |  | Y |

