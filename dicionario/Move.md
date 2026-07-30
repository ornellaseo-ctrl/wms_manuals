# Tabelas — Move

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **4**.

## `C_MOVE`

- **Tipo:** Transactional
- **Categoria:** Move
- **Campos:** 40
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MOVE_SEQ_NUM` | Move_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 6 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 7 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 8 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 11 | `MOVE_QTY` | Moveessorial Qty | NUMBER | 22 | 9 | Y |
| 12 | `MOVE_WGT` | Moveessorial Wgt | NUMBER | 22 | 16 | Y |
| 13 | `MOVE_CUBE` | Moveessorial Cube | NUMBER | 22 | 16 | Y |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 17 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 18 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 19 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 20 | `MOVE_DATE` | Moveessorial Date | DATE | 7 |  | Y |
| 21 | `MOVE_AUDIT_NUM` | Move_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 22 | `MOVE_SPOOL_FILE_NAME_LABEL` | Move_Spool_File_Nameessorial Label | VARCHAR2 | 60 |  | Y |
| 23 | `MOVE_SPOOL_FILE_ARCH_ID_LABEL` | Move_Spool_File_Arch_Idessorial Label | VARCHAR2 | 80 |  | Y |
| 24 | `OP_CODE_LABEL` | Op_Codeessorial Label | VARCHAR2 | 20 |  | Y |
| 25 | `MOVE_LABEL_PRT_DATE` | Move_Label_Prtessorial Date | DATE | 7 |  | Y |
| 26 | `MOVE_LABEL_PRT_CNT` | Move_Label_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 27 | `MOVE_SPOOL_FILE_NAME_REP` | Move_Spool_File_Nameessorial Rep | VARCHAR2 | 60 |  | Y |
| 28 | `MOVE_SPOOL_FILE_ARCH_ID_REP` | Move_Spool_File_Arch_Idessorial Rep | VARCHAR2 | 80 |  | Y |
| 29 | `OP_CODE_REP` | Op_Codeessorial Rep | VARCHAR2 | 20 |  | Y |
| 30 | `MOVE_REP_PRT_DATE` | Move_Rep_Prtessorial Date | DATE | 7 |  | Y |
| 31 | `MOVE_REP_PRT_CNT` | Move_Rep_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 32 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 33 | `MOVE_REF1` | Moveessorial Ref1 | VARCHAR2 | 200 |  | Y |
| 34 | `ITEM_LOC_PROF_SEQ_NUM` | Item_Loc_Prof_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 35 | `MOVE_MODE_CODE` | Move_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 36 | `DOC_DIST_DOC_NUM` | Doc_Dist_Docessorial Num | NUMBER | 22 | 9 | Y |
| 37 | `DOC_DIST_DOC_LINE_NUM` | Doc_Dist_Doc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 38 | `DOC_DIST_DOC_LOC_LINE_NUM` | Doc_Dist_Doc_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 39 | `MOVE_RES_FOR_PARTL_PLT_CODE` | Move_Res_For_Partl_Pltessorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `MOVE_MAX_QTY_PER_INVT_ACCESS` | Move_Max_Qty_Per_Invtessorial Access | NUMBER | 22 | 9 | Y |

## `C_MVT_D`

- **Tipo:** Transactional
- **Categoria:** Move
- **Campos:** 12
- **Campos-chave prováveis:** MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_REM_LINE_NUM` | Doc_Rem_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `REM_TEXT` | Remessorial Text | VARCHAR2 | 45 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_MVT_H`

- **Tipo:** Transactional
- **Categoria:** Move
- **Campos:** 59
- **Campos-chave prováveis:** MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `MVT_TRANS_DATE` | Mvt_Transessorial Date | DATE | 7 |  | N |
| 4 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | N |
| 13 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | N |
| 14 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 15 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 17 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 18 | `LOC_BILL_CODE` | Location Bill Code | VARCHAR2 | 4 |  | N |
| 19 | `MVT_EFF_TRANS_DATE` | Mvt_Eff_Transessorial Date | DATE | 7 |  | N |
| 20 | `TRANS_UNIT` | Transessorial Unit | VARCHAR2 | 20 |  | N |
| 21 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 22 | `MVT_CNVC_QTY` | Mvt_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 23 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 24 | `TRANS_WGT` | Transessorial Wgt | NUMBER | 22 | 16 | N |
| 25 | `MVT_WGT` | Mvtessorial Wgt | NUMBER | 22 | 16 | N |
| 26 | `TRANS_WGT_NET` | Trans_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 27 | `MVT_WGT_NET` | Mvt_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 28 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 29 | `TRANS_CUBE` | Transessorial Cube | NUMBER | 22 | 16 | N |
| 30 | `MVT_CUBE` | Mvtessorial Cube | NUMBER | 22 | 16 | N |
| 31 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 32 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 33 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 34 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 35 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 36 | `EDI_AUDIT_NUM` | Edi_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 37 | `MVT_REF1` | Mvtessorial Ref1 | VARCHAR2 | 10 |  | N |
| 38 | `MVT_REF2` | Mvtessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 39 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 40 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 41 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | Y |
| 42 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 43 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | Y |
| 44 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 45 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 46 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 47 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 48 | `MON_END_PROS_FLAG` | Mon_End_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `MVT_REP_FLAG` | Mvt_Repessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `ALT_BILL_GRP_CODE` | Alt_Bill_Grpessorial Code | VARCHAR2 | 20 |  | Y |
| 51 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 52 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 53 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 54 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 55 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 56 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 57 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 58 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 59 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_MOVE`

