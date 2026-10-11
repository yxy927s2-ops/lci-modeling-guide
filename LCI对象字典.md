# LCI 对象字典
## 1. 结构与代码含义

词组代码采用“大类码-对象码”。实际记录再加序号，如 `PKG-PEB-001`：PKG＝Packaging（包装），PEB＝PE bag（PE袋），001＝该系统中一个包装投入位置。

本字典面向酵母蛋白验收报告。各条目说明英文含义、中文对象和报告依据。英文代码为本项目约定；中文对象以来源为准。方向、位置、规格、发生状态和数值形成方式分别登记。

混合对象表按 [LCI命名规则](LCI命名规则.md) 增加性质前缀 `F` 或 `N`。本字典只定义“大类码-对象码”；前缀、位置序号和具体数据行由登记时确定。

| 性质码 | 含义 | 适用范围 |
|---|---|---|
| F | Flow，输入输出流 | 物料、水、能源、公用介质、产品、废物及排放等交换对象 |
| N | Non-flow，非流记录 | 参数、指标、观测、限值、人员人数／劳动时间、设备、资产及经济记录 |

按记录所描述的实际内容判断性质。例如废水交换量属于流，废水浓度属于非流指标；公式引用两者的数据行。人员和设备可作为活动投入条件登记，其人数、台数与物理交换数量分别处理。

### 大类码

| 大类码 | 英文含义 | 中文含义与用途 |
|---|---|---|
| MAT | Material | 生产物料，如水解糖、糖蜜、营养原料 |
| CHE | Chemical | 营养盐、化学品和处理药剂 |
| BIO | Biological material | 菌种、培养材料和酶制剂 |
| PKG | Packaging | 包装材料和容器 |
| WAT | Water | 各类水和废水，按边界登记方向 |
| ENE | Energy | 电力、蒸汽和燃料 |
| UTL | Utility | 空气、氮气等公用介质 |
| PRD | Product | 产品、副产品和可识别中间物 |
| EMG | Emission to air | 废气及具体大气排放对象 |
| WST | Waste | 废物，物态与危险性另记 |
| LAB | Labour | 人员和劳动投入 |
| EQP | Equipment | 设备类型 |
| AST | Asset | 建筑、构筑物和土地 |
| ECO | Economic record | 投资、费用与经济记录 |
| PAR | Parameter | 运行条件、计算系数及方法参数 |
| IND | Indicator | 介质属性和污染测度指标 |
| OBS | Observation | 外部环境和监测条件的观测 |
| LIM | Limit | 标准限值、批准总量等约束 |

### 报告依据索引

本表位置均指 `mineru_std/一期酵母蛋白1.1w吨阶段性验收报告（备案版）.md` 的章节或表号。

| 索引 | 报告位置 | 内容及证据角色 |
|---|---|---|
| S01 | 表3.2-1 | 项目、人数、班制、工作时间、土地和投资 |
| S02 | 表3.2-2 | 建设与配套设施对照；含设计和实际描述 |
| S03 | 表3.3-1 | 产品与副产品规模；发生状态结合工况核查 |
| S04 | 表3.4-1 | 25项生产原辅料、7项公辅药剂、13项包装；含设计、实际及未使用项 |
| S05 | 表3.5-1 | 设备数量和规格对照 |
| S06 | 第3.6节、表3.6-1、图3.6-1/2 | 水和蒸汽账、系数与计算文字 |
| S07 | 第3.7节、图3.7-1、表3.7-1/2 | 工艺对象与产污节点；提及对象未必给数量 |
| S08 | 表4.1-1 | 废气对象与排放方式 |
| S09 | 表4.1-2 | 固废数量和去向，含回用与合并项 |
| S10 | 表4.3-1、文末“三同时”登记表 | 投资汇总及分项 |
| S11 | 第6/7章 | 标准、批准总量和监测方案；区别实际数值 |
| S12 | 表7.1-1（正文第9.1节）、表9.1-2/3 | 产品与锅炉工况、监测量与负荷 |
| S13 | 表9.2-1至9.2-9 | 实测水质、废气、气象及厂界噪声 |
| S14 | 表9.2-10至9.2-12 | 年排放量核算、运行时间、负荷和公式 |
| S15 | 表9.3-1/2 | 敏感点噪声与地下水观测 |
| S16 | 附件3/4/5 | 废物合同与台账；范围和期间另核实 |

