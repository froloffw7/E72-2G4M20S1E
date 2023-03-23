TI SimpleLink cc13xx/cc26xx SDK 6.40.00.13 doesn't save correlation value from coprocessor and doesn't provide source code for rxPayloadIsr() 
(ti/simplelink_cc13xx_cc26xx_sdk_6_40_00_13/source/ti/ti154stack/low_level/cc13xx/mac_rx.c)

To activate LQI adjusting according to correlation value I have to patch object module (maclib_nosecure_cc13x2_2_4g_tirtos7.a:mac_rx.o)

| Address | OpCode | Mnemonic      | Patch | Assembler       |
|---------|--------|---------------|-------|-----------------|
| 10800   | 565c   | ldrb r6,...   | 565a  | ldrh r6,...     |
| 1087a   | 0021   | movs r1,#0x00 | 370a  | lsrs r7,r6,#0x8 |
| 1087c   | 0027   | movs r7,#0x00 | 3900  | movs r1,r7      |
