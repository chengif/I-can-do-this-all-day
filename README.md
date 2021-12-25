

This is the source code of LiteOS-intermitter (dual-mode version in Lab). 

#### Basic feature of LiteOS-intermitter:

- support working under normal LiteOS mode
- support working under Intermittent mode
- support switch back and forth between those two modes

#### Programmer manual

1. Task creation API
   - `Int_TASK`: create task working under both normal and Intermittent mode;
   - `Nor_TASK`: creat task working only in normal mode, and will be suspended when swiching into Intermittent mode, and re-initialized when switching back.

#### Q&S

1. How to set working mode?

   Config the value of `g_sysmode`, In line 294 of  `../src/LiteOS/middleware/kernel/los_init.c`:

   - `g_sysmode = LOSCFG_NOR_MOD;` or `g_sysmode = LOSCFG_INT_MOD;`

2. How to switch mode?

   Press button2(P5.5).

   