# Tabelas — Customer

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **60**.

## `CUST_AUDIT`

- **Tipo:** Misc
- **Categoria:** Customer
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 3 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 9 | Y |

## `C_CUST_CON_ITEM_LAST_SHIP`

- **Tipo:** Transactional
- **Categoria:** Customer
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `LAST_SHIP_EXPY_DATE` | Last_Ship_Expyessorial Date | DATE | 7 |  | N |
| 7 | `LAST_SHIP_INVT_ACCESS` | Last_Ship_Invtessorial Access | VARCHAR2 | 5 |  | N |
| 8 | `LAST_SHIP_ORD_NUM` | Last_Ship_Ordessorial Num | NUMBER | 22 | 9 | N |
| 9 | `LAST_SHIP_ORD_LINE_NUM` | Last_Ship_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 10 | `LAST_SHIP_DATE` | Last_Shipessorial Date | DATE | 7 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_CUST_CON_OUTB_RULE_FAIL`

- **Tipo:** Transactional
- **Categoria:** Customer
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 5 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 6 | `CUST_CON_OUTB_RULE_FAIL_TP` | Cust_Con_Outb_Rule_Failessorial Tp | VARCHAR2 | 2 |  | Y |
| 7 | `CUST_CON_OUTB_RULE_FAIL_TEXT` | Cust_Con_Outb_Rule_Failessorial Text | VARCHAR2 | 1500 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_CUST_FIX_CHG_RUN`

- **Tipo:** Transactional
- **Categoria:** Customer
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 6 | `CUST_FIX_CHG_DATE_LAST` | Cust_Fix_Chg_Dateessorial Last | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_SESSION`

- **Tipo:** Transactional
- **Categoria:** Customer
- **Campos:** 19

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CLIENT_SESSION_ID` | Client_Sessionessorial Id | VARCHAR2 | 250 |  | N |
| 2 | `CLIENT_EXPY_TIME` | Client_Expyessorial Time | NUMBER | 22 | 6 | Y |
| 3 | `CLIENT_OP_CODE` | Client_Opessorial Code | VARCHAR2 | 250 |  | N |
| 4 | `CLIENT_DB_CONN` | Client_Dbessorial Conn | VARCHAR2 | 250 |  | N |
| 5 | `CLIENT_HOST_IP` | Client_Hostessorial Ip | VARCHAR2 | 250 |  | Y |
| 6 | `CLIENT_HOST_NAME` | Client_Hostessorial Name | VARCHAR2 | 250 |  | Y |
| 7 | `CLIENT_REFRESH_TIME` | Client_Refreshessorial Time | DATE | 7 |  | Y |
| 8 | `SERVER_SESSION_ID` | Server_Sessionessorial Id | VARCHAR2 | 250 |  | Y |
| 9 | `SERVER_LOGIN_TIME` | Server_Loginessorial Time | DATE | 7 |  | N |
| 10 | `SERVER_LOGIN_ERR` | Server_Loginessorial Err | VARCHAR2 | 250 |  | Y |
| 11 | `SERVER_EXPY_TIME` | Server_Expyessorial Time | NUMBER | 22 | 6 | Y |
| 12 | `SERVER_REFRESH_TIME` | Server_Refreshessorial Time | DATE | 7 |  | Y |
| 13 | `SERVER_REFRESH_ERR` | Server_Refreshessorial Err | VARCHAR2 | 250 |  | Y |
| 14 | `SERVER_LOGOUT_TIME` | Server_Logoutessorial Time | DATE | 7 |  | Y |
| 15 | `SERVER_LOGOUT_ERR` | Server_Logoutessorial Err | VARCHAR2 | 250 |  | Y |
| 16 | `SERVER_HOST` | Serveressorial Host | VARCHAR2 | 250 |  | N |
| 17 | `SERVER_PROD_ID` | Server_Prodessorial Id | VARCHAR2 | 250 |  | N |
| 18 | `SERVER_CONN_TP` | Server_Connessorial Tp | VARCHAR2 | 250 |  | N |
| 19 | `SERVER_LICENSE` | Serveressorial License | VARCHAR2 | 250 |  | Y |

## `H_CUST_CON_ITEM_LAST_SHIP`

- **Tipo:** Historical
- **Categoria:** Customer
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INSERT_TO_HISTORY_DATE` | Insert_To_Historyessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `LAST_SHIP_EXPY_DATE` | Last_Ship_Expyessorial Date | DATE | 7 |  | N |
| 8 | `LAST_SHIP_INVT_ACCESS` | Last_Ship_Invtessorial Access | VARCHAR2 | 5 |  | N |
| 9 | `LAST_SHIP_ORD_NUM` | Last_Ship_Ordessorial Num | NUMBER | 22 | 9 | N |
| 10 | `LAST_SHIP_ORD_LINE_NUM` | Last_Ship_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 11 | `LAST_SHIP_DATE` | Last_Shipessorial Date | DATE | 7 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_CUST_FIX_CHG_RUN`

- **Tipo:** Historical
- **Categoria:** Customer
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `ACCSS_NUM` | Access Number | NUMBER | 22 | 9 | N |
| 6 | `CUST_FIX_CHG_DATE_LAST` | Cust_Fix_Chg_Dateessorial Last | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ALT_CUST_REP_D`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ALT_CUST_REP_TP_CODE` | Alt_Cust_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ALT_CUST_REP_CODE` | Alt_Cust_Repessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `ALT_CUST_REP_DES` | Alt_Cust_Repessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `ALT_CUST_REP_STAT` | Alt_Cust_Repessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ALT_CUST_REP_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ALT_CUST_REP_TP_CODE` | Alt_Cust_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ALT_CUST_REP_TP_DES` | Alt_Cust_Rep_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ALT_CUST_REP_TP_STAT` | Alt_Cust_Rep_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_AUTH`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CONTACT_NAME` | Contactessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `CONTACT_TEL_NUM` | Contact_Telessorial Num | VARCHAR2 | 10 |  | N |
| 5 | `CONTACT_TEL_NUM_EXT` | Contact_Tel_Numessorial Ext | VARCHAR2 | 10 |  | N |
| 6 | `CUST_AUTH_STAT` | Cust_Authessorial Stat | VARCHAR2 | 1 |  | N |