“数量表”表示来源列了数量字段，包括设计量、实际量或零；“文字”表示类型被提及；“待核实”表示名称或口径有歧义。

## 2. 输入及公用对象

### 2.1 生产物料 MAT

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| MAT-HYS | Hydrolysed sugar | 水解糖溶液；浓度另记 | S04，数量表 |
| MAT-MOL | Molasses | 糖蜜；未使用状态另记 | S04，数量表 |
| MAT-YEX | Yeast extract | 营养原料抽提物；来源牌号LA00 | S04，数量表 |

### 2.2 生物及培养材料 BIO

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| BIO-CUL | Culture / inoculum | 菌种或接种材料；株系及供给形式另记 | S07，文字 |
| BIO-MWT | Malt wort | 麦芽汁，培养基组成材料 | S07，文字 |
| BIO-AGR | Agar | 琼脂，培养基组成材料 | S07，文字 |
| BIO-ENZ | Enzyme preparation | 各类酶，来源未区分具体种类的数量 | S04，数量表 |
| BIO-PRO | Protease | 蛋白酶，工艺描述中的具体酶类型 | S07，文字 |

### 2.3 化学品 CHE

| 词组代码 | 对象码英文含义或化学式 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| CHE-NHW | Aqueous ammonia | 氨水；浓度和食品级另记 | S04 |
| CHE-MAP | Monoammonium phosphate | 磷酸二氢铵 | S04 |
| CHE-MG7 | MgSO₄·7H₂O | 七水硫酸镁；7表示结晶水数 | S04 |
| CHE-ZN7 | ZnSO₄·7H₂O | 七水硫酸锌 | S04 |
| CHE-KCL | KCl | 氯化钾 | S04 |
| CHE-CA2 | CaCl₂·2H₂O | 二水氯化钙 | S04 |
| CHE-CU5 | CuSO₄·5H₂O | 五水硫酸铜 | S04 |
| CHE-VTB | Vitamin B | 维生素B，具体组分未明 | S04 |
| CHE-DCP | D-calcium pantothenate | D-泛酸钙 | S04 |
| CHE-NIA | Niacin | 烟酸 | S04 |
| CHE-FE7 | FeSO₄·7H₂O | 七水硫酸亚铁 | S04 |
| CHE-MSG | Monosodium glutamate | 味精；纯度另记 | S04 |
| CHE-H3PO4 | H₃PO₄ | 磷酸；浓度另记 | S04 |
| CHE-H2SO4 | H₂SO₄ | 硫酸；设计量和未使用状态另记 | S04 |
| CHE-CAM | Citric acid monohydrate | 一水柠檬酸 | S04 |
| CHE-CAS | Citric acid solution | 柠檬酸溶液，如30%柠檬酸 | S04 |
| CHE-NACL | NaCl | 氯化钠；来源写无碘食用盐 | S04 |
| CHE-AFO | Antifoam | 消泡剂；成分和牌号另记 | S04 |
| CHE-ETA | Ethyl acetate | 乙酸乙酯 | S04 |
| CHE-NAOH | NaOH / caustic soda | 氢氧化钠或液碱；规格和用途另记 | S04 |
| CHE-LAC | Lactic acid | 乳酸 | S04 |
| CHE-HCL | Hydrochloric acid | 盐酸溶液 | S04 |
| CHE-ACL | Acid cleaner | 成分未明的酸性清洗剂，来源GSP-116 | S04 |
| CHE-NACO | Sodium hypochlorite | 次氯酸钠，来源GSP-131 | S04、S07 |
| CHE-PFS | Polyferric sulfate | 聚合硫酸铁；来源英文缩写写FSP | S04 |
| CHE-PAM | Polyacrylamide | 聚丙烯酰胺 | S04 |
| CHE-R134A | Refrigerant R134a | 制冷剂R134a；消耗、充注等指标另记 | S04 |
| CHE-NA2CO3 | Na₂CO₃ | 碳酸钠；配制及储罐文字，不据此认定用量 | S02、S05 |

