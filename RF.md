# Tabelas — RF

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **13**.

## `M_BARCODE_PROF`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BARCODE_PROF_CODE` | Barcode_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `BARCODE_PROF_DES` | Barcode_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SCAN_PROF_CODE` | Scan_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `BARCODE_LEN` | Barcodeessorial Len | NUMBER | 22 | 3 | Y |
| 7 | `BARCODE_START_POS` | Barcode_Startessorial Pos | NUMBER | 22 | 3 | Y |
| 8 | `BARCODE_END_POS` | Barcode_Endessorial Pos | NUMBER | 22 | 3 | Y |
| 9 | `BARCODE_ID` | Barcodeessorial Id | VARCHAR2 | 40 |  | Y |
| 10 | `BARCODE_TP_CODE` | Barcode_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `BARCODE_VAR_LEN_FLAG` | Barcode_Var_Lenessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `BARCODE_FIX_LEN_SIZE` | Barcode_Fix_Lenessorial Size | NUMBER | 22 | 3 | Y |
| 13 | `BARCODE_VAR_LEN_SEP` | Barcode_Var_Lenessorial Sep | NUMBER | 22 | 3 | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BARCODE_PROF_CUST_REST`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `BARCODE_PROF_CODE` | Barcode_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RF_DEVICE`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RF_DEVICE_CODE` | Rf_Deviceessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `RF_DEVICE_DES` | Rf_Deviceessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `RF_DEVICE_STAT` | Rf_Deviceessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `RF_DEVICE_SER_NUM` | Rf_Device_Seressorial Num | VARCHAR2 | 80 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_RF_LAB`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `RF_LAB_TRANS_LEV_FLAG` | Rf_Lab_Trans_Levessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `RF_LAB_STAT` | Rf_Labessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `FLOW_PROS_CODE_NEXT` | Flow_Pros_Codeessorial Next | VARCHAR2 | 4 |  | Y |

## `M_RF_PARAM`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LBX` | Lbxessorial Lbx | VARCHAR2 | 3 |  | Y |
| 2 | `LBY` | Lbyessorial Lby | VARCHAR2 | 3 |  | Y |
| 3 | `LB_NAME` | Lbessorial Name | VARCHAR2 | 20 |  | Y |
| 4 | `LB_FLD` | Lbessorial Fld | VARCHAR2 | 20 |  | Y |
| 5 | `FLDX` | Fldxessorial Fldx | VARCHAR2 | 3 |  | Y |
| 6 | `FLDY` | Fldyessorial Fldy | VARCHAR2 | 3 |  | Y |
| 7 | `FLD_SEQ` | Fldessorial Seq | VARCHAR2 | 2 |  | Y |
| 8 | `PRG_NAME` | Prgessorial Name | VARCHAR2 | 20 |  | Y |
| 9 | `PRG_DES` | Prgessorial Des | VARCHAR2 | 15 |  | Y |
| 10 | `PRG_TP` | Prgessorial Tp | VARCHAR2 | 1 |  | Y |

## `M_RF_PARAM_H`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LBX` | Lbxessorial Lbx | NUMBER | 22 | 3 | Y |
| 2 | `LBY` | Lbyessorial Lby | NUMBER | 22 | 3 | Y |
| 3 | `LB_NAME` | Lbessorial Name | VARCHAR2 | 20 |  | Y |
| 4 | `LB_FLD` | Lbessorial Fld | VARCHAR2 | 20 |  | Y |
| 5 | `FLDX` | Fldxessorial Fldx | NUMBER | 22 | 3 | Y |
| 6 | `FLDY` | Fldyessorial Fldy | NUMBER | 22 | 3 | Y |
| 7 | `FLD_SEQ` | Fldessorial Seq | NUMBER | 22 | 2 | Y |
| 8 | `PRG_NAME` | Prgessorial Name | VARCHAR2 | 20 |  | Y |