## `M_CUST_BILL_PROF`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 62
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_BILL_PROF_CODE` | Cust_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_BILL_PROF_DES` | Cust_Bill_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_BILL_PROF_STAT` | Cust_Bill_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | Y |
| 7 | `TERM_CODE` | Termessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `CUST_BILL_PROF_CHG_INT_FLAG` | Cust_Bill_Prof_Chg_Intessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CUST_BILL_PROF_CRT_LMT_AMT` | Cust_Bill_Prof_Crt_Lmtessorial Amt | NUMBER | 22 | 10 | N |
| 10 | `CUST_BILL_PROF_SEND_STMT_FLAG` | Cust_Bill_Prof_Send_Stmtessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CUST_BILL_PROF_ORG_RATE_FLAG` | Cust_Bill_Prof_Org_Rateessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `CUST_BILL_PROF_RATE_QUAL_FLAG` | Cust_Bill_Prof_Rate_Qualessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `CUST_BILL_PROF_SEND_INV_FLAG` | Cust_Bill_Prof_Send_Invessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `INV_PRT_PROF_CODE` | Inv_Prt_Professorial Code | VARCHAR2 | 4 |  | N |
| 15 | `CUST_BILL_PROF_RENW_INCL_FLAG` | Cust_Bill_Prof_Renw_Inclessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CHG_CODE_RCPT` | Chg_Codeessorial Rcpt | VARCHAR2 | 6 |  | Y |
| 17 | `CHG_CODE_RENW` | Chg_Codeessorial Renw | VARCHAR2 | 6 |  | Y |
| 18 | `CHG_CODE_ACC` | Chg_Codeessorial Acc | VARCHAR2 | 6 |  | Y |
| 19 | `CUST_BILL_PROF_RENW_DAY_FLAG` | Cust_Bill_Prof_Renw_Dayessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `TAX_CODE` | Tax Code | VARCHAR2 | 4 |  | N |
| 21 | `CUST_BILL_PROF_RCPT_RATE_FLAG` | Cust_Bill_Prof_Rcpt_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CHG_CODE_ACC_THRSH` | Chg_Code_Accessorial Thrsh | VARCHAR2 | 6 |  | Y |
| 23 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `RENW_SUMM_CODE` | Renw_Summessorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `CHG_CODE_RCPT_SURCHG1` | Chg_Code_Rcptessorial Surchg1 | VARCHAR2 | 6 |  | Y |
| 26 | `CHG_CODE_RCPT_SURCHG2` | Chg_Code_Rcptessorial Surchg2 | VARCHAR2 | 6 |  | Y |
| 27 | `RCPT_SURCHG2_INCL_FLAG` | Rcpt_Surchg2_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `CHG_CODE_RCPT_SURCHG3` | Chg_Code_Rcptessorial Surchg3 | VARCHAR2 | 6 |  | Y |
| 29 | `RCPT_SURCHG3_INCL_FLAG` | Rcpt_Surchg3_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 30 | `CHG_CODE_RENW_SURCHG1` | Chg_Code_Renwessorial Surchg1 | VARCHAR2 | 6 |  | Y |
| 31 | `CHG_CODE_RENW_SURCHG2` | Chg_Code_Renwessorial Surchg2 | VARCHAR2 | 6 |  | Y |
| 32 | `RENW_SURCHG2_INCL_FLAG` | Renw_Surchg2_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `CHG_CODE_RENW_SURCHG3` | Chg_Code_Renwessorial Surchg3 | VARCHAR2 | 6 |  | Y |
| 34 | `RENW_SURCHG3_INCL_FLAG` | Renw_Surchg3_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `CHG_CODE_ACCSS_SURCHG1` | Chg_Code_Accssessorial Surchg1 | VARCHAR2 | 6 |  | Y |
| 36 | `CHG_CODE_ACCSS_SURCHG2` | Chg_Code_Accssessorial Surchg2 | VARCHAR2 | 6 |  | Y |
| 37 | `ACCSS_SURCHG2_INCL_FLAG` | Accss_Surchg2_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `CHG_CODE_ACCSS_SURCHG3` | Chg_Code_Accssessorial Surchg3 | VARCHAR2 | 6 |  | Y |
| 39 | `ACCSS_SURCHG3_INCL_FLAG` | Accss_Surchg3_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `CHG_CODE_IINV_SURCHG1` | Chg_Code_Iinvessorial Surchg1 | VARCHAR2 | 6 |  | Y |
| 41 | `CHG_CODE_IINV_SURCHG2` | Chg_Code_Iinvessorial Surchg2 | VARCHAR2 | 6 |  | Y |
| 42 | `IINV_SURCHG2_INCL_FLAG` | Iinv_Surchg2_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `CHG_CODE_IINV_SURCHG3` | Chg_Code_Iinvessorial Surchg3 | VARCHAR2 | 6 |  | Y |
| 44 | `IINV_SURCHG3_INCL_FLAG` | Iinv_Surchg3_Inclessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `CHK_CRT_LMT_FLAG` | Chk_Crt_Lmtessorial Flag | VARCHAR2 | 1 |  | N |
| 46 | `CUST_BILL_PROF_UNQ_LEV_FLAG` | Cust_Bill_Prof_Unq_Levessorial Flag | VARCHAR2 | 1 |  | Y |
| 47 | `ANNIV_MON_INV_FLAG` | Anniv_Mon_Invessorial Flag | VARCHAR2 | 1 |  | Y |
| 48 | `ANNIV_NXT_INV_NUM_DAYS` | Anniv_Nxt_Inv_Numessorial Days | NUMBER | 22 | 3 | Y |
| 49 | `CUST_BILL_PROF_INV_CUR_FLAG` | Cust_Bill_Prof_Inv_Curessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `CUST_BILL_PROF_INV_CUR_LINE` | Cust_Bill_Prof_Inv_Curessorial Line | VARCHAR2 | 1 |  | Y |
| 51 | `CREATE_RENW_INV_ZERO_INVT` | Create_Renw_Inv_Zeroessorial Invt | VARCHAR2 | 1 |  | Y |
| 52 | `CUST_RENW_RES_QTY` | Cust_Renw_Resessorial Qty | NUMBER | 22 | 16 | Y |
| 53 | `CHG_CODE_MIN_TOT_INV` | Chg_Code_Min_Totessorial Inv | VARCHAR2 | 6 |  | Y |
| 54 | `CHG_CODE_RCPT_ACCSS_INV` | Chg_Code_Rcpt_Accssessorial Inv | VARCHAR2 | 6 |  | Y |
| 55 | `CHG_CODE_ORD_ACCSS_INV` | Chg_Code_Ord_Accssessorial Inv | VARCHAR2 | 6 |  | Y |
| 56 | `COST_ENTRY_FLAG` | Cost_Entryessorial Flag | VARCHAR2 | 1 |  | Y |
| 57 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 58 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 59 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 60 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 61 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 62 | `CUST_BILL_PROF_OPID_STOR` | Cust_Bill_Prof_Opidessorial Stor | VARCHAR2 | 1 |  | Y |

## `M_CUST_CARR_CHG`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_FORUL` | Chgessorial Forul | VARCHAR2 | 30 |  | N |

