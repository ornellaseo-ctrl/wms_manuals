# Tabelas — Printer

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **11**.

## `D4_PRT_ATTR_NAME_STD`

- **Tipo:** Misc
- **Categoria:** Printer
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_ATTR_NAME` | Prt_Attressorial Name | VARCHAR2 | 50 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `PRT_ATTR_DES` | Prt_Attressorial Des | VARCHAR2 | 50 |  | N |

## `M_PRT`

- **Tipo:** Master
- **Categoria:** Printer
- **Campos:** 20

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 3 | `PRT_DES` | Prtessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PRT_STAT` | Prtessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `SYS_PRT_CODE` | Sys_Prtessorial Code | VARCHAR2 | 30 |  | N |
| 6 | `PRT_SIZE_FLAG` | Prt_Sizeessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `PRT_COMPRS_ESC_SEQ` | Prt_Comprs_Escessorial Seq | VARCHAR2 | 30 |  | Y |
| 8 | `PRT_RESET_ESC_SEQ` | Prt_Reset_Escessorial Seq | VARCHAR2 | 30 |  | Y |
| 9 | `PRT_COMMD_TP` | Prt_Commdessorial Tp | VARCHAR2 | 1 |  | Y |
| 10 | `PRT_COMMD` | Prtessorial Commd | VARCHAR2 | 100 |  | Y |
| 11 | `PRT_SYS_FLAG` | Prt_Sysessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `PRT_PROF_CODE` | Prt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `LABEL_SWARE_CONN_PARA` | Label_Sware_Connessorial Para | VARCHAR2 | 60 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 19 | `PRT_REF_IP` | Prt_Refessorial Ip | VARCHAR2 | 20 |  | Y |
| 20 | `PRT_REF_MODEL` | Prt_Refessorial Model | VARCHAR2 | 30 |  | Y |

## `M_PRT_PROF_D`

- **Tipo:** Master
- **Categoria:** Printer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `PRT_PROF_CODE` | Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `FAX_OVRL_CODE` | Fax_Ovrlessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `PRT_PROF_MACRO_FILE_NAME` | Prt_Prof_Macro_Fileessorial Name | VARCHAR2 | 250 |  | N |
| 6 | `PRT_PROF_MACRO_ESC_SEQ` | Prt_Prof_Macro_Escessorial Seq | VARCHAR2 | 250 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PRT_PROF_H`

- **Tipo:** Master
- **Categoria:** Printer
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `PRT_PROF_CODE` | Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PRT_PROF_DES` | Prt_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PRT_PROF_STAT` | Prt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `PRT_TP` | Prtessorial Tp | VARCHAR2 | 20 |  | Y |
| 6 | `PRT_PROF_FAX_OVRL_USE_FLAG` | Prt_Prof_Fax_Ovrl_Useessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PRT_PRTY`

- **Tipo:** Master
- **Categoria:** Printer
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_PRTY_CODE` | Prt_Prtyessorial Code | VARCHAR2 | 1 |  | N |
| 2 | `PRT_PRTY_DES` | Prt_Prtyessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `PRT_PRTY_STAT` | Prt_Prtyessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_SPOOL`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SPOOL_SEQ_NUM` | Spool_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SPOOL_BAT_FLAG` | Spool_Batessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `SPOOL_DATE` | Spoolessorial Date | DATE | 7 |  | N |
| 5 | `SPOOL_FILE_EXACT` | Spool_Fileessorial Exact | VARCHAR2 | 20 |  | N |
| 6 | `SPOOL_FILE_DIR` | Spool_Fileessorial Dir | VARCHAR2 | 60 |  | N |
| 7 | `SPOOL_FILE_TP` | Spool_Fileessorial Tp | VARCHAR2 | 10 |  | N |
| 8 | `SPOOL_STAT_CODE` | Spool_Statessorial Code | VARCHAR2 | 1 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | N |
| 11 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 12 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 13 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 14 | `SYS_PRT_CODE` | Sys_Prtessorial Code | VARCHAR2 | 30 |  | N |
| 15 | `SPOOL_COMPRS_FLAG` | Spool_Comprsessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `SPOOL_PAGE_SIZE` | Spool_Pageessorial Size | NUMBER | 22 | 3 | Y |
| 17 | `SPOOL_STAT_MES1` | Spool_Statessorial Mes1 | VARCHAR2 | 255 |  | Y |
| 18 | `SPOOL_STAT_MES2` | Spool_Statessorial Mes2 | VARCHAR2 | 255 |  | Y |
| 19 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 250 |  | Y |
| 20 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 250 |  | Y |
| 21 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 60 |  | Y |
| 22 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | Y |
| 23 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | Y |
| 24 | `FAX_COMMENT1` | Faxessorial Comment1 | VARCHAR2 | 60 |  | Y |
| 25 | `FAX_COMMENT2` | Faxessorial Comment2 | VARCHAR2 | 60 |  | Y |
| 26 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `FAX_OVERLAY_CODE` | Fax_Overlayessorial Code | VARCHAR2 | 4 |  | Y |
| 28 | `FAX_SEND_TIME` | Fax_Sendessorial Time | NUMBER | 22 | 4 | Y |
| 29 | `SPOOL_STAT_TIME` | Spool_Statessorial Time | NUMBER | 22 | 4 | Y |
| 30 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 31 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 32 | `SPOOL_PROS_DATE` | Spool_Prosessorial Date | DATE | 7 |  | Y |
| 33 | `SPOOL_OS_FAX_REF` | Spool_Os_Faxessorial Ref | VARCHAR2 | 30 |  | Y |
| 34 | `SPOOL_SEQ_NUM_REF` | Spool_Seq_Numessorial Ref | NUMBER | 22 | 9 | Y |