## `M_RF_PROF`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 185
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RF_PROF_CODE` | Rf_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `RF_PROF_DES` | Rf_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `RF_PROF_STAT` | Rf_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `RF_PROF_CALC_VARI_TP` | Rf_Prof_Calc_Variessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `RF_PROF_ALLOW_LOAD_PICK_FLAG` | Rf_Prof_Allow_Load_Pickessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `RF_PROF_VAL_LEV_NUM` | Rf_Prof_Val_Levessorial Num | NUMBER | 22 | 1 | Y |
| 9 | `RF_PROF_DOC_CODE_PRT` | Rf_Prof_Doc_Codeessorial Prt | VARCHAR2 | 4 |  | Y |
| 10 | `RF_PROF_DEF_QTY_FLAG` | Rf_Prof_Def_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `RF_PROF_VAL_PICK_RELO_FLAG` | Rf_Prof_Val_Pick_Reloessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `RF_PROF_VAL_PICK_PUT_FLAG` | Rf_Prof_Val_Pick_Putessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `RF_PROF_QU_RESULT_FLAG` | Rf_Prof_Qu_Resultessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `RF_PROF_RCPT_FLAG` | Rf_Prof_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `RF_PROF_RCPT_LINE_FLAG` | Rf_Prof_Rcpt_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `RF_PROF_CUST_FLAG` | Rf_Prof_Custessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `RF_PROF_INVT_LEV1_FLAG` | Rf_Prof_Invt_Lev1essorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `RF_PROF_INVT_LEV2_FLAG` | Rf_Prof_Invt_Lev2essorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `RF_PROF_INVT_LEV3_FLAG` | Rf_Prof_Invt_Lev3essorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `RF_PROF_INVT_LEV4_FLAG` | Rf_Prof_Invt_Lev4essorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `RF_PROF_WHSE_FLAG` | Rf_Prof_Whseessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `RF_PROF_QTY_FLAG` | Rf_Prof_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `RF_PROF_HOLD_FLAG` | Rf_Prof_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `RF_PROF_DISP_ORD_LINE_FLAG` | Rf_Prof_Disp_Ord_Lineessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `RF_PROF_REPL_VAL_LOW_LEV_FLAG` | Rf_Prof_Repl_Val_Low_Levessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `RF_PROF_REPL_VAL_LOC_TO_FLAG` | Rf_Prof_Repl_Val_Loc_Toessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `RF_PROF_OUTB_PICK_MODE_TP` | Rf_Prof_Outb_Pick_Modeessorial Tp | VARCHAR2 | 1 |  | Y |
| 28 | `RF_PROF_INVT_CNT_ACTIVE_TP` | Rf_Prof_Invt_Cnt_Activeessorial Tp | VARCHAR2 | 4 |  | Y |
| 29 | `RF_PROF_INVT_CNT_VAL_TP` | Rf_Prof_Invt_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | Y |
| 30 | `RF_PROF_ALLOW_DUP_INVT` | Rf_Prof_Allow_Dupessorial Invt | VARCHAR2 | 1 |  | Y |
| 31 | `RF_PROF_PICK_ALLW_DUP_TAG_CODE` | Rf_Prof_Pick_Allw_Dup_Tagessorial Code | VARCHAR2 | 1 |  | Y |
| 32 | `RF_PROF_OM_VAL_QTY_FLAG` | Rf_Prof_Om_Val_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `RF_PROF_OM_VAL_LOC_FROM_FLAG` | Rf_Prof_Om_Val_Loc_Fromessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `RF_PROF_OM_LOC_TO_OPT_TP_CODE` | Rf_Prof_Om_Loc_To_Opt_Tpessorial Code | VARCHAR2 | 1 |  | Y |
| 35 | `RF_PROF_PUT_ALLOW_STAG_FLAG` | Rf_Prof_Put_Allow_Stagessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `RF_PROF_VALID_SER_PROS` | Rf_Prof_Valid_Seressorial Pros | VARCHAR2 | 1 |  | Y |
| 37 | `RF_PROF_DISP_CARR_PALL_FLAG` | Rf_Prof_Disp_Carr_Pallessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `RF_PROF_DISP_TRAILER_QUEST` | Rf_Prof_Disp_Traileressorial Quest | VARCHAR2 | 1 |  | Y |
| 39 | `RF_PROF_STAG_DEF_LOC_CODE` | Rf_Prof_Stag_Def_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 40 | `RF_PROF_STAG_DEF_WHSE_LOC_CODE` | Rf_Prof_Stag_Def_Whse_Locessorial Code | VARCHAR2 | 20 |  | Y |
| 41 | `RF_PROF_ALLOW_PART_PICK_NM` | Rf_Prof_Allow_Part_Pickessorial Nm | VARCHAR2 | 1 |  | Y |
| 42 | `RF_PROF_ASSIGN_OPID_FULL_PLT` | Rf_Prof_Assign_Opid_Fullessorial Plt | VARCHAR2 | 1 |  | Y |
| 43 | `RF_PROF_LAB_DOC_CODE` | Rf_Prof_Lab_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 44 | `RF_PROF_QRS_LAB_DOC_CODE` | Rf_Prof_Qrs_Lab_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 45 | `RF_PROF_AUTO_ASSIGN_OPID` | Rf_Prof_Auto_Assignessorial Opid | VARCHAR2 | 1 |  | Y |
| 46 | `RF_PROF_CHECK_MATCH_QTY` | Rf_Prof_Check_Matchessorial Qty | VARCHAR2 | 1 |  | Y |
| 47 | `RF_PROF_ALLOW_NEW_LINE_RFCH` | Rf_Prof_Allow_New_Lineessorial Rfch | VARCHAR2 | 1 |  | Y |
| 48 | `RF_PROF_CHK_LABEL_DAYS_RFPIC` | Rf_Prof_Chk_Label_Daysessorial Rfpic | NUMBER | 22 | 3 | Y |
| 49 | `RF_PROF_ALLOW_SUSP_HOLD_RFPIC` | Rf_Prof_Allow_Susp_Holdessorial Rfpic | VARCHAR2 | 1 |  | Y |
| 50 | `RF_PROF_DISALLOW_PROS_RFPIC` | Rf_Prof_Disallow_Prosessorial Rfpic | VARCHAR2 | 1 |  | Y |
| 51 | `RF_PROF_ALLOW_VAR_RFCH` | Rf_Prof_Allow_Varessorial Rfch | VARCHAR2 | 1 |  | Y |
| 52 | `RF_PROF_REQ_SUPER_OVRR_RFPU_CH` | Rf_Prof_Req_Super_Ovrr_Rfpuessorial Ch | VARCHAR2 | 1 |  | Y |
| 53 | `RF_PROF_ALLOW_OVERPICK_FLAG` | Rf_Prof_Allow_Overpickessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `RF_PROF_ACT_DIRECT_MOVE_RFRL` | Rf_Prof_Act_Direct_Moveessorial Rfrl | VARCHAR2 | 1 |  | Y |
| 55 | `RF_PROF_THL_RECV_QTY_RFCH` | Rf_Prof_Thl_Recv_Qtyessorial Rfch | VARCHAR2 | 1 |  | Y |
| 56 | `RF_PROF_RELO_PICKLIST_FLAG` | Rf_Prof_Relo_Picklistessorial Flag | VARCHAR2 | 1 |  | Y |
| 57 | `RF_PROF_PICKLINE_PICK_ANY_LOC` | Rf_Prof_Pickline_Pick_Anyessorial Loc | VARCHAR2 | 1 |  | Y |
| 58 | `RF_PROF_ALLOW_REPI_PICK_MODE` | Rf_Prof_Allow_Repi_Pickessorial Mode | VARCHAR2 | 1 |  | Y |
| 59 | `RF_PROF_DISP_RELO_QTY_FLAG` | Rf_Prof_Disp_Relo_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 60 | `RF_PROF_RFPIC_SORT_SEQ_CODE` | Rf_Prof_Rfpic_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `RF_PROF_RFPIC_SORT_SEQ_FLAG` | Rf_Prof_Rfpic_Sort_Seqessorial Flag | VARCHAR2 | 1 |  | Y |
| 62 | `RF_PROF_ALLOW_VAR_RFPU` | Rf_Prof_Allow_Varessorial Rfpu | VARCHAR2 | 1 |  | Y |
| 63 | `RF_PROF_VAL_RULES_SYS_ASS_LOC` | Rf_Prof_Val_Rules_Sys_Assessorial Loc | VARCHAR2 | 1 |  | Y |
| 64 | `RF_PROF_COPI_PICK_DISP_ORD` | Rf_Prof_Copi_Pick_Dispessorial Ord | VARCHAR2 | 1 |  | Y |
| 65 | `RF_PROF_PICK_PAL_BLOCK_TP` | Rf_Prof_Pick_Pal_Blockessorial Tp | VARCHAR2 | 1 |  | Y |
| 66 | `RF_PROF_SORT_ITEM_QTY_FLAG` | Rf_Prof_Sort_Item_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 67 | `RF_PROF_SORT_CART_PALL_PROMPT` | Rf_Prof_Sort_Cart_Pallessorial Prompt | VARCHAR2 | 1 |  | Y |
| 68 | `RF_PROF_SORT_WHSE_LOC_CODE` | Rf_Prof_Sort_Whse_Locessorial Code | VARCHAR2 | 20 |  | Y |
| 69 | `RF_PROF_RFPU_EVENT_CYC_PROF` | Rf_Prof_Rfpu_Event_Cycessorial Prof | VARCHAR2 | 4 |  | Y |
| 70 | `RF_PROF_MOVE_EVENT_CYC_PROF` | Rf_Prof_Move_Event_Cycessorial Prof | VARCHAR2 | 4 |  | Y |
| 71 | `RF_PROF_OVRR_RCPT_TLR` | Rf_Prof_Ovrr_Rcptessorial Tlr | VARCHAR2 | 1 |  | Y |
| 72 | `RF_PROF_RFCH_QTY_BKD_FLAG` | Rf_Prof_Rfch_Qty_Bkdessorial Flag | VARCHAR2 | 1 |  | Y |
| 73 | `RF_PROF_RFCH_ITEM_MES_FLAG` | Rf_Prof_Rfch_Item_Mesessorial Flag | VARCHAR2 | 1 |  | Y |
| 74 | `RF_PROF_RFPU_QTY_UPD_REST` | Rf_Prof_Rfpu_Qty_Updessorial Rest | VARCHAR2 | 1 |  | Y |
| 75 | `RF_PROF_RFPIC_PRT_OPID` | Rf_Prof_Rfpic_Prtessorial Opid | VARCHAR2 | 1 |  | Y |
| 76 | `RF_PROF_RFCY_SUPER_COUNT_FLAG` | Rf_Prof_Rfcy_Super_Countessorial Flag | VARCHAR2 | 1 |  | Y |
| 77 | `RF_PROF_REPI_PRT_LABEL_FLAG` | Rf_Prof_Repi_Prt_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 78 | `RF_PROF_REPI_PROF_DOC_CODE` | Rf_Prof_Repi_Prof_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 79 | `RF_PROF_RFPIC_OPID_ENTRY` | Rf_Prof_Rfpic_Opidessorial Entry | VARCHAR2 | 1 |  | Y |
| 80 | `RF_RFPIC_EXTRA_CHG_TP` | Rf_Rfpic_Extra_Chgessorial Tp | VARCHAR2 | 1 |  | Y |
| 81 | `RF_RFPIC_DISP_LOC_UI` | Rf_Rfpic_Disp_Locessorial Ui | VARCHAR2 | 1 |  | Y |
| 82 | `RF_PROF_APPLY_UI_MASK_VAL` | Rf_Prof_Apply_Ui_Maskessorial Val | VARCHAR2 | 4 |  | Y |
| 83 | `RF_PROF_RFPIC_ITEM_HAZMAT_FLAG` | Rf_Prof_Rfpic_Item_Hazmatessorial Flag | VARCHAR2 | 1 |  | Y |
| 84 | `RF_PROF_DSBL_RF_WAVE` | Rf_Prof_Dsbl_Rfessorial Wave | VARCHAR2 | 1 |  | Y |
| 85 | `RF_PROF_PICK_PATH_MODE_CART` | Rf_Prof_Pick_Path_Modeessorial Cart | VARCHAR2 | 1 |  | Y |
| 86 | `RF_PROF_SPC_STAG_WHSE_LOC_CODE` | Rf_Prof_Spc_Stag_Whse_Locessorial Code | VARCHAR2 | 20 |  | Y |
| 87 | `RF_PROF_CART_SORT_SEQ_CODE` | Rf_Prof_Cart_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 88 | `RF_PROF_INVT_ITEM_VAL_FLAG` | Rf_Prof_Invt_Item_Valessorial Flag | VARCHAR2 | 1 |  | Y |
| 89 | `RF_PROF_EXPY_DATE_RFCH` | Rf_Prof_Expy_Dateessorial Rfch | VARCHAR2 | 1 |  | Y |
| 90 | `RF_PROF_RFCH_ALLOW_HOLD_FLAG` | Rf_Prof_Rfch_Allow_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 91 | `RF_PROF_SER_NUM_CAPT_FLAG` | Rf_Prof_Ser_Num_Captessorial Flag | VARCHAR2 | 1 |  | Y |
| 92 | `RF_PROF_RFCH_CHECK_WGT_CUBE` | Rf_Prof_Rfch_Check_Wgtessorial Cube | VARCHAR2 | 1 |  | Y |
| 93 | `RF_PROF_RFMG_ALLOW_OPID_MERGE` | Rf_Prof_Rfmg_Allow_Opidessorial Merge | VARCHAR2 | 1 |  | Y |
| 94 | `RF_PROF_OPID_CUBE_DIM_FLAG` | Rf_Prof_Opid_Cube_Dimessorial Flag | VARCHAR2 | 1 |  | Y |
| 95 | `RF_RFCH_EXTRA_CHG_TP` | Rf_Rfch_Extra_Chgessorial Tp | VARCHAR2 | 1 |  | Y |
| 96 | `RF_PROF_LAST_LABEL_SCAN_DISABL` | Rf_Prof_Last_Label_Scanessorial Disabl | VARCHAR2 | 1 |  | Y |
| 97 | `RF_ADV_RCPT_FLOW_LASTLINE_FLAG` | Rf_Adv_Rcpt_Flow_Lastlineessorial Flag | VARCHAR2 | 1 |  | Y |
| 98 | `RF_PROF_RFPIC_BOOKMARK` | Rf_Prof_Rfpicessorial Bookmark | VARCHAR2 | 1 |  | Y |
| 99 | `RF_PROF_RFCH_CONCAT_LEV` | Rf_Prof_Rfch_Concatessorial Lev | VARCHAR2 | 1 |  | Y |
| 100 | `RF_PROF_RFPU_ALLOW_HOLD_FLAG` | Rf_Prof_Rfpu_Allow_Holdessorial Flag | VARCHAR2 | 1 |  | Y |
| 101 | `RF_PROF_RFRL_REFRESH_FLAG` | Rf_Prof_Rfrl_Refreshessorial Flag | VARCHAR2 | 1 |  | Y |
| 102 | `RF_PROF_RFCO_PICK_METH` | Rf_Prof_Rfco_Pickessorial Meth | VARCHAR2 | 1 |  | Y |
| 103 | `RF_PROF_RFRL_RULES` | Rf_Prof_Rfrlessorial Rules | VARCHAR2 | 1 |  | Y |
| 104 | `RF_PROF_MIXED_PLT` | Rf_Prof_Mixedessorial Plt | VARCHAR2 | 1 |  | Y |
| 105 | `RF_PROF_RFPK_LESS_THAN_PLT` | Rf_Prof_Rfpk_Less_Thanessorial Plt | VARCHAR2 | 1 |  | Y |
| 106 | `RF_PROF_RFPK_REUSABLE_OPID` | Rf_Prof_Rfpk_Reusableessorial Opid | VARCHAR2 | 1 |  | Y |
| 107 | `RF_PROF_RFPK_VAL_INVT_LEV` | Rf_Prof_Rfpk_Val_Invtessorial Lev | VARCHAR2 | 1 |  | Y |
| 108 | `RF_PROF_RFPK_CART_PICK_STYLE` | Rf_Prof_Rfpk_Cart_Pickessorial Style | VARCHAR2 | 1 |  | Y |
| 109 | `RF_PROF_RFPK_BAPT_EXPT_FLAG` | Rf_Prof_Rfpk_Bapt_Exptessorial Flag | VARCHAR2 | 1 |  | Y |
| 110 | `RF_PROF_MAX_RECD_QTY` | Rf_Prof_Max_Recdessorial Qty | NUMBER | 22 | 9 | Y |
| 111 | `RF_PROF_RFCH_SKIP_LOC_FLAG` | Rf_Prof_Rfch_Skip_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 112 | `RF_PROF_RFCO_SUMM` | Rf_Prof_Rfcoessorial Summ | VARCHAR2 | 1 |  | Y |
| 113 | `RF_PROF_RFCO_AUDIT` | Rf_Prof_Rfcoessorial Audit | VARCHAR2 | 1 |  | Y |
| 114 | `RF_PROF_RFCH_ALLOW_CHG_FLAG` | Rf_Prof_Rfch_Allow_Chgessorial Flag | VARCHAR2 | 1 |  | Y |
| 115 | `RF_PROF_RFPIC_CONF_ORD` | Rf_Prof_Rfpic_Confessorial Ord | VARCHAR2 | 1 |  | Y |
| 116 | `RF_PROF_RFOA_AUD_LEV_NUM` | Rf_Prof_Rfoa_Aud_Levessorial Num | NUMBER | 22 | 1 | Y |
| 117 | `RF_PROF_RFCH_SPC_MODE` | Rf_Prof_Rfch_Spcessorial Mode | VARCHAR2 | 1 |  | Y |
| 118 | `RF_PROF_RFOPS_SORT_SEQ_CODE` | Rf_Prof_Rfops_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 119 | `RF_PROF_RFPU_MAX_NUM_NXTKEY` | Rf_Prof_Rfpu_Max_Numessorial Nxtkey | NUMBER | 22 | 2 | Y |
| 120 | `RF_PROF_RFCH_VAL_LEV_SCPR_CODE` | Rf_Prof_Rfch_Val_Lev_Scpressorial Code | VARCHAR2 | 4 |  | Y |
| 121 | `RF_PROF_RFIPS_SORT_SEQ_CODE` | Rf_Prof_Rfips_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 122 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 123 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 124 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 125 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 126 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 127 | `RF_PROF_RFPU_ALLOW_MULTI_PLT` | Rf_Prof_Rfpu_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 128 | `RF_PROF_RFPIC_ENT_PLT_TP` | Rf_Prof_Rfpic_Ent_Pltessorial Tp | VARCHAR2 | 1 |  | Y |
| 129 | `RF_PROF_RFMG_ALLOW_MERGE_LEV` | Rf_Prof_Rfmg_Allow_Mergeessorial Lev | VARCHAR2 | 1 |  | Y |
| 130 | `RF_PROF_INVT_CNT_THRESH_QTY` | Rf_Prof_Invt_Cnt_Threshessorial Qty | NUMBER | 22 | 6 | Y |
| 131 | `RF_PROF_MISC_CNT_PGM` | Rf_Prof_Misc_Cntessorial Pgm | VARCHAR2 | 1 |  | Y |
| 132 | `RF_PROF_MISC_CNT_ACTIVE_TP` | Rf_Prof_Misc_Cnt_Activeessorial Tp | VARCHAR2 | 1 |  | Y |
| 133 | `RF_PROF_MISC_CNT_VAL_TP` | Rf_Prof_Misc_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | Y |
| 134 | `RF_PROF_MISC_CNT_THRESH_QTY` | Rf_Prof_Misc_Cnt_Threshessorial Qty | NUMBER | 22 | 6 | Y |
| 135 | `RF_PROF_INVT_CNT_BASE_TP` | Rf_Prof_Invt_Cnt_Baseessorial Tp | VARCHAR2 | 1 |  | Y |
| 136 | `RF_PROF_RFPIC_CALL_RFRL` | Rf_Prof_Rfpic_Callessorial Rfrl | VARCHAR2 | 1 |  | Y |
| 137 | `RF_PROF_RFPIC_PICK_SKU` | Rf_Prof_Rfpic_Pickessorial Sku | VARCHAR2 | 1 |  | Y |
| 138 | `RF_PROF_RFCH_DOOR_MODE` | Rf_Prof_Rfch_Dooressorial Mode | VARCHAR2 | 1 |  | Y |
| 139 | `RF_PROF_RFPIC_ALLOW_MULTI_PLT` | Rf_Prof_Rfpic_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 140 | `RF_PROF_RFST_DISP_LOC_TO` | Rf_Prof_Rfst_Disp_Locessorial To | VARCHAR2 | 1 |  | Y |
| 141 | `RF_PROF_RFCH_DISP_QTY_BKD` | Rf_Prof_Rfch_Disp_Qtyessorial Bkd | VARCHAR2 | 1 |  | Y |
| 142 | `RF_PROF_AUTO_LOC_TO` | Rf_Prof_Auto_Locessorial To | VARCHAR2 | 1 |  | Y |
| 143 | `RF_PROF_RFPU_MULTI_LINE` | Rf_Prof_Rfpu_Multiessorial Line | VARCHAR2 | 1 |  | Y |
| 144 | `RF_PROF_RFIPS_NOT_ALLOW_DEL` | Rf_Prof_Rfips_Not_Allowessorial Del | VARCHAR2 | 1 |  | Y |
| 145 | `RF_PROF_RFPIC_PND_LOC` | Rf_Prof_Rfpic_Pndessorial Loc | VARCHAR2 | 1 |  | Y |
| 146 | `RF_PROF_RFST_SUG_LOC_RULE` | Rf_Prof_Rfst_Sug_Locessorial Rule | VARCHAR2 | 1 |  | Y |
| 147 | `RF_PROF_RFPU_CHANGE_WHSE` | Rf_Prof_Rfpu_Changeessorial Whse | VARCHAR2 | 1 |  | Y |
| 148 | `RF_PROF_RFPIC_PLIST_DISP_ITEM` | Rf_Prof_Rfpic_Plist_Dispessorial Item | VARCHAR2 | 1 |  | Y |
| 149 | `RF_RFPIC_DISP_QTY_HIGH_UOM` | Rf_Rfpic_Disp_Qty_Highessorial Uom | VARCHAR2 | 1 |  | Y |
| 150 | `RF_RFPIC_VALID_OPID_MSVS_CODE` | Rf_Rfpic_Valid_Opid_Msvsessorial Code | VARCHAR2 | 4 |  | Y |
| 151 | `RF_CASE_STAG_DEF_WHSE_LOC_CODE` | Rf_Case_Stag_Def_Whse_Locessorial Code | VARCHAR2 | 20 |  | Y |
| 152 | `RF_RFAJ_ENT_ADJ_INFO` | Rf_Rfaj_Ent_Adjessorial Info | VARCHAR2 | 1 |  | Y |
| 153 | `RF_PROF_SORT_BY_LEV` | Rf_Prof_Sort_Byessorial Lev | VARCHAR2 | 1 |  | Y |
| 154 | `RF_RFPIC_CAPT_PLT_SPOT` | Rf_Rfpic_Capt_Pltessorial Spot | VARCHAR2 | 1 |  | Y |
| 155 | `RF_PROF_RFRL_ALLOW_MULTI_PLT` | Rf_Prof_Rfrl_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 156 | `RF_PROF_RFRP_ALLOW_MULTI_PLT` | Rf_Prof_Rfrp_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 157 | `RF_PROF_RFCH_ALLOW_MULTI_PLT` | Rf_Prof_Rfch_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 158 | `RF_PROF_MULTI_PLT_MOVE_TP` | Rf_Prof_Multi_Plt_Moveessorial Tp | VARCHAR2 | 1 |  | Y |
| 159 | `RF_RFPIC_SCAN_FROM_LOC` | Rf_Rfpic_Scan_Fromessorial Loc | VARCHAR2 | 1 |  | Y |
| 160 | `RF_RFCH_QTY_BKD_FLAG_P_LINE` | Rf_Rfch_Qty_Bkd_Flag_Pessorial Line | VARCHAR2 | 1 |  | Y |
| 161 | `RF_PROF_EXPY_DATE_RFCH_P_LINE` | Rf_Prof_Expy_Date_Rfch_Pessorial Line | VARCHAR2 | 1 |  | Y |
| 162 | `RF_PROF_CHG_SYS_LOC_REAS_FLAG` | Rf_Prof_Chg_Sys_Loc_Reasessorial Flag | VARCHAR2 | 1 |  | Y |
| 163 | `RF_PROF_RFRL_MAX_NUM_NXTKEY` | Rf_Prof_Rfrl_Max_Numessorial Nxtkey | NUMBER | 22 | 2 | Y |
| 164 | `RF_PROF_RFST_ALLOW_MULTI_PLT` | Rf_Prof_Rfst_Allow_Multiessorial Plt | VARCHAR2 | 1 |  | Y |
| 165 | `RF_PROF_RFCH_IMAGE_OPEN_RCPT` | Rf_Prof_Rfch_Image_Openessorial Rcpt | VARCHAR2 | 1 |  | Y |
| 166 | `RF_PROF_RFCH_IMAGE_HOLD` | Rf_Prof_Rfch_Imageessorial Hold | VARCHAR2 | 1 |  | Y |
| 167 | `RF_PROF_SHOW_QTY_BKD_SCRN` | Rf_Prof_Show_Qty_Bkdessorial Scrn | VARCHAR2 | 1 |  | Y |
| 168 | `RF_PROF_PUTA_PARTL_PLT` | Rf_Prof_Puta_Partlessorial Plt | VARCHAR2 | 1 |  | Y |
| 169 | `RF_RFOPS_IGNORE_SER_NUM_INB` | Rf_Rfops_Ignore_Ser_Numessorial Inb | VARCHAR2 | 1 |  | Y |
| 170 | `RF_RFOPS_ALLOW_REDUCE_STD_WGT` | Rf_Rfops_Allow_Reduce_Stdessorial Wgt | VARCHAR2 | 1 |  | Y |
| 171 | `RF_PROF_RFSC_ENT_WGT_FLAG` | Rf_Prof_Rfsc_Ent_Wgtessorial Flag | VARCHAR2 | 1 |  | Y |
| 172 | `RF_PROF_RFCH_SHORT_QTY_FLAG` | Rf_Prof_Rfch_Short_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 173 | `RF_PROF_RFCH_MIX_PLT_ILOP_FLAG` | Rf_Prof_Rfch_Mix_Plt_Ilopessorial Flag | VARCHAR2 | 1 |  | Y |
| 174 | `RF_PROF_RFCH_SCAN_ALIT_LEV` | Rf_Prof_Rfch_Scan_Alitessorial Lev | VARCHAR2 | 1 |  | Y |
| 175 | `RF_PROF_REPI_PUT_BACK_FLAG` | Rf_Prof_Repi_Put_Backessorial Flag | VARCHAR2 | 1 |  | Y |
| 176 | `RF_PROF_RFCYE_SCAN_UI` | Rf_Prof_Rfcye_Scanessorial Ui | VARCHAR2 | 1 |  | Y |
| 177 | `RF_PROF_RFOA_FLOW_ADV_SUSP` | Rf_Prof_Rfoa_Flow_Advessorial Susp | VARCHAR2 | 1 |  | Y |
| 178 | `RF_PROF_RFMG_RETAIN_OPID_TO` | Rf_Prof_Rfmg_Retain_Opidessorial To | VARCHAR2 | 1 |  | Y |
| 179 | `RF_PROF_RFCH_SORT_SEQ_CODE` | Rf_Prof_Rfch_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 180 | `RF_PROF_RFOPS_VAL_MAN_PROS` | Rf_Prof_Rfops_Val_Manessorial Pros | VARCHAR2 | 1 |  | Y |
| 181 | `RF_RFCH_LESS_EQL_ITEM_PLT_QTY` | Rf_Rfch_Less_Eql_Item_Pltessorial Qty | VARCHAR2 | 1 |  | Y |
| 182 | `RF_RFCH_SKIP_PROS_VAL_FLAG` | Rf_Rfch_Skip_Pros_Valessorial Flag | VARCHAR2 | 1 |  | Y |
| 183 | `RF_RFRP_DISALLOW_REPI_MAX_CPAC` | Rf_Rfrp_Disallow_Repi_Maxessorial Cpac | VARCHAR2 | 1 |  | Y |
| 184 | `RF_RFSC_VALIDATE_SERIAL_FLAG` | Rf_Rfsc_Validate_Serialessorial Flag | VARCHAR2 | 1 |  | Y |
| 185 | `RF_PROF_REPI_DEM_MIN_REC_FLAG` | Rf_Prof_Repi_Dem_Min_Recessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_RF_TER`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `RF_TER_CODE` | Rf_Teressorial Code | VARCHAR2 | 20 |  | N |
| 2 | `RF_TER_DES` | Rf_Teressorial Des | VARCHAR2 | 30 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `RF_TER_STAT` | Rf_Teressorial Stat | VARCHAR2 | 1 |  | N |

## `M_SCAN_PARAM`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SCAN_PARAM_CODE` | Scan_Paramessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SCAN_PARAM_DES` | Scan_Paramessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SCAN_PARAM_STAT` | Scan_Paramessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `SCAN_PARAM_LEN` | Scan_Paramessorial Len | NUMBER | 22 | 3 | N |
| 7 | `SCAN_PARAM_START` | Scan_Paramessorial Start | NUMBER | 22 | 3 | N |
| 8 | `SCAN_PARAM_END` | Scan_Paramessorial End | NUMBER | 22 | 3 | N |
| 9 | `SCAN_PARAM_WGT_MODY` | Scan_Param_Wgtessorial Mody | NUMBER | 22 | 9 | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SCAN_PROF_D`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SCAN_PROF_CODE` | Scan_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SCAN_PROF_INB_OUTB_FLAG` | Scan_Prof_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SCAN_PROF_SEQ_NUM` | Scan_Prof_Seqessorial Num | NUMBER | 22 | 3 | N |
| 6 | `SCAN_PROF_TP_CODE` | Scan_Prof_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `SCAN_PROF_START_POS` | Scan_Prof_Startessorial Pos | NUMBER | 22 | 3 | Y |
| 8 | `SCAN_PROF_END_POS` | Scan_Prof_Endessorial Pos | NUMBER | 22 | 3 | Y |
| 9 | `SCAN_PROF_START_CHAR` | Scan_Prof_Startessorial Char | VARCHAR2 | 1 |  | Y |
| 10 | `SCAN_PROF_END_CHAR` | Scan_Prof_Endessorial Char | VARCHAR2 | 1 |  | Y |
| 11 | `SCAN_PROF_TP_CODE_LEN` | Scan_Prof_Tp_Codeessorial Len | NUMBER | 22 | 3 | Y |
| 12 | `SCAN_PROF_ACTN_CODE` | Scan_Prof_Actnessorial Code | VARCHAR2 | 2 |  | Y |
| 13 | `SCAN_PROF_UNIT_MEAS_CODE` | Scan_Prof_Unit_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `SCAN_PROF_TYPE` | Scan_Professorial Type | VARCHAR2 | 4 |  | Y |
| 15 | `SCAN_PROF_DEC_POS` | Scan_Prof_Decessorial Pos | NUMBER | 22 | 3 | Y |
| 16 | `SCAN_PROF_ITEM_CODE_FLAG` | Scan_Prof_Item_Codeessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `SCAN_PROF_ITEM_CODE_START_POS` | Scan_Prof_Item_Code_Startessorial Pos | NUMBER | 22 | 3 | Y |
| 18 | `SCAN_PROF_ITEM_CODE_END_POS` | Scan_Prof_Item_Code_Endessorial Pos | NUMBER | 22 | 3 | Y |
| 19 | `SCAN_PROF_ITEM_CODE_LEN` | Scan_Prof_Item_Codeessorial Len | NUMBER | 22 | 3 | Y |
| 20 | `SCAN_PROF_MODY` | Scan_Professorial Mody | NUMBER | 22 | 16 | Y |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 26 | `SCAN_PROF_DATE_FORUL` | Scan_Prof_Dateessorial Forul | VARCHAR2 | 500 |  | Y |