## `M_CUST_CARR_CON_CART`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `CUST_CARR_CON_CART_FORCE_FLAG` | Cust_Carr_Con_Cart_Forceessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CUBE_MAX` | Cubeessorial Max | NUMBER | 22 | 16 | Y |
| 8 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 9 | `WGT_MAX` | Wgtessorial Max | NUMBER | 22 | 16 | Y |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 11 | `OPID_ASSIGN_FLAG` | Opid_Assignessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `ALLOW_PART_PICK_NM` | Allow_Part_Pickessorial Nm | VARCHAR2 | 1 |  | Y |
| 13 | `A1SHIP_INPROGRESS_FLAG` | A1Ship In Progress Flag | VARCHAR2 | 1 |  | Y |
| 14 | `CARTNZ_SORT_RULE_TP` | Cartnz_Sort_Ruleessorial Tp | VARCHAR2 | 1 |  | Y |
| 15 | `CARTNZ_BREAK_BY_ZONE_TP_CODE` | Cartnz_Break_By_Zone_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `RF_PROF_OUTB_PICK_MODE_TP` | Rf_Prof_Outb_Pick_Modeessorial Tp | VARCHAR2 | 1 |  | Y |
| 18 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 19 | `A1SHIP_CURR_DATE_FLAG` | A1Ship Current Date Flag | VARCHAR2 | 1 |  | Y |
| 20 | `PALL_WRAP_NUM_TIME` | Pall_Wrap_Numessorial Time | NUMBER | 22 | 1 | Y |
| 21 | `PALL_WRAP_PALL_PICK_NUM_TIME` | Pall_Wrap_Pall_Pick_Numessorial Time | NUMBER | 22 | 1 | Y |
| 22 | `PALL_REL_HOUR_FROM_SHIP_DATE` | Pall_Rel_Hour_From_Shipessorial Date | NUMBER | 22 | 6 | Y |
| 23 | `CUST_CARR_CON_UCC128_PKG_TP` | Cust_Carr_Con_Ucc128_Pkgessorial Tp | VARCHAR2 | 1 |  | Y |
| 24 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | Y |
| 25 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 26 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 27 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 28 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 29 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 30 | `OPID_MAX_WGT` | Opid_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 31 | `OPID_MAX_WGT_NET` | Opid_Max_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 32 | `OPID_MAX_WGT_MEAS_CODE` | Opid_Max_Wgt_Measessorial Code | VARCHAR2 | 4 |  | Y |
| 33 | `OPID_WGT_ALERT_PCENT` | Opid_Wgt_Alertessorial Pcent | NUMBER | 22 | 3 | Y |
| 34 | `A1SHIP_ADV_FLOW_TP` | A1Ship Advance Flow Type | VARCHAR2 | 1 |  | Y |
| 35 | `A1SHIP_ORD_SHIPMENT_FLAG` | A1Ship Order Shipment Flag | VARCHAR2 | 1 |  | Y |
| 36 | `CARTNZ_ROUT_OVER_TP` | Cartnz_Rout_Overessorial Tp | VARCHAR2 | 4 |  | Y |
| 37 | `RF_PICK_SORT_SEQ_CODE` | Rf_Pick_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |

## `M_CUST_CARR_CON_CART_DOC_MES`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 8 | `DOC_MES_SORT_SEQ` | Doc_Mes_Sortessorial Seq | NUMBER | 22 | 2 | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CARR_CON_CART_SIZE`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CARR_CON_LABEL_SKU`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 6 | `SKU_CLASS_NUM1_LABEL_FLAG` | Sku_Class_Num1_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `SKU_CLASS_NUM2_LABEL_FLAG` | Sku_Class_Num2_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `SKU_CLASS_NUM3_LABEL_FLAG` | Sku_Class_Num3_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `SKU_CLASS_NUM4_LABEL_FLAG` | Sku_Class_Num4_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `SKU_CLASS_NUM5_LABEL_FLAG` | Sku_Class_Num5_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `SKU_CLASS_NUM1_PACKAGE_TP` | Sku_Class_Num1_Packageessorial Tp | NUMBER | 22 | 1 | Y |
| 12 | `SKU_CLASS_NUM2_PACKAGE_TP` | Sku_Class_Num2_Packageessorial Tp | NUMBER | 22 | 1 | Y |
| 13 | `SKU_CLASS_NUM3_PACKAGE_TP` | Sku_Class_Num3_Packageessorial Tp | NUMBER | 22 | 1 | Y |
| 14 | `SKU_CLASS_NUM4_PACKAGE_TP` | Sku_Class_Num4_Packageessorial Tp | NUMBER | 22 | 1 | Y |
| 15 | `SKU_CLASS_NUM5_PACKAGE_TP` | Sku_Class_Num5_Packageessorial Tp | NUMBER | 22 | 1 | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CHG_CONFIG`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 5 | `CHG_QTY` | Charge Quantity | NUMBER | 22 | 16 | N |
| 6 | `FRQ_CODE` | Frqessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `DATE_PROF_CODE` | Date_Professorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `CUST_CHG_CONFIG_START_DATE` | Cust_Chg_Config_Startessorial Date | DATE | 7 |  | N |
| 9 | `CUST_CHG_CONFIG_END_DATE` | Cust_Chg_Config_Endessorial Date | DATE | 7 |  | Y |
| 10 | `CUST_CHG_CONFIG_REM_TEXT` | Cust_Chg_Config_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_COMD_CON_RELATE`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | N |
| 6 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | N |
| 7 | `RGE_DAY_TO_NUM` | Rge_Day_Toessorial Num | NUMBER | 22 | 4 | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_COMD_ITEM_CON_RELATE`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 7 | `COMD_CODE` | Comdessorial Code | VARCHAR2 | 6 |  | Y |
| 8 | `COMD_SUB_CODE` | Comd_Subessorial Code | VARCHAR2 | 2 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CON_ITEM`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | N |
| 7 | `ITEM_QTY_BKD_QTY_PER_LAY` | Item_Qty_Bkd_Qty_Peressorial Lay | NUMBER | 22 | 3 | N |
| 8 | `ITEM_QTY_BKD_QTY_ODD_LAY` | Item_Qty_Bkd_Qty_Oddessorial Lay | NUMBER | 22 | 3 | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CON_OUTB_RULE`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `CUST_CON_SHIP_NEW_INVT_FLAG` | Cust_Con_Ship_New_Invtessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CUST_CON_OPID_MIX_INVT_TP` | Cust_Con_Opid_Mix_Invtessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `CUST_CON_OPID_EXPY_DATE_TP` | Cust_Con_Opid_Expy_Dateessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `OPID_MIN_EXPY_SHELF_DAY` | Opid_Min_Expy_Shelfessorial Day | NUMBER | 22 | 4 | Y |
| 9 | `OPID_MAX_EXPY_SHELF_DAY` | Opid_Max_Expy_Shelfessorial Day | NUMBER | 22 | 4 | Y |
| 10 | `OPID_MIN_MAX_EXPY_SHELF_DAY` | Opid_Min_Max_Expy_Shelfessorial Day | NUMBER | 22 | 4 | Y |
| 11 | `OPID_NUM_DAY_MULT_EXPY_SHELF` | Opid_Num_Day_Mult_Expyessorial Shelf | NUMBER | 22 | 4 | Y |
| 12 | `CUST_CON_ITEM_CONF_FLAG` | Cust_Con_Item_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CUST_CON_UCC128_REQ_FLAG` | Cust_Con_Ucc128_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |
| 15 | `CUST_CON_CLNT_UCC128_FLAG` | Cust_Con_Clnt_Ucc128essorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CUST_CON_RETAIL_READY_FLAG` | Cust_Con_Retail_Readyessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `CUST_CON_UCC128_LABEL_NUM` | Cust_Con_Ucc128_Labelessorial Num | NUMBER | 22 | 2 | Y |
| 18 | `CUST_CON_PRT_CUST_NAME` | Cust_Con_Prt_Custessorial Name | VARCHAR2 | 1 |  | N |
| 19 | `CUST_CON_PRT_INVT_LEVEL` | Cust_Con_Prt_Invtessorial Level | VARCHAR2 | 1 |  | Y |
| 20 | `CUST_CON_OPID_SGL_ORD_FLAG` | Cust_Con_Opid_Sgl_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `CUST_CON_MCP_LABEL_REG_FLAG` | Cust_Con_Mcp_Label_Regessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_CON_SORT_DOC`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 6 | `PICK_METH` | Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 8 | `DOC_INTFACE_FLAG` | Doc_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D1`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_INB_OUTB_FLAG` | Cust_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CUST_LEV_NUM` | Cust_Levessorial Num | NUMBER | 22 | 1 | N |
| 6 | `INVT_TERMGY_CODE` | Invt_Termgyessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D2`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `ALT_CUST_REP_TP_CODE` | Alt_Cust_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ALT_CUST_REP_CODE` | Alt_Cust_Repessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D3`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_PREF_NUM` | Cust_Prefessorial Num | NUMBER | 22 | 1 | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D4`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_CODE_BROK` | Cust_Codeessorial Brok | VARCHAR2 | 10 |  | N |
| 5 | `ALLOW_ALLOC_INVT_FLAG` | Allow_Alloc_Invtessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D5`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `SEL_DOC_CODE` | Sel_Docessorial Code | VARCHAR2 | 6 |  | N |
| 5 | `SEL_DOC_TP_CODE` | Sel_Doc_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 6 | `ACC_TP_CODE` | Acc_Tpessorial Code | VARCHAR2 | 10 |  | N |
| 7 | `FAX_ACC_CODE` | Fax_Accessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `CUST_EFF_DATE` | Cust_Effessorial Date | DATE | 7 |  | N |
| 9 | `FAX_TO_NAME` | Fax_Toessorial Name | VARCHAR2 | 60 |  | N |
| 10 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 250 |  | N |
| 11 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 250 |  | Y |
| 12 | `FAX_TO_COMP_NAME` | Fax_To_Compessorial Name | VARCHAR2 | 30 |  | N |
| 13 | `FAX_FROM_NAME` | Fax_Fromessorial Name | VARCHAR2 | 30 |  | N |
| 14 | `FAX_COMMENT1` | Faxessorial Comment1 | VARCHAR2 | 60 |  | Y |
| 15 | `FAX_COMMENT2` | Faxessorial Comment2 | VARCHAR2 | 60 |  | Y |
| 16 | `FAX_COVER_CODE` | Fax_Coveressorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `FAX_OVERLAY_CODE` | Fax_Overlayessorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `CUST_BAT_FLAG` | Cust_Batessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `FAX_WEEK_DAY` | Fax_Weekessorial Day | VARCHAR2 | 10 |  | N |
| 20 | `FAX_OCCR_TIME` | Fax_Occressorial Time | NUMBER | 22 | 4 | N |
| 21 | `FAX_TIME` | Faxessorial Time | NUMBER | 22 | 4 | N |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_D6`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_CODE_AR_INV` | Cust_Code_Aressorial Inv | VARCHAR2 | 10 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_DAY_ACT`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CUST_DAY_ACT_TP_FLAG` | Cust_Day_Act_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `M_CUST_DEPT`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `DEPT_CODE` | Deptessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `DEPT_NAME` | Deptessorial Name | VARCHAR2 | 30 |  | N |
| 6 | `DEPT_STAT` | Deptessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_DOC_MES`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `FAX_CODE` | Faxessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `FAX_TP` | Faxessorial Tp | VARCHAR2 | 4 |  | N |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 8 | `ALLOW_RF_DISP_MES_FLAG` | Allow_Rf_Disp_Mesessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_FLOW_PROS_MES`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_FRT_PROF_D1`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 5 | `CUST_FRT_AS_CLASS_CODE` | Cust_Frt_As_Classessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CUST_FRT_CLASS_PCENT` | Cust_Frt_Classessorial Pcent | NUMBER | 22 | 6 | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_FRT_PROF_D2`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `FRT_QTY_BK_NUM_BK` | Frt_Qty_Bk_Numessorial Bk | NUMBER | 22 | 2 | N |
| 6 | `CUST_FRT_BK_FACT` | Cust_Frt_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 7 | `CUST_FRT_WGT_VALUE_FACT` | Cust_Frt_Wgt_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `CUST_FRT_AS_VALUE_FACT` | Cust_Frt_As_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 9 | `CUST_FRT_FLAT_FACT` | Cust_Frt_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 10 | `CUST_FRT_DISC_FACT` | Cust_Frt_Discessorial Fact | VARCHAR2 | 240 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_FRT_PROF_D2_TEMP`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 10 |  | N |
| 3 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_QTY_BK_NUM_BK` | Frt_Qty_Bk_Numessorial Bk | NUMBER | 22 | 2 | N |
| 5 | `CUST_FRT_BK_FACT` | Cust_Frt_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 6 | `CUST_FRT_WGT_VAL_FACT` | Cust_Frt_Wgt_Valessorial Fact | VARCHAR2 | 240 |  | N |
| 7 | `CUST_FRT_AS_VAL_FACT` | Cust_Frt_As_Valessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `CUST_FRT_FLAT_FACT` | Cust_Frt_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 9 | `CUST_FRT_DISC_FACT` | Cust_Frt_Discessorial Fact | VARCHAR2 | 240 |  | N |