- **Tipo:** Historical
- **Categoria:** Move
- **Campos:** 42
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INSERT_TO_H_MOVE_DATE` | Insert_To_H_Moveessorial Date | DATE | 7 |  | N |
| 2 | `MOVE_SEQ_NUM` | Move_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 7 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 8 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 9 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 12 | `MOVE_QTY` | Moveessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `MOVE_WGT` | Moveessorial Wgt | NUMBER | 22 | 16 | Y |
| 14 | `MOVE_CUBE` | Moveessorial Cube | NUMBER | 22 | 16 | Y |
| 15 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 16 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 18 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 19 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 20 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 21 | `MOVE_DATE` | Moveessorial Date | DATE | 7 |  | Y |
| 22 | `MOVE_AUDIT_NUM` | Move_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 23 | `MOVE_SPOOL_FILE_NAME_LABEL` | Move_Spool_File_Nameessorial Label | VARCHAR2 | 60 |  | Y |
| 24 | `MOVE_SPOOL_FILE_ARCH_ID_LABEL` | Move_Spool_File_Arch_Idessorial Label | VARCHAR2 | 80 |  | Y |
| 25 | `OP_CODE_LABEL` | Op_Codeessorial Label | VARCHAR2 | 20 |  | Y |
| 26 | `MOVE_LABEL_PRT_DATE` | Move_Label_Prtessorial Date | DATE | 7 |  | Y |
| 27 | `MOVE_LABEL_PRT_CNT` | Move_Label_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 28 | `MOVE_SPOOL_FILE_NAME_REP` | Move_Spool_File_Nameessorial Rep | VARCHAR2 | 60 |  | Y |
| 29 | `MOVE_SPOOL_FILE_ARCH_ID_REP` | Move_Spool_File_Arch_Idessorial Rep | VARCHAR2 | 80 |  | Y |
| 30 | `OP_CODE_REP` | Op_Codeessorial Rep | VARCHAR2 | 20 |  | Y |
| 31 | `MOVE_REP_PRT_DATE` | Move_Rep_Prtessorial Date | DATE | 7 |  | Y |
| 32 | `MOVE_REP_PRT_CNT` | Move_Rep_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 33 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 34 | `MOVE_REF1` | Moveessorial Ref1 | VARCHAR2 | 200 |  | Y |
| 35 | `ITEM_LOC_PROF_SEQ_NUM` | Item_Loc_Prof_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 36 | `MOVE_MODE_CODE` | Move_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 37 | `TER_CODE_DEL` | Ter_Codeessorial Del | VARCHAR2 | 10 |  | Y |
| 38 | `DOC_DIST_DOC_NUM` | Doc_Dist_Docessorial Num | NUMBER | 22 | 9 | Y |
| 39 | `DOC_DIST_DOC_LINE_NUM` | Doc_Dist_Doc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 40 | `DOC_DIST_DOC_LOC_LINE_NUM` | Doc_Dist_Doc_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 41 | `MOVE_RES_FOR_PARTL_PLT_CODE` | Move_Res_For_Partl_Pltessorial Code | VARCHAR2 | 4 |  | Y |
| 42 | `MOVE_MAX_QTY_PER_INVT_ACCESS` | Move_Max_Qty_Per_Invtessorial Access | NUMBER | 22 | 9 | Y |