## `S_SPOOL_CONT`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SPOOL_NAME` | Spoolessorial Name | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 4 | `PRT_PRTY_CODE` | Prt_Prtyessorial Code | VARCHAR2 | 1 |  | N |
| 5 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 6 | `NUM_CP` | Numessorial Cp | NUMBER | 22 | 2 | N |
| 7 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 8 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 10 | `SPOOL_DATE` | Spoolessorial Date | DATE | 7 |  | N |
| 11 | `DET_LINE_CNT` | Det_Lineessorial Cnt | NUMBER | 22 | 9 | N |
| 12 | `HEAD_LINE_CNT` | Head_Lineessorial Cnt | NUMBER | 22 | 2 | N |
| 13 | `PRT_LINE_PER_PAGE` | Prt_Line_Peressorial Page | NUMBER | 22 | 3 | N |
| 14 | `PRT_CNT` | Prtessorial Cnt | NUMBER | 22 | 3 | N |
| 15 | `PRT_FLAG` | Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `MAND_PRT_FLAG` | Mand_Prtessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `PRT_REGEN_FLAG` | Prt_Regenessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `PRT_PARA_CODE` | Prt_Paraessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `EXE_JOB_FMT_CODE` | Exe_Job_Fmtessorial Code | VARCHAR2 | 10 |  | Y |

## `S_SPOOL_CTRL`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SPOOL_CTRL_LAST_DATE` | Spool_Ctrl_Lastessorial Date | DATE | 7 |  | N |

## `S_SPOOL_FAX_BAT`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 5 | `ACC_TP_CODE` | Acc_Tpessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `FAX_ACC_CODE` | Fax_Accessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `CUST_BAT_FLAG` | Cust_Batessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `FAX_TIME` | Faxessorial Time | NUMBER | 22 | 4 | N |
| 9 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 250 |  | N |
| 10 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 250 |  | Y |
| 11 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 60 |  | N |
| 12 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | N |
| 13 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | N |
| 14 | `FAX_COMMENT1` | Faxessorial Comment1 | VARCHAR2 | 60 |  | Y |
| 15 | `FAX_COMMENT2` | Faxessorial Comment2 | VARCHAR2 | 60 |  | Y |
| 16 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `FAX_OVERLAY_CODE` | Fax_Overlayessorial Code | VARCHAR2 | 4 |  | Y |

## `S_SPOOL_NAME`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SPOOL_NAME_DATE` | Spool_Nameessorial Date | DATE | 7 |  | N |
| 2 | `SPOOL_NAME` | Spoolessorial Name | VARCHAR2 | 6 |  | N |

## `S_SPOOL_TRANS`

- **Tipo:** System Setup Related
- **Categoria:** Printer
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SPOOL_BAT_FLAG` | Spool_Batessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `SPOOL_DATE` | Spoolessorial Date | DATE | 7 |  | N |
| 4 | `SPOOL_FILE_EXACT` | Spool_Fileessorial Exact | VARCHAR2 | 20 |  | N |
| 5 | `SPOOL_FILE_DIR` | Spool_Fileessorial Dir | VARCHAR2 | 60 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | N |
| 8 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 9 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 10 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 11 | `SYS_PRT_CODE` | Sys_Prtessorial Code | VARCHAR2 | 30 |  | N |
| 12 | `SPOOL_TRANS_PRTY_NUM` | Spool_Trans_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 13 | `SPOOL_COMPRS_FLAG` | Spool_Comprsessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `SPOOL_PAGE_SIZE` | Spool_Pageessorial Size | NUMBER | 22 | 3 | Y |
| 15 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 250 |  | Y |
| 16 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 250 |  | Y |
| 17 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 60 |  | Y |
| 18 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | Y |
| 19 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | Y |
| 20 | `FAX_COMMENT1` | Faxessorial Comment1 | VARCHAR2 | 60 |  | Y |
| 21 | `FAX_COMMENT2` | Faxessorial Comment2 | VARCHAR2 | 60 |  | Y |
| 22 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `FAX_OVERLAY_CODE` | Fax_Overlayessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `FAX_SEND_TIME` | Fax_Sendessorial Time | NUMBER | 22 | 4 | Y |
| 25 | `SPOOL_STAT_TIME` | Spool_Statessorial Time | NUMBER | 22 | 4 | Y |
| 26 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 27 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 28 | `SPOOL_SEQ_NUM` | Spool_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 29 | `BAT_SPOOL_SEQ_NUM` | Bat_Spool_Seqessorial Num | NUMBER | 22 | 9 | Y |