## `M_CUST_FRT_PROF_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_FRT_PROF_DES` | Cust_Frt_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_FRT_INV_BY_FLAG` | Cust_Frt_Inv_Byessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_FRT_FLAT_AMT` | Cust_Frt_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 8 | `CUST_FRT_SAV_PCENT` | Cust_Frt_Savessorial Pcent | NUMBER | 22 | 6 | Y |
| 9 | `CUST_FRT_FRT_PCENT` | Cust_Frt_Frtessorial Pcent | NUMBER | 22 | 6 | Y |
| 10 | `CUST_FRT_DISC_PCENT` | Cust_Frt_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 11 | `CUST_FRT_PROF_STAT` | Cust_Frt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 67
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | N |
| 5 | `CUST_STAT` | Customer Status | VARCHAR2 | 1 |  | N |
| 6 | `CUST_ADD1` | Custessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `CUST_ADD2` | Custessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `CUST_ADD3` | Custessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `SMAN_CODE` | Smanessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `CUST_TP_FLAG` | Cust_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `GL_MODY_CODE` | Gl_Modyessorial Code | VARCHAR2 | 10 |  | Y |
| 14 | `CUST_CODE_PAY_OFFC` | Cust_Code_Payessorial Offc | VARCHAR2 | 10 |  | N |
| 15 | `CUST_BILL_PROF_CODE` | Cust_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 16 | `CUST_OPS_PROF_CODE` | Cust_Ops_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 18 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CUST_ITEM_PROF_CODE` | Cust_Item_Professorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 21 | `CUST_START_BUS_DATE` | Cust_Start_Busessorial Date | DATE | 7 |  | N |
| 22 | `CUST_LAST_ACT_DATE` | Cust_Last_Actessorial Date | DATE | 7 |  | Y |
| 23 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `FRT_PAY_OFFC_CODE` | Frt_Pay_Offcessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `CUST_UPC_PREX` | Cust_Upcessorial Prex | VARCHAR2 | 6 |  | Y |
| 27 | `CUST_TRF_PROF_CODE` | Cust_Trf_Professorial Code | VARCHAR2 | 4 |  | Y |
| 28 | `CUST_DEF_RCPT_SKU_FLAG` | Cust_Def_Rcpt_Skuessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `CUST_DEF_ORD_SKU_FLAG` | Cust_Def_Ord_Skuessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `CUST_DEF_ADJ_SKU_FLAG` | Cust_Def_Adj_Skuessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `CUST_LAB_CAPT_JOB_LEV_FLAG` | Cust_Lab_Capt_Job_Levessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `CUST_ORD_LEV_RES_NUM` | Cust_Ord_Lev_Resessorial Num | NUMBER | 22 | 1 | Y |
| 33 | `CUST_CNVC_NUM` | Cust_Cnvcessorial Num | NUMBER | 22 | 1 | Y |
| 34 | `CUST_LAB_STD_MODY_NUM` | Cust_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 35 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 36 | `CUST_ADD4` | Custessorial Add4 | VARCHAR2 | 30 |  | Y |
| 37 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 38 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 39 | `ITEM_HIER_PROF_CODE` | Item_Hier_Professorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `GEO_HIER_PROF_CODE` | Geo_Hier_Professorial Code | VARCHAR2 | 4 |  | Y |
| 41 | `RF_PROF_CODE` | Rf_Professorial Code | VARCHAR2 | 4 |  | Y |
| 42 | `CUST_RES_MODE_NUM` | Cust_Res_Modeessorial Num | VARCHAR2 | 1 |  | Y |
| 43 | `CUST_ALLOC_CONSL_TP_CODE` | Cust_Alloc_Consl_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 44 | `CUST_EPC_PARTIT` | Cust_Epcessorial Partit | NUMBER | 22 | 1 | Y |
| 45 | `CUST_EPC_COMP_PREX` | Cust_Epc_Compessorial Prex | NUMBER | 22 | 12 | Y |
| 46 | `CUST_EDI_PARTNER_ID` | Cust_Edi_Partneressorial Id | VARCHAR2 | 10 |  | Y |
| 47 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | Y |
| 48 | `CUST_EAN_UCC_COMP_PREX` | Cust_Ean_Ucc_Compessorial Prex | VARCHAR2 | 20 |  | Y |
| 49 | `CUST_REF_NUM` | Cust_Refessorial Num | VARCHAR2 | 10 |  | Y |
| 50 | `CUST_FX_INTERCHANGE_QUAL` | Cust_Fx_Interchangeessorial Qual | VARCHAR2 | 2 |  | Y |
| 51 | `CUST_FX_INTERCHANGE_ID` | Cust_Fx_Interchangeessorial Id | VARCHAR2 | 15 |  | Y |
| 52 | `CUST_UNIQUE_INVT_LEV_NUM` | Cust_Unique_Invt_Levessorial Num | NUMBER | 22 | 1 | Y |
| 53 | `CUST_ORD_LINE_TP_U_TO_R_FLAG` | Cust_Ord_Line_Tp_U_To_Ressorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |
| 55 | `INV_BY_INVT_LEV` | Inv_By_Invtessorial Lev | NUMBER | 22 | 1 | Y |
| 56 | `CUST_NAME_EXTN` | Cust_Nameessorial Extn | VARCHAR2 | 250 |  | Y |
| 57 | `CUST_ADD1_EXTN` | Cust_Add1essorial Extn | VARCHAR2 | 250 |  | Y |
| 58 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 59 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 60 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 61 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 62 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 63 | `CUST_DATA_SERVICE_ID` | Cust_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 64 | `CUST_EMP_ID_NUM` | Cust_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 65 | `CUST_WAVE_DEALLOC_RULE_TP` | Cust_Wave_Dealloc_Ruleessorial Tp | VARCHAR2 | 1 |  | Y |
| 66 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |
| 67 | `CUST_PRE_RENW_FLAG` | Cust_Pre_Renwessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_CUST_HOLD_REST_UNREST_PAIR`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `HOLD_CODE_REST` | Hold_Codeessorial Rest | VARCHAR2 | 4 |  | N |
| 5 | `HOLD_CODE_UNREST` | Hold_Codeessorial Unrest | VARCHAR2 | 4 |  | N |
| 6 | `HOLD_CODE_EDI_CODE` | Hold_Code_Ediessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INSTALL`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE_SITE` | Cust_Codeessorial Site | VARCHAR2 | 10 |  | N |
| 3 | `SITE_NAME` | Siteessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |

## `M_CUST_INVT_ASS_PROF_D`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `CUST_INVT_ASS_PROF_PREX` | Cust_Invt_Ass_Professorial Prex | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_INVT_ASS_PROF_SUFX` | Cust_Invt_Ass_Professorial Sufx | VARCHAR2 | 10 |  | Y |
| 8 | `CUST_INVT_ASS_PROF_PAD_FLAG` | Cust_Invt_Ass_Prof_Padessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CUST_INVT_ASS_PROF_DATE_FMT` | Cust_Invt_Ass_Prof_Dateessorial Fmt | VARCHAR2 | 20 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_ASS_PROF_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_ASS_PROF_DES` | Cust_Invt_Ass_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_INVT_ASS_PROF_STAT` | Cust_Invt_Ass_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ASS_PARA_OPT_CODE_WHEN` | Ass_Para_Opt_Codeessorial When | VARCHAR2 | 4 |  | N |
| 7 | `CUST_INVT_ASS_PROF_FREQ_CODE` | Cust_Invt_Ass_Prof_Freqessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `CUST_INVT_ASS_PROF_FREQ_NUM` | Cust_Invt_Ass_Prof_Freqessorial Num | NUMBER | 22 | 2 | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 14 | `CUST_INVT_ASS_PROF_SPC_FUN` | Cust_Invt_Ass_Prof_Spcessorial Fun | VARCHAR2 | 30 |  | Y |