除单列的文字条目外，本组来自S04数量表；来源发生状态分别保留。

### 2.4 包装 PKG

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| PKG-AFF | Aluminium foil film | 铝箔卷膜 | S04 |
| PKG-CTN | Carton | 纸箱，大包装纸箱 | S04 |
| PKG-PEB | PE bag | PE袋 | S04 |
| PKG-ALB | Aluminised bag | 镀铝袋 | S04 |
| PKG-KPB | Kraft paper bag | 牛皮纸袋，来源含PE内袋，按整体包装记 | S04 |
| PKG-PLD | Plastic drum | 塑料桶，含盖 | S04 |
| PKG-SWF | Stretch wrap film | 手工缠绕膜 | S04 |
| PKG-KPF | KPET film | KPET膜，保留来源材料名称 | S04 |
| PKG-POF | POF film | POF膜，保留来源材料名称 | S04 |
| PKG-LPP | Laminated paper | 淋膜纸 | S04 |
| PKG-PDR | Paper drum | 纸桶 | S04 |
| PKG-IBG | Inner bag | 内袋，解析原名“20司内袋”待核实 | S04，待核实 |
| PKG-NYB | Nylon bag | 尼龙袋 | S04 |

本组13项均对应S04包装数量表，含未使用项。废弃后的包装查WST类。未报告的新耗材投入先保留证据缺口。

### 2.5 水、能源和公用介质

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| WAT-FWT | Fresh water | 新鲜水、自来水，投入位置用序号区分 | S06 |
| WAT-PWT | Purified water | 纯水；制备、使用和交换位置另记 | S06 |
| WAT-CND | Condensate | 冷凝水；蒸汽或MVR来源、去向另记 | S06、S07 |
| WAT-CWW | Circulating cooling water | 循环冷却水，用于解释循环口径 | S06 |
| WAT-WW | Wastewater | 废水；工艺、清洗、生活等位置用序号区分 | S06、S07 |
| WAT-BRN | Concentrated reject water | 纯水制备浓水 | S06 |
| WAT-RAIN | Rainwater | 雨水；收集处理条件和去向另记 | 第4.2.1节，文字 |
| ENE-STM | Steam | 蒸汽；外供或锅炉接口另记 | S06 |
| ENE-ELE | Electricity | 电力；供电描述，不推定年度用电量 | S02，文字 |
| ENE-BGS | Biogas | 沼气；产生与利用边界另记 | S02、S07，文字 |
| UTL-AIR | Air | 发酵通风空气 | S07，文字 |
| UTL-CPA | Compressed air | 压缩空气；供应能力与用量分别记录 | S02、S05 |
| UTL-N2 | Nitrogen | 氮气；制氮和氮封描述 | S02，文字 |

### 2.6 人员 LAB

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| LAB-PER | Personnel | 人员／劳动投入；人数是本报告指标，人时需另有依据 | S01 |

## 3. 输出相关对象

### 3.1 产品与中间物 PRD

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| PRD-YPR | Yeast protein | 酵母蛋白 | S03、S12 |
| PRD-YXP | Yeast extract paste | 膏状酵母抽提物 | S03、S12 |
| PRD-YXD | Dried yeast extract | 粉状酵母抽提物 | S03、S12 |
| PRD-YDF | Yeast dietary fibre | 酵母膳食纤维 | S03、S12 |
| PRD-CWT | Cell wall | 酵母细胞壁 | S03、S07 |
| PRD-BFC | Broth concentrate | 酵母发酵液浓缩料，MVR副产物 | S03、S07 |
| PRD-YML | Yeast milk | 酵母乳，中间物；折干指标另记 | S07、第9.2.1节 |
| PRD-YBR | Yeast broth | 酵母醪液，工艺中间物 | S07，文字 |