## `M_SCAN_PROF_DD`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SCAN_PROF_CODE` | Scan_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SCAN_PROF_INB_OUTB_FLAG` | Scan_Prof_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SCAN_PROF_SEQ_NUM` | Scan_Prof_Seqessorial Num | NUMBER | 22 | 3 | N |
| 6 | `SCAN_PROF_SEQ_NUM_AI_CNT` | Scan_Prof_Seq_Num_Aiessorial Cnt | NUMBER | 22 | 3 | N |
| 7 | `SCAN_PROF_AI_VAL` | Scan_Prof_Aiessorial Val | VARCHAR2 | 4 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SCAN_PROF_H`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SCAN_PROF_CODE` | Scan_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SCAN_PROF_DES` | Scan_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SCAN_PROF_LEN` | Scan_Professorial Len | NUMBER | 22 | 3 | N |
| 6 | `SCAN_PROF_STAT` | Scan_Professorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `SCAN_PROF_INDUSTRY_TP` | Scan_Prof_Industryessorial Tp | VARCHAR2 | 4 |  | Y |
| 8 | `SCAN_PROF_VAR_LEN_FLAG` | Scan_Prof_Var_Lenessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_UCC_PROF`

- **Tipo:** Master
- **Categoria:** RF
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `UCC_PROF_CODE` | Ucc_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `UCC_PROF_DES` | Ucc_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `UCC_PROF_STAT` | Ucc_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `UCC_TP_CODE` | Ucc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `UCC_CTRL_CODE` | Ucc_Ctrlessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `UCC_MEMB_ACCT` | Ucc_Membessorial Acct | VARCHAR2 | 6 |  | N |
| 8 | `UCC_START_SEQ_NUM` | Ucc_Start_Seqessorial Num | NUMBER | 22 | 9 | N |
| 9 | `UCC_END_SEQ_NUM` | Ucc_End_Seqessorial Num | NUMBER | 22 | 9 | N |
| 10 | `UCC_NXT_SEQ_NUM` | Ucc_Nxt_Seqessorial Num | NUMBER | 22 | 9 | N |