## `M_CUST_INVT_PROF_D`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_PROF_LEV_NUM` | Cust_Invt_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `INVT_TERMGY_CODE` | Invt_Termgyessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CUST_INVT_PROF_DES_FLAG` | Cust_Invt_Prof_Desessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CUST_INVT_PROF_SEQ_NUM_FLAG` | Cust_Invt_Prof_Seq_Numessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CUST_INVT_PROF_ASS_FLAG` | Cust_Invt_Prof_Assessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CUST_INVT_PROF_CHG_STOR_FLAG` | Cust_Invt_Prof_Chg_Storessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CHG_CODE_BILL_ENTI` | Chg_Code_Billessorial Enti | VARCHAR2 | 6 |  | Y |
| 11 | `CUST_INVT_ASS_PROF_CODE` | Cust_Invt_Ass_Professorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `CHG_CODE_RENW` | Chg_Codeessorial Renw | VARCHAR2 | 6 |  | Y |
| 13 | `CHG_CODE_STOR` | Chg_Codeessorial Stor | VARCHAR2 | 6 |  | Y |
| 14 | `CHG_CODE_HAND` | Chg_Codeessorial Hand | VARCHAR2 | 6 |  | Y |
| 15 | `CUST_INVT_PROF_SGLTN_FLAG` | Cust_Invt_Prof_Sgltnessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `CUST_INVT_LEV_VER_PROF_CODE` | Cust_Invt_Lev_Ver_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `CUST_INVT_PROF_PEND_CONTI_FLAG` | Cust_Invt_Prof_Pend_Contiessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `CUST_INVT_PROF_ASS_TP_FLAG` | Cust_Invt_Prof_Ass_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CUST_INVT_PROF_VAL_FLAG` | Cust_Invt_Prof_Valessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_PROF_DD`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_PROF_LEV_NUM` | Cust_Invt_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `CUST_INVT_PROF_PARTIT_NUM` | Cust_Invt_Prof_Partitessorial Num | NUMBER | 22 | 2 | N |
| 6 | `CUST_INVT_PROF_PARTIT_LEN` | Cust_Invt_Prof_Partitessorial Len | NUMBER | 22 | 2 | N |
| 7 | `CUST_INVT_PROF_PARTIT_VAL_CHAR` | Cust_Invt_Prof_Partit_Valessorial Char | VARCHAR2 | 45 |  | N |
| 8 | `CUST_INVT_PROF_EXACT_LEN_FLAG` | Cust_Invt_Prof_Exact_Lenessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_PROF_DDD`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_PROF_LEV_NUM` | Cust_Invt_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `CUST_INVT_PROF_PARTIT_NUM` | Cust_Invt_Prof_Partitessorial Num | NUMBER | 22 | 2 | N |
| 6 | `CUST_INVT_PROF_PARTIT_LEN` | Cust_Invt_Prof_Partitessorial Len | NUMBER | 22 | 2 | N |
| 7 | `CUST_INVT_PROF_PARTIT_VAL_CHAR` | Cust_Invt_Prof_Partit_Valessorial Char | VARCHAR2 | 45 |  | N |
| 8 | `CUST_INVT_PROF_EXACT_LEN_FLAG` | Cust_Invt_Prof_Exact_Lenessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_PROF_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_PROF_DES` | Cust_Invt_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_INVT_PROF_STAT` | Cust_Invt_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_STAT_PROS_CFG_EDI`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 7 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | N |
| 8 | `HOLD_CODE_REST` | Hold_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 9 | `HOLD_CODE_UNREST` | Hold_Codeessorial Unrest | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INVT_STAT_PROS_CONFIG`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `HOLD_CODE_REST_ALLOW_SHIP` | Hold_Code_Rest_Allowessorial Ship | VARCHAR2 | 1 |  | N |
| 5 | `HOLD_CODE_ADJ_FLAG` | Hold_Code_Adjessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ADJ_HOLD_CODE` | Adj_Holdessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `ADJ_HOLD_CODE_REST` | Adj_Hold_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 8 | `ADJ_HOLD_CODE_UNREST` | Adj_Hold_Codeessorial Unrest | VARCHAR2 | 4 |  | Y |
| 9 | `ADJ_HOLD_NON_EDI_RCPT` | Adj_Hold_Non_Ediessorial Rcpt | VARCHAR2 | 4 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_INV_REG_D`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INV_REG_RECAP_NUM` | Inv_Reg_Recapessorial Num | NUMBER | 22 | 1 | N |
| 4 | `INV_BKD_CODE` | Inv_Bkdessorial Code | VARCHAR2 | 4 |  | N |

## `M_CUST_INV_REG_H`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INV_REG_RECAP_NUM` | Inv_Reg_Recapessorial Num | NUMBER | 22 | 1 | N |

## `M_CUST_ITEM_PROF`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_ITEM_PROF_CODE` | Cust_Item_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_ITEM_PROF_DES` | Cust_Item_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_ITEM_PROF_STAT` | Cust_Item_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUST_ITEM_PROF_TRACK_COST_FLAG` | Cust_Item_Prof_Track_Costessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CUST_ITEM_PROF_NUM_COST_BUK` | Cust_Item_Prof_Num_Costessorial Buk | NUMBER | 22 | 2 | Y |
| 8 | `CUST_ITEM_PROF_MNT_PRI_FLAG` | Cust_Item_Prof_Mnt_Priessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 10 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_LOAD_TP_CHG`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INB_OUTB_FLAG` | Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_OPS_PROF`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_OPS_PROF_CODE` | Cust_Ops_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_OPS_PROF_DES` | Cust_Ops_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_OPS_PROF_STAT` | Cust_Ops_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUST_OPS_PROF_INTRA_RCPT_FLAG` | Cust_Ops_Prof_Intra_Rcptessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CUST_OPS_PROF_COMPL_ORD_FLAG` | Cust_Ops_Prof_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CUST_OPS_PROF_PO_ORD_REQ_FLAG` | Cust_Ops_Prof_Po_Ord_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | N |
| 10 | `CUST_OPS_PROF_PEND_ZERO_FLAG` | Cust_Ops_Prof_Pend_Zeroessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `CUST_OPS_PROF_BORD_FLAG` | Cust_Ops_Prof_Bordessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `WHSE_REST_CODE` | Warehouse Rest Code | VARCHAR2 | 1 |  | Y |
| 13 | `PUT_PROF_CODE` | Put_Professorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `CUST_OPS_PROF_ORD_STATS_FLAG` | Cust_Ops_Prof_Ord_Statsessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `CUST_OPS_PROF_BORD_ALLOC_FLAG` | Cust_Ops_Prof_Bord_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `CUST_OPS_PROF_OPT_REPI_FLAG` | Cust_Ops_Prof_Opt_Repiessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `CUST_OPS_PROF_VQB_SKU_ALLO_TP` | Cust_Ops_Prof_Vqb_Sku_Alloessorial Tp | VARCHAR2 | 1 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_PARCEL_SCAC_ACC`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `SCAC_CODE` | Scacessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ACC_NUM` | Accessorial Num | VARCHAR2 | 20 |  | N |
| 6 | `ACC_PICKUP_SEQ_NUM_START` | Acc_Pickup_Seq_Numessorial Start | NUMBER | 22 | 9 | Y |
| 7 | `ACC_PICKUP_SEQ_NUM_END` | Acc_Pickup_Seq_Numessorial End | NUMBER | 22 | 9 | Y |
| 8 | `ACC_PICKUP_SEQ_NUM_CRNT` | Acc_Pickup_Seq_Numessorial Crnt | NUMBER | 22 | 9 | Y |
| 9 | `CUST_PARCEL_SCAC_ACC_PREX` | Cust_Parcel_Scac_Accessorial Prex | VARCHAR2 | 10 |  | Y |
| 10 | `CUST_PARCEL_SCAC_ACC_SUFX` | Cust_Parcel_Scac_Accessorial Sufx | VARCHAR2 | 10 |  | Y |
| 11 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_PROS_CHG`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INB_OUTB_FLAG` | Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CHG_FORUL` | Chgessorial Forul | VARCHAR2 | 30 |  | N |

## `M_CUST_REPS`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_REPS_CODE` | Cust_Repsessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_REPS_NAME` | Cust_Repsessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `CUST_REPS_STAT` | Cust_Repsessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CUST_RF_MES`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `FAX_CODE` | Faxessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `FAX_TP` | Faxessorial Tp | VARCHAR2 | 4 |  | N |
| 5 | `RF_ACT_NUM` | Rf_Actessorial Num | NUMBER | 22 | 2 | N |
| 6 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | N |

## `M_CUST_TRF_PROF`

- **Tipo:** Master
- **Categoria:** Customer
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_TRF_PROF_CODE` | Cust_Trf_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_TRF_PROF_DES` | Cust_Trf_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CUST_TRF_PROF_STAT` | Cust_Trf_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUST_TRF_PROF_RCPT_CHG_FLAG` | Cust_Trf_Prof_Rcpt_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CUST_TRF_PROF_RENW_TP_FLAG` | Cust_Trf_Prof_Renw_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 10 | `CUST_TRF_PROF_FREE_STOR_FLAG` | Cust_Trf_Prof_Free_Storessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `CUST_TRF_PROF_FREE_DAYS` | Cust_Trf_Prof_Freeessorial Days | NUMBER | 22 | 4 | Y |
| 12 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 13 | `CUST_TRF_PROF_CHG_TP_FLAG` | Cust_Trf_Prof_Chg_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `X_CUST_FRT_PROF_D1`

- **Tipo:** Misc
- **Categoria:** Customer
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 10 |  | N |
| 3 | `CLASS_CODE` | Class Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_FRT_AS_CLASS_CODE` | Cust_Frt_As_Classessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CUST_FRT_CLASS_PCENT` | Cust_Frt_Classessorial Pcent | NUMBER | 22 | 6 | Y |

## `X_CUST_FRT_PROF_D2`

- **Tipo:** Misc
- **Categoria:** Customer
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 10 |  | N |
| 3 | `FRT_QTY_BK_CODE` | Frt_Qty_Bkessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `FRT_QTY_BK_NUM_BK` | Frt_Qty_Bk_Numessorial Bk | NUMBER | 22 | 2 | N |
| 5 | `CUST_FRT_BK_FACT` | Cust_Frt_Bkessorial Fact | VARCHAR2 | 60 |  | N |
| 6 | `CUST_FRT_WGT_VALUE_FACT` | Cust_Frt_Wgt_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 7 | `CUST_FRT_AS_VALUE_FACT` | Cust_Frt_As_Valueessorial Fact | VARCHAR2 | 240 |  | N |
| 8 | `CUST_FRT_FLAT_FACT` | Cust_Frt_Flatessorial Fact | VARCHAR2 | 240 |  | N |
| 9 | `CUST_FRT_DISC_FACT` | Cust_Frt_Discessorial Fact | VARCHAR2 | 240 |  | N |

## `X_CUST_FRT_PROF_H`

- **Tipo:** Misc
- **Categoria:** Customer
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_FRT_PROF_CODE` | Cust_Frt_Professorial Code | VARCHAR2 | 10 |  | N |
| 3 | `CUST_FRT_PROF_DES` | Cust_Frt_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `CUST_FRT_INV_BY_FLAG` | Cust_Frt_Inv_Byessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 6 | `CUST_FRT_FLAT_AMT` | Cust_Frt_Flatessorial Amt | NUMBER | 22 | 9 | Y |
| 7 | `CUST_FRT_SAV_PCENT` | Cust_Frt_Savessorial Pcent | NUMBER | 22 | 6 | Y |
| 8 | `CUST_FRT_FRT_PCENT` | Cust_Frt_Frtessorial Pcent | NUMBER | 22 | 6 | Y |
| 9 | `CUST_FRT_DISC_PCENT` | Cust_Frt_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 10 | `CUST_FRT_PROF_STAT` | Cust_Frt_Professorial Stat | VARCHAR2 | 1 |  | N |

