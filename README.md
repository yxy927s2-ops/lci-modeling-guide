# LCI 前景模型构建指南 / LCI Foreground Model Building Guide

[中文](#中文) | [English](#english)

<a id="中文"></a>

## 中文

本项目以工业报告、原始清单及其解析结果为证据，构建可追溯的生命周期清单（LCI）前景模型。先明确活动，再用输入输出流连接活动，并把原始数量填入各活动清单。

当前有 **四份核心文件：三份 Markdown 规范和一份 Excel 模板**。本 README 是使用入口，介绍它们如何配合；具体定义以对应规范为准。

## 1. 四份文件的分工

| 核心文件 | 解决的问题 | 使用结果 |
| --- | --- | --- |
| [LCI命名规则.md](LCI命名规则.md) | 如何识别对象、确定同一对象、分配编号，并区分流与非流数据 | 稳定的对象编号和可追溯的数据行编号 |
| [LCI对象字典.md](LCI对象字典.md) | 对象属于哪一类、采用什么英文编码、编码含义是什么 | 有明确含义的“大类码＋对象码” |
| [LCI流关系与工艺建模规范.md](LCI流关系与工艺建模规范.md) | 如何识别活动、确定流的输出端和输入端、组织活动清单及核查 | 活动骨架、流关系和建模步骤 |
| [LCI前景模型清单.xlsx](LCI前景模型清单.xlsx) | 上述信息填写在哪里、如何形成可查看的模型清单 | 原始证据、对象、活动、关系、活动输入输出和核查记录 |

命名规则与字典共同确定对象身份；建模规范确定对象与活动的关系；Excel 承载这些信息及其证据。四份文件共同构成建模指南，填写后的 Excel 才是具体产品系统的模型成果。

## 2. 模型中各类信息的关系

- **原始数据**是事实和证据：原文、数量、单位、期间、工况、位置描述及来源定位。原始数据表不分配模型编号。
- **对象**是从证据中识别出的事物或指标，包括输入输出流，以及人员、设备、参数、观测指标等非流对象。
- **数据行**记录对象的一条具体数值或描述。同一对象可以有多条数据，例如设计量、实测量、不同期间或不同来源的记录。
- **活动**是执行功能的过程，例如发酵、分离。设备及位置用于描述活动，设备名称本身不等于活动。
- **流关系**记录某条流从哪个输出活动流出、进入哪个输入活动，或连接到哪个环境端点。
- **活动清单**按活动分别列出输入与输出，并引用对应数据行，呈现原始数量及其依据。

活动构成模型骨架，流把活动连接起来，数据行给流附上数量，原始证据支持上述识别和连接。

### 编号分别指什么

| 编号 | 含义 | 示例 |
| --- | --- | --- |
| 对象编号 | 标识“哪一种东西、在哪个投入或产出位置”；例如同一位置投入的水解糖 | `MAT-HYS-001` |
| 混合对象表中的显示编号 | 用 `F` 区分流，用 `N` 区分非流对象 | `F-MAT-HYS-001`、`N-PAR-DAYS-001` |
| 数据行 ID | 对象的一条具体数值或描述 | `R0001` |
| 活动 ID | 产品系统内的一个活动 | `A0001` |
| 连接 ID | 一条流关系 | `C0001` |

上述示例仅说明格式，不代表已完成实际报告数据的编号。对象编号中的序号用于区分同类对象在不同位置或接口的身份；同一对象的不同观测值用不同数据行 ID 记录。产品系统作为索引范围登记在表头及相应字段中。

## 3. 按 Excel 的七张工作表构建模型

先复制模板作为具体产品系统的工作文件，再依次开展以下工作。原始模板保留为空白模板。**各数据 Sheet 逐张交付核查；上一张经用户确认后，再制作下一张，不一次性填完全部工作表。**

### 第一步：说明——确定本次模型的范围

填写产品系统、目标产品、系统边界、资料范围和期间，以及所用规则、字典、建模规范和模板版本。

本阶段整理原始清单。若数据存在不同数量基准，先逐条注明，后续再统一功能单位。

### 第二步：原始数据表——摘录证据

**在约定的报告范围内，必须将几乎所有数值先抓取到原始数据表，不按当前是否属于流、是否有建模用途提前筛选。** 正文、表格、图示、注释和附录中的数量、比例、范围、日期、设计值、实测值、参数、设备和人员数据等，连同单位、文字描述及前后文一起保留。登记文件、页码、表号或图号、行列等来源定位；后续在对象表中分类、编号并说明用途。

页码、章节号、表图编号等版式定位数字作为来源信息登记，无须逐个建立数据项；确实不收取的内容列明范围和理由。重复数值保留各自出处，未检出、未报告及区间表达保留原状。

保留原文对来源、去向、位置、期间和工况的描述。解析结果用于查找；表格错位、单位不清或上下文有歧义时，回到原始文件确认。原始数据表不加入对象、活动或连接编号。

### 第三步：对象表——逐项登记“这是什么”和“记录了什么”

逐条查看已核查的原始数据，先写清这条记录描述什么，再查字典并分配对象编号。流加 `F`，非流对象加 `N`。每一项具体数值或描述另分配数据行 ID，并填写它在原始数据表中的位置。

例如，某一加料位置的水解糖是一个对象；报告给出的设计投入量和实测投入量是这个对象的两条数据。两条记录使用同一对象编号、不同数据行 ID。另一加料位置的水解糖另设对象编号。以上仅是说明，不是实际报告数据。

同一流有多条原始数量时，全部保留为不同数据行，不预先选出唯一采用值。人员、设备、工作天数、浓度、排放限值等按性质登记；它们可以描述活动或支持后续计算，不自动成为输入输出流。

字典未覆盖的新对象，先保留原名并标记待分类，再依据来源补充含义和编码。字典中的条目也不意味着该产品系统实际存在这项投入或产出。

### 第四步：活动表——建立活动骨架

根据原始数据中的工艺描述、设备功能和位置说明识别活动，登记活动 ID、名称、功能、粒度、覆盖范围及证据。

对象识别和活动识别都来自原始证据；核查发现需要补充时，返回前一张表修订并重新确认。只有整体数据时，先建立对应的汇总活动；粒度或边界不清时，保留待核实状态。

同类活动或同一工艺段的活动可以安排在同一 Sheet 的不同区块，分别保留活动 ID 和输入输出。**放在同一 Sheet 是展示分组，不代表合并活动或数量。**

### 第五步：流关系表——把流与活动连接起来

从对象表识别出的流中，确定每条关系的输出活动和输入活动，登记连接 ID、流编号及对应数据行 ID。

保留原文的来源与去向说法，并注明映射依据：原文明确、依据上下文还原、建模假设或待核实。端点尽量采用可比较的活动层次，数据不支持细分时保留原有范围。

- 活动之间的流：连接输出活动与输入活动。
- 从自然界取得的资源：连接环境资源端点与输入活动。
- 直接排入自然界的排放：连接输出活动与环境端点，并注明空气、水、土壤等介质。
- 产品、副产品及送往外部处理的废物：登记已知去向；去向不清时保留待核实端点。

同一内部交换可在输出活动和输入活动的清单中分别出现，两端引用同一连接关系，不能在系统总量中重复计入。当前优先明确物理来源与去向，分配、替代和背景数据库匹配后续开展。

### 第六步：清单——按活动列出全部输入输出

每个活动单独设置表头及“输入”“输出”两个区域。表头写一次活动名称、ID、产品系统、覆盖范围、期间和数量基准；明细行列出流编号、名称、原始数量、原单位、来自或去往、状态、数量基准、期间或工况、数据行 ID 和来源定位。

模板预留两个活动区块，可继续向下增加；不同活动组可复制工作表，并放在核查表之前。流关系的完整登记保留在流关系表，活动页面以输入输出清单为主。

数量通过数据行 ID 引用对象表。**当前不设置数量处理表，不选取唯一采用值，不统一单位或功能单位。** 同一流的多个原始值分别列行，注明各自依据；不能把不同期间、工况或基准的数据直接相加。

模板现有数量引用范围为对象表第 7—106 行；对象数据超过该范围时，同步扩展引用范围。需要后续换算时，在活动清单中保留原值、原单位及换算依据。

### 第七步：核查表——检查模型是否有依据、是否连接完整

核查对象和数据行编号、证据定位、活动范围、流端点、原值与单位、多来源冲突、重复总量及共享投入。缺失、未报告、未检出和零值分别记录。

具备可比较单位、期间、数量基准及完整边界时，再进行相关平衡核查；条件不足时登记缺口。核查结果应明确哪些关系已确认，哪些数量或端点仍待核实。

## 4. 逐表交付与防止漏编

### 交付顺序

说明页随第一批交付，明确本次整理范围。各数据表按以下顺序逐张交付：

| 批次 | 本次交付 | 用户核查重点 |
| --- | --- | --- |
| 1 | 原始数据表 | 约定范围内的原文数据是否收取完整，数值、单位、上下文及来源是否准确 |
| 2 | 对象表 | 每项证据是否有去向，对象是否分对类，是否漏编或重复编号 |
| 3 | 活动表 | 活动是否齐全，功能、位置和覆盖范围是否符合原文 |
| 4 | 流关系表 | 每条流从哪里来、到哪里去，端点及映射依据是否清楚 |
| 5 | 清单：按活动组逐 Sheet 交付 | 各活动的输入输出是否齐全，原值、单位和来源是否对应 |
| 6 | 核查表 | 汇总各阶段检查结果、修订情况及剩余缺口 |

每批交付当前累计工作簿，指出本次新增或修订的 Sheet；后续未开展的表保持空白，并在说明页注明进度。收到用户核查意见后修订；用户确认该批次后才进入下一批。各阶段即时记录检查结果，最后交付完整核查表。全部确认后，汇总工作簿形成前景模型清单。

### 怎样发现漏收、漏编和漏列

编号不会自动保证完整。需要沿着原文逐项核对，而不是只检查编号是否连续。

1. **原文到原始数据表：检查漏收。** 列出本批处理的文件、章节、页码和表图范围，逐页、逐表图核对几乎所有数值是否已收取，不仅检查输入输出流；解析失败、尚未处理或明确排除的范围及理由单独列出。
2. **原始数据表到对象表：检查漏编。** 对每条原始记录中的每项数据，登记其处理结果：已关联对象及数据行 ID、待分类，或不纳入对象表及理由。一个原始单元格包含多项数据时分别登记；重复证据保留对应关系。
3. **待分类项：保留可查的缺口。** 尚不能确定对象代码时，先保留原名、来源和数据行 ID，明确标记“待分类／待编号”，不随意套码。交付时单独列出，不能隐藏在空白单元格中，也不能称为编号已齐全。
4. **对象表到流关系表和清单：检查漏列。** 每条流数据都应有对应关系和清单位置，或者明确记录待连接、范围外等状态及理由。非流参数、人员、设备等保留在对象表，关联相应活动或用途。
5. **反向检查错误引用。** 每个清单数据行 ID 能找到对象表记录，每个对象记录能回到原始证据；同时检查数据行 ID 重复、对象编号误复用、空编号和错误来源。

对象表的交付核查应包含一份覆盖对照，写明原始数据表的 Sheet／单元格或行列、对应对象编号及数据行 ID、处理状态和理由。这是追溯定位，不给原始数据表新增模型编号。覆盖对照可附在对象表中，检查结论写入核查表。

完整性按约定的来源范围逐项确认；存在未处理或待编号数据时，交付中明确列出，不能仅凭总行数或编号连续声称完整。

这份成果构成可追溯的前景物理模型。进入后续计算前，再确定参考数量及功能单位，统一数量基准，匹配上游背景数据库和环境流，并依据研究方法处理多功能过程的分配或替代。产品输出的登记本身不决定其分配系数或可替代对象。

当前四份核心文件是规范和空白模板，尚未完成实际报告数据填入，因此不能视为已经建成或可直接计算环境结果的产品模型。

## 5. 项目文件与版本管理

- `原始数据/`：原始报告等证据文件，保持原件。
- `mineru_std/`：报告解析结果，辅助查找和提取。
- 项目根目录：保留四份核心文件的最新版本和本 README。
- `归档/`：保存历史版本及备份。
- `LC命名规则记录/`（本地项目记录，本发布包不包含）：保存版本改进、制定经验和使用记录。

生成新版本时，前一版放入归档，改动原因与经验另写记录；同步更新本 README 的文件链接。具体模型文件也采用清晰的产品系统名称和版本号，避免覆盖已有成果。

---

<a id="english"></a>

## English

### LCI Foreground Model Building Guide

This project uses industrial reports, source inventories, and parsed documents as evidence to build a traceable life cycle inventory (LCI) foreground model. Identify activities, connect them through input and output flows, and attach the reported quantities to each activity inventory.

There are **four core files: three Markdown specifications and one Excel template**. This README explains how to use them together. Refer to the relevant specification for detailed definitions. The English section corresponds to the Chinese guide; the core documents, filenames, and worksheet names remain in Chinese.

### 1. Roles of the Four Core Files

| Core file | Question it answers | Result |
| --- | --- | --- |
| [LCI命名规则.md](LCI命名规则.md) — Naming rules | How are objects identified, distinguished, and assigned IDs? How are flows separated from non-flow records? | Stable object IDs and traceable data-row IDs |
| [LCI对象字典.md](LCI对象字典.md) — Object dictionary | Which category and object code apply, and what does each code mean? | Defined category and object codes |
| [LCI流关系与工艺建模规范.md](LCI流关系与工艺建模规范.md) — Flow relationships and process modeling specification | How are activities identified, flow endpoints determined, inventories organized, and checks performed? | Activity structure, flow connections, and modeling steps |
| [LCI前景模型清单.xlsx](LCI前景模型清单.xlsx) — Foreground inventory workbook | Where is the information recorded, and how does it become a model inventory? | Source evidence, objects, activities, connections, activity inputs and outputs, and check results |

The naming rules and dictionary define object identity. The modeling specification defines the relationships between objects and activities. Excel holds the records and their evidence. These four files provide the guide; a completed workbook is the model deliverable for a specific product system.

### 2. How the Records Relate

- **Raw data** are source facts and evidence: text, quantities, units, periods, operating conditions, locations, and source references. The raw data sheet has no model IDs.
- **Objects** are the things or indicators identified in the evidence. They include input and output flows, as well as non-flow objects such as personnel, equipment, parameters, and observed indicators.
- **Data rows** record individual values or descriptions for an object. One object can have several rows for design values, measured values, different periods, or different sources.
- **Activities** are operations that perform a function, such as fermentation or separation. Equipment and locations describe an activity; an equipment name alone does not define an activity.
- **Flow relationships** identify the activity a flow leaves and the activity it enters, or its environmental endpoint.
- **Activity inventories** list inputs and outputs for each activity and reference the corresponding data rows to show reported quantities and their evidence.

Activities form the model structure. Flows connect activities. Data rows attach quantities to flows. Source evidence supports the identification and connections.

#### What Each ID Identifies

| ID | Meaning | Example |
| --- | --- | --- |
| Object ID | The type of thing and its input or output location; for example, hydrolyzed sugar added at one feed point | `MAT-HYS-001` |
| Display ID in a mixed object sheet | `F` identifies flows; `N` identifies non-flow objects | `F-MAT-HYS-001`, `N-PAR-DAYS-001` |
| Data-row ID | One specific value or description for an object | `R0001` |
| Activity ID | One activity within a product system | `A0001` |
| Connection ID | One flow relationship | `C0001` |

These examples explain the format; they are not assignments to actual report data. The sequence in an object ID distinguishes objects of the same type at different locations or interfaces. Different observations of the same object have different data-row IDs. Record the product system in the relevant headers and fields to define the ID scope.

### 3. Build the Model Using the Seven Worksheets

Copy the template to create a working file for the product system. Keep the original template blank. **Deliver each data worksheet for review separately. Prepare the next worksheet only after the user confirms the preceding one; do not complete all worksheets in a single batch.**

#### Step 1: 说明 — Define the Scope

Record the product system, target product, system boundary, source coverage, period, and the versions of the rules, dictionary, modeling specification, and template used.

At this stage, organize the reported inventory. If quantities use different bases, record each basis separately. Align the functional unit later.

#### Step 2: 原始数据表 — Collect the Evidence

**Within the agreed report coverage, collect nearly all numerical values before deciding whether they are flows or useful for modeling.** Include quantities, ratios, ranges, dates, design values, measurements, parameters, equipment data, and personnel data from the main text, tables, figures, notes, and appendices. Preserve units, descriptions, and context. Record the file, page, table or figure number, and row or column location. Classify, assign IDs, and determine uses later in the object sheet.

Page numbers, section numbers, and table or figure labels are source-location metadata and do not need separate data entries. State the scope and reason for any deliberate exclusion. Keep the source of each repeated value. Preserve non-detects, unreported values, and ranges as reported.

Retain source descriptions of origin, destination, location, period, and operating conditions. Use parsed documents to find information. Check the original file when tables are misaligned, units are unclear, or context is ambiguous. Do not add object, activity, or connection IDs to the raw data sheet.

#### Step 3: 对象表 — Record What Each Item Is and What Was Reported

Review each confirmed source record. Describe what it refers to, consult the dictionary, and assign an object ID. Prefix flows with `F` and non-flow objects with `N`. Assign a separate data-row ID to each specific value or description and record its location in the raw data sheet.

For example, hydrolyzed sugar at one feed point is one object. Its reported design input and measured input are two data rows with the same object ID and different data-row IDs. Hydrolyzed sugar at another feed point receives a different object ID. This is an illustration, not actual report data.

Keep all reported quantities for a flow as separate data rows. Do not select a single adopted value in advance. Classify personnel, equipment, operating days, concentrations, and emission limits by their nature. They can describe activities or support later calculations without becoming input or output flows automatically.

If the dictionary does not cover an object, retain its original name, mark it as pending classification, and add a definition and code based on evidence. A dictionary entry does not establish that the product system actually has that input or output.

#### Step 4: 活动表 — Establish the Activity Structure

Identify activities from process descriptions, equipment functions, and location descriptions. Record each activity's ID, name, function, level of detail, coverage, and evidence.

Both object and activity identification depend on source evidence. If review reveals missing information, revise the preceding sheet and seek confirmation again. If only aggregate data are available, establish an activity at that aggregate scope. Keep unclear activity boundaries or levels of detail pending verification.

Activities of the same type or process section can share a worksheet in separate blocks, each with its own ID, inputs, and outputs. **Grouping activities on one worksheet is a presentation choice; it does not merge activities or quantities.**

#### Step 5: 流关系表 — Connect Flows to Activities

For each flow identified in the object sheet, determine the activity it leaves and the activity it enters. Record the connection ID, flow ID, and corresponding data-row IDs.

Preserve the original descriptions of origin and destination. State whether the mapping is explicit in the source, reconstructed from context, a modeling assumption, or pending verification. Use comparable activity levels where possible. Retain the reported scope when the evidence does not support a finer split.

- Between activities: connect the output activity to the input activity.
- Resources taken from nature: connect an environmental resource endpoint to the input activity.
- Direct releases to nature: connect the output activity to an environmental endpoint and state the compartment, such as air, water, or soil.
- Products, co-products, and waste sent for external treatment: record the known destination; keep unknown destinations pending verification.

An internal exchange can appear in both the output activity inventory and the input activity inventory. Both views refer to the same connection; do not count it twice in system totals. Establish physical origins and destinations first. Allocation, substitution, and background database matching follow later.

#### Step 6: 清单 — List All Inputs and Outputs by Activity

Give each activity a header and separate input and output sections. State the activity name, ID, product system, coverage, period, and quantity basis once in the header. Each detail row records the flow ID, name, reported quantity, original unit, origin or destination, status, quantity basis, period or operating conditions, data-row ID, and source location.

The template provides two activity blocks. Add more blocks below as needed. Copy worksheets for different activity groups and place them before the check sheet. Keep the full connection records in the flow relationship sheet; the activity pages present input and output inventories.

Quantities reference the object sheet through data-row IDs. **At this stage, there is no separate quantity-processing sheet, no selection of a single adopted value, and no unit or functional-unit alignment.** List multiple reported values for the same flow in separate rows and state their respective bases. Do not add values from incompatible periods, operating conditions, or quantity bases.

The template currently references rows 7–106 of the object sheet for quantities. Extend the references when records exceed this range. When conversions are needed later, preserve the original values, units, and conversion basis in the activity inventory.

#### Step 7: 核查表 — Check Evidence and Model Connections

Check object and data-row IDs, source locations, activity coverage, flow endpoints, original values and units, conflicting sources, duplicate totals, and shared inputs. Distinguish missing data, unreported values, non-detects, and zero.

Perform applicable balance checks only when units, periods, quantity bases, and boundaries are sufficiently comparable and complete. Otherwise, record the gaps. State which relationships are confirmed and which quantities or endpoints remain pending verification.

### 4. Deliver Worksheets Separately and Check for Omissions

#### Delivery Order

Include the introduction sheet with the first delivery to define the scope. Deliver data worksheets in this order:

| Batch | Deliverable | User review focus |
| --- | --- | --- |
| 1 | Raw data sheet — 原始数据表 | Coverage of the agreed source scope; accuracy of values, units, context, and source locations |
| 2 | Object sheet — 对象表 | Disposition of each evidence item; correct classification; missing or duplicate IDs |
| 3 | Activity sheet — 活动表 | Complete activities; source-supported functions, locations, and coverage |
| 4 | Flow relationship sheet — 流关系表 | Origins, destinations, endpoints, and mapping evidence |
| 5 | Inventories — 清单, one activity-group worksheet at a time | Complete activity inputs and outputs; correct original values, units, and references |
| 6 | Check sheet — 核查表 | Consolidated check results, revisions, and remaining gaps |

Deliver the current cumulative workbook with each batch and identify the new or revised worksheet. Leave future worksheets blank and state progress in the introduction sheet. Revise after user review. Proceed to the next batch only after the user confirms the current batch. Record checks during each stage and deliver the complete check sheet last. After all batches are confirmed, the consolidated workbook becomes the foreground model inventory.

#### Detect Missing Extraction, IDs, and Inventory Entries

IDs do not guarantee completeness. Compare records against the source item by item instead of checking only whether IDs are consecutive.

1. **Source to raw data: check extraction coverage.** List the files, sections, pages, tables, and figures covered by the batch. Check nearly all numerical values page by page and table or figure by table or figure, including non-flow data. List parsing failures, unprocessed areas, and explicit exclusions with reasons.
2. **Raw data to objects: check ID coverage.** Record the disposition of each data item: linked to an object and data-row ID, pending classification, or excluded from the object sheet with a reason. Separate multiple data items within one source cell. Retain mappings for duplicate evidence.
3. **Pending classification: keep gaps visible.** If an object code cannot yet be determined, retain the original name, source, and data-row ID. Mark it as pending classification or ID assignment. Do not force a code. List these items in the delivery rather than hiding them in blank cells or claiming complete ID coverage.
4. **Objects to connections and inventories: check missing entries.** Each flow data row must have a connection and inventory location, or an explicit status and reason, such as pending connection or outside scope. Retain non-flow parameters, personnel, and equipment in the object sheet and link them to the relevant activity or use.
5. **Check references in reverse.** Each inventory data-row ID must resolve to an object-sheet record, and each object record must trace back to source evidence. Check duplicate data-row IDs, incorrect reuse of object IDs, blank IDs, and incorrect sources.

Object-sheet review must include a coverage mapping: the raw data sheet and cell or row/column location, corresponding object and data-row IDs, processing status, and reason. This is a traceability reference; it does not add model IDs to the raw data sheet. Include the mapping in the object sheet and record conclusions in the check sheet.

Verify completeness item by item within the agreed source coverage. Explicitly list unprocessed records and pending IDs. Row counts or consecutive IDs alone do not establish completeness.

The resulting deliverable is a traceable physical foreground model. Before subsequent calculations, define the reference quantity and functional unit, align quantity bases, match upstream background datasets and environmental flows, and handle allocation or substitution for multifunctional processes according to the research method. Recording a product output does not by itself determine an allocation factor or a displaced product.

The four core files currently contain specifications and a blank template. Actual report data have not yet been entered, so they do not constitute a completed product model or one ready for environmental impact calculation.

### 5. Project Files and Version Management

- `原始数据/`: original reports and other evidence; preserve the originals.
- `mineru_std/`: parsed report files for searching and extraction.
- Project root: the latest four core files and this README.
- `归档/`: historical versions and backups.
- `LC命名规则记录/` (local project records; not included in this package): changes, lessons, and usage records.

When producing a new version, archive the preceding one. Record changes and lessons separately and update README links. Name specific model workbooks with a clear product-system name and version to avoid overwriting earlier deliverables.
