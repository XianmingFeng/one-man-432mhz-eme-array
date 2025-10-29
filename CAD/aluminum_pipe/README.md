# Aluminum Pipe Machining Instructions

[English](#english) | [中文 (Chinese)](#中文-chinese) | [Deutsche (German)](#deutsche-german) | [日本語 (Japanese)](#日本語-japanese)

---

## English

### Overview
This directory contains all `.step` CAD files for the 6063 aluminum alloy tubes required for the antenna array. These components form the foldable Yagi booms and the main H-shaped stacking frame.

All parts must be precisely cut to length and drilled. The provided `.step` files are dimensionally accurate and can be used for both manual (DIY) manufacturing and professional CAM processing.

### General Manufacturing Recommendations

There are two primary methods to manufacture these parts:

**1. Manual (DIY) Machining**
* Parts can be cut to length with a hand saw and drilled using a hand drill or drill press.
* **Drilling Jigs (CRITICAL):** For all critical hole alignments (e.g., hinge and latch holes on the booms, hinge holes on the H-frame), it is **ESSENTIAL** to 3D print and use the corresponding drilling jigs available in the `../3d_print/drilling_jig/` directory. This ensures all folding components align and operate smoothly.
    * Use `hinge_drill_jig.step` for Yagi boom sections.
    * Use `mast_drill_jig.step` for the vertical masts.
    * Use `spreader_drill_jig.step` for the horizontal spreader.

**2. Professional (CNC) Machining**
* The `.step` files provided are **CAM-ready**.
* You can send these files directly to a machining service (e.g., for laser cutting or CNC milling) for professional and highly accurate manufacturing.

---

### Bill of Materials (BOM) & Machining Details

#### Module 1: Yagi Antenna Booms (4 Assemblies total)
These components assemble to create four individual, three-section, foldable 14-element Yagis.

| Part File (STEP)        | Material              | Qty (per Array) | Description & Machining Notes                                                                                                                                                                                                                                                     |
|:------------------------|:----------------------|:----------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yagi_boom_front.step`  | 20x20x1mm Square Tube | 4               | **Front Boom Section.** <br> • **Element Holes:** Spaced holes for antenna elements. <br> • **Hinge/Latch Holes:** Densely clustered holes at the ends for folding hinges and latches. <br> • **Jig:** Must use `hinge_drill_jig.step` for manual drilling of hinge/latch holes.  |
| `yagi_boom_middle.step` | 20x20x1mm Square Tube | 4               | **Middle Boom Section.** <br> • **Element Holes:** Spaced holes for antenna elements. <br> • **Hinge/Latch Holes:** Densely clustered holes at the ends for folding hinges and latches. <br> • **Jig:** Must use `hinge_drill_jig.step` for manual drilling of hinge/latch holes. |
| `yagi_boom_rear.step`   | 20x20x1mm Square Tube | 4               | **Rear Boom Section.** <br> • **Element Holes:** Spaced holes for antenna elements. <br> • **Hinge/Latch Holes:** Densely clustered holes at the ends for folding hinges and latches. <br> • **Jig:** Must use `hinge_drill_jig.step` for manual drilling of hinge/latch holes.   |

---
#### Module 2: H-Frame (Stacking Frame) (1 Assembly total)
These components form the main folding H-frame used to stack the four Yagi antennas.

| Part File (STEP)                    | Material              | Qty (per Array) | Description & Machining Notes                                                                                                                                                                                                                                                                                           |
|:------------------------------------|:----------------------|:----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stacking_vertical_mast.step`       | 25x25x1mm Square Tube | 4               | **Vertical Mast.** <br> • These four tubes form the two vertical "legs" of the H-frame. <br> • **Hinge Holes:** Holes at one end are for mounting the 90-degree folding hinges. <br> • **Jig:** Highly recommend using `mast_drill_jig.step` for manual drilling.                                                       |
| `stacking_horizontal_spreader.step` | 30x30x1mm Square Tube | 1               | **Horizontal Spreader.** <br> • This single, heavy-duty tube is the central horizontal spine that bears the weight of the entire array. <br> • **Hinge Holes:** Holes at both ends are for mounting the 90-degree folding hinges. <br> • **Jig:** Highly recommend using `spreader_drill_jig.step` for manual drilling. |

---
#### Module 3: Interface & Adapter Parts
This part serves as a shim or sleeve to ensure a tight fit between the booms and the mounting connectors.

| Part File (STEP)   | Material                | Qty (per Array) | Description & Machining Notes                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------|:----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `boom_sleeve.step` | 25x25x2.5mm Square Tube | 8               | **Boom Sleeve / Adapter.** <br> • This part adapts the 20x20mm Yagi boom to fit snugly inside the 25x25mm quick-release T-connectors. <br> • **Manufacture:** Simply cut the 25x25x2.5mm tube in half lengthwise (longitudinally). <br> • **Precision:** No high precision is required for this part. |

---
---

## 中文 (Chinese)

### 概览
此目录包含本天线阵列所需的所有 6063 铝合金管材的 `.step` CAD 文件。这些组件用于构成可折叠的八木天线主梁 (Yagi Booms) 和 H 型主支撑框架 (H-frame)。

所有零件都必须被精确地切割到指定长度并钻孔。所提供的 `.step` 文件尺寸精确，既可用于手动 (DIY) 制造，也可直接用于专业的 CAM 加工。

### 通用制造建议

有两种主要方法来制造这些零件：

**1. 手动 (DIY) 加工**
* 可以使用手锯切割长度，并使用手电钻或台钻钻孔。
* **钻孔夹具 (关键):** 对于所有关键的孔位对齐（例如，主梁上的铰链和锁扣孔，H 型框架上的铰链孔），**必须** 3D 打印并使用 `../3d_print/drilling_jig/` 目录中相应的钻孔夹具。这能确保所有折叠部件正确对齐且运行顺畅。
    * 八木主梁 (Yagi boom) 请使用 `hinge_drill_jig.step`。
    * 垂直梁 (Vertical mast) 请使用 `mast_drill_jig.step`。
    * 水平梁 (Horizontal spreader) 请使用 `spreader_drill_jig.step`。

**2. 专业 (CNC) 加工**
* 此目录中提供的 `.step` 文件是**符合 CAM 加工标准**的。
* 您可以将这些文件直接发送给机械加工服务商 (例如，激光切割或 CNC 铣削)，以进行专业且高精度的制造。

---

### 物料清单 (BOM) 与加工详情

#### 模块 1: 八木天线主梁 (Yagi Booms) (共 4 套)
这些组件用于组装成四根独立、三段式、可折叠的 14 单元八木天线。

| 零件文件 (STEP)             | 材料           | 阵列所需数量 | 描述与加工说明                                                                                                                                              |
|:------------------------|:-------------|:-------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `yagi_boom_front.step`  | 20x20x1mm 方管 | 4      | **主梁 - 前段。** <br> • **振子孔:** 沿主梁分布的孔洞，用于安装天线振子。 <br> • **铰链/锁扣孔:** 两端密集的孔洞，用于安装折叠铰链和弹簧锁扣。 <br> • **夹具:** 手动钻铰链/锁扣孔时，**必须**使用 `hinge_drill_jig.step`。 |
| `yagi_boom_middle.step` | 20x20x1mm 方管 | 4      | **主梁 - 中段。** <br> • **振子孔:** 沿主梁分布的孔洞，用于安装天线振子。 <br> • **铰链/锁扣孔:** 两端密集的孔洞，用于安装折叠铰链和弹簧锁扣。 <br> • **夹具:** 手动钻铰链/锁扣孔时，**必须**使用 `hinge_drill_jig.step`。 |
| `yagi_boom_rear.step`   | 20x20x1mm 方管 | 4      | **主梁 - 后段。** <br> • **振子孔:** 沿主梁分布的孔洞，用于安装天线振子。 <br> • **铰链/锁扣孔:** 两端密集的孔洞，用于安装折叠铰链和弹簧锁扣。 <br> • **夹具:** 手动钻铰链/锁扣孔时，**必须**使用 `hinge_drill_jig.step`。 |

---
#### 模块 2: H型框架 (Stacking Frame) (共 1 套)
这些组件构成了用于堆叠四根八木天线的主折叠 H 型框架。

| 零件文件 (STEP)                         | 材料           | 阵列所需数量 | 描述与加工说明                                                                                                                                                   |
|:------------------------------------|:-------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stacking_vertical_mast.step`       | 25x25x1mm 方管 | 4      | **H型架垂直梁。** <br> • 这四根管子组成了 H 型框架的两条垂直“腿”。 <br> • **铰链孔:** 一端的孔洞用于安装 90 度折叠“桌腿”铰链。 <br> • **夹具:** 手动钻孔时，**强烈建议**使用 `mast_drill_jig.step`。                 |
| `stacking_horizontal_spreader.step` | 30x30x1mm 方管 | 1      | **H型架水平梁。** <br> • 这根单独的、加强的管材是 H 型架的中央水平脊柱，承载整个阵列的重量。 <br> • **铰链孔:** 两端的孔洞用于安装 90 度折叠“桌腿”铰链。 <br> • **夹具:** 手动钻孔时，**强烈建议**使用 `spreader_drill_jig.step`。 |

---
#### 模块 3: 转接与适配零件
此零件用作垫片或套筒，以确保主梁和安装连接件之间紧密配合。

| 零件文件 (STEP)        | 材料             | 阵列所需数量 | 描述与加工说明                                                                                                                                                    |
|:-------------------|:---------------|:-------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `boom_sleeve.step` | 25x25x2.5mm 方管 | 8      | **主梁套筒 / 转接件。** <br> • 用于将 20x20mm 的八木主梁适配，使其能紧密安装在 25x25mm 内径的快装 T 型连接件中。 <br> • **制造:** 只需将 25x25x2.5mm 的管材沿长度方向（纵向）锯成两半。 <br> • **精度:** 此零件**没有高精度要求**。 |

---
---

## Deutsche (German)

### Übersicht
Dieses Verzeichnis enthält alle `.step` CAD-Dateien für die 6063-Aluminiumlegierungsrohre, die für das Antennen-Array benötigt werden. Diese Komponenten bilden die faltbaren Yagi-Antennenbäume und den H-förmigen Haupt-Stacking-Rahmen.

Alle Teile müssen präzise auf Länge zugeschnitten und gebohrt werden. Die bereitgestellten `.step`-Dateien sind maßgenau und können sowohl für die manuelle (DIY) Fertigung als auch für die professionelle CAM-Verarbeitung verwendet werden.

### Allgemeine Fertigungsempfehlungen

Es gibt zwei Hauptmethoden, um diese Teile herzustellen:

**1. Manuelle (DIY) Bearbeitung**
* Teile können mit einer Handsäge auf Länge geschnitten und mit einer Handbohrmaschine oder Ständerbohrmaschine gebohrt werden.
* **Bohrschablonen (ENTSCHEIDEND):** Für alle kritischen Lochausrichtungen (z. B. Scharnier- und Riegellöcher an den Booms, Scharnierlöcher am H-Rahmen) ist es **UNERLÄSSLICH**, die entsprechenden Bohrschablonen aus dem Verzeichnis `../3d_print/drilling_jig/` in 3D zu drucken und zu verwenden. Dies stellt sicher, dass alle Klappkomponenten ausgerichtet sind und reibungslos funktionieren.
    * Verwenden Sie `hinge_drill_jig.step` für die Yagi-Boom-Abschnitte.
    * Verwenden Sie `mast_drill_jig.step` für die vertikalen Masten.
    * Verwenden Sie `spreader_drill_jig.step` für die horizontale Traverse.

**2. Professionelle (CNC) Bearbeitung**
* Die bereitgestellten `.step`-Dateien sind **CAM-fähig**.
* Sie können diese Dateien direkt an einen Bearbeitungsservice (z. B. zum Laserschneiden oder CNC-Fräsen) senden, um sie professionell und präzise fertigen zu lassen.

---

### Stückliste (BOM) & Bearbeitungsdetails

#### Modul 1: Yagi-Antennenbäume (Insgesamt 4 Baugruppen)
Diese Komponenten werden zu vier einzelnen, dreiteiligen, faltbaren 14-Element-Yagis zusammengebaut.

| Bauteildatei (STEP)     | Material               | Menge (pro Array) | Beschreibung & Bearbeitungshinweise                                                                                                                                                                                                                                                                                            |
|:------------------------|:-----------------------|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yagi_boom_front.step`  | 20x20x1mm Vierkantrohr | 4                 | **Vorderer Boom-Abschnitt.** <br> • **Elementlöcher:** Löcher zur Montage der Antennenelemente. <br> • **Scharnier-/Riegellöcher:** Dichte Lochgruppen an den Enden für Klappscharniere und Riegel. <br> • **Bohrschablone:** Beim manuellen Bohren der Scharnier-/Riegellöcher muss `hinge_drill_jig.step` verwendet werden.  |
| `yagi_boom_middle.step` | 20x20x1mm Vierkantrohr | 4                 | **Mittlerer Boom-Abschnitt.** <br> • **Elementlöcher:** Löcher zur Montage der Antennenelemente. <br> • **Scharnier-/Riegellöcher:** Dichte Lochgruppen an den Enden für Klappscharniere und Riegel. <br> • **Bohrschablone:** Beim manuellen Bohren der Scharnier-/Riegellöcher muss `hinge_drill_jig.step` verwendet werden. |
| `yagi_boom_rear.step`   | 20x20x1mm Vierkantrohr | 4                 | **Hinterer Boom-Abschnitt.** <br> • **Elementlöcher:** Löcher zur Montage der Antennenelemente. <br> • **Scharnier-/Riegellöcher:** Dichte Lochgruppen an den Enden für Klappscharniere und Riegel. <br> • **Bohrschablone:** Beim manuellen Bohren der Scharnier-/Riegellöcher muss `hinge_drill_jig.step` verwendet werden.  |

---
#### Modul 2: H-Rahmen (Stacking Frame) (Insgesamt 1 Baugruppe)
Diese Komponenten bilden den faltbaren Haupt-H-Rahmen, der zur Stapelung der vier Yagi-Antennen verwendet wird.

| Bauteildatei (STEP)                 | Material               | Menge (pro Array) | Beschreibung & Bearbeitungshinweise                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stacking_vertical_mast.step`       | 25x25x1mm Vierkantrohr | 4                 | **Vertikaler Mast.** <br> • Diese vier Rohre bilden die beiden vertikalen "Beine" des H-Rahmens. <br> • **Scharnierlöcher:** Löcher an einem Ende zur Montage der 90-Grad-Klappscharniere. <br> • **Bohrschablone:** Beim manuellen Bohren wird dringend empfohlen, `mast_drill_jig.step` zu verwenden.                                                              |
| `stacking_horizontal_spreader.step` | 30x30x1mm Vierkantrohr | 1                 | **Horizontale Traverse.** <br> • Dieses einzelne, hochbelastbare Rohr ist das zentrale horizontale Rückgrat, das das Gewicht des gesamten Arrays trägt. <br> • **Scharnierlöcher:** Löcher an beiden Enden zur Montage der 90-Grad-Klappscharniere. <br> • **Bohrschablone:** Beim manuellen Bohren wird dringend empfohlen, `spreader_drill_jig.step` zu verwenden. |

---
#### Modul 3: Schnittstellen- & Adapterteile
Dieses Teil dient als Distanzstück oder Hülse, um einen festen Sitz zwischen den Booms und den Montageverbindern zu gewährleisten.

| Bauteildatei (STEP) | Material                 | Menge (pro Array) | Beschreibung & Bearbeitungshinweise                                                                                                                                                                                                                                                            |
|:--------------------|:-------------------------|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `boom_sleeve.step`  | 25x25x2.5mm Vierkantrohr | 8                 | **Boom-Hülse / Adapter.** <br> • Passt den 20x20mm Yagi-Boom an, damit er fest in die 25x25mm Schnellverschluss-T-Verbinder passt. <br> • **Herstellung:** Das 25x25x2.5mm Rohr einfach der Länge nach halbieren. <br> • **Präzision:** Für dieses Teil ist keine hohe Präzision erforderlich. |

---
---

## 日本語 (Japanese)

### 概要
このディレクトリには、アンテナアレイに必要なすべての 6063 アルミニウム合金チューブの `.step` CADファイルが含まれています。これらのコンポーネントは、折りたたみ式の八木アンテナブームと、H型メイン・スタッキングフレームを構成します。

すべての部品は、指定された長さに正確に切断し、穴あけ加工する必要があります。提供される `.step` ファイルは寸法が正確であり、手動 (DIY) での製造と、専門的なCAM（キャム）加工の両方に使用できます。

### 一般的な製造推奨事項

これらの部品を製造するには、主に2つの方法があります。

**1. 手動 (DIY) 加工**
* 部品は手鋸で長さに切断し、ハンドドリルやボール盤で穴をあけることができます。
* **穴あけ治具 (重要):** すべての重要な穴の位置合わせ（例: ブームのヒンジやラッチの穴、Hフレームのヒンジ穴）には、`../3d_print/drilling_jig/` ディレクトリにある対応する穴あけ治具を3Dプリントして**必ず使用**してください。これにより、すべての折りたたみコンポーネントが正しく位置合わせされ、スムーズに動作することが保証されます。
    * 八木ブーム（Yagi boom）には `hinge_drill_jig.step` を使用します。
    * 垂直マスト（Vertical mast）には `mast_drill_jig.step` を使用します。
    * 水平スプレッダー（Horizontal spreader）には `spreader_drill_jig.step` を使用します。

**2. 専門業者 (CNC) 加工**
* 提供されている `.step` ファイルは**CAM対応**です。
* これらのファイルを（レーザーカットやCNCフライス加工などの）機械加工サービスに直接送信して、専門的かつ高精度に製造してもらうことができます。

---

### 部品表 (BOM) と加工詳細

#### モジュール 1: 八木アンテナブーム (Yagi Booms) (合計 4 セット)
これらのコンポーネントは、4本（それぞれ3セクションで構成される）の折りたたみ式14エレメント八木アンテナを組み立てるために使用されます。

| パーツファイル (STEP)          | 材質             | アレイあたりの数量 | 説明と加工ノート                                                                                                                                                                                        |
|:------------------------|:---------------|:----------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yagi_boom_front.step`  | 20x20x1mm 角パイプ | 4         | **ブーム - フロントセクション。** <br> • **エレメント用の穴:** アンテナエレメント（素子）を取り付けるための穴。 <br> • **ヒンジ/ラッチ用の穴:** 両端に集中している穴は、折りたたみヒンジとラッチ用。 <br> • **治具:** 手動でヒンジ/ラッチの穴をあける際は、**必ず** `hinge_drill_jig.step` を使用してください。 |
| `yagi_boom_middle.step` | 20x20x1mm 角パイプ | 4         | **ブーム - ミドルセクション。** <br> • **エレメント用の穴:** アンテナエレメント（素子）を取り付けるための穴。 <br> • **ヒンジ/ラッチ用の穴:** 両端に集中している穴は、折りたたみヒンジとラッチ用。 <br> • **治具:** 手動でヒンジ/ラッチの穴をあける際は、**必ず** `hinge_drill_jig.step` を使用してください。  |
| `yagi_boom_rear.step`   | 20x20x1mm 角パイプ | 4         | **ブーム - リアセクション。** <br> • **エレメント用の穴:** アンテナエレメント（素子）を取り付けるための穴。 <br> • **ヒンジ/ラッチ用の穴:** 両端に集中している穴は、折りたたみヒンジとラッチ用。 <br> • **治具:** 手動でヒンジ/ラッチの穴をあける際は、**必ず** `hinge_drill_jig.step` を使用してください。   |

---
#### モジュール 2: Hフレーム (Stacking Frame) (合計 1 セット)
これらのコンポーネントは、4本の八木アンテナをスタックするために使用される、メインの折りたたみ式Hフレームを構成します。

| パーツファイル (STEP)                      | 材質             | アレイあたりの数量 | 説明と加工ノート                                                                                                                                                                               |
|:------------------------------------|:---------------|:----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stacking_vertical_mast.step`       | 25x25x1mm 角パイプ | 4         | **垂直マスト。** <br> • これら4本のパイプがHフレームの2本の垂直な「脚」を構成します。 <br> • **ヒンジ用の穴:** 一方の端にある穴は、90度折りたたみヒンジを取り付けるためのものです。 <br> • **治具:** 手動で穴をあける際は、`mast_drill_jig.step` の使用を**強く推奨**します。             |
| `stacking_horizontal_spreader.step` | 30x30x1mm 角パイプ | 1         | **水平スプレッダー。** <br> • この1本の頑丈なパイプは、アレイ全体の重量を支える中央の水平な背骨となります。 <br> • **ヒンジ用の穴:** 両端にある穴は、90度折りたたみヒンジを取り付けるためのものです。 <br> • **治具:** 手動で穴をあける際は、`spreader_drill_jig.step` の使用を**強く推奨**します。 |

---
#### モジュール 3: インターフェースとアダプター部品
この部品は、ブームと取り付けコネクタ間の確実な固定を保証するためのシム（詰め物）またはスリーブとして機能します。

| パーツファイル (STEP)     | 材質               | アレイあたりの数量 | 説明と加工ノート                                                                                                                                                                   |
|:-------------------|:-----------------|:----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `boom_sleeve.step` | 25x25x2.5mm 角パイプ | 8         | **ブームスリーブ / アダプター。** <br> • 20x20mmの八木ブームを、内径25x25mmのクイックリリースT型コネクタにぴったりと適合させます。 <br> • **製造:** 25x25x2.5mmのパイプを長手方向に沿って半分に切断するだけです。 <br> • **精度:** この部品に**高い精度は要求されません**。 |