产品系统变化时，同一物质身份保留对应词组代码，方向按边界登记。水解糖作为另一系统输出仍查MAT-HYS。中间物的收录用于识别，不自动进入系统外部输出合计。

### 3.2 废气和排放对象 EMG

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| EMG-FGS | Flue / waste gas | 废气总体，体积和体积流率分别记 | S13 |
| EMG-PM | Particulate matter | 颗粒物，含烟尘或工业粉尘；来源另记 | S08、S13、S14 |
| EMG-NMHC | Non-methane hydrocarbons | 非甲烷总烃，来源定义和计量基准另记 | S08、S13、S14 |
| EMG-VOC | Volatile organic compounds | VOCs，批准及汇总中的类别 | S11、S14 |
| EMG-NH3 | Ammonia | 氨气，与氨水投入CHE-NHW区分 | S08、S13 |
| EMG-H2S | Hydrogen sulfide | 硫化氢 | S08、S13 |
| EMG-HCG | Hydrogen chloride gas | 氯化氢气体，与盐酸溶液区分 | S08、S13 |
| EMG-SAM | Sulfuric acid mist | 硫酸雾，污染对象描述 | S07、S10，文字 |
| EMG-SO2 | Sulfur dioxide | 二氧化硫 | S08、S13、S14 |
| EMG-NOX | Nitrogen oxides | 氮氧化物，计量基准另记 | S08、S13、S14 |

本组对象的浓度、速率及年总量是不同指标，挂在同一排口对象下。臭气浓度与烟气黑度查第五部分。水中污染测度也查第五部分。

### 3.3 废物 WST

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| WST-WFM | Waste filter membrane | 废滤膜 | S09 |
| WST-SGR | Sugar residue | 糖渣，设计及发生状态另记 | S09 |
| WST-DSD | Settled dust | 沉降粉尘 | S09 |
| WST-WPK | Waste packaging | 合并废包装材料，未分材质 | S09 |
| WST-DCD | Collected dust | 除尘器收尘，回用去向另记 | S09 |
| WST-WFB | Waste filter bag | 废布袋 | S09 |
| WST-WIR | Waste ion-exchange resin | 废离子交换树脂 | S09 |
| WST-WSL | Wastewater sludge | 污水处理污泥 | S09 |
| WST-MSW | Municipal / domestic waste | 生活垃圾 | S09 |
| WST-WMO | Waste mineral oil | 废矿物油／废机油 | 第4.1.4节、S16 |
| WST-WOR | Waste oily rag | 废含油抹布，合列时保留整体数量 | S09，合列 |
| WST-WMX | Waste oil and rag mixture | 废油与含油抹布的来源合并项 | S09，合列 |
| WST-WPD | Waste plastic drum | 废塑料桶 | S16 |
| WST-WCS | Waste carbon steel | 废碳钢，含明确碳钢的废金属称呼 | S16 |
| WST-WSS | Waste stainless steel | 废不锈钢 | S16 |
| WST-WFE | Waste iron | 废铁，具体材质未明 | S16 |
| WST-WMT | Waste metal | 废金属，具体材质未明 | S16 |
| WST-WTB | Waste bulk bag | 作为废物移交的吨袋 | S16 |
| WST-DGT | Digestate | 来源合同写“沼渣”，与污泥关系待核实 | S16 |

## 4. 资产和经济对象

### 4.1 设备 EQP

以下代码对应报告设备或设施类型，实际台数、能力、尺寸和功率分别作为数量或参数记录。

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| EQP-TNK | Tank | 储罐／缓冲罐，用途和位置另记 | S05 |
| EQP-MXT | Mixing tank | 营养源配制罐 | S05 |
| EQP-AGT | Agitator | 搅拌器 | S05 |
| EQP-KBF | Carlsberg flask | 卡氏瓶／卡式瓶 | S05、S07 |
| EQP-PCT | PC culture tank | PC培养罐，保留来源简称 | S05、S07 |
| EQP-FMT | Fermentation tank | 发酵罐，种子和商品位置另记 | S05 |
| EQP-BLW | Blower | 风机 | S05 |
| EQP-PMP | Pump | 泵，供料、循环、转料等用途另记 | S05 |
| EQP-DPM | Dosing pump | 计量泵 | S05 |
| EQP-SEP | Yeast separator | 酵母分离机 | S05 |
| EQP-CEN | Centrifuge | 离心机 | S05 |
| EQP-AUT | Autolysis tank | 自溶罐 | S05 |
| EQP-EVA | Evaporation equipment | 蒸发成套设备 | S05 |
| EQP-FFE | Falling-film evaporator | 降膜蒸发器 | S05 |
| EQP-CNT | Concentration tank | 浓缩罐 | S05 |
| EQP-FIL | Membrane filtration system | 膜过滤系统，超滤／微滤名称待核实 | S05、S07 |
| EQP-SET | Settling tank | RNA沉降罐 | S05 |
| EQP-DRY | Dryer | 干燥塔 | S05 |
| EQP-PKM | Packaging machine | 包装机 | S05 |
| EQP-FLM | Filling machine | 灌装机 | S05 |
| EQP-CMP | Compressor | 空压机 | S05 |
| EQP-NGE | Nitrogen generator | PSA制氮机 | S05 |
| EQP-CHL | Chiller | 冷水机组 | S05 |
| EQP-CTW | Cooling tower / system | 冷却塔与循环冷却装置 | S02、S05 |
| EQP-MVR | Mechanical vapour recompression | MVR蒸发系统 | S05 |
| EQP-BLR | Boiler | 锅炉，燃料名称差异待核实 | S02、S12 |
| EQP-SCR | Scrubber | 洗涤塔 | S02、第4.1.1节 |
| EQP-CYC | Cyclone | 旋风分离器 | S02、第4.1.1节 |
| EQP-BHF | Baghouse filter | 布袋除尘器 | S02、第4.1.1节 |
| EQP-WDC | Water-film dust collector | 水膜除尘器 | S02、第4.1.1节 |
| EQP-WTP | Water treatment facility | 水处理设施，实际类型另记 | S02、第4.1.2节 |
| EQP-SUB | Substation | 变电设施 | S02 |

### 4.2 其他资产 AST 与投资 ECO

| 词组代码 | 对象码英文含义 | 中文对象与定义 | 报告依据 |
|---|---|---|---|
| AST-BLD | Building | 建筑物，厂房、仓库等位置分别登记 | S02 |
| AST-STR | Structure | 构筑物，如围堰、事故池和雨水池 | S02、第4.2.1节 |
| AST-LND | Land | 土地，面积与金额分别记 | S01 |
| ECO-TINV | Total investment | 项目总投资，汇总父项 | S01、S10 |
| ECO-EINV | Environmental investment | 环保投资，关联总投资 | S01、S10 |
| ECO-WINV | Wastewater investment | 废水治理投资 | S10 |
| ECO-AINV | Air-pollution investment | 废气治理投资 | S10 |
| ECO-SINV | Solid-waste investment | 固废治理投资 | S10 |
| ECO-NINV | Noise-control investment | 噪声治理投资 | S10 |
| ECO-GINV | Greening investment | 绿化及生态投资 | S10 |
| ECO-RINV | Risk-control investment | 风险防范、应急和消防投资 | S10 |
| ECO-GWIV | Groundwater-protection investment | 地下水防治与监测井投资 | S10 |
| ECO-OINV | Other investment | 来源其他投资，具体项目另记 | S10 |

## 5. 参数、指标、观测与限值

本部分描述数值含义及关系。参数可以是来源给定、实测或计算值；同一个实测数值可以被公式引用。“是否公式输入”是使用角色，“如何得到数值”是形成方式，两者分别记录。

### 5.1 运行条件和公式参数 PAR

| 词组代码 | 英文含义 | 中文含义与使用方式 | 单位或口径 | 报告依据 |
|---|---|---|---|---|
| PAR-DAYS | Operating days | 年工作天数，用于日量转年量 | d/a | S01、S06 |
| PAR-RHRS | Running hours | 年运行小时，用于速率转年量 | h/a | S14 |
| PAR-SHFT | Shift arrangement | 班制，描述人员与运行组织 | 原文班制 | S01 |
| PAR-SHRS | Hours per shift | 每班工作时间，描述班次长度 | h/班 | S01 |
| PAR-LOAD | Production load | 实际产量相对设计能力的比例；报告用于负荷折算 | %或小数，换算注明 | S12、S14 |
| PAR-WWCF | Wastewater coefficient | 用水转废水量的产污／排污系数；适用对象分别关联 | 小数或% | S06 |
| PAR-CNDR | Condensate recovery fraction | 蒸汽使用量转冷凝水量的比例，来源按80%计 | 小数或% | S06 |
| PAR-PWYR | Purified-water yield | 纯水产水率，用于纯水量与制备用水量关系 | 小数或% | S06，75% |
| PAR-WUPC | Water use per capita | 人均日用水定额，用于人数×天数×定额算生活用水 | L/(人·d) | S06，120 |
| PAR-DTMP | Temperature difference | 冷却水进出温差，参与蒸发损耗公式 | ℃ | S06 |
| PAR-EVCO | Evaporation formula coefficient | 来源蒸发公式分母600对应的计算系数；单位及适用条件随公式核实 | 原公式口径 | S06 |
| PAR-DUR | Operation duration | 培养、灭菌、自溶等持续时间 | s、min、h | S07 |
| PAR-FREQ | Cleaning / replacement schedule | 清洗或换水间隔、频率；间隔时间与操作时长分别注明 | 来源单位 | S06 |
| PAR-POW | Rated power | 设备额定功率，是设备条件；与实际电耗区分 | kW | S05 |
| PAR-CAPA | Capacity | 容量或处理能力，注明是罐容积还是处理速率 | m³、m³/h、t/h等 | S02、S05 |
| PAR-RPM | Rotational speed | 设备转速 | r/min | S05 |
| PAR-GEOM | Geometry | 设备尺寸、烟道面积、排气筒高度等几何条件 | m、m²等 | S05、S13 |
| PAR-DLIM | Detection limit | 检测方法检出限；与ND状态及替代计算关联 | 对应检测单位 | 表8.1-1、S13 |
| PAR-UPR | Unit price | 合同或台账单价，可参与金额＝数量×单价 | 元/t等 | S16 |
| PAR-TAX | Tax rate | 合同税率，描述经济计算口径 | % | S16 |

### 5.2 介质属性和污染测度 IND

| 词组代码 | 英文含义 | 中文含义与使用方式 | 单位或口径 | 报告依据 |
|---|---|---|---|---|
| IND-CONC | Concentration / content | 浓度或含量；关联具体物质和介质，注明质量/体积及干湿基 | %、mg/L、mg/m³等 | S04、S07、S13 |
| IND-TEMP | Temperature | 工艺或烟气温度，描述状态条件 | ℃ | S02、S07、S13 |
| IND-PRES | Pressure | 供水、设备或气体压力，注明绝压或表压依据 | Pa、kPa、MPa等 | S02、S05 |
| IND-VEL | Velocity | 烟气流速，描述排放状态，可参与体积流率核算 | m/s | S13 |
| IND-HUM | Moisture content | 烟气含湿量或材料含水率；对象和基准分别说明 | % | S13、S16 |
| IND-OXC | Oxygen content | 烟气含氧量，参与来源浓度折算 | % | S13 |
| IND-PH | pH | 酸碱性测度；不是一股物料 | 无量纲 | S13、S15 |
| IND-CHRM | Colour | 水的色度测度 | 稀释倍数 | S13 |
| IND-ODR | Odour concentration | 臭气浓度测度；无直接质量意义 | 来源无量纲指标 | S13 |
| IND-BLK | Smoke blackness | 烟气黑度测度 | 林格曼级 | S13 |
| IND-COD | Chemical oxygen demand | 化学需氧量；浓度或计算污染负荷，关联废水，非单一物质 | mg/L或来源负荷单位 | S13、S14 |
| IND-BOD5 | Five-day biochemical oxygen demand | 五日生化需氧量；关联废水的综合测度 | mg/L等来源单位 | S13 |
| IND-SS | Suspended solids | 悬浮物浓度或负荷指标，关联废水 | mg/L等来源单位 | S13 |
| IND-NHN | Ammonia nitrogen | 氨氮浓度或负荷指标，注明以N计 | mg/L或t/a等 | S13、S14、S15 |
| IND-TN | Total nitrogen | 总氮浓度或负荷指标，注明以N计 | mg/L等来源单位 | S13 |
| IND-TP | Total phosphorus | 总磷浓度或负荷指标，注明计量基准 | mg/L或t/a等 | S13、S14 |

污染负荷可为后续排放建模提供数据；浓度、负荷和承载它们的废水体积属于不同指标。实测浓度被公式引用时，直接关联该数据行。

### 5.3 环境与气象观测 OBS

| 词组代码 | 英文含义 | 中文含义与使用方式 | 单位或口径 | 报告依据 |
|---|---|---|---|---|
| OBS-NOIS | Noise level | 厂界或敏感点噪声，位置与昼夜另记 | Leq、dB(A) | S13、S15 |
| OBS-GWL | Groundwater level | 地下水监测井水位 | m；高程/埋深口径核实 | S15 |
| OBS-CODMN | Permanganate index | 地下水耗氧量／高锰酸盐指数，以来源方法为准 | mg/L | S15、表8.1-1 |
| OBS-SO4 | Sulfate | 地下水硫酸盐浓度，不视为项目排放量 | mg/L | S15 |
| OBS-ATMP | Ambient temperature | 监测期间气温 | ℃ | 表9.2-7 |
| OBS-APRS | Atmospheric pressure | 监测期间气压 | kPa | 表9.2-7 |
| OBS-WSPD | Wind speed | 监测期间风速 | m/s | 表9.2-7 |
| OBS-WDIR | Wind direction | 监测期间风向 | 方位 | 表9.2-7 |
| OBS-RHUM | Ambient relative humidity | 监测期间环境湿度 | % | 表9.2-7 |

地下水中的pH和氨氮分别引用IND-PH、IND-NHN，记录性质标“环境质量观测”。厂界污染物浓度关联监测位置，区别排口质量排放。

### 5.4 限值与约束 LIM

| 词组代码 | 英文含义 | 中文含义与使用方式 | 单位或口径 | 报告依据 |
|---|---|---|---|---|
| LIM-CONC | Concentration limit | 浓度标准限值，关联被限制物质或指标 | 对应指标单位 | S11、S13 |
| LIM-RATE | Emission-rate limit | 排放速率限值 | kg/h等 | S11、S13 |
| LIM-TOT | Approved total load | 批准总量或总量控制指标 | t/a等 | S11、S14 |
| LIM-QUAL | Quality / observation limit | pH范围、臭气、噪声等标准界限 | 对应指标单位 | S11、S13、S15 |

## 6. 字典登记与扩展

每个新增词组代码记录：大类、对象码英文含义、中文定义、名称索引、报告位置和证据角色。数量未给出时保留“仅文字提及”；名称有歧义时标“待核实”。

流数量和关联参数通过对象编号与数据行ID连接。字典条目存在与某条数量实际发生分别判断。
