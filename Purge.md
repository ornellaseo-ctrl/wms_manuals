# Tabelas — Purge

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **11**.

## `H_ARCH_PURGE_D`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 4 | `ARCH_PURGE_TABLE_NAME` | Arch_Purge_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `ARCH_PURGE_TABLE_REC_CNT` | Arch_Purge_Table_Recessorial Cnt | NUMBER | 22 | 9 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ARCH_PURGE_DEL_D`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ARCH_PURGE_DEL_SEQ_NUM` | Arch_Purge_Del_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ARCH_PURGE_TABLE_NAME` | Arch_Purge_Tableessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `ARCH_PURGE_TABLE_REC_CNT` | Arch_Purge_Table_Recessorial Cnt | NUMBER | 22 | 9 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ARCH_PURGE_DEL_H`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ARCH_PURGE_DEL_SEQ_NUM` | Arch_Purge_Del_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | Y |
| 5 | `ARCH_PURGE_REG_DEL_CUT_DATE` | Arch_Purge_Reg_Del_Cutessorial Date | DATE | 7 |  | Y |
| 6 | `ARCH_PURGE_REG_DEL_RUN_DATE` | Arch_Purge_Reg_Del_Runessorial Date | DATE | 7 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ARCH_PURGE_H`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 4 | `ARCH_PURGE_REG_DATE` | Arch_Purge_Regessorial Date | DATE | 7 |  | N |
| 5 | `ARCH_PURGE_REG_RUN_DATE` | Arch_Purge_Reg_Runessorial Date | DATE | 7 |  | N |
| 6 | `CUST_CODE_REST` | Cust_Codeessorial Rest | VARCHAR2 | 10 |  | Y |
| 7 | `ARCH_PURGE_ORD_COMPL_FLAG` | Arch_Purge_Ord_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ARCH_PURGE_RCPT_COMPL_FLAG` | Arch_Purge_Rcpt_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `ARCH_PURGE_INVT_COMPL_FLAG` | Arch_Purge_Invt_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `ARCH_PURGE_ACCSS_COMPL_FLAG` | Arch_Purge_Accss_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ARCH_PURGE_IMM_INV_COMPL_FLAG` | Arch_Purge_Imm_Inv_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_PURGE`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 3 | `PURGE_REG_DATE` | Purge_Regessorial Date | DATE | 7 |  | N |
| 4 | `PURGE_REG_RUN_DATE` | Purge_Reg_Runessorial Date | DATE | 7 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 240 |  | Y |
| 6 | `PURGE_NAME_ORD` | Purge_Nameessorial Ord | VARCHAR2 | 20 |  | N |
| 7 | `PURGE_NAME_RCPT` | Purge_Nameessorial Rcpt | VARCHAR2 | 20 |  | N |
| 8 | `PURGE_NAME_INVT` | Purge_Nameessorial Invt | VARCHAR2 | 20 |  | N |
| 9 | `PURGE_ORD_COMPL_FLAG` | Purge_Ord_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `PURGE_RCPT_COMPL_FLAG` | Purge_Rcpt_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `PURGE_INVT_COMPL_FLAG` | Purge_Invt_Complessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_PURGE_INVT`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `PURGE_NAME_INVT` | Purge_Nameessorial Invt | VARCHAR2 | 20 |  | N |
| 10 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 11 | `PURGE_REG_DATE` | Purge_Regessorial Date | DATE | 7 |  | N |

## `H_PURGE_ORD`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `PURGE_NAME_ORD` | Purge_Nameessorial Ord | VARCHAR2 | 20 |  | N |
| 5 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 6 | `PURGE_REG_DATE` | Purge_Regessorial Date | DATE | 7 |  | N |
| 7 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 8 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |

## `H_PURGE_RCPT`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `PURGE_NAME_RCPT` | Purge_Nameessorial Rcpt | VARCHAR2 | 20 |  | N |
| 5 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 6 | `PURGE_REG_DATE` | Purge_Regessorial Date | DATE | 7 |  | N |
| 7 | `RCPT_PREX` | Rcptessorial Prex | VARCHAR2 | 4 |  | N |
| 8 | `RCPT_SUFX` | Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |

## `H_RCPT_D1`

- **Tipo:** Historical
- **Categoria:** Purge
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 8 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 9 | `RCPT_REM_LINE_NUM` | Rcpt_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 10 | `RCPT_REM_LINE_TEXT` | Rcpt_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_PURGE_CTRL_D`

- **Tipo:** System Setup Related
- **Categoria:** Purge
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 11 |  | N |
| 4 | `FILE_NAME` | Fileessorial Name | VARCHAR2 | 255 |  | N |
| 5 | `LINE_CNT` | Lineessorial Cnt | NUMBER | 22 | 9 | N |

## `S_PURGE_CTRL_H`

- **Tipo:** System Setup Related
- **Categoria:** Purge
- **Campos:** 48
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PURGE_REG_NUM` | Purge_Regessorial Num | NUMBER | 22 | 6 | N |
| 3 | `PURGE_STAT` | Purgeessorial Stat | NUMBER | 22 | 3 | N |
| 4 | `TODAY_DATE` | Todayessorial Date | DATE | 7 |  | N |
| 5 | `SYS_PRT_CODE` | Sys_Prtessorial Code | VARCHAR2 | 31 |  | N |
| 6 | `ARCH_FLAG` | Archessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `ORD_IN_MVT_FLAG` | Ord_In_Mvtessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `LIMIT_DATE` | Limitessorial Date | DATE | 7 |  | N |
| 9 | `VERBOSITY_LEVEL` | Verbosityessorial Level | NUMBER | 22 | 1 | N |
| 10 | `COMP_NAME` | Compessorial Name | VARCHAR2 | 31 |  | N |
| 11 | `SEL_DES` | Selessorial Des | VARCHAR2 | 31 |  | N |
| 12 | `CUST_CODE_RESTRICT` | Cust_Codeessorial Restrict | VARCHAR2 | 255 |  | Y |
| 13 | `ORD_REP_FLAG` | Ord_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `RCPT_REP_FLAG` | Rcpt_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `INVT_REP_FLAG` | Invt_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `TRANS_HIST_REP_FLAG` | Trans_Hist_Repessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `ORD_REP_SEQ_FLAG` | Ord_Rep_Seqessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `RCPT_REP_SEQ_FLAG` | Rcpt_Rep_Seqessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `CUST_DATE_CHAR` | Cust_Dateessorial Char | VARCHAR2 | 21 |  | N |
| 20 | `CUST_DATE_FORMAT` | Cust_Dateessorial Format | VARCHAR2 | 21 |  | N |
| 21 | `CUST_DES` | Custessorial Des | VARCHAR2 | 31 |  | N |
| 22 | `PRINT_PATH` | Printessorial Path | VARCHAR2 | 255 |  | N |
| 23 | `ARCHIVE_PATH` | Archiveessorial Path | VARCHAR2 | 255 |  | N |
| 24 | `MAX_INVT_LEVELS` | Max_Invtessorial Levels | NUMBER | 22 | 1 | N |
| 25 | `ACTIVITY_REQUIRED_FLAG` | Activity_Requiredessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `PROBLEM_FILE` | Problemessorial File | VARCHAR2 | 255 |  | N |
| 27 | `WHERE_FILE` | Whereessorial File | VARCHAR2 | 255 |  | N |
| 28 | `REPORT_FINAL_FILE` | Report_Finalessorial File | VARCHAR2 | 255 |  | N |
| 29 | `REPORT_DONE_FILE` | Report_Doneessorial File | VARCHAR2 | 255 |  | N |
| 30 | `ORD_ARCHIVE_FILE` | Ord_Archiveessorial File | VARCHAR2 | 255 |  | Y |
| 31 | `ORD_XREF_REP_FILE` | Ord_Xref_Repessorial File | VARCHAR2 | 255 |  | Y |
| 32 | `ORD_XREF_LINE_CNT` | Ord_Xref_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 33 | `ORD_SHORT_REP_FILE` | Ord_Short_Repessorial File | VARCHAR2 | 255 |  | Y |
| 34 | `ORD_SHORT_LINE_CNT` | Ord_Short_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 35 | `ORD_LONG_REP_FILE` | Ord_Long_Repessorial File | VARCHAR2 | 255 |  | Y |
| 36 | `ORD_LONG_LINE_CNT` | Ord_Long_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 37 | `RCPT_ARCHIVE_FILE` | Rcpt_Archiveessorial File | VARCHAR2 | 255 |  | Y |
| 38 | `RCPT_XREF_REP_FILE` | Rcpt_Xref_Repessorial File | VARCHAR2 | 255 |  | Y |
| 39 | `RCPT_XREF_LINE_CNT` | Rcpt_Xref_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 40 | `RCPT_SHORT_REP_FILE` | Rcpt_Short_Repessorial File | VARCHAR2 | 255 |  | Y |
| 41 | `RCPT_SHORT_LINE_CNT` | Rcpt_Short_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 42 | `RCPT_LONG_REP_FILE` | Rcpt_Long_Repessorial File | VARCHAR2 | 255 |  | Y |
| 43 | `RCPT_LONG_LINE_CNT` | Rcpt_Long_Lineessorial Cnt | NUMBER | 22 | 6 | Y |
| 44 | `INVT_REP_FILE` | Invt_Repessorial File | VARCHAR2 | 255 |  | Y |
| 45 | `INVT_ARCHIVE_FILE` | Invt_Archiveessorial File | VARCHAR2 | 255 |  | Y |
| 46 | `TRANS_HIST_REP_FILE` | Trans_Hist_Repessorial File | VARCHAR2 | 255 |  | Y |
| 47 | `TRANS_HIST_ARCHIVE_FILE` | Trans_Hist_Archiveessorial File | VARCHAR2 | 255 |  | Y |
| 48 | `INVT_TRANS_HIST_ARCHIVE_FILE` | Invt_Trans_Hist_Archiveessorial File | VARCHAR2 | 255 |  | Y |

