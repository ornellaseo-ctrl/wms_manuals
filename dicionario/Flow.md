# Tabelas — Flow

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **9**.

## `C_FLOW_TIME`

- **Tipo:** Transactional
- **Categoria:** Flow
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 4 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | N |
| 5 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 6 | `FLOW_INB_OUTB_FLAG` | Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `FLOW_DATE` | Flow Date | DATE | 7 |  | N |
| 8 | `FLOW_CODE` | Flowessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `FLOW_CODE_TP_FLAG` | Flow_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | Y |
| 11 | `FLOW_INFO_DATE` | Flow_Infoessorial Date | DATE | 7 |  | Y |
| 12 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 13 | `SPOOL_FILE_NAME` | Spool_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 14 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 15 | `SPOOL_FILE_ARCH_ID` | Spool_File_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 16 | `FRONT_FAX_OVRL_ARCH_ID` | Front_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 17 | `BACK_FAX_OVRL_ARCH_ID` | Back_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 18 | `EXT_FILE_SEQ_NUM` | Ext_File_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_FLOW_TIME`

- **Tipo:** Historical
- **Categoria:** Flow
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_PREX` | Docessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `DOC_SUFX` | Docessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `FLOW_INB_OUTB_FLAG` | Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `FLOW_DATE` | Flow Date | DATE | 7 |  | N |
| 9 | `FLOW_CODE` | Flowessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `FLOW_CODE_TP_FLAG` | Flow_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | Y |
| 12 | `FLOW_INFO_DATE` | Flow_Infoessorial Date | DATE | 7 |  | Y |
| 13 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 14 | `SPOOL_FILE_NAME` | Spool_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 15 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 16 | `SPOOL_FILE_ARCH_ID` | Spool_File_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 17 | `FRONT_FAX_OVRL_ARCH_ID` | Front_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 18 | `BACK_FAX_OVRL_ARCH_ID` | Back_Fax_Ovrl_Archessorial Id | VARCHAR2 | 80 |  | Y |
| 19 | `EXT_FILE_SEQ_NUM` | Ext_File_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_D`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_INB_OUTB_FLAG` | Info_Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_PROS_MAND_FLAG` | Info_Flow_Pros_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INFO_FLOW_ASS_LOC_FLAG` | Info_Flow_Ass_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `INFO_FLOW_DEALLOC_FLAG` | Info_Flow_Deallocessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 12 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `INFO_FLOW_CREATE_PROF_FLAG` | Info_Flow_Create_Professorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `INFO_FLOW_CREATE_DRMS_FLAG` | Info_Flow_Create_Drmsessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `INFO_FLOW_ALERT_TIME` | Info_Flow_Alertessorial Time | VARCHAR2 | 6 |  | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_D2`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_INB_OUTB_FLAG` | Info_Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INFO_FLOW_SUMM_LEV_NUM` | Info_Flow_Summ_Levessorial Num | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE_START` | Flow_Pros_Codeessorial Start | VARCHAR2 | 4 |  | N |
| 7 | `FLOW_PROS_CODE_END` | Flow_Pros_Codeessorial End | VARCHAR2 | 4 |  | N |
| 8 | `JOB_TP_CODE` | Job_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_DD1`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_INB_OUTB_FLAG` | Info_Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 8 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 9 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_DD2`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_INB_OUTB_FLAG` | Info_Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `INFO_FLOW_SPC_VER_SEQ_NUM` | Info_Flow_Spc_Ver_Seqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `SPC_VER_CODE` | Spc_Veressorial Code | VARCHAR2 | 4 |  | N |
| 8 | `INFO_FLOW_SPC_VER_COMPL_FLAG` | Info_Flow_Spc_Ver_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `INFO_FLOW_SPC_VER_SEQ_FLAG` | Info_Flow_Spc_Ver_Seqessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `INFO_FLOW_SPC_VER_DISP_FLAG` | Info_Flow_Spc_Ver_Dispessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_DD3`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_INB_OUTB_FLAG` | Info_Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_INCL_FLAG` | Info_Flow_Inclessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INFO_FLOW_PROF_H`

- **Tipo:** Master
- **Categoria:** Flow
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 4 | `INFO_FLOW_PROF_DES` | Info_Flow_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INFO_FLOW_PROF_STAT` | Info_Flow_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `T_FLOW_TIME`

- **Tipo:** Temporary
- **Categoria:** Flow
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 3 | `FLOW_INB_OUTB_FLAG` | Flow_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `FLOW_DATE` | Flow Date | DATE | 7 |  | Y |
| 5 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | Y |
| 6 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `SUPERVISOR_CODE` | Supervisoressorial Code | VARCHAR2 | 20 |  | Y |
| 9 | `PICK_OP_CODE` | Pick_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 10 | `SUPERVISOR_APPRV_FLAG` | Supervisor_Apprvessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `SYSTEM_QTY` | Systemessorial Qty | NUMBER | 22 | 9 | Y |
| 12 | `SCAN_QTY` | Scanessorial Qty | NUMBER | 22 | 9 | Y |

