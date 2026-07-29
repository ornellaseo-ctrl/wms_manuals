# Tabelas — Task

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **3**.

## `C_TASK_COMPL`

- **Tipo:** Transactional
- **Categoria:** Task
- **Campos:** 30
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TASK_PEND_ID` | Task_Pendessorial Id | RAW | 32 |  | N |
| 3 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 4 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | N |
| 5 | `TASK_SKIP_FLAG` | Task_Skipessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 8 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 10 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 9 | N |
| 11 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 12 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 13 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 14 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 16 | `PICK_METH` | Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 17 | `PRTY_NUM` | Prtyessorial Num | NUMBER | 22 | 2 | Y |
| 18 | `OP_CODE_ASS` | Op_Codeessorial Ass | VARCHAR2 | 20 |  | Y |
| 19 | `SORT_SEQ_NUM` | Sort_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 20 | `PREREQUISITE_TASK_ID` | Prerequisite_Taskessorial Id | RAW | 32 |  | Y |
| 21 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 22 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 23 | `TASK_PEND_RELEASE_DATE` | Task_Pend_Releaseessorial Date | DATE | 7 |  | Y |
| 24 | `LOC_AISLE_FROM` | Loc_Aisleessorial From | VARCHAR2 | 12 |  | Y |
| 25 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 26 | `TASK_COMPL_MES` | Task_Complessorial Mes | VARCHAR2 | 2000 |  | Y |
| 27 | `PRTY_NUM_OVRR` | Prty_Numessorial Ovrr | NUMBER | 22 | 9 | Y |
| 28 | `TASK_SUSP_FLAG` | Task_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `OP_CODE_SUSP` | Op_Codeessorial Susp | VARCHAR2 | 20 |  | Y |
| 30 | `TASK_SUSP_SRCE_SEL_CODE` | Task_Susp_Srce_Selessorial Code | VARCHAR2 | 6 |  | Y |

## `C_TASK_MGR`

- **Tipo:** Transactional
- **Categoria:** Task
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TASK_RQST_SEQ_NUM` | Task_Rqst_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `TASK_TP_CODE` | Task_Tpessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `TASK_NUM` | Taskessorial Num | NUMBER | 22 | 9 | N |
| 5 | `TASK_LINE_NUM` | Task_Lineessorial Num | NUMBER | 22 | 6 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 7 | `TASK_RQST_CODE` | Task_Rqstessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `TASK_RQST_DATE` | Task_Rqstessorial Date | DATE | 7 |  | N |
| 9 | `TASK_START_DATE` | Task_Startessorial Date | DATE | 7 |  | Y |
| 10 | `TASK_END_DATE` | Task_Endessorial Date | DATE | 7 |  | Y |
| 11 | `TASK_ERR_DATE` | Task_Erressorial Date | DATE | 7 |  | Y |
| 12 | `TASK_ERR_NUM` | Task_Erressorial Num | NUMBER | 22 | 3 | Y |
| 13 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 14 | `TASK_RQST_PRTY_NUM` | Task_Rqst_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 15 | `TASK_TP_PRTY_NUM` | Task_Tp_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 16 | `TASK_LOC_LINE_NUM` | Task_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |

## `C_TASK_PEND`

- **Tipo:** Transactional
- **Categoria:** Task
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 6 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 7 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 8 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 9 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 10 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 12 | `PICK_METH` | Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 13 | `PRTY_NUM` | Prtyessorial Num | NUMBER | 22 | 2 | Y |
| 14 | `OP_CODE_ASS` | Op_Codeessorial Ass | VARCHAR2 | 20 |  | Y |
| 15 | `SORT_SEQ_NUM` | Sort_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 16 | `PREREQUISITE_TASK_ID` | Prerequisite_Taskessorial Id | RAW | 32 |  | Y |
| 17 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 18 | `TASK_PEND_RELEASE_DATE` | Task_Pend_Releaseessorial Date | DATE | 7 |  | Y |
| 19 | `LOC_AISLE_FROM` | Loc_Aisleessorial From | VARCHAR2 | 12 |  | Y |
| 20 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 21 | `PRTY_NUM_OVRR` | Prty_Numessorial Ovrr | NUMBER | 22 | 9 | Y |
| 22 | `TASK_SUSP_FLAG` | Task_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `OP_CODE_SUSP` | Op_Codeessorial Susp | VARCHAR2 | 20 |  | Y |
| 24 | `TASK_SUSP_SRCE_SEL_CODE` | Task_Susp_Srce_Selessorial Code | VARCHAR2 | 6 |  | Y |

