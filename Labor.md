# Tabelas — Labor

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **9**.

## `C_DSHB_DOC_FLOW`

- **Tipo:** Transactional
- **Categoria:** Labor
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | N |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 4 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_CODE` | Flow_Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 6 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 8 | `LAB_STD_UOM_CRNT` | Lab_Std_Uomessorial Crnt | VARCHAR2 | 4 |  | Y |
| 9 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 11 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 12 | `LAB_STD_CLASS1_NUM` | Lab_Std_Class1essorial Num | NUMBER | 22 | 10 | Y |
| 13 | `LAB_STD_CLASS2_NUM` | Lab_Std_Class2essorial Num | NUMBER | 22 | 10 | Y |
| 14 | `LAB_STD_CLASS3_NUM` | Lab_Std_Class3essorial Num | NUMBER | 22 | 10 | Y |
| 15 | `LAB_STD_CLASS4_NUM` | Lab_Std_Class4essorial Num | NUMBER | 22 | 10 | Y |
| 16 | `LAB_STD_CLASS5_NUM` | Lab_Std_Class5essorial Num | NUMBER | 22 | 10 | Y |
| 17 | `FLOW_PROS_PCENT_COMPL_NUM` | Flow_Pros_Pcent_Complessorial Num | NUMBER | 22 | 4 | Y |
| 18 | `FLOW_PROS_PCENT_COMPL_DATE` | Flow_Pros_Pcent_Complessorial Date | DATE | 7 |  | Y |
| 19 | `ALERT_TIME` | Alertessorial Time | VARCHAR2 | 6 |  | Y |

## `C_LAB`

- **Tipo:** Transactional
- **Categoria:** Labor
- **Campos:** 67
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `LAB_DATE` | Labessorial Date | DATE | 7 |  | N |
| 7 | `LAB_TP_FLAG` | Lab_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 9 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 10 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 11 | `LAB_START_DATE` | Lab_Startessorial Date | DATE | 7 |  | Y |
| 12 | `LAB_END_DATE` | Lab_Endessorial Date | DATE | 7 |  | Y |
| 13 | `LAB_SYS_FLAG` | Lab_Sysessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `LAB_DES` | Labessorial Des | VARCHAR2 | 40 |  | Y |
| 15 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 16 | `LAB_UNIT` | Labessorial Unit | NUMBER | 22 | 9 | Y |
| 17 | `SESSION_ID` | Sessionessorial Id | VARCHAR2 | 16 |  | Y |
| 18 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 19 | `LAB_UNIQUE_SEQ_NUM` | Lab_Unique_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 20 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 21 | `DOC_LINE_PICK_METH` | Doc_Line_Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 22 | `LAB_GOAL_TIME` | Lab_Goalessorial Time | NUMBER | 22 | 16 | Y |
| 23 | `LAB_DIRECT_TIME` | Lab_Directessorial Time | NUMBER | 22 | 16 | Y |
| 24 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 26 | `EMP_HOURLY_PAY` | Emp_Hourlyessorial Pay | NUMBER | 22 | 8 | Y |
| 27 | `LAB_INDIRECT_TIME` | Lab_Indirectessorial Time | NUMBER | 22 | 16 | Y |
| 28 | `LAB_IDLE_TIME` | Lab_Idleessorial Time | NUMBER | 22 | 16 | Y |
| 29 | `LAB_ACTUAL_TIME` | Lab_Actualessorial Time | NUMBER | 22 | 16 | Y |
| 30 | `LAB_CUST_TIME` | Lab_Custessorial Time | NUMBER | 22 | 16 | Y |
| 31 | `LAB_ADJACENT_CUST_TIME` | Lab_Adjacent_Custessorial Time | NUMBER | 22 | 16 | Y |
| 32 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 33 | `LAB_ACT_NOT_PROS_FLAG` | Lab_Act_Not_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 35 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 36 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 37 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 38 | `LAB_WGT` | Labessorial Wgt | NUMBER | 22 | 16 | Y |
| 39 | `LAB_WGT_NET` | Lab_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 40 | `LAB_CUBE` | Labessorial Cube | NUMBER | 22 | 12 | Y |
| 41 | `LAB_LOC_FROM_ENTER_DATE` | Lab_Loc_From_Enteressorial Date | DATE | 7 |  | Y |
| 42 | `LAB_UI_ENTER_DATE` | Lab_Ui_Enteressorial Date | DATE | 7 |  | Y |
| 43 | `LAB_QTY_ENTER_DATE` | Lab_Qty_Enteressorial Date | DATE | 7 |  | Y |
| 44 | `LAB_PICK_SHORT_QTY` | Lab_Pick_Shortessorial Qty | NUMBER | 22 | 9 | Y |
| 45 | `LAB_PICK_AVAIL_QTY_LOC_FROM` | Lab_Pick_Avail_Qty_Locessorial From | NUMBER | 22 | 9 | Y |
| 46 | `LAB_ENTITY_CNT_LOC_FROM` | Lab_Entity_Cnt_Locessorial From | NUMBER | 22 | 9 | Y |
| 47 | `LAB_ENTITY_CNT_LOC_TO` | Lab_Entity_Cnt_Locessorial To | NUMBER | 22 | 9 | Y |
| 48 | `LAB_PICK_RESIDUAL_QTY` | Lab_Pick_Residualessorial Qty | NUMBER | 22 | 9 | Y |
| 49 | `LAB_PICK_QTY_HANDL_MANUAL` | Lab_Pick_Qty_Handlessorial Manual | NUMBER | 22 | 9 | Y |
| 50 | `MHE_MOVE_GRP_SEQ_NUM` | Mhe_Move_Grp_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 51 | `LAB_EXT_SWARE_ASS_ID` | Lab_Ext_Sware_Assessorial Id | VARCHAR2 | 100 |  | Y |
| 52 | `LAB_EXT_SWARE_GOAL_TIME` | Lab_Ext_Sware_Goalessorial Time | NUMBER | 22 | 9 | Y |
| 53 | `LAB_AUDIT_NUM` | Lab_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 54 | `LAB_AUDIT_DATE` | Lab_Auditessorial Date | DATE | 7 |  | Y |
| 55 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 56 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 57 | `LAB_DOC_FIRST_LAST_FLAG` | Lab_Doc_First_Lastessorial Flag | VARCHAR2 | 1 |  | Y |
| 58 | `LAB_DOC_LOC_TP_FIRST_LAST_FLAG` | Lab_Doc_Loc_Tp_First_Lastessorial Flag | VARCHAR2 | 1 |  | Y |
| 59 | `WHSE_CODE_TO_MHE_LEG` | Warehouse Code To Mhe Leg | VARCHAR2 | 4 |  | Y |
| 60 | `LOC_CODE_TO_MHE_LEG` | Loc_Code_To_Mheessorial Leg | VARCHAR2 | 12 |  | Y |
| 61 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 62 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 63 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 64 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 65 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 66 | `RF_DEVICE_CODE` | Rf_Deviceessorial Code | VARCHAR2 | 4 |  | Y |
| 67 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |

## `C_LAB_TIME`

- **Tipo:** Transactional
- **Categoria:** Labor
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

## `C_LAB_TIME_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Labor
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LAB_TIME_SEQ_NUM` | Lab_Time_Seqessorial Num | NUMBER | 22 | 9 | N |

## `H_C_LAB`

- **Tipo:** Historical
- **Categoria:** Labor
- **Campos:** 66
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `LAB_DATE` | Labessorial Date | DATE | 7 |  | N |
| 7 | `LAB_TP_FLAG` | Lab_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 9 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 10 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 11 | `LAB_START_DATE` | Lab_Startessorial Date | DATE | 7 |  | Y |
| 12 | `LAB_END_DATE` | Lab_Endessorial Date | DATE | 7 |  | Y |
| 13 | `LAB_SYS_FLAG` | Lab_Sysessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `LAB_DES` | Labessorial Des | VARCHAR2 | 40 |  | Y |
| 15 | `LAB_SEQ_NUM` | Lab_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 16 | `LAB_UNIT` | Labessorial Unit | NUMBER | 22 | 9 | Y |
| 17 | `SESSION_ID` | Sessionessorial Id | VARCHAR2 | 16 |  | Y |
| 18 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 19 | `LAB_UNIQUE_SEQ_NUM` | Lab_Unique_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 20 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 21 | `DOC_LINE_PICK_METH` | Doc_Line_Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 22 | `LAB_GOAL_TIME` | Lab_Goalessorial Time | NUMBER | 22 | 16 | Y |
| 23 | `LAB_DIRECT_TIME` | Lab_Directessorial Time | NUMBER | 22 | 16 | Y |
| 24 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 26 | `EMP_HOURLY_PAY` | Emp_Hourlyessorial Pay | NUMBER | 22 | 8 | Y |
| 27 | `LAB_INDIRECT_TIME` | Lab_Indirectessorial Time | NUMBER | 22 | 16 | Y |
| 28 | `LAB_IDLE_TIME` | Lab_Idleessorial Time | NUMBER | 22 | 16 | Y |
| 29 | `LAB_ACTUAL_TIME` | Lab_Actualessorial Time | NUMBER | 22 | 16 | Y |
| 30 | `LAB_CUST_TIME` | Lab_Custessorial Time | NUMBER | 22 | 16 | Y |
| 31 | `LAB_ADJACENT_CUST_TIME` | Lab_Adjacent_Custessorial Time | NUMBER | 22 | 16 | Y |
| 32 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 33 | `LAB_ACT_NOT_PROS_FLAG` | Lab_Act_Not_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 35 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 36 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 37 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 38 | `LAB_WGT` | Labessorial Wgt | NUMBER | 22 | 16 | Y |
| 39 | `LAB_WGT_NET` | Lab_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 40 | `LAB_CUBE` | Labessorial Cube | NUMBER | 22 | 12 | Y |
| 41 | `LAB_LOC_FROM_ENTER_DATE` | Lab_Loc_From_Enteressorial Date | DATE | 7 |  | Y |
| 42 | `LAB_UI_ENTER_DATE` | Lab_Ui_Enteressorial Date | DATE | 7 |  | Y |
| 43 | `LAB_QTY_ENTER_DATE` | Lab_Qty_Enteressorial Date | DATE | 7 |  | Y |
| 44 | `LAB_PICK_SHORT_QTY` | Lab_Pick_Shortessorial Qty | NUMBER | 22 | 9 | Y |
| 45 | `LAB_PICK_AVAIL_QTY_LOC_FROM` | Lab_Pick_Avail_Qty_Locessorial From | NUMBER | 22 | 9 | Y |
| 46 | `LAB_ENTITY_CNT_LOC_FROM` | Lab_Entity_Cnt_Locessorial From | NUMBER | 22 | 9 | Y |
| 47 | `LAB_ENTITY_CNT_LOC_TO` | Lab_Entity_Cnt_Locessorial To | NUMBER | 22 | 9 | Y |
| 48 | `LAB_PICK_RESIDUAL_QTY` | Lab_Pick_Residualessorial Qty | NUMBER | 22 | 9 | Y |
| 49 | `LAB_PICK_QTY_HANDL_MANUAL` | Lab_Pick_Qty_Handlessorial Manual | NUMBER | 22 | 9 | Y |
| 50 | `MHE_MOVE_GRP_SEQ_NUM` | Mhe_Move_Grp_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 51 | `LAB_EXT_SWARE_ASS_ID` | Lab_Ext_Sware_Assessorial Id | VARCHAR2 | 100 |  | Y |
| 52 | `LAB_EXT_SWARE_GOAL_TIME` | Lab_Ext_Sware_Goalessorial Time | NUMBER | 22 | 9 | Y |
| 53 | `LAB_AUDIT_NUM` | Lab_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 54 | `LAB_AUDIT_DATE` | Lab_Auditessorial Date | DATE | 7 |  | Y |
| 55 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 56 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 57 | `LAB_DOC_FIRST_LAST_FLAG` | Lab_Doc_First_Lastessorial Flag | VARCHAR2 | 1 |  | Y |
| 58 | `LAB_DOC_LOC_TP_FIRST_LAST_FLAG` | Lab_Doc_Loc_Tp_First_Lastessorial Flag | VARCHAR2 | 1 |  | Y |
| 59 | `WHSE_CODE_TO_MHE_LEG` | Warehouse Code To Mhe Leg | VARCHAR2 | 4 |  | Y |
| 60 | `LOC_CODE_TO_MHE_LEG` | Loc_Code_To_Mheessorial Leg | VARCHAR2 | 12 |  | Y |
| 61 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 62 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 63 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 64 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 65 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 66 | `RF_DEVICE_CODE` | Rf_Deviceessorial Code | VARCHAR2 | 4 |  | Y |

## `H_C_LAB_TIME`

- **Tipo:** Historical
- **Categoria:** Labor
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

## `M_LAB_STD_MODY_PROF`

- **Tipo:** Master
- **Categoria:** Labor
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LAB_STD_MODY_PROF_DES` | Lab_Std_Mody_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LAB_STD_MODY_PROF_STAT` | Lab_Std_Mody_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LAB_STD_MODY_ITEM_FLAG` | Lab_Std_Mody_Itemessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `LAB_STD_MODY_WHSE_FLAG` | Lab_Std_Mody_Whseessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LAB_STD_MODY_CUST_FLAG` | Lab_Std_Mody_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `LAB_STD_MODY_SHIP_CON_FLAG` | Lab_Std_Mody_Ship_Conessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `LAB_STD_MODY_OP_FLAG` | Lab_Std_Mody_Opessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `LAB_STD_MODY_LOC_FLAG` | Lab_Std_Mody_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `LAB_STD_MODY_LOC_TP_FLAG` | Lab_Std_Mody_Loc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `LAB_STD_MODY_CARR_FLAG` | Lab_Std_Mody_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `LAB_STD_MODY_LOAD_FLAG` | Lab_Std_Mody_Loadessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `LAB_STD_MODY_MHE_TP_FLAG` | Lab_Std_Mody_Mhe_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `LAB_STD_MODY_ZONE_FLAG` | Lab_Std_Mody_Zoneessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `LAB_STD_MODY_DATE` | Lab_Std_Modyessorial Date | DATE | 7 |  | Y |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LAB_STD_NUM_PROF_D`

- **Tipo:** Master
- **Categoria:** Labor
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | N |
| 5 | `LAB_STD_CLASS1_NUM` | Lab_Std_Class1essorial Num | NUMBER | 22 | 10 | Y |
| 6 | `LAB_STD_CLASS2_NUM` | Lab_Std_Class2essorial Num | NUMBER | 22 | 10 | Y |
| 7 | `LAB_STD_CLASS3_NUM` | Lab_Std_Class3essorial Num | NUMBER | 22 | 10 | Y |
| 8 | `LAB_STD_CLASS4_NUM` | Lab_Std_Class4essorial Num | NUMBER | 22 | 10 | Y |
| 9 | `LAB_STD_CLASS5_NUM` | Lab_Std_Class5essorial Num | NUMBER | 22 | 10 | Y |
| 10 | `LAB_STD_STAT` | Lab_Stdessorial Stat | VARCHAR2 | 1 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LAB_STD_NUM_PROF_H`

- **Tipo:** Master
- **Categoria:** Labor
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LAB_STD_NUM_PROF_DES` | Lab_Std_Num_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LAB_STD_NUM_PROF_STAT` | Lab_Std_Num_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 7 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

