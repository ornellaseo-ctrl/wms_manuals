# Tabelas — Attributes

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **4**.

## `M_MOVE_ATTR_PROF`

- **Tipo:** Master
- **Categoria:** Attributes
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MOVE_ATTR_PROF_CODE` | Move_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `MOVE_ATTR_PROF_DES` | Move_Attr_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MOVE_ATTR_PROF_STAT` | Move_Attr_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DOC_CODE_REP` | Doc_Codeessorial Rep | VARCHAR2 | 4 |  | Y |
| 7 | `DOC_CODE_LABEL` | Doc_Codeessorial Label | VARCHAR2 | 4 |  | Y |
| 8 | `TAKE_OFF_AUTO_HOLD_FLAG` | Take_Off_Auto_Holdessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `MOVE_ATTR_PROF_TASK_FLAG` | Move_Attr_Prof_Taskessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `SUPERVISOR_OVRR_FLAG` | Supervisor_Ovrressorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 16 | `MOVE_ATTR_PROF_CONSL_FLAG` | Move_Attr_Prof_Conslessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WHSE_CODE_STAG` | Whse_Codeessorial Stag | VARCHAR2 | 4 |  | Y |
| 18 | `LOC_CODE_STAG` | Loc_Codeessorial Stag | VARCHAR2 | 12 |  | Y |

## `S_PRT_ATTR_D`

- **Tipo:** System Setup Related
- **Categoria:** Attributes
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_ATTR_SEQ_NUM` | Prt_Attr_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PRT_ATTR_LINE_NUM` | Prt_Attr_Lineessorial Num | NUMBER | 22 | 2 | N |
| 3 | `PRT_ATTR_CODE` | Prt_Attressorial Code | VARCHAR2 | 50 |  | N |
| 4 | `PRT_ATTR_VAL` | Prt_Attressorial Val | VARCHAR2 | 100 |  | N |

## `S_PRT_ATTR_H`

- **Tipo:** System Setup Related
- **Categoria:** Attributes
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRT_ATTR_SEQ_NUM` | Prt_Attr_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 3 | `PRT_ATTR_DATE` | Prt_Attressorial Date | DATE | 7 |  | N |
| 4 | `PRT_FILE_NAME` | Prt_Fileessorial Name | VARCHAR2 | 50 |  | N |

## `S_WHSE_ATTR_TP`

- **Tipo:** System Setup Related
- **Categoria:** Attributes
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `WHSE_ATTR_TP_NUM` | Whse_Attr_Tpessorial Num | NUMBER | 22 | 3 | N |
| 3 | `WHSE_ATTR_TP_OPT_NUM` | Whse_Attr_Tp_Optessorial Num | NUMBER | 22 | 3 | N |
| 4 | `WHSE_ATTR_TP_DES` | Whse_Attr_Tpessorial Des | VARCHAR2 | 60 |  | N |
| 5 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |

