# Printing Instructions

[English](#english) | [中文 (Chinese)](#中文-chinese) | [Deutsche (German)](#deutsche-german) | [日本語 (Japanese)](#日本語-japanese)

---

## English

### Parts
* `feed_box_front.step`
* `feed_box_middle.step`
* `feed_box_rear.step`
* `feed_box_isolator.step`

### Purpose
These parts assemble into a weatherproof box for the antenna's feed point. This box protects the feed point, secures the driven element, and holds the feedline connector (e.g., N-type connector). It consists of three shell components and one T-shaped isolator.

### Note
These parts are under moderate stress. The following general-purpose mechanical part settings are recommended.

### Recommended General Print Settings
The following settings apply to **all four parts** in this directory. Part-specific instructions for orientation and supports are listed below.

| Parameter           | Value       |
|:--------------------|:------------|
| **Material**        | PETG        |
| **Nozzle Diameter** | 0.4mm       |
| **Layer Height**    | 0.2mm       |
| **Wall Thickness**  | 4 Layers    |
| **Top Layers**      | 4 Layers    |
| **Bottom Layers**   | 4 Layers    |
| **Infill Density**  | 25%         |
| **Infill Pattern**  | Cross Hatch |

---

### Part-Specific Instructions

#### 1. `feed_box_front`
* **Orientation:** Place the large flat face down on the print bed. The square opening should face upwards.
* **Supports:** **Manual (Custom) Supports Required.**
    * **Enable supports** *only* for the three countersunk "steps" (which are for the heat-set brass nuts).
    * **Disable supports** for all other areas. Note that the small groove (for the N-connector's waterproof O-ring) also **does not require support**.

#### 2. `feed_box_middle`
* **Orientation:** Place the large flat face down on the print bed. The semi-cylindrical groove should face upwards.
* **Supports:** **Must be enabled.**

#### 3. `feed_box_rear`
* **Orientation:** Place the large flat face down on the print bed. The semi-cylindrical groove should face upwards.
* **Supports:** **Must be enabled.**

#### 4. `feed_box_isolator`
* **Orientation:** Lay the part flat on the bed (in its "T" shape).
* **Supports:** **Not required.**

---
---

## 中文 (Chinese)

### 零件
* `feed_box_front.step`
* `feed_box_middle.step`
* `feed_box_rear.step`
* `feed_box_isolator.step`

### 用途
这些零件用于组装成一个馈电点防水盒。它用于保护馈电点、固定激励振子，并固定馈线连接座 (例如 N 型连接器)。它由三个外壳零件和一个 T 字形的绝缘零件组成。

### 注意
这些零件承受中等强度的受力，建议使用以下通用的机械零件参数进行打印。

### 推荐的通用打印参数
以下参数适用于此文件夹中的**所有四个零件**。每个零件特定的打印方向和支撑设置请见下方。

| 参数       | 数值                 |
|:---------|:-------------------|
| **材料**   | PETG               |
| **喷嘴直径** | 0.4mm              |
| **层高**   | 0.2mm              |
| **壁厚**   | 4 层                |
| **顶部层数** | 4 层                |
| **底部层数** | 4 层                |
| **填充密度** | 25%                |
| **填充图案** | 交叉层叠 (Cross Hatch) |

---

### 零件专属设置

#### 1. `feed_box_front`
* **打印方向:** 将大平面朝下放置在打印床上，方形槽口朝上。
* **支撑:** **需要手动绘制支撑 (Custom Supports)**。
    * **仅**为 3 个用于嵌入铜螺母的沉孔台阶**启用支撑**。
    * 在所有其他位置**禁用支撑**。请注意，用于安装 N 型连接器 (N-type connector) 防水O形圈的凹槽也**无须支撑**。

#### 2. `feed_box_middle`
* **打印方向:** 将大平面朝下放置在打印床上，半圆柱凹槽朝上。
* **支撑:** **必须启用支撑**。

#### 3. `feed_box_rear`
* **打印方向:** 将大平面朝下放置在打印床上，半圆柱凹槽朝上。
* **支撑:** **必须启用支撑**。

#### 4. `feed_box_isolator`
* **打印方向:** 将零件 T 字形平放在打印床上。
* **支撑:** **无须开启支撑。**

---
---

## Deutsche (German)

### Bauteile
* `feed_box_front.step`
* `feed_box_middle.step`
* `feed_box_rear.step`
* `feed_box_isolator.step`

### Zweck
Diese Teile werden zu einer wetterfesten Box für den Speisepunkt der Antenne zusammengebaut. Diese Box schützt den Speisepunkt, fixiert das Erregerelement und hält den Speiseleitungsanschluss (z. B. N-Buchse). Sie besteht aus drei Gehäusekomponenten und einem T-förmigen Isolator.

### Hinweis
Diese Teile sind einer mäßigen Belastung ausgesetzt. Die folgenden Einstellungen für mechanische Standardbauteile werden empfohlen.

### Empfohlene Allgemeine Druckeinstellungen
Die folgenden Einstellungen gelten für **alle vier Bauteile** in diesem Verzeichnis. Teilespezifische Anweisungen zur Ausrichtung und zu Stützstrukturen sind unten aufgeführt.

| Parameter            | Wert        |
|:---------------------|:------------|
| **Material**         | PETG        |
| **Düsendurchmesser** | 0.4mm       |
| **Schichthöhe**      | 0.2mm       |
| **Wandstärke**       | 4 Schichten |
| **Obere Schichten**  | 4 Schichten |
| **Untere Schichten** | 4 Schichten |
| **Fülldichte**       | 25%         |
| **Füllmuster**       | Cross Hatch |

---

### Teilespezifische Anweisungen

#### 1. `feed_box_front`
* **Ausrichtung:** Legen Sie die große, flache Seite nach unten auf das Druckbett. Die quadratische Öffnung sollte nach oben zeigen.
* **Stützstrukturen:** **Manuelle (benutzerdefinierte) Stützstrukturen erforderlich.**
    * Stützstrukturen **nur** für die drei Senkungen (Stufen) **aktivieren**, die für die Messing-Gewindeeinsätze vorgesehen sind.
    * Stützstrukturen für alle anderen Bereiche **deaktivieren**. Beachten Sie, dass die kleine Nut (für den wasserdichten O-Ring des N-Steckers) ebenfalls **keine Stützstruktur benötigt**.

#### 2. `feed_box_middle`
* **Ausrichtung:** Legen Sie die große, flache Seite nach unten auf das Druckbett. Die halbzylindrische Nut sollte nach oben zeigen.
* **Stützstrukturen:** **Müssen aktiviert sein.**

#### 3. `feed_box_rear`
* **Ausrichtung:** Legen Sie die große, flache Seite nach unten auf das Druckbett. Die halbzylindrische Nut sollte nach oben zeigen.
* **Stützstrukturen:** **Müssen aktiviert sein.**

#### 4. `feed_box_isolator`
* **Ausrichtung:** Legen Sie das Teil flach (in seiner "T"-Form) auf das Druckbett.
* **Stützstrukturen:** **Nicht erforderlich.**

---
---

## 日本語 (Japanese)

### パーツ
* `feed_box_front.step`
* `feed_box_middle.step`
* `feed_box_rear.step`
* `feed_box_isolator.step`

### 目的
これらのパーツは、アンテナの給電点用の耐候性ボックス（防水箱）を構成します。このボックスは給電点を保護し、給電素子を固定し、給電コネクタ（N型コネクタなど）を保持します。3つのシェルパーツと1つのT字型絶縁パーツで構成されています。

### 注意
これらのパーツには中程度の負荷がかかります。以下の一般的な機械部品用の設定で印刷することを推奨します。

### 推奨共通印刷設定
以下の設定は、このディレクトリ内の**4つのパーツすべて**に適用されます。パーツごとの配置とサポートに関する指示は、下記を参照してください。

| パラメータ      | 値                    |
|:-----------|:---------------------|
| **素材**     | PETG                 |
| **ノズル径**   | 0.4mm                |
| **積層ピッチ**  | 0.2mm                |
| **壁の厚さ**   | 4 層                  |
| **上部レイヤー** | 4 層                  |
| **底部レイヤー** | 4 層                  |
| **充填密度**   | 25%                  |
| **充填パターン** | クロスハッチ (Cross Hatch) |

---

### パーツ別設定

#### 1. `feed_box_front`
* **配置:** 大きな平らな面をプリントベッド側（下）に向け、四角い開口部が上を向くように配置します。
* **サポート:** **手動（カスタム）サポートが必要**です。
    * 熱圧入ナット用の3つの皿穴（段差部分）**にのみサポートを有効**にしてください。
    * 他のすべての領域ではサポートを**無効**にしてください。なお、N型コネクタの防水Oリング用の小さな溝も**サポート不要**です。

#### 2. `feed_box_middle`
* **配置:** 大きな平らな面をプリントベッド側（下）に向け、半円筒形の溝が上を向くように配置します。
* **サポート:** **有効にする必要があります。**

#### 3. `feed_box_rear`
* **配置:** 大きな平らな面をプリントベッド側（下）に向け、半円筒形の溝が上を向くように配置します。
* **サポート:** **有効にする必要があります。**

#### 4. `feed_box_isolator`
* **配置:** パーツを「T」の字になるように平らにプリントベッドに配置します。
* **サポート:** **不要です。**