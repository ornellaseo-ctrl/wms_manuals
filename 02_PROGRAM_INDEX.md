# Índice de Programas / Menus — Körber / AccellosOne Enterprise 3PL

> Gerado a partir da segunda aba da planilha. Útil para relacionar código de programa, descrição, subsistema, executável e menu.

- Total de registros: **788**

| Código | Descrição | Subsistema | Seq. | Job/Executável | Form | Menu | Report | Help |
|---|---|---|---:|---|---|---|---|---|
| `MOHO` | Move Hold to Hold | ADPR | 250 | `ad_133` |  | MAIN |  | 30 |
| `BILL` | Billing (Invoicing) | WO | 60 | `` |  | MAIN |  |  |
| `ACIN` | Accessorial Invoicing | BILL | 10 | `iv_102` |  | MAIN |  |  |
| `REIN` | Renewal Invoicing | BILL | 20 | `iv_103` |  | MAIN |  |  |
| `IMIN` | Immediate Invoice Invoicing | BILL | 30 | `iv_105` |  | MAIN |  |  |
| `EXIN` | Extra Charge Invoicing | BILL | 40 | `iv_108` |  | MAIN |  |  |
| `DLRE` | Daily Invoice Register | BILL | 50 | `iv_109` |  | MAIN |  |  |
| `ENAC` | Bill Later - Enter Charges | BILL | 60 | `iv_101` |  | MAIN |  | 10 |
| `ENIN` | Bill Immediate - Enter Charges | BILL | 70 | `iv_104` |  | MAIN |  | 10 |
| `ACAU` | Accessorial Authorization | BILL | 80 | `iv_106` |  | MAIN |  | 10 |
| `RENW` | Renewal Recalculations | BILL | 90 | `rp_118` |  | MAIN |  | 10 |
| `BILB` | Billing Batch | BILL | 100 | `scr_040` |  | MAIN |  | 10 |
| `CTIN` | Cost Tracking in Invoice | BILL | 110 | `iv_114` |  | MAIN |  | 10 |
| `RECE` | Receiving | WO | 70 | `` |  | MAIN |  |  |
| `LORE` | Look Up Receipts | RECE | 20 | `iq_101` |  | MAIN |  | 30 |
| `PRRE` | Print Receiving Documents - All | RECE | 30 | `pr_101` |  | MAIN |  | 30 |
| `RERE` | Requeue Receipt Documents | RECE | 40 | `pr_103` |  | MAIN |  | 30 |
| `REPE` | Entry of Receipt Process Values | RECE | 50 | `rp_119` |  | MAIN |  | 35 |
| `ENRE` | Enter, Modify and Delete Receipts | RECE | 60 | `rp_101` |  | MAIN |  | 30 |
| `PRRM` | Print Receiving Documents - Specific | RECE | 70 | `pr_106` |  | MAIN |  | 30 |
| `CORL` | Confirm Receipts - Line at a Time | RECE | 80 | `rp_105` |  | MAIN |  | 30 |
| `CHRF` | Time Stamp and Confirm Receipts | RECE | 90 | `rp_106` |  | MAIN |  | 30 |
| `RERA` | Requeue Receipt for Rating | RECE | 100 | `rp_107` |  | MAIN |  | 30 |
| `RCRA` | Receipt Rater | RECE | 110 | `rp_117` |  | MAIN |  | 30 |
| `LOPR` | Look Up Pending Receipts | RECE | 120 | `iq_112` |  | MAIN |  | 30 |
| `REXC` | Enter Receipt Extra Charges | RECE | 130 | `rp_123` |  | MAIN |  | 10 |
| `CICP` | Check-In Configuration Parameters | RECE | 140 | `im_716` |  | MAIN |  | 30 |
| `RCIR` | Receipt Check-In Report | RECE | 150 | `qd_242` | 811 | MAIN |  | 25 |
| `RCIS` | Receipt Check-In at Staging | RECE | 170 | `iq_224` | 811 | MAIN |  | 30 |
| `RECH` | Receipt Charges | RECE | 180 | `iv_111` |  | MAIN |  | 10 |
| `ORDE` | Orders (Shipping) | WO | 80 | `` |  | MAIN |  |  |
| `ENOR` | Enter, Modify and Delete Order(s) | ORDE | 10 | `op_101` |  | MAIN |  | 30 |
| `REOR` | Requeue Order Documents | ORDE | 20 | `pr_104` |  | MAIN |  | 30 |
| `ORPE` | Entry of Order Process Values | ORDE | 30 | `op_119` |  | MAIN |  | 35 |
| `PROR` | Print Shipping Documents - All | ORDE | 40 | `pr_102` |  | MAIN |  | 30 |
| `PROM` | Print Shipping Documents - Specific | ORDE | 50 | `pr_105` |  | MAIN |  | 30 |
| `COOL` | Confirm Orders - Line at a Time | ORDE | 60 | `op_105` |  | MAIN |  | 30 |
| `CHOF` | Time Stamp and Confirm Order(s) | ORDE | 70 | `op_106` |  | MAIN |  | 30 |
| `RERO` | Requeue a Range of Orders | ORDE | 80 | `op_144` |  | MAIN |  | 30 |
| `LOOR` | Look Up Orders | ORDE | 90 | `iq_102` |  | MAIN |  | 30 |
| `GEBA` | Generate Batch Order | ORDE | 100 | `op_127` |  | MAIN |  | 35 |
| `POBA` | Post Batch Order to Consolidated Orders | ORDE | 110 | `op_128a` |  | MAIN |  | 35 |
| `COCB` | Clear Order from Closed Batch | ORDE | 130 | `op_155` |  | MAIN |  | 35 |
| `UOCP` | Update Order Carrier/Pallet | ORDE | 140 | `op_183` |  | MAIN |  | 35 |
| `EPSD` | Enter Packing Details | ORDE | 150 | `op_193` |  | MAIN |  | 45 |
| `DOWA` | Deallocate Orders by Wave | ORDE | 160 | `op_194` |  | MAIN |  | 05 |
| `MAOE` | Manual Order Entry | ORDE | 170 | `op_195` |  | MAIN |  | 30 |
| `RPPL` | Reprocess/Print Packing Labels | ORDE | 180 | `op_196` |  | MAIN |  | 35 |
| `ORCH` | Order Charges | ORDE | 190 | `iv_112` |  | MAIN |  | 10 |
| `ORSP` | Order Special Functions | ORDE | 240 | `` |  | MAIN |  |  |
| `CHAT` | Change Auto Transfer Order to Regular | ORSP | 20 | `op_107` |  | MAIN |  | 30 |
| `POD` | Proof of Delivery | ORSP | 30 | `op_141` |  | MAIN |  | 30 |
| `ASOR` | Assign Locations to Orders | ORSP | 40 | `op_102` |  | MAIN |  | 05 |
| `REPI` | Relocate to Pick Line | ORSP | 50 | `ad_105` |  | MAIN |  | 05 |
| `COPI` | Consolidated Pick | ORSP | 60 | `op_109` |  | MAIN |  | 35 |
| `DEOR` | De-Allocate Order | ORSP | 70 | `op_131` |  | MAIN |  | 05 |
| `ENOP` | Order Packing Entry Screen | ORSP | 80 | `op_138` |  | MAIN |  | 35 |
| `ENPA` | Enter Packing Details | ORSP | 100 | `op_153` |  | MAIN |  | 35 |
| `OEXC` | Add Access. Charge to Order | ORSP | 110 | `op_123` |  | MAIN |  | 10 |
| `ORVE` | Order Verification Total Unit | ORSP | 120 | `op_114` |  | MAIN |  |  |
| `SELO` | Set Up Load | ORSP | 130 | `scr_005` | 811 | MAIN |  | 35 |
| `CCOP` | Customer/Consignee Override of PIPR | ORSP | 150 | `scr_021` |  | MAIN |  | 05 |
| `WAPC` | Warehouse Attribute Profile Code | ORSP | 160 | `im_708` |  | MAIN |  | 35 |
| `LOOP` | Look Up Carton Information | ORSP | 170 | `iq_115` |  | MAIN |  | 35 |
| `LOLD` | Look Up Load Details | ORSP | 180 | `iq_210` |  | MAIN |  | 35 |
| `MAOP` | Setup of Order Packing | ORSP | 190 | `im_347` |  | MAIN |  | 35 |
| `PKST` | Packing Station Code | ORSP | 200 | `im_364` |  | MAIN |  | 35 |
| `ENPX` | Packing Exception Report | ORSP | 210 | `re_146` | 811 | MAIN |  | 25 |
| `VBOL` | VICS Bill of Lading | ORSP | 220 | `im_384` | 811 | MAIN |  | 30 |
| `HISR` | Hazardous Inventory Stock Report | ORSP | 230 | `qd_253` | 811 | MAIN |  | 25 |
| `QR` | Quick Response | ORSP | 260 | `` |  | MAIN |  |  |
| `QURE` | Quick Response Setup | QR | 10 | `im_310` |  | MAIN |  | 35 |
| `QRLE` | Quick Response Label Entry | QR | 20 | `op_110` |  | MAIN |  | 35 |
| `QRLR` | Quick Response Label Reprint | QR | 30 | `op_133` |  | MAIN |  | 35 |
| `4PL` | 4PL | WO | 90 | `` |  | MAIN |  |  |
| `IERR` | Error Look Up | 4PL | 10 | `iq_122` |  | MAIN |  |  |
| `UPCR` | Cross Reference Set Up | 4PL | 20 | `im_504` |  | MAIN |  |  |
| `IMES` | Message Look Up | 4PL | 30 | `im_503` |  | MAIN |  |  |
| `INMENU` | Interface Menu | 4PL | 40 | `l_hc_101` |  | MAIN |  |  |
| `PHIN` | Physical Inventory | WO | 100 | `` |  | MAIN |  |  |
| `ENPH` | Enter Physical Parameters | PHIN | 10 | `pi_110` |  | MAIN |  | 40 |
| `PHTI` | Create Physical Inventory Tickets | PHIN | 20 | `pi_101` |  | MAIN |  | 40 |
| `ENTI` | Enter Tickets/Count Sheets | PHIN | 30 | `pi_102` |  | MAIN |  | 40 |
| `PPIT` | Print Physical Inventory Tickets | PHIN | 40 | `pi_111` | 811 | MAIN |  | 40 |
| `PHUP` | Physical to Inventory Update | PHIN | 50 | `pi_105` |  | MAIN |  | 40 |
| `TIDE` | Ticket Discrepancy Report - A Vs. B | PHIN | 60 | `pi_103` | 811 | MAIN |  | 40 |
| `PHTL` | Physical Tickets by Customer by Ticket | PHIN | 70 | `pi_107` | 811 | MAIN |  | 40 |
| `PIAR` | Physical Inventory Adjustment Report | PHIN | 80 | `pi_112` | 811 | MAIN |  | 40 |
| `PHRE` | Physical Inventory Ticket Report | PHIN | 90 | `pi_106` | 811 | MAIN |  | 40 |
| `BOOK` | Physical versus Book Report | PHIN | 100 | `pi_104` | 811 | MAIN |  | 40 |
| `BKDT` | Detail Book Report | PHIN | 110 | `pi_117` | 811 | MAIN |  | 40 |
| `APPO` | Appointment System | WO | 110 | `` |  | MAIN |  |  |
| `BLDG` | Building | APPO | 10 | `im_315` |  | MAIN |  | 35 |
| `DOOR` | Door | APPO | 20 | `im_314` |  | MAIN |  | 35 |
| `APPL` | Appointment Planner | APPO | 30 | `as_150` |  | MAIN |  | 35 |
| `SAPR` | Scheduled Appointment Report | APPO | 40 | `re_123` | 811 | MAIN |  | 25 |
| `SAIR` | Scheduled Appointment Item Report | APPO | 50 | `re_166` | 811 | MAIN |  | 25 |
| `PACO` | Pallet Control System | WO | 120 | `` |  | MAIN |  |  |
| `ADPC` | Adjust Pallet Control | PACO | 10 | `ad_109` |  | MAIN |  | 35 |
| `LOPC` | Look Up Pallet Control | PACO | 20 | `iq_109` |  | MAIN |  | 35 |
| `IB` | In Bond Operations | WO | 130 | `` |  | MAIN |  |  |
| `CUBR` | Custom Broker (Bonds) | IB | 10 | `im_323` |  | MAIN |  | 35 |
| `BOND` | Bond Setup | IB | 20 | `ad_123` |  | MAIN |  | 35 |
| `BORL` | Bond Release Adjustment | IB | 30 | `ad_124` |  | MAIN |  | 35 |
| `LOBO` | Look Up Bonds | IB | 40 | `iq_111` |  | MAIN |  | 35 |
| `OPBO` | Open Bond Report | IB | 50 | `re_160` | 811 | MAIN |  | 25 |
| `CLBO` | Closed Bond Report | IB | 60 | `re_161` | 811 | MAIN |  | 25 |
| `REBO` | Released Bond Report | IB | 70 | `re_162` | 811 | MAIN |  | 25 |
| `BOAC` | 300 (Bond Activity) Report | IB | 80 | `re_164` | 811 | MAIN |  | 25 |
| `CYCL` | Cycle Count Operations | WO | 140 | `` |  | MAIN |  |  |
| `CYCP` | Cycle Count Profile | CYCL | 10 | `cy_101` |  | MAIN |  | 20 |
| `CYEN` | Create Cycle Count | CYCL | 20 | `cy_102` |  | MAIN |  | 20 |
| `CYGT` | Generate Cycle Count Tickets | CYCL | 30 | `cy_103` |  | MAIN |  | 20 |
| `CYTI` | Print Cycle Count Tickets | CYCL | 40 | `cy_112` | 811 | MAIN |  | 20 |
| `CYET` | Enter Cycle Count Tickets | CYCL | 50 | `cy_104` |  | MAIN |  | 20 |
| `CYFO` | Force Cycle Count Balance | CYCL | 60 | `cy_107` |  | MAIN |  | 20 |
| `CYCO` | Close Cycle Count | CYCL | 70 | `cy_105` |  | MAIN |  | 20 |
| `CYCC` | Cancel Cycle Count | CYCL | 80 | `cy_106` |  | MAIN |  | 20 |
| `CYDE` | Delete Cycle Count | CYCL | 90 | `cy_114` |  | MAIN |  | 20 |
| `ADNC` | Adjust Number of Cycle Counts | CYCL | 100 | `ad_128` |  | MAIN |  | 20 |
| `CYBK` | Cycle Count Book Report | CYCL | 110 | `cy_108` | 811 | MAIN |  | 20 |
| `CYPC` | Cycle Count Profile Code Report | CYCL | 120 | `cy_113` | 811 | MAIN |  | 20 |
| `CYTL` | Cycle Count Ticket List | CYCL | 130 | `cy_111` | 811 | MAIN |  | 20 |
| `CYTR` | Cycle Count Ticket Report | CYCL | 140 | `cy_110` | 811 | MAIN |  | 20 |
| `CYAB` | Cycle Count Ticket Discrepancy Report | CYCL | 150 | `cy_109` | 811 | MAIN |  | 20 |
| `PCLR` | Pre-Cycle Count Location Report | CYCL | 160 | `cy_118` | 811 | MAIN |  | 20 |
| `CYSR` | Cycle Count Summary Report | CYCL | 170 | `cy_121` | 811 | MAIN |  |  |
| `CYCD` | Closed Cycle Count Detail Report | CYCL | 180 | `re_130` | 811 | MAIN |  | 20 |
| `CYUP` | Cycle Count Update Inventory | CYCL | 200 | `scr_070` |  | MAIN |  | 20 |
| `LAB` | Labels | WO | 150 | `` |  | MAIN |  |  |
| `RELA` | Reprint Labels | LAB | 10 | `rp_116` |  | MAIN |  | 30 |
| `TASK` | Task Related | WO | 160 | `` |  | MAIN |  |  |
| `VOPR` | Voice Profile (Task Profile) | TASK | 10 | `scr_033` |  | MAIN |  | 45 |
| `VOPC` | Voice Profile (Customer) | TASK | 20 | `scr_033` |  | MAIN |  | 45 |
| `REGI` | Task Profile | TASK | 30 | `scr_030` |  | MAIN |  | 45 |
| `RFOP` | RF Operator | TASK | 40 | `scr_032` |  | MAIN |  | 45 |
| `RFOT` | RF Operator Task Assign | TASK | 50 | `scr_031` |  | MAIN |  | 45 |
| `CTPA` | Clear Terminal Pick Assignments | TASK | 60 | `iq_125` |  | MAIN |  | 45 |
| `SU` | Set Up All Codes | MAIN | 40 | `` |  | MAIN |  |  |
| `FINR` | Financial Related Jobs | SU | 10 | `` |  | MAIN |  |  |
| `TERM` | Billing Terms | FINR | 10 | `im_104` |  | MAIN |  | 50 |
| `CURR` | Currency | FINR | 20 | `im_108` |  | MAIN |  | 50 |
| `CURX` | Currency Exchange Rate | FINR | 30 | `im_108a` |  | MAIN |  |  |
| `GLCH` | G.L. Chart of Accounts | FINR | 40 | `im_116` |  | MAIN |  | 50 |
| `GLMO` | G/L Modifier Code | FINR | 50 | `im_195` |  | MAIN |  | 50 |
| `BANK` | Bank Code | FINR | 60 | `im_107` |  | MAIN |  | 10 |
| `CURE` | Customer Related | SU | 20 | `` |  | MAIN |  |  |
| `CUST` | Customer Codes | CURE | 10 | `im_106` |  | MAIN |  | 50 |
| `CUSE` | Customer Service Representative(s) | CURE | 20 | `im_140` |  | MAIN |  | 50 |
| `CPSA` | Customer Parcel SCAC Account | CURE | 30 | `scr_065` |  | MAIN |  | 10 |
| `SAPE` | Salesperson(s) | CURE | 40 | `im_105` |  | MAIN |  | 50 |
| `CUDE` | Customer Department | CURE | 50 | `im_387` |  | MAIN |  | 10 |
| `DEPR` | Depositor Profiles | CURE | 70 | `` |  | MAIN |  |  |
| `DITP` | Depositor Item Profile | DEPR | 10 | `im_171` |  | MAIN |  | 50 |
| `DSRP` | Depositor Shipping and Receiving | DEPR | 20 | `im_168` |  | MAIN |  | 50 |
| `DBIP` | Depositor Billing Profile | DEPR | 30 | `im_169` |  | MAIN |  | 50 |
| `DILP` | Depositor Inventory Level Profile | DEPR | 40 | `im_161` |  | MAIN |  | 50 |
| `DIFP` | Depositor Workflow Profile | DEPR | 50 | `im_156` |  | MAIN |  | 50 |
| `DIAP` | Depositor Inventory Assign Profile(s) | DEPR | 60 | `im_120` |  | MAIN |  | 50 |
| `DLVP` | Depositor Level Validation Profile | DEPR | 70 | `im_330` |  | MAIN |  | 50 |
| `PIPR` | Picking Profile | DEPR | 80 | `im_325` |  | MAIN |  | 05 |
| `PUPR` | Put-Away Profile Code | DEPR | 90 | `im_361` |  | MAIN |  | 05 |
| `DEAS` | Depositor Alternate Sort(s) | DEPR | 100 | `im_145` |  | MAIN |  | 50 |
| `DAPR` | Date Profile(s) | DEPR | 110 | `im_187` |  | MAIN |  | 50 |
| `DEME` | Depositor Message(s) | DEPR | 120 | `im_128` |  | MAIN |  | 50 |
| `TRPR` | Transfer Profile | DEPR | 130 | `im_117` |  | MAIN |  | 30 |
| `DPME` | Depositor Print Messages | DEPR | 140 | `im_311` |  | MAIN |  | 50 |
| `CHRE` | Charge Related | SU | 30 | `` |  | MAIN |  |  |
| `RATE` | Depositor Billing Rates | CHRE | 10 | `im_189` |  | MAIN |  | 50 |
| `CHAR` | Charge Code | CHRE | 20 | `im_188` |  | MAIN |  | 50 |
| `DECH` | Density Charge Code(s) | CHRE | 30 | `im_114` |  | MAIN |  | 10 |
| `IDRA` | Increase/Decrease Rates | CHRE | 40 | `im_172` |  | MAIN |  | 10 |
| `RADS` | Rate Description | CHRE | 50 | `im_318` |  | MAIN |  | 25 |
| `GEXC` | General Extra Charges | CHRE | 60 | `im_344` |  | MAIN |  | 10 |
| `DELO` | Depositor Load Type Charges | CHRE | 70 | `im_173` |  | MAIN |  | 10 |
| `ECHP` | Extra Charge Profile | CHRE | 80 | `im_346` |  | MAIN |  | 10 |
| `DPRO` | Discount Profile | CHRE | 90 | `im_313` |  | MAIN |  | 10 |
| `ACCA` | Accessorial Charge Changes Report | CHRE | 100 | `iv_107` | 811 | MAIN |  | 10 |
| `ACAL` | Look Up Changes to Accss. Charges | CHRE | 110 | `iq_124` |  | MAIN |  | 10 |
| `PACA` | Purge Changes to Accss. Charges | CHRE | 120 | `im_707` |  | MAIN |  | 10 |
| `CHGR` | Charge Group | CHRE | 130 | `scr_075` |  | MAIN |  | 10 |
| `BTCS` | Bill To Customer Subscription | CHRE | 140 | `scr_076` |  | MAIN |  | 10 |
| `ITRE` | Item Related | SU | 40 | `` |  | MAIN |  |  |
| `VAIN` | Value Index | ITRE | 10 | `im_348` |  | MAIN |  |  |
| `COMM` | Commodities | ITRE | 20 | `im_134` |  | MAIN |  | 50 |
| `HAZA` | Hazardous Material Messages | ITRE | 30 | `im_138` |  | MAIN |  | 50 |
| `CLAS` | Freight Class Codes | ITRE | 40 | `im_112` |  | MAIN |  | 50 |
| `ALIT` | Alternate Item and Language | ITRE | 50 | `im_360` |  | MAIN |  | 50 |
| `IIHO` | Item Incubation Hold Code | ITRE | 60 | `im_338` |  | MAIN |  | 50 |
| `CTSZ` | Carton Size Setup | ITRE | 80 | `scr_068` |  | MAIN |  | 10 |
| `IHZV` | Item Hazardous Material Validation | ITRE | 90 | `im_321` |  | MAIN |  | 45 |
| `IMAS` | Item Value Mass Update | ITRE | 100 | `im_166m` |  | MAIN |  | 55 |
| `CCCC` | Outbound Process Configuration | ITRE | 110 | `scr_074` |  | MAIN |  | 45 |
| `ICNP` | Item Cartonization Profile Code | ITRE | 120 | `im_198` |  | MAIN |  | 45 |
| `IPBR` | Item Pallet Build Restrictions | ITRE | 130 | `im_385` |  | MAIN |  | 45 |
| `IAPR` | Inventory Attributes Profile | ITRE | 140 | `im_386` |  | MAIN |  | 35 |
| `ITPR` | Item Profiles | ITRE | 170 | `` |  | MAIN |  |  |
| `ITSH` | Item Shipping Profile | ITPR | 10 | `im_155` |  | MAIN |  | 50 |
| `IHAP` | Item Handling Profile | ITPR | 20 | `im_179` |  | MAIN |  | 50 |
| `IRSP` | Item Renewal Storage Profile | ITPR | 30 | `im_178` |  | MAIN |  | 50 |
| `IISP` | Item Initial Storage Profile | ITPR | 40 | `im_176` |  | MAIN |  | 50 |
| `IXDP` | Item X-Dock Profile | ITPR | 50 | `im_180` |  | MAIN |  | 10 |
| `IBIP` | Item Billing Profile | ITPR | 60 | `im_184` |  | MAIN |  | 50 |
| `IINP` | General Item Information Profile | ITPR | 70 | `im_185` |  | MAIN |  | 50 |
| `IPRP` | Item Process Profile | ITPR | 80 | `im_183` |  | MAIN |  | 35 |
| `IQBP` | Item Quantity Breakdown Profile | ITPR | 90 | `im_162` |  | MAIN |  | 50 |
| `ILOP` | Item Location Profile | ITPR | 100 | `im_194` |  | MAIN |  | 05 |
| `ITAP` | Item Tare Profile | ITPR | 110 | `im_115` |  | MAIN |  | 50 |
| `IPRO` | Item Process(es) | ITPR | 120 | `im_165` |  | MAIN |  | 35 |
| `ITVP` | Item Value Profile | ITPR | 130 | `im_366` |  | MAIN |  |  |
| `ITEM` | Item Code(s) | ITPR | 140 | `im_166` |  | MAIN |  | 50 |
| `ITAS` | Item Alternate Sort(s) | ITPR | 150 | `im_144` |  | MAIN |  | 50 |
| `IHOP` | Item Hold Profile | ITPR | 160 | `im_333` |  | MAIN |  | 50 |
| `IMSL` | Item Minimum Shipping Level | ITPR | 170 | `im_335` |  | MAIN |  | 05 |
| `IRHP` | Item Receipt Hold Profile | ITPR | 180 | `im_362` |  | MAIN |  | 05 |
| `ALTP` | Alternate Type | ITPR | 190 | `im_367` |  | MAIN |  | 50 |
| `MIRP` | Item RF Profile | ITPR | 200 | `scr_033` |  | MAIN |  | 45 |
| `WARR` | Warehouse Related | SU | 50 | `` |  | MAIN |  |  |
| `WALO` | Warehouse(s) and Location(s) | WARR | 10 | `` |  | MAIN |  |  |
| `LOCA` | Location(s) | WALO | 10 | `im_153` |  | MAIN |  | 50 |
| `ISOL` | Isolator(s) | WALO | 20 | `im_149` |  | MAIN |  | 50 |
| `WARE` | Warehouse(s) and Location Format | WALO | 30 | `im_152` |  | MAIN |  | 50 |
| `LODE` | Location Billing Code | WALO | 40 | `im_159` |  | MAIN |  | 50 |
| `SOSE` | Sort Sequence Code | WALO | 50 | `im_326` |  | MAIN |  | 55 |
| `PIIT` | Pick Line Item Assignments | WALO | 60 | `im_177` |  | MAIN |  | 05 |
| `LPPR` | Location Print Profile | WALO | 70 | `im_113` |  | MAIN |  | 50 |
| `LOTP` | Location Type | WALO | 80 | `im_331` |  | MAIN |  | 50 |
| `LOCS` | Location Size Codes | WALO | 90 | `im_337` |  | MAIN |  | 05 |
| `WHZO` | Warehouse Zone Codes | WALO | 100 | `im_327` |  | MAIN |  | 45 |
| `PROA` | Processing Area Code | WALO | 110 | `im_369` |  | MAIN |  | 50 |
| `PRTP` | Processing Area Type Code | WALO | 120 | `im_371` |  | MAIN |  | 50 |
| `DMPA` | Directed Move Profile | WALO | 130 | `im_705` |  | MAIN |  | 05 |
| `WATP` | Warehouse Activity Type Priority | WALO | 140 | `im_724` |  | MAIN |  | 45 |
| `DORE` | Document Related | WARR | 20 | `` |  | MAIN |  |  |
| `DOCU` | Document(s) | DORE | 20 | `im_174` |  | MAIN |  | 15 |
| `DONU` | Document Numbers | DORE | 30 | `im_186` |  | MAIN |  | 50 |
| `DOTP` | Document Types | DORE | 40 | `im_164` |  | MAIN |  | 15 |
| `CCDU` | Customer / Consignee Document Setup | DORE | 50 | `scr_067` |  | MAIN |  | 45 |
| `BIRE` | Billing Related | WARR | 30 | `` |  | MAIN |  |  |
| `REVA` | Revenue Analysis | BIRE | 10 | `im_139` |  | MAIN |  | 50 |
| `INRE` | Invoice Register Definition | BIRE | 20 | `im_143` |  | MAIN |  | 10 |
| `INTP` | Invoice Type(s) | BIRE | 30 | `im_132` |  | MAIN |  | 50 |
| `REGR` | Revenue Groups | BIRE | 40 | `im_343` |  | MAIN |  | 50 |
| `CLOL` | Close Open Lots | BIRE | 50 | `l_la_109` |  | MAIN |  | 10 |
| `OAUD` | Accessorial Charges Authorization Audit | BIRE | 60 | `re_102` |  | MAIN |  | 10 |
| `GENE` | General | WARR | 40 | `` |  | MAIN |  |  |
| `RETP` | Retail Profiles | GENE | 10 | `im_119` |  | MAIN |  | 50 |
| `SOLD` | Sold-To Codes | GENE | 20 | `im_158` |  | MAIN |  | 50 |
| `CARR` | Carriers | GENE | 30 | `im_137` |  | MAIN |  | 50 |
| `SHIP` | Shipper(s) | GENE | 40 | `im_157` |  | MAIN |  | 50 |
| `CONS` | Consignee(s) | GENE | 50 | `im_136` |  | MAIN |  | 50 |
| `LDAN` | Load Analysis | GENE | 60 | `im_175` |  | MAIN |  | 50 |
| `FPAY` | Freight Paying Office Code(s) | GENE | 70 | `im_126` |  | MAIN |  |  |
| `TRMO` | Transport Mode Code(s) | GENE | 80 | `im_370` |  | MAIN |  | 50 |
| `MISC` | Miscellaneous | WARR | 50 | `` |  | MAIN |  |  |
| `REAS` | Reason Codes | MISC | 10 | `im_317` |  | MAIN |  | 10 |
| `HOLI` | Holidays | MISC | 20 | `ms_023` |  | MAIN |  | 50 |
| `LOAD` | Load Type | MISC | 30 | `im_151` |  | MAIN |  | 50 |
| `HOLD` | Hold Types | MISC | 40 | `im_133` |  | MAIN |  | 50 |
| `HORP` | Hold Restriction Pairs | MISC | 50 | `im_133m` |  | MAIN |  |  |
| `MESS` | Messages | MISC | 60 | `im_130` |  | MAIN |  | 50 |
| `PALL` | Pallet Types | MISC | 70 | `im_146` |  | MAIN |  | 35 |
| `INTE` | Inventory Terminology | MISC | 80 | `im_160` |  | MAIN |  | 50 |
| `SKUS` | Stock Keeping Units | MISC | 90 | `im_135` |  | MAIN |  | 50 |
| `TELE` | Telephone Number(s) | MISC | 100 | `im_148` |  | MAIN |  | 50 |
| `ZIPO` | ZIP/Postal Code | MISC | 110 | `im_102` |  | MAIN |  | 50 |
| `STPR` | States/Provinces | MISC | 120 | `im_101` |  | MAIN |  | 50 |
| `TETP` | Telephone List Type(s) | MISC | 130 | `im_129` |  | MAIN |  | 50 |
| `SKCL` | SKU Class | MISC | 140 | `im_196` |  | MAIN |  | 50 |
| `DRIV` | Driver(s) | MISC | 150 | `im_182` |  | MAIN |  | 50 |
| `ADJU` | Adjustment Type Code(s) | MISC | 160 | `im_111` |  | MAIN |  | 50 |
| `SCPA` | Scan Parameter(s) | MISC | 170 | `im_312` |  | MAIN |  |  |
| `ORPR` | Order Priorities | MISC | 180 | `im_332` |  | MAIN |  | 05 |
| `HOSP` | Hold Shipping Sequence Profile Code | MISC | 190 | `im_334` |  | MAIN |  | 50 |
| `DAPC` | Day Profile Code | MISC | 200 | `im_336` |  | MAIN |  | 35 |
| `RCPR` | Receipt Priorities | MISC | 210 | `im_345` |  | MAIN |  | 35 |
| `STTX` | State Tax | MISC | 220 | `im_350` |  | MAIN |  |  |
| `CNTY` | Country Codes | MISC | 230 | `im_355` |  | MAIN |  | 50 |
| `NUSE` | Number Series | MISC | 240 | `im_127` |  | MAIN |  | 50 |
| `FLPR` | Flow Process | MISC | 250 | `im_197` |  | MAIN |  | 50 |
| `DIST` | Distribution Types | MISC | 260 | `im_368` |  | MAIN |  |  |
| `ADIM` | Inventory Messages | MISC | 270 | `ad_113` |  | MAIN |  | 50 |
| `SCPR` | Scan Parameter Profile | MISC | 280 | `im_500` |  | MAIN |  | 45 |
| `RFRE` | Radio Frequency Related | WARR | 60 | `` |  | MAIN |  |  |
| `BAPR` | Bar Code Profile | RFRE | 10 | `im_380` |  | MAIN |  | 45 |
| `MRFP` | RF Profile | RFRE | 20 | `scr_033` |  | MAIN |  | 45 |
| `PSPR` | RF Substitution Profile Code | RFRE | 30 | `im_382` |  | MAIN |  | 45 |
| `EOSU` | Exclude Orders from Substi./Over-Picking | RFRE | 40 | `scr_006` |  | MAIN |  | 45 |
| `MCHK` | RF Checklist | RFRE | 50 | `im_388` |  | MAIN |  | 45 |
| `RFIG` | RFID Tag Generate | RFRE | 60 | `scr_023` |  | MAIN |  | 35 |
| `MORE` | Additional Info | RFRE | 70 | `rf_java` |  | MAIN |  |  |
| `EDIR` | EDI Related | SU | 60 | `` |  | MAIN |  |  |
| `EDTS` | EDI Transaction Set Code(s) | EDIR | 10 | `do_101` |  | MAIN |  | 35 |
| `EDDI` | EDI Data ID Code(s) | EDIR | 20 | `do_102` |  | MAIN |  | 35 |
| `EDCA` | EDI Program/Routine/Case Code(s) | EDIR | 30 | `do_103` |  | MAIN |  | 35 |
| `MAEP` | EDI Purge Parameters | EDIR | 40 | `im_353` |  | MAIN |  |  |
| `CEDI` | Copy EDI Profile Codes | EDIR | 50 | `im_376` |  | MAIN |  | 35 |
| `DEDP` | Depositor EDI Profile Code(s) | EDIR | 60 | `im_125` |  | MAIN |  | 35 |
| `LOEH` | Look Up EDI History | EDIR | 70 | `im_349` |  | MAIN |  |  |
| `EDIA` | EDI Adjustment Audit | EDIR | 80 | `re_105` |  | MAIN |  | 35 |
| `INEDI` | EDI Inventory Flat File | EDIR | 90 | `iq_108` |  | MAIN |  | 35 |
| `UEDI` | Update EDI Info. for Confirm Orders | EDIR | 100 | `op_219` |  | MAIN |  | 35 |
| `EDIV` | EDI 811 Transaction Invoicing | EDIR | 110 | `im_378` |  | MAIN |  | 35 |
| `ECID` | EDI Customer / Invoice / Document | EDIR | 120 | `im_377` |  | MAIN |  | 35 |
| `LABR` | Labor System | SU | 70 | `` |  | MAIN |  |  |
| `MHET` | Material Handling Types | LABR | 10 | `la_003` |  | MAIN |  | 45 |
| `MHEC` | Material Handling Equipment Code | LABR | 20 | `la_004` |  | MAIN |  | 45 |
| `WASH` | Warehouse Shift Setup | LABR | 30 | `la_008` |  | MAIN |  | 45 |
| `JBTP` | Job Type Code | LABR | 40 | `la_009` |  | MAIN |  | 35 |
| `LSOA` | Labor Standard Profile Codes | LABR | 50 | `la_014` |  | MAIN |  | 35 |
| `ULSO` | Update Labor Standard for Open Documents | LABR | 60 | `ad_140` |  | MAIN |  | 35 |
| `LPTR` | Labor Productivity Time Report | LABR | 70 | `lr_001n` | 811 | MAIN |  | 25 |
| `LPOR` | Labor Productivity Operation Report | LABR | 80 | `lr_002n` | 811 | MAIN |  | 25 |
| `PALR` | Profit and Loss Report | LABR | 110 | `qd_234` | 811 | MAIN |  |  |
| `LSMP` | Labor Standard Modifier Profile | LABR | 120 | `la_015` |  | MAIN |  | 35 |
| `ELIP` | External Labor system integration Param | LABR | 130 | `la_010` |  | MAIN |  | 35 |
| `FR` | Freight Systems | MAIN | 50 | `` |  | MAIN |  |  |
| `FIPR` | Freight Interface Profile | FR | 10 | `im_381` |  | MAIN |  |  |
| `FRMA` | Freight Maintenance | FR | 20 | `` |  | MAIN |  |  |
| `DEGR` | Destination Group Codes | FRMA | 10 | `im_301` |  | MAIN |  |  |
| `DECO` | Destination Codes | FRMA | 20 | `im_302` |  | MAIN |  |  |
| `ZONE` | Zone/Lane Codes | FRMA | 30 | `im_303` |  | MAIN |  |  |
| `FRTY` | Freight Type Codes | FRMA | 40 | `im_307` |  | MAIN |  |  |
| `TERL` | Freight Terminal Codes | FRMA | 50 | `im_308` |  | MAIN |  |  |
| `FRBR` | Freight Quantity Break(s) | FRMA | 60 | `im_163` |  | MAIN |  |  |
| `FRCP` | Customer Freight Profile Code | FRMA | 70 | `im_309` |  | MAIN |  |  |
| `FROP` | Freight Operations | FR | 30 | `` |  | MAIN |  |  |
| `SCHE` | Schedule Orders for Delivery | FROP | 10 | `fp_105` |  | MAIN |  |  |
| `SERV` | Service Update | FROP | 20 | `fp_106` |  | MAIN |  |  |
| `FX` | Faxing | MAIN | 60 | `` |  | MAIN |  |  |
| `LOFX` | Look Up Transmitted Faxes | FX | 10 | `ms_025` |  | MAIN |  |  |
| `SEFX` | Send Faxes | FX | 20 | `ms_018` |  | MAIN |  | 35 |
| `FXCS` | Fax Cover Sheet | FX | 30 | `im_316` |  | MAIN |  | 35 |
| `FXOL` | Document Overlay | FX | 40 | `im_328` |  | MAIN |  | 35 |
| `REPO` | Reports Related | MAIN | 70 | `` |  | MAIN |  |  |
| `ADAU` | Adjustment Audit Report | REPO | 10 | `re_101` | 811 | MAIN |  | 25 |
| `ADRE` | Adjustment Transaction Report | REPO | 20 | `re_112` | 811 | MAIN |  | 25 |
| `BIRR` | Billing Renewals Report | REPO | 30 | `re_111` | 811 | MAIN |  | 25 |
| `CARL` | Carrier Listing | REPO | 40 | `qd_188` | 811 | MAIN |  | 25 |
| `CONL` | Consignee Listing | REPO | 50 | `qd_189` | 811 | MAIN |  | 25 |
| `CUPR` | Customer Listing - Details | REPO | 60 | `qd_165` | 811 | MAIN |  | 25 |
| `CYCR` | Cycle Count Report | REPO | 70 | `qd_166` | 811 | MAIN |  | 20 |
| `DEHA` | Deferred Handling Report | REPO | 80 | `qd_158` | 811 | MAIN |  | 25 |
| `DLCR` | Daily Activity Recap: By Date | REPO | 90 | `dp_103a` | 811 | MAIN |  | 25 |
| `DORR` | Daily Order / Receipt Report | REPO | 100 | `dp_104` | 811 | MAIN |  | 25 |
| `EMLO` | Empty Location Report | REPO | 110 | `qd_184` | 811 | MAIN |  | 25 |
| `EXRE` | Aging - level 3 by Expy./Rcvd. Report | REPO | 120 | `qd_153` | 811 | MAIN |  | 25 |
| `HOIR` | Hold Inventory Report | REPO | 130 | `qd_142` | 811 | MAIN |  | 25 |
| `IAGR` | Inventory Aging Report | REPO | 140 | `qd_186` | 811 | MAIN |  | 25 |
| `IATR` | Inventory Activity Turns Report | REPO | 150 | `qd_154` | 811 | MAIN |  | 25 |
| `IATC` | Inventory Activity Turns By Customer Rep | REPO | 160 | `re_117` | 811 | MAIN |  | 25 |
| `IILR` | Inventory by Item Report and Location | REPO | 170 | `qd_127` | 811 | MAIN |  | 25 |
| `IBOR` | Item Back Order Report | REPO | 180 | `re_127` | 811 | MAIN |  |  |
| `INAS` | Inventory Report by Alternate Sort | REPO | 190 | `qd_177` | 811 | MAIN |  | 25 |
| `INDS` | Inventory Hold-Date Sensitive | REPO | 200 | `qd_126` | 811 | MAIN |  | 25 |
| `INHD` | Inventory - Level 3 with Desc. Report | REPO | 210 | `qd_176` | 811 | MAIN |  | 25 |
| `INHK` | Inventory Location with Holds 4 Level | REPO | 220 | `re_126` | 811 | MAIN |  | 25 |
| `INHL` | Inventory Report with Hold Level 2 | REPO | 230 | `qd_157` | 811 | MAIN |  | 25 |
| `INHC` | Inventory by Lot with Locations Report | REPO | 240 | `qd_125` | 811 | MAIN |  | 25 |
| `INHR` | Inventory Report with Hold - Level 1 | REPO | 250 | `qd_155` | 811 | MAIN |  | 25 |
| `INHJ` | Inventory with Hold and Location - Lev3 | REPO | 260 | `qd_110` | 811 | MAIN |  | 25 |
| `CUMI` | Inventory Status Level 2 Report | REPO | 270 | `qd_111` | 811 | MAIN |  | 25 |
| `IMBR` | Inventory Minimum Balance Report | REPO | 280 | `re_109` | 811 | MAIN |  | 25 |
| `IEAR` | Inventory Expiry Aging Report | REPO | 290 | `qd_221` | 811 | MAIN |  | 25 |
| `INLO` | Location Rpt-3 Lev by Loc or Ware | REPO | 300 | `qd_139` | 811 | MAIN |  | 25 |
| `INQB` | Inventory Available in High and Low SKU | REPO | 310 | `qd_118` | 811 | MAIN |  | 25 |
| `IRDR` | Inventory Relocation Daily Report | REPO | 320 | `qd_209` | 811 | MAIN |  | 25 |
| `INVR` | Invoice Report | REPO | 330 | `qd_170` | 811 | MAIN |  | 25 |
| `ISAC` | Item Summary Activity Report | REPO | 340 | `re_114` | 811 | MAIN |  | 25 |
| `ITLI` | Item - Sku and Size Report | REPO | 350 | `qd_101` | 811 | MAIN |  | 25 |
| `IWPL` | Items Without Pick Line Assignment List | REPO | 360 | `qd_193` | 811 | MAIN |  | 25 |
| `ILTR` | Inventory Level 4 with Lot Total Report | REPO | 370 | `qd_243` | 811 | MAIN |  | 25 |
| `IPOR` | Invt. Pend Order/Receipt By Broker | REPO | 380 | `qd_244` | 811 | MAIN |  | 25 |
| `LOCR` | Location - Level 3 with Isol. Report | REPO | 390 | `qd_160` | 811 | MAIN |  | 25 |
| `LOCT` | Location with Item Desc. Report | REPO | 400 | `qd_102` | 811 | MAIN |  | 25 |
| `LRID` | Location with Level 2 Description | REPO | 410 | `qd_175` | 811 | MAIN |  | 25 |
| `LWMI` | Location with Mixed Inventory Report | REPO | 420 | `qd_152a` | 811 | MAIN |  | 25 |
| `BCOR` | Broker Customers Orders Report | REPO | 430 | `qd_202` | 811 | MAIN |  | 25 |
| `IADR` | Inventory Rcvd/Expy Aging Days Report | REPO | 440 | `qd_203` | 811 | MAIN |  | 25 |
| `IABR` | Inventory Aging Broker Report | REPO | 450 | `qd_204` | 811 | MAIN |  | 25 |
| `THBR` | Transaction History Broker Report | REPO | 460 | `qd_205` | 811 | MAIN |  | 25 |
| `OLSR` | Order Line Status Report | REPO | 470 | `qd_207` | 811 | MAIN |  | 25 |
| `HTBR` | Hold Transaction Broker Report | REPO | 480 | `qd_210` | 811 | MAIN |  | 25 |
| `CICR` | Customer Invoice Charge Report | REPO | 490 | `qd_211` | 811 | MAIN |  | 25 |
| `GLCR` | Cost Analysis GL Report | REPO | 500 | `qd_206` | 811 | MAIN |  | 25 |
| `LOAN` | Location Analysis Report | REPO | 510 | `qd_130` | 811 | MAIN |  | 25 |
| `LHIS` | Location History Report | REPO | 520 | `qd_120` | 811 | MAIN |  | 25 |
| `OFRR` | Order Fill Rate Report | REPO | 530 | `qd_238` | 811 | MAIN |  | 25 |
| `OQVR` | Order Quantity Variance Report | REPO | 540 | `qd_222` | 811 | MAIN |  | 25 |
| `PABA` | Pallet Account Balance Report | REPO | 550 | `re_104` | 811 | MAIN |  | 25 |
| `PATH` | Pallet Transaction History Report | REPO | 560 | `re_103` | 811 | MAIN |  | 25 |
| `PECX` | Pending Order by Item Report | REPO | 570 | `qd_172` | 811 | MAIN |  | 25 |
| `PEOX` | Pending Orders Report | REPO | 580 | `qd_167` | 811 | MAIN |  | 25 |
| `PIIL` | Pick Line Item Listing | REPO | 590 | `qd_192` | 811 | MAIN |  | 25 |
| `PLSR` | Pick Line Status Report | REPO | 600 | `qd_183` | 811 | MAIN |  | 25 |
| `PRAR` | Product Receiving Analysis Report | REPO | 610 | `qd_212` | 811 | MAIN |  | 25 |
| `RECR` | Receiving Summary Report | REPO | 620 | `qd_214` | 811 | MAIN |  | 25 |
| `RARE` | Rate Report | REPO | 630 | `qd_137` | 811 | MAIN |  | 25 |
| `RECW` | Receipt Summary by Warehouse Report | REPO | 640 | `qd_116` | 811 | MAIN |  | 25 |
| `RPAU` | Relocate To Pickline Audit Report | REPO | 650 | `qd_164` | 811 | MAIN |  | 25 |
| `RPAUA` | Relocate Pickline Audit without Report | REPO | 660 | `qd_164a` |  | MAIN |  | 05 |
| `PERR` | Pending Renewals Report | REPO | 670 | `re_120` | 811 | MAIN |  | 25 |
| `RSAR` | Receiving/Shipping Analysis Report | REPO | 680 | `re_125` | 811 | MAIN |  | 25 |
| `SALE` | 12-Month Sales Report | REPO | 690 | `qd_131` | 811 | MAIN |  | 25 |
| `SHAN` | Shipping Analysis Report | REPO | 700 | `qd_213` | 811 | MAIN |  | 25 |
| `SSRA` | Summary Sales By Revenue Analysis | REPO | 710 | `re_106` | 811 | MAIN |  | 25 |
| `THIC` | Trans. History with Hold Trans. Report | REPO | 720 | `qd_114` | 811 | MAIN |  | 25 |
| `THIB` | Transaction History - Running Balance | REPO | 730 | `qd_178` | 811 | MAIN |  | 25 |
| `THIL` | Transaction History High/Low Sku Report | REPO | 740 | `qd_196` | 811 | MAIN |  | 25 |
| `THIS` | Transaction History Report | REPO | 750 | `qd_185` | 811 | MAIN |  | 25 |
| `THIT` | Transaction History Report - Level 4 | REPO | 760 | `qd_156` | 811 | MAIN |  | 25 |
| `THLR` | Transaction History Location report | REPO | 770 | `qd_112` | 811 | MAIN |  | 25 |
| `TOSA` |  Tonnage Sales Report | REPO | 780 | `qd_135a` | 811 | MAIN |  | 25 |
| `UNCH` | Unbilled Charges Report | REPO | 790 | `re_107` | 811 | MAIN |  | 25 |
| `UNOS` | Order Status Report | REPO | 800 | `op_501d` | 811 | MAIN |  | 25 |
| `UNRE` | Receipt Status Report | REPO | 810 | `rp_501d` | 811 | MAIN |  | 25 |
| `SHOS` | Shipped Order Report | REPO | 820 | `qd_105` | 811 | MAIN |  | 25 |
| `USDA` | Monthly Cold Storage Report | REPO | 830 | `qd_113` | 811 | MAIN |  | 25 |
| `DLOP` | Daily Operator Performance Report | REPO | 840 | `qd_115` | 811 | MAIN |  | 25 |
| `WESA` | Weekly Sales Report | REPO | 850 | `qd_151` | 811 | MAIN |  | 25 |
| `WSDR` | Weekly Sales Date Range Report | REPO | 860 | `qd_151a` | 811 | MAIN |  | 25 |
| `COWE` | Consignee Weight Report | REPO | 870 | `qd_123` | 811 | MAIN |  | 25 |
| `WPDR` | Weekly Pick by Days Report | REPO | 880 | `qd_224` | 811 | MAIN |  | 25 |
| `OPIR` | Outbound Pallet ID (Exit Tag) Report | REPO | 890 | `qd_225` | 811 | MAIN |  | 25 |
| `IKRE` | Item Kitting Report | REPO | 900 | `re_110` | 811 | MAIN |  | 35 |
| `LOSR` | Load Status Report | REPO | 910 | `qd_223` | 811 | MAIN |  | 25 |
| `SHSH` | Short Shipped Report | REPO | 920 | `l_ax_109` | 811 | MAIN |  | 25 |
| `PRAC` | Product Activity Report | REPO | 930 | `qd_163` | 811 | MAIN |  | 25 |
| `CAVR` | Consignee Analysis Value Report | REPO | 940 | `qd_182` | 811 | MAIN |  | 25 |
| `PECR` | Pending/Unpicked/Picked Orders Report | REPO | 950 | `qd_215` | 811 | MAIN |  | 25 |
| `IOSR` | Inbound / Outbound Summary Report | REPO | 960 | `qd_235` | 811 | MAIN |  |  |
| `LOCP` | Location by Pallet Quantity Report | REPO | 970 | `qd_237` | 811 | MAIN |  |  |
| `DRRC` | Daily Receipts with Charges Report | REPO | 980 | `re_128` | 811 | MAIN |  |  |
| `ULCR` | Unique Invt. Level Count Lev4 Report | REPO | 990 | `qd_251` | 811 | MAIN |  | 25 |
| `WCUR` | Warehouse Customer Utilization Report | REPO | 990 | `qd_247` | 811 | MAIN |  | 25 |
| `WLUR` | Warehouse Location Utilization Report | REPO | 990 | `qd_248` | 811 | MAIN |  | 25 |
| `SHOW` | Shipped Order Summary by Warehouse | REPO | 990 | `qd_249` | 811 | MAIN |  | 25 |
| `INAI` | Inventory by Alternate Sort | REPO | 990 | `qd_216` | 811 | MAIN |  | 25 |
| `SHLA` | Shipping Lanes | REPO | 990 | `la_018` |  | MAIN |  | 05 |
| `FLAT` | Flat Files | MAIN | 80 | `` |  | MAIN |  |  |
| `IOFF` | Inbound/Outbound Confirmation Flat File | FLAT | 10 | `ff_004` | 811 | MAIN |  |  |
| `INFF` | Inventory by Customer Flat File | FLAT | 20 | `ff_006` | 811 | MAIN |  |  |
| `THFF` | Transaction History Flat File | FLAT | 30 | `ff_008` | 811 | MAIN |  |  |
| `IFFH` | Inventory With Hold Flat File | FLAT | 40 | `ff_101` | 811 | MAIN |  |  |
| `PEBR` | Pending/Unpicked/Picked Orders By Broker | FLAT | 60 | `qd_245` | 811 | MAIN |  |  |
| `PIRA` | Pick Ratio Report | FLAT | 70 | `re_149` | 811 | MAIN |  |  |
| `AR` | Account Receivable | MAIN | 90 | `` |  | MAIN |  |  |
| `ARCP` | Check/Cash Entry | AR | 10 | `im_510` |  | MAIN |  | 10 |
| `CHPO` | Check Posting | AR | 20 | `scr_058` |  | MAIN |  | 10 |
| `CRIN` | Credit Invoice | AR | 30 | `scr_056` |  | MAIN |  | 10 |
| `CUCR` | AR Customer Cross Reference | AR | 40 | `scr_059` |  | MAIN |  | 10 |
| `ARAR` | Account Receivable Aging Report | AR | 50 | `qd_240` | 811 | MAIN |  | 25 |
| `INPR` | Invoice Payment Report | AR | 60 | `qd_239` | 811 | MAIN |  | 25 |
| `CRPR` | Cash/Check Posting Report | AR | 70 | `qd_241` | 811 | MAIN |  |  |
| `UPGD` | Upgrades | MAIN | 100 | `` |  | MAIN |  |  |
| `TEST` | Test | UPGD | 10 | `test` |  | MAIN |  |  |
| `SS` | Special Systems | MAIN | 110 | `` |  | MAIN |  |  |
| `MSVS` | Special Verifier SQL | SS | 10 | `scr_078` |  | MAIN |  | 55 |
| `RFMN` | RF Main Menu |  | 20 | `` |  | RFMN |  |  |
| `RFINB` | Inbound | RFMN | 10 | `` |  | RFMN |  |  |
| `RFUNC` | Unload | RFINB | 10 | `rf_140` |  | RFMN |  |  |
| `RFCH` | Receiving | RFINB | 20 | `rf_140a` |  | RFMN |  |  |
| `RFIPS` | Inbound Process Scan | RFINB | 30 | `rf_140f` |  | RFMN |  |  |
| `RFPU` | Put-Away | RFINB | 40 | `rf_142` |  | RFMN |  |  |
| `RFVA` | Variance Inbound | RFINB | 50 | `rf_140g` |  | RFMN |  |  |
| `MAIN` | Main Menu |  | 10 | `` |  | MAIN |  |  |
| `CS` | Customer Service | MAIN | 10 | `` |  | MAIN |  |  |
| `LOOK` | Look Up Programs | CS | 10 | `` |  | MAIN |  |  |
| `LOTE` | Look Up Telephone Numbers | LOOK | 10 | `iq_104` |  | MAIN |  | 30 |
| `LOEN` | Look Up Entity Information | LOOK | 20 | `iq_105` |  | MAIN |  | 30 |
| `LOLO` | Look Up Location Information | LOOK | 30 | `iq_106` |  | MAIN |  | 30 |
| `LOIN` | Look Up Invoices | LOOK | 40 | `iq_107` |  | MAIN |  | 10 |
| `LOAC` | Look Up Accessorial Charges | LOOK | 50 | `iq_113` |  | MAIN |  | 10 |
| `LOSV` | Look Up Special Verification | LOOK | 60 | `iq_123` |  | MAIN |  | 55 |
| `LOIP` | Look Up Item Process | LOOK | 70 | `iq_116` |  | MAIN |  | 35 |
| `LOWU` | Look Up Warehouse Utilization | LOOK | 80 | `scr_008` |  | MAIN |  | 55 |
| `SAM` | Supervisor Activity Management | LOOK | 90 | `scr_002` |  | MAIN |  | 55 |
| `SAMC` | Supervisor Activity Management Center | LOOK | 100 | `.net` |  | MAIN |  | 55 |
| `LOCN` | Look Up Carton | LOOK | 110 | `scr_024` |  | MAIN |  | 35 |
| `COIP` | Consignee Item Price | LOOK | 120 | `im_373` |  | MAIN |  |  |
| `CRMA` | Customer Service Management | CS | 20 | `` |  | MAIN |  |  |
| `CRMC` | Customer Service Management Code | CRMA | 10 | `im_375` |  | MAIN |  | 35 |
| `CRME` | Customer Service Management Entry | CRMA | 20 | `cr_001` |  | MAIN |  | 35 |
| `ICIN` | Inventory Count Investigation | CRMA | 30 | `scr_001` |  | MAIN |  | 45 |
| `CRMR` | Customer Service Management Report | CRMA | 40 | `cr_005` | 811 | MAIN |  | 25 |
| `SA` | System Administration | MAIN | 20 | `` |  | MAIN |  |  |
| `DATE` | Change Company Date | SA | 10 | `im_103` |  | MAIN |  | 55 |
| `BACO` | Batch Control | SA | 20 | `ms_060` |  | MAIN |  | 10 |
| `COMR` | Company Related | SA | 30 | `` |  | MAIN |  |  |
| `INST` | Installation Parameters | COMR | 10 | `ms_001` |  | MAIN |  | 55 |
| `COMP` | Company Code | COMR | 20 | `ms_002` |  | MAIN |  | 55 |
| `LANG` | Language Code | COMR | 30 | `im_356` |  | MAIN |  | 50 |
| `COCO` | Copy Codes Between Companies | COMR | 40 | `ms_150` |  | MAIN |  | 55 |
| `JORE` | Job Related | SA | 40 | `` |  | MAIN |  |  |
| `EXJO` | Executable Job Code | JORE | 10 | `ms_005` |  | MAIN |  | 55 |
| `JOSE` | Job Selection Code | JORE | 20 | `ms_006` |  | MAIN |  | 55 |
| `COAC` | Company Access | JORE | 30 | `ms_007` |  | MAIN |  | 55 |
| `OPAC` | Operator Access | JORE | 40 | `ms_024` |  | MAIN |  | 55 |
| `LOAV` | Look Up Application Version | JORE | 50 | `ms_032` |  | MAIN |  | 55 |
| `TRMA` | Translation Manager | JORE | 60 | `ml_002` |  | MAIN |  | 55 |
| `OPRE` | Operator Related | SA | 50 | `` |  | MAIN |  |  |
| `OPER` | Operator Code | OPRE | 10 | `ms_011` |  | MAIN |  | 55 |
| `OPAL` | Operator Alias Code | OPRE | 20 | `ms_012` |  | MAIN |  |  |
| `OPRS` | Operator Restrictions | OPRE | 30 | `ms_014` |  | MAIN |  | 55 |
| `COOA` | Copy Operator Access | OPRE | 40 | `ms_015` |  | MAIN |  | 55 |
| `ROMA` | Roles | OPRE | 50 | `scr_027` |  | MAIN |  | 55 |
| `ADSA` | ActiveDesktop Security Administrators | OPRE | 60 | `scr_028` |  | MAIN |  | 55 |
| `PRIR` | Printer Related | SA | 60 | `` |  | MAIN |  |  |
| `FORM` | Form Code | PRIR | 10 | `ms_004` |  | MAIN |  | 15 |
| `PRIN` | Printer Code | PRIR | 20 | `ms_016` |  | MAIN |  | 50 |
| `PRPF` | Print Profile | PRIR | 30 | `ms_033` |  | MAIN |  | 15 |
| `LMPR` | Load Macro to Printer | PRIR | 40 | `im_700` |  | MAIN |  | 15 |
| `DEAC` | Accellos Access Only | SA | 70 | `` |  | MAIN |  |  |
| `BATP` | Batch Type Code | DEAC | 10 | `im_192` |  | MAIN |  | 15 |
| `ATMP` | Action Template Setup | DEAC | 20 | `im_365` |  | MAIN |  |  |
| `HSKE` | Housekeeping | SA | 80 | `` |  | MAIN |  |  |
| `PURG` | Purge Receipts, Orders, Inventory | HSKE | 10 | `hk_101` |  | MAIN |  | 55 |
| `PRPU` | Print Purge | HSKE | 20 | `hk_102` |  | MAIN |  | 55 |
| `PROP` | Print Order Purge | HSKE | 30 | `hk_103` |  | MAIN |  | 55 |
| `PRRP` | Print Receipt Purge | HSKE | 40 | `hk_104` |  | MAIN |  | 55 |
| `PRIP` | Print Inventory Purge | HSKE | 50 | `hk_105` |  | MAIN |  | 55 |
| `PURB` | Purge Batch | HSKE | 60 | `hk_106` |  | MAIN |  | 55 |
| `PURA` | Purge Accessorial Batch | HSKE | 70 | `hk_107` |  | MAIN |  | 55 |
| `PZEL` | Purge Zero Locations | HSKE | 80 | `ad_131` |  | MAIN |  |  |
| `PUWM` | Purge Warnings/Messages | HSKE | 90 | `hk_111` |  | MAIN |  | 55 |
| `CNBC` | Clear Non-Billing Customer | HSKE | 100 | `hk_115` |  | MAIN |  | 55 |
| `CLTL` | Clear Terminal Locks | HSKE | 110 | `ms_089` |  | MAIN |  | 55 |
| `SPPA` | Spool Parameters | HSKE | 120 | `ms_027` |  | MAIN |  | 55 |
| `WAME` | Look Up Warnings/Messages | HSKE | 120 | `ms_091` |  | MAIN |  | 55 |
| `LOSP` | Look Up Spooler Activity | HSKE | 130 | `ms_021` |  | MAIN |  | 55 |
| `LOAU` | Look Up Audit Trail | HSKE | 140 | `iq_114` |  | MAIN |  |  |
| `CONV` | Conversion | SA | 90 | `` |  | MAIN |  |  |
| `LOCO` | Load Conversion | CONV | 10 | `cv_101` |  | MAIN |  | 55 |
| `PRCO` | Process Conversion | CONV | 20 | `cv_102` |  | MAIN |  | 55 |
| `MOCO` | Modify Conversion Data | CONV | 30 | `cv_104` |  | MAIN |  | 55 |
| `DEPC` | Data Extraction Process for Conversion | CONV | 40 | `cv_105` |  | MAIN |  | 55 |
| `COER` | Conversion Exception Report | CONV | 50 | `cv_103` | 811 | MAIN |  | 55 |
| `ITCO` | Item Conversion | CONV | 60 | `cv_106` |  | MAIN |  | 35 |
| `EVISTA` | e-Vista Support Utilities | SA | 100 | `` |  | MAIN |  |  |
| `EVORD` | e-Vista Outbound Order Request | EVISTA | 10 | `` |  | MAIN |  |  |
| `EVPOD` | e-Vista POD | EVISTA | 20 | `` |  | MAIN |  |  |
| `EVQRY` | e-Vista Queries | EVISTA | 30 | `` |  | MAIN |  |  |
| `EVRCPT` | e-Vista Inbound Receipt Notice | EVISTA | 40 | `` |  | MAIN |  |  |
| `EVINVO` | e-Vista Invoice Queries | EVISTA | 50 | `` |  | MAIN |  |  |
| `EVBROK` | e-Vista Broker Orders | EVISTA | 60 | `` |  | MAIN |  |  |
| `EVIGO` | e-Vista Dos Amigos | EVISTA | 70 | `` |  | MAIN |  |  |
| `EVHIST` | e-Vista Inventory History | EVISTA | 80 | `` |  | MAIN |  |  |
| `ACTIVE` | Active Desktop Security | SA | 110 | `` |  | MAIN |  |  |
| `ADLERT` | Alerts | ACTIVE | 10 | `` |  | MAIN |  |  |
| `ADMIGO` | dAmigo | ACTIVE | 20 | `` |  | MAIN |  |  |
| `ADEFIL` | e-Filing | ACTIVE | 30 | `` |  | MAIN |  |  |
| `ADDASH` | Dashboard | ACTIVE | 40 | `` |  | MAIN |  |  |
| `ADVIST` | e-Vista | ACTIVE | 50 | `` |  | MAIN |  |  |
| `ADBART` | BarTender | ACTIVE | 60 | `` |  | MAIN |  |  |
| `ADSIGN` | Signature | ACTIVE | 70 | `` |  | MAIN |  |  |
| `ADSQL` | SQL Pad | ACTIVE | 80 | `` |  | MAIN |  |  |
| `ADWAVE` | Wave Manager | ACTIVE | 90 | `` |  | MAIN |  |  |
| `BB` | Billing Batch Security | SA | 120 | `` |  | MAIN |  |  |
| `BBACCE` | Accessorial Invoice | BB | 10 | `` |  | MAIN |  |  |
| `BBDLRE` | Daily Invoice Register | BB | 20 | `` |  | MAIN |  |  |
| `BBEXCH` | Extra Charge Rater | BB | 30 | `` |  | MAIN |  |  |
| `BBIINV` | Immediate Invoice | BB | 40 | `` |  | MAIN |  |  |
| `BBMINV` | Minimum Total Invoices | BB | 50 | `` |  | MAIN |  |  |
| `BBRENW` | Renewal Invoice | BB | 60 | `` |  | MAIN |  |  |
| `WO` | Warehouse Operations | MAIN | 30 | `` |  | MAIN |  |  |
| `IFFI` | Interface from File | WO | 10 | `scr_080` |  | MAIN |  | 55 |
| `TURE` | Top Up Replenishment | WO | 30 | `ad_143` |  | MAIN |  | 05 |
| `ADPR` | Adjustment Programs | WO | 50 | `` |  | MAIN |  |  |
| `RELO` | Relocate Inventory | ADPR | 10 | `ad_104` |  | MAIN |  | 30 |
| `ENAJ` | Enter Adjustment | ADPR | 20 | `ad_107` |  | MAIN |  | 30 |
| `WEAD` | Weight Adjustments | ADPR | 30 | `ad_106` |  | MAIN |  | 30 |
| `HOAD` | Hold Adjustments | ADPR | 40 | `ad_102` |  | MAIN |  | 30 |
| `CHEI` | Change Entity Information | ADPR | 50 | `ad_103` |  | MAIN |  | 30 |
| `CLWE` | Clear Weights | ADPR | 60 | `ad_110` |  | MAIN |  | 30 |
| `AIQB` | Adjust Item Quantity Breakdown | ADPR | 70 | `ad_112` |  | MAIN |  | 55 |
| `ADBD` | Adjust Billing Data | ADPR | 80 | `ad_101` |  | MAIN |  | 10 |
| `CHCD` | Change Order Confirmation Date | ADPR | 90 | `ad_111` |  | MAIN |  | 30 |
| `POHO` | Put On Hold | ADPR | 100 | `ad_117` |  | MAIN |  | 30 |
| `MARL` | Massive Relocate | ADPR | 110 | `ad_114` |  | MAIN |  | 30 |
| `MAHO` | Take Off Holds | ADPR | 120 | `ad_115` |  | MAIN |  | 30 |
| `MATR` | Massive Adjustment | ADPR | 130 | `ad_116` |  | MAIN |  | 30 |
| `HATO` | Holds Auto Take-Off | ADPR | 140 | `ad_122` | 811 | MAIN |  | 30 |
| `REEX` | Reset Inventory Expiry Date | ADPR | 150 | `ad_119` |  | MAIN |  | 55 |
| `RESW` | Recalculate Standard Weight | ADPR | 160 | `ad_125` |  | MAIN |  | 30 |
| `ADLT` | Adjust Location Type | ADPR | 170 | `ad_129` |  | MAIN |  | 55 |
| `ADLB` | Adjust Location Bill Code | ADPR | 180 | `ad_108` |  | MAIN |  | 55 |
| `COIT` | Copy Items from One to Another | ADPR | 190 | `im_354` |  | MAIN |  | 55 |
| `DMPR` | Directed Move Processing | ADPR | 200 | `ad_137` |  | MAIN |  | 05 |
| `AEQB` | Adjust Entity Quantity Breakdown | ADPR | 210 | `ad_141` |  | MAIN |  | 55 |
| `CHIA` | Change Inventory Attributes | ADPR | 220 | `ad_142` |  | MAIN |  | 35 |
| `RVDF` | Reverse Document Flow | ADPR | 230 | `scr_026` |  | MAIN |  | 30 |
| `RFITLV` | Interleaving | RFINB | 60 | `rf_188a` |  | RFMN |  |  |
| `RFINC` | Incident | RFINB | 70 | `rf_199` |  | RFMN |  |  |
| `RFTT` | RF Temperature and Trailer | RFINB | 80 | `rf_103` |  | RFMN |  |  |
| `RFRPE` | RF Receipt Pallet Entry | RFINB | 100 | `rf_101er` |  | RFMN |  |  |
| `RFDL` | RF Deleting Line | RFINB | 110 | `rf_180` |  | RFMN |  |  |
| `RFVNA` | RF in Very Narrow Aisle | RFINB | 120 | `rf_188b` |  | RFMN |  |  |
| `RFOUTB` | Outbound | RFMN | 20 | `` |  | RFMN |  |  |
| `RFPIC` | Pick | RFOUTB | 10 | `rf_143` |  | RFMN |  |  |
| `RFPI` | Pick | RFOUTB | 20 | `rf_136` |  | RFMN |  |  |
| `RFST` | Stage | RFOUTB | 30 | `rf_144` |  | RFMN |  |  |
| `RFRP` | Replenishment under/over pick | RFOUTB | 50 | `rf_157` |  | RFMN |  |  |
| `UOPR` | Update Order Process | RFOUTB | 60 | `rf_java` |  | RFMN |  |  |
| `OLOP` | Outbound Loading Process | RFOUTB | 80 | `rf_java` |  | RFMN |  |  |
| `RFOLP` | Outbound Label Printing | RFOUTB | 140 | `rf_801` |  | RFMN |  |  |
| `CASE` | Case Pick | RFOUTB | 150 | `rf_152` |  | RFMN |  |  |
| `RFOPS` | Outbound Process Scanning | RFOUTB | 160 | `rf_143f` |  | RFMN |  |  |
| `RFMG` | Merge OPID | RFOUTB | 170 | `rf_148` |  | RFMN |  |  |
| `RFCO` | Confirm OPID | RFOUTB | 180 | `rf_149` |  | RFMN |  |  |
| `RFSC` | Sort To Carton | RFOUTB | 190 | `rf_169a` |  | RFMN |  |  |
| `RFCA` | RF Carton Audit | RFOUTB | 200 | `rf_174` |  | RFMN |  |  |
| `RFPK` | RF Wave Pick | RFOUTB | 210 | `rf_601` |  | RFMN |  |  |
| `RFCC` | RF Carton Cubic | RFOUTB | 220 | `rf_178` |  | RFMN |  |  |
| `RFOPE` | RF Order Pallet Entry | RFOUTB | 230 | `rf_101eo` |  | RFMN |  |  |
| `RFOA` | RF Outbound Audit | RFOUTB | 240 | `rf_181` |  | RFMN |  |  |
| `RFOPB` | RF Outbound Pallet Build | RFOUTB | 250 | `rf_177` |  | RFMN |  |  |
| `RFINVT` | Inventory | RFMN | 30 | `` |  | RFMN |  |  |
| `RFRL` | Relocate | RFINVT | 10 | `rf_139` |  | RFMN |  |  |
| `RFCW` | Catch Weights | RFINVT | 20 | `rf_138` |  | RFMN |  |  |
| `RFMI` | RF Merge Inventory | RFINVT | 30 | `rf_165` |  | RFMN |  |  |
| `RFAJ` | Adjustment | RFINVT | 40 | `rf_166` |  | RFMN |  |  |
| `RFAJB` | Adjustment By Bar Code | RFINVT | 50 | `rf_151` |  | RFMN |  |  |
| `RFCL` | Count Log | RFINVT | 60 | `rf_155` |  | RFMN |  |  |
| `RFCY` | Cycle Count | RFINVT | 70 | `rf_127` |  | RFMN |  |  |
| `RFCYE` | Cycle Count | RFINVT | 80 | `rf_127n` |  | RFMN |  |  |
| `RFCYS` | Cycle Supervisor | RFINVT | 90 | `rf_127s` |  | RFMN |  |  |
| `RFPH` | Physical Inventory | RFINVT | 100 | `rf_124` |  | RFMN |  |  |
| `RFEC` | RF Extra Charge | RFINVT | 110 | `rf_172` |  | RFMN |  |  |
| `RFCD` | RF Check Digits | RFINVT | 120 | `rf_173` |  | RFMN |  |  |
| `RFLS` | RF CHECKLIST | RFINVT | 140 | `rf_388` |  | RFMN |  |  |
| `RFATT` | RF ATTributes | RFINVT | 150 | `rf_201` |  | RFMN |  |  |
| `RFLOOK` | Look Ups | RFMN | 40 | `` |  | RFMN |  |  |
| `LORERF` | Look Up Receipt | RFLOOK | 10 | `iq_101rf` |  | RFMN |  |  |
| `LOORRF` | Look Up Order | RFLOOK | 20 | `iq_102rf` |  | RFMN |  |  |
| `LOENRF` | Look Up Entity Information | RFLOOK | 30 | `iq_105rf` |  | RFMN |  |  |
| `RFPR` | Product Lookup by Locations | RFLOOK | 50 | `rf_106` |  | RFMN |  |  |
| `RFIL` | Receipt Line Lookup | RFLOOK | 60 | `rf_116` |  | RFMN |  |  |
| `RFOL` | Order Line Lookup | RFLOOK | 70 | `rf_118` |  | RFMN |  |  |
| `RFIR` | Inbound Remark Lookup | RFLOOK | 80 | `rf_119` |  | RFMN |  |  |
| `RFIT` | Item Lookup | RFLOOK | 90 | `rf_117` |  | RFMN |  |  |
| `RFLOIP` | Look Up Item Process | RFLOOK | 110 | `rf_115` |  | RFMN |  |  |
| `RFBR` | RF Bar Code Read | RFLOOK | 120 | `rf_105` |  | RFMN |  |  |
| `RFLR` | Look Up Reserve Inventory by Location | RFLOOK | 130 | `rf_106b` |  | RFMN |  |  |
| `LOLOAD` | Look Up Load | RFLOOK | 140 | `rf_java` |  | RFMN |  |  |
| `LOLORF` | Look Up Location | RFLOOK | 40 | `iq_106rf` |  | RFMN |  |  |
| `RFAU` | RF AUDIT | RFOUTB | 90 | `rf_194` |  | RFMN |  |  |
| `RFRBL` | RF Receiving Barcode Labels | RFINB | 90 | `rf_240` |  | RFMN |  |  |
| `RFTEST` | RF TEST | RFINB | 90 | `qw_888` |  | RFMN |  |  |
| `RESWT` | RESW Test, include zero inventory | ADPR | 160 | `ad_125t` |  | MAIN |  | 30 |
| `ZEE` | zee test program | RFINB | 90 | `rf_zee` |  | RFMN |  |  |
| `BBPRNW` | Pre-Renewal | BB | 70 | `` |  | MAIN |  |  |
| `CUOB` | Customer Occupancy Billing | BIRE | 80 | `ez_220` |  | MAIN |  | 10 |
| `ARPU` | Archive/Purge Processing | HSKE | 150 | `scr_086` |  | MAIN |  | 55 |
| `DEAR` | Delete Archive Purge | HSKE | 160 | `scr_089` |  | MAIN |  | 55 |
| `HATR` | Hold Adjusment for ITGR | ADPR | 90 | `l_em_102` | 811 | MAIN |  |  |
| `ADOREP` | Reports | ACTIVE | 110 | `` |  | MAIN |  |  |
| `INTF` | Query Interface Action Details | WO | 20 | `scr_103` |  | MAIN |  | 55 |
| `MORD` | Massive Pending Order/Receipt Delete | WO | 40 | `scr_090` |  | MAIN |  | 05 |
| `ADIP` | Adjust Inventory Process | ADPR | 240 | `ad_132` |  | MAIN |  | 30 |
| `MART` | Massive Adjustment | ADPR | 260 | `scr_109` |  | MAIN |  | 30 |
| `CHRL` | Change Inventory Level on Receipt Line | RECE | 190 | `rp_192` |  | MAIN |  | 30 |
| `RCLO` | Receipt Loading | RECE | 200 | `rp_187a` |  | MAIN |  | 10 |
| `INLD` | Inbound Load | RECE | 210 | `rp_187` |  | MAIN |  | 10 |
| `PABU` | Pallet Build (Task Assignment) | ORDE | 200 | `scr_101` | 811 | MAIN |  | 45 |
| `OPLU` | Order Line Inventory / Location Update | ORDE | 210 | `im_395` |  | MAIN |  | 05 |
| `IKCR` | Kit Component Available Report | ORDE | 220 | `kit_avail` | 811 | MAIN |  |  |
| `DCAR` | Delete Carton | ORDE | 230 | `op_197` |  | MAIN |  | 45 |
| `RETO` | Return Order | ORSP | 90 | `op_161` |  | MAIN |  | 35 |
| `COLO` | Set Up Consignee Loading | ORSP | 140 | `scr_005c` | 811 | MAIN |  |  |
| `WPIR` | Wave Pick Report | ORSP | 240 | `or_wpir` | 811 | MAIN |  | 45 |
| `ULSD` | Update load ship date | ORSP | 250 | `scr_084` | 811 | MAIN |  | 90 |
| `PBFF` | Physical versus Book Flat File Report | PHIN | 120 | `pi_204` | 811 | MAIN |  |  |
| `ALIR` | All Location Inventory Report | PHIN | 130 | `pi_121` | 811 | MAIN |  |  |
| `PPLL` | Pre Physical Location Report - LS | PHIN | 140 | `pi_121l` | L180 | MAIN |  |  |
| `AECS` | Automatic Email Setup | CURE | 60 | `scr_088` |  | MAIN |  | 10 |
| `IIHP` | Incubation Hold Profile | ITRE | 70 | `im_339a` |  | MAIN |  | 50 |
| `LTRE` | Load Type / Task Profiles | ITRE | 150 | `scr_077` |  | MAIN |  | 55 |
| `VELO` | Velocity Code Maintenance | ITRE | 160 | `ez_160` |  | MAIN |  | 05 |
| `IPUP` | Item Put-Away Parameters | ITPR | 210 | `scr_107` |  | MAIN |  | 05 |
| `WCCO` | Warehouse-Customer-Consignee OPID Rule | WALO | 150 | `im_730` |  | MAIN |  | 45 |
| `IVLP` | Item Velocity Location Profile | WALO | 160 | `im_731` |  | MAIN |  | 05 |
| `WCLC` | Warehouse-Customer-Location Config | WALO | 170 | `im_732` |  | MAIN |  | 45 |
| `INAT` | Inventory Attributes Factors | WALO | 180 | `ez_110` |  | MAIN |  | 05 |
| `ADOP` | Auto-Document Operator Printer | DORE | 10 | `scr_105` |  | MAIN |  | 15 |
| `CUDO` | Customer Workflow Document Override | DORE | 60 | `ez_180` |  | MAIN |  | 45 |
| `CUFC` | Customer Fixed Charges | BIRE | 70 | `im_520` |  | MAIN |  | 10 |
| `ICOC` | Item Consignee Configuration | MISC | 290 | `im_391` |  | MAIN |  | 45 |
| `RPRO` | Replenishment Priority Override | MISC | 300 | `im_393` |  | MAIN |  | 10 |
| `CCOR` | Customer / Consignee Outbound Rules | MISC | 310 | `im_392` |  | MAIN |  | 45 |
| `REIGTR` | Reprocess IGTR API | RECE | 90 | `l_em_103` |  | MAIN |  |  |
| `SLAS` | Shipping Lane Assignment | REPO | 990 | `la_021` |  | MAIN |  | 05 |
| `ORPACK` | Packing Slip -sample | REPO | 990 | `ORA_PACK` |  | MAIN |  |  |
| `ORBAR` | Oracle Report with Barcode | REPO | 990 | `ORABAR` |  | MAIN |  |  |
| `APBR` | Assignment-Pallet Build Report | REPO | 990 | `or_apbr` | 811 | MAIN |  | 45 |
| `LHTL` | Location Hold L4 Report - LS | REPO | 990 | `re_126l` | L180 | MAIN |  |  |
| `CYRL` | Cycle Count Report - LS | REPO | 990 | `qd_166l` | L180 | MAIN |  |  |
| `THOL` | Transaction History L1 Report - LS | REPO | 990 | `qd_185l` | L180 | MAIN |  |  |
| `THTL` | Transaction History L2 Report - LS | REPO | 990 | `qd_114l` | L180 | MAIN |  |  |
| `LHRL` | Location History L4 Report - LS | REPO | 990 | `qd_120l` | L180 | MAIN |  |  |
| `IWAR` | Item Weight by Alternate Sort Report | REPO | 990 | `qd_254` | 811 | MAIN |  | 25 |
| `OOFF` | Open Orders Flat File Report | FLAT | 50 | `ff_111` | 811 | MAIN |  |  |
| `RSFF` | Revenue Summary Flat File | FLAT | 110 | `ff_113` | 811 | MAIN |  | 55 |
| `HTFF` | Hold Transactions Flat File | FLAT | 130 | `ff_115` | 811 | MAIN |  | 55 |
| `RFRU` | RF Receiving Unsorted | RFINB | 130 | `rf_218` |  | RFMN |  |  |
| `RFRIL` | RF Reprint Inbound Label | RFINB | 150 | `rf_223` |  | RFMN |  |  |
| `RFCV` | RF Clear Receipt THL | RFINB | 170 | `rf_242` |  | RFMN |  |  |
| `OLCO` | Outbound Loading by Consignee | RFOUTB | 70 | `rf_java` |  | RFMN |  |  |
| `ADLO` | Adjust Load | RFOUTB | 100 | `rf_java` |  | RFMN |  |  |
| `RFAOL` | RF Add Order Line | RFOUTB | 110 | `rf_java` |  | RFMN |  |  |
| `RFCU` | RF Confirm UI | RFOUTB | 260 | `rf_195` |  | RFMN |  |  |
| `RFPA` | RF Pallet Code Update | RFOUTB | 270 | `rf_622` |  | RFMN |  |  |
| `RFRD` | RF Replace Damage | RFOUTB | 280 | `rf_208` |  | RFMN |  |  |
| `RFCI` | Clear Inventory Count Investigation | RFOUTB | 290 | `rf_618` |  | RFMN |  |  |
| `RFZO` | RF Zero Ship Line from Order | RFOUTB | 300 | `rf_620` |  | RFMN |  |  |
| `RFCE` | RF Customer Service Management Entry | RFINVT | 130 | `rf_200` |  | RFMN |  |  |
| `RFHO` | RF Hold Adjustment | RFINVT | 160 | `rf_215` |  | RFMN |  |  |
| `RFSUN` | RF Supervisor Notice | RFINVT | 170 | `rf_216` |  | RFMN |  |  |
| `RFITA` | Item Lookup with Available | RFLOOK | 100 | `rf_117a` |  | RFMN |  |  |
| `RFNCO` | Lookup OPID | RFLOOK | 150 | `rf_613` |  | RFMN |  |  |
| `AMN` | RF Main Menu |  | 30 | `` |  | AMN |  |  |
| `AINB` | Inbound | AMN | 10 | `` |  | AMN |  |  |
| `AIUNL` | Unloading | AINB | 10 | `rf_140a` |  | AMN |  |  |
| `AIIPS` | Add Values In | AINB | 20 | `rf_172i` |  | AMN |  |  |
| `AIECH` | Extra Charges In | AINB | 30 | `rf_140f` |  | AMN |  |  |
| `AIPU` | Put-Away | AINB | 40 | `rf_142` |  | AMN |  |  |
| `AOUTB` | Outbound | AMN | 20 | `` |  | AMN |  |  |
| `AOUTP` | Picking | AOUTB | 10 | `` |  | AMN |  |  |
| `AOPIC` | Default Picking | AOUTP | 10 | `rf_143` |  | AMN |  |  |
| `AOPK` | Wave Picking | AOUTP | 20 | `rf_601x` |  | AMN |  |  |
| `AOOPS` | Add Values Out | AOUTB | 20 | `rf_143f` |  | AMN |  |  |
| `AOECH` | Extra Charges Out | AOUTB | 30 | `rf_172o` |  | AMN |  |  |
| `AOLOD` | Loading | AOUTB | 40 | `AOLOD` |  | AMN |  |  |
| `AORFSC` | Carton Sorting | AOUTB | 50 | `rf_169a` |  | AMN |  |  |
| `AORFMG` | Merging Pallets | AOUTB | 60 | `rf_148` |  | AMN |  |  |
| `AORFRP` | Replenishment | AOUTB | 70 | `AORFRP` |  | AMN |  |  |
| `AINVT` | Inventory | AMN | 30 | `` |  | AMN |  |  |
| `AIREL` | Relocating | AINVT | 10 | `rf_139` |  | AMN |  |  |
| `AIHLD` | Hold Adjustment | AINVT | 20 | `rf_215` |  | AMN |  |  |
| `AIATT` | Adding Attributes | AINVT | 30 | `rf_201` |  | AMN |  |  |
| `ALOOK` | Look Ups | AMN | 40 | `` |  | AMN |  |  |
| `ALINV` | Inventory | ALOOK | 10 | `ALINV` |  | AMN |  |  |
| `ALRCP` | Receipt | ALOOK | 20 | `ALRCP` |  | AMN |  |  |
| `ALORD` | Order | ALOOK | 30 | `ALORD` |  | AMN |  |  |
| `ALOPID` | Outbound Pallet | ALOOK | 40 | `ALOPID` |  | AMN |  |  |
| `RFLAT` | RF LOOKUP ATTRIBUTES | RFLOOK | 90 | `rf_201q` |  | RFMN |  |  |
| `EDOL` | Enter DOL Document | ORDE | 93 | `l_em_104` |  | MAIN |  |  |
| `ENRET` | ENRE Test | RECE | 60 | `rp_101t` |  | MAIN |  |  |
| `RFDYTR` | Dynamic Tare | RFINB | 90 | `l_rf_dyntr` |  | RFMN |  |  |
| `AJRE` | Ajustes de Retencion (HOAD) | ADPR | 40 | `ad_102` |  | MAIN |  |  |
| `CINP` | Consultar Informacion de Producto (LOEN) | LOOK | 20 | `iq_105` |  | MAIN |  |  |
| `COSA` | Consultar ordenes de Salida-LOOR | ORDE | 90 | `iq_102` |  | MAIN |  |  |
| `CREC` | Consultar Recibos (LORE) | RECE | 10 | `iq_101` |  | MAIN |  |  |
| `CAJC` | Configurar-Ajustar-Asignar Carga (SELO) | ORSP | 110 | `scr_005` | 811 | MAIN |  |  |
| `COFP` | Confirmar Flujos de Pedido (CHOF) | ORDE | 70 | `op_106` |  | MAIN |  |  |
| `COFR` | Confirmar Flujos de Recibo (CHRF) | RECE | 80 | `rp_106` |  | MAIN |  |  |
| `IMBO` | Ingresar-Modificar y Borrar Orden (ENOR) | ORDE | 10 | `op_101` |  | MAIN |  |  |
| `IMBRE` | Ingresa, Modifica y Borra Recibos (ENRE) | RECE | 50 | `rp_101` |  | MAIN |  |  |
| `RCIL` | Receipt Check-In Report(Landscape) | RECE | 160 | `qd_242l` | L180 | MAIN |  | 25 |
| `CCRC` | Closed Cycle Real Count (B) Report | CYCL | 190 | `re_130b` | 811 | MAIN |  | 20 |
| `ITFF` | Inventory Activity Turns Flat File Repor | FLAT | 120 | `ff_114` | 811 | MAIN |  | 55 |
| `OSPL` | Outbound Split Order Loading Process | RFOUTB | 90 | `rf_java` |  | RFMN |  |  |
| `ENORT` | ENOR Test | ORDE | 10 | `op_101_em` |  | MAIN |  |  |
| `IQBAL` | Testing Program IQBAL | WO | 90 | `iqbal` | 811 | MAIN |  |  |
| `RFPUO` | RFPU Olivo | RFINB | 90 | `l_rf_142eo` |  | RFMN |  |  |
| `RFZEE` | Zee TEST | RFINB | 90 | `rf_zee` |  | RFMN |  |  |
| `RFRECI` | Recibo | RFINB | 20 | `rf_140a` |  | RFMN |  |  |
| `RFUBIC` | Ubicar | RFINB | 40 | `rf_142` |  | RFMN |  |  |
| `IDDE` | Imprimir Doctos Despacho-Especif (PROM) | ORDE | 50 | `pr_105` |  | MAIN |  |  |
| `RFSUP` | Surtido / Picking | RFOUTB | 10 | `rf_143` |  | RFMN |  |  |
| `RFECF` | RF Extra Charge Friasla | RFINVT | 110 | `l_rf_172` |  | RFMN |  |  |
| `IDRE` | Imprimir Doctos Recibo Especifico (PRRM) | RECE | 60 | `pr_106` |  | MAIN |  |  |
| `RNOS` | Reorganiza Nuevamente Ord. Salida (REOR) | ORDE | 20 | `pr_104` |  | MAIN |  |  |
| `FPIC` | Facturar Posterior Ingresar Cargos(ENAC) | BILL | 10 | `iv_101` |  | MAIN |  |  |
| `REUB` | Reubicar-RFRL | RFINVT | 10 | `rf_139` |  | RFMN |  |  |
| `RFREUB` | Reubicar | RFINVT | 10 | `rf_139` |  | RFMN |  |  |
| `REUBI` | Reubicar inventario (RELO) | WARR | 90 | `ad_104` |  | MAIN |  |  |
| `COLOAD` | Container load (Emergent) | RFOUTB | 130 | `rf_java` |  | RFMN |  |  |
| `RFBOXT` | RFBOXT RF BOX TASK oubound | RFOUTB | 90 | `l_rf_188em` |  | RFMN |  |  |
| `RFOUTP` | RFOUTP RF Outbound Processing | RFOUTB | 90 | `l_rf_188em` |  | RFMN |  |  |
| `RFCHB` | Unload Receiving Box to Box | RFINB | 90 | `l_kc_189a` |  | RFMN |  |  |
| `BOXP` | Conversion - Pros Data Create-BOX to BOX | CONV | 90 | `l_em_105` | 811 | MAIN |  |  |
| `BOXM` | Conversion - Pros Data Mod - BOX to BOX | CONV | 90 | `l_em_105b` | 811 | MAIN |  |  |
| `BOXL` | Conversion - Pros Data Load - BOX to BOX | CONV | 90 | `l_em_105a` | 811 | MAIN |  |  |
| `RFWCS` | RF Automation Storage | RFINB | 90 | `l_eo_621` |  | RFMN |  |  |
| `RFMX` | RF merge mixed pallet | RFOUTB | 90 | `l_rf_163em` |  | RFMN |  |  |
| `RFMV` | RF MOVE | RFINB | 90 | `rf_196` |  | RFMN |  |  |
| `RFPPAJ` | RF Pallet Picking Inventory Adjustment | RFINVT | 90 | `l_rf_166em` |  | RFMN |  |  |
| `RFBOXE` | RF BOX TASK EMERGENT | RFOUTB | 90 | `l_rf_188ex` |  | RFMN |  |  |
