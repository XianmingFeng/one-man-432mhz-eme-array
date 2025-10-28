# Printing Instructions

[English](#english) | [中文 (Chinese)](#中文-chinese) | [Deutsche (German)](#deutsche-german) | [日本語 (Japanese)](#日本語-japanese)

---

## English

This directory contains two types of drilling jigs:
1.  **Driven Element Jig:** `driven_element_drill_jig_upper.step` & `driven_element_drill_jig_lower.step`
2.  **Parasitic Element Jig:** `element_drill_jig.step`

Please use the specific settings for each part.

### 1. Driven Element Jig
* **Parts:**
    * `driven_element_drill_jig_upper.step`
    * `driven_element_drill_jig_lower.step`
* **Purpose:** These two parts are used as a pair to clamp the bent driven element. They are held together tightly in a bench vise for drilling.
* **Note:** The parts will be under significant pressure from the vise.

#### Recommended Print Settings

| Parameter           | Value       |
|:--------------------|:------------|
| **Material**        | PETG        |
| **Nozzle Diameter** | 0.4mm       |
| **Layer Height**    | 0.2mm       |
| **Wall Thickness**  | 4 Layers    |
| **Top Layers**      | 3 Layers    |
| **Bottom Layers**   | 3 Layers    |
| **Infill Density**  | 25%         |
| **Infill Pattern**  | Cross Hatch |

#### Orientation & Supports
* **Orientation:** Place the large flat side down on the print bed. The slanted/angled side should face upwards.
* **Supports:** **Not required.**

---

### 2. Parasitic Element Jig
* **Part:**
    * `element_drill_jig.step`
* **Purpose:** Used for drilling all other parasitic elements (reflectors and directors).
* **Note:** This jig is designed to be used with a drill bushing to protect the print from wear, as it will be used many times.

#### Recommended Print Settings

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

#### Orientation & Supports
* **Orientation:** Place the slotted face down on the print bed. The countersink hole for the drill bushing should face upwards.
* **Supports:** **Not required.**

---
---

## 中文 (Chinese)

此文件夹包含两种类型的钻孔夹具：
1.  **激励振子夹具:** `driven_element_drill_jig_upper.step` & `driven_element_drill_jig_lower.step`
2.  **无源振子夹具:** `element_drill_jig.step`

请对不同零件使用对应的特定设置。

### 1. 激励振子钻孔夹具
* **零件:**
    * `driven_element_drill_jig_upper.step`
    * `driven_element_drill_jig_lower.step`
* **用途:** 这两个零件（上、下）配对使用，用于夹住弯曲成型的激励振子。使用时，它们会被老虎钳夹紧以进行钻孔。
* **注意:** 零件会承受来自老虎钳的较大压力。

#### 推荐打印参数

| 参数       | 数值                 |
|:---------|:-------------------|
| **材料**   | PETG               |
| **喷嘴直径** | 0.4mm              |
| **层高**   | 0.2mm              |
| **壁厚**   | 4 层                |
| **顶部层数** | 3 层                |
| **底部层数** | 3 层                |
| **填充密度** | 25%                |
| **填充图案** | 交叉层叠 (Cross Hatch) |

#### 打印方向与支撑
* **打印方向:** 将大平面朝下放置在打印床上，斜面朝上。
* **支撑:** **无须开启支撑。**

---

### 2. 无源振子钻孔夹具
* **零件:**
    * `element_drill_jig.step`
* **用途:** 用于钻孔所有其他的无源振子（反射器和引向器）。
* **注意:** 由于使用次数非常多，此夹具设计用于安装一个钻套，以保护打印件免受磨损。

#### 推荐打印参数

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

#### 打印方向与支撑
* **打印方向:** 将开缝面朝下放置在打印床上，用于安装钻套的沉孔朝上。
* **支撑:** **无须开启支撑。**

---
---

## Deutsche (German)

Dieses Verzeichnis enthält zwei Arten von Bohrlehren:
1.  **Bohrlehre für Erregerelement:** `driven_element_drill_jig_upper.step` & `driven_element_drill_jig_lower.step`
2.  **Bohrlehre für Parasitärelemente:** `element_drill_jig.step`

Bitte verwenden Sie die spezifischen Einstellungen für jedes Bauteil.

### 1. Bohrlehre für Erregerelement
* **Bauteile:**
    * `driven_element_drill_jig_upper.step`
    * `driven_element_drill_jig_lower.step`
* **Zweck:** Diese beiden Teile (oben und unten) werden als Paar verwendet, um das gebogene Erregerelement einzuklemmen. Sie werden zum Bohren fest in einen Schraubstock gespannt.
* **Hinweis:** Die Teile stehen unter erheblichem Druck durch den Schraubstock.

#### Empfohlene Druckeinstellungen

| Parameter            | Wert        |
|:---------------------|:------------|
| **Material**         | PETG        |
| **Düsendurchmesser** | 0.4mm       |
| **Schichthöhe**      | 0.2mm       |
| **Wandstärke**       | 4 Schichten |
| **Obere Schichten**  | 3 Schichten |
| **Untere Schichten** | 3 Schichten |
| **Fülldichte**       | 25%         |
| **Füllmuster**       | Cross Hatch |

#### Ausrichtung & Stützstrukturen
* **Ausrichtung:** Legen Sie die große, flache Seite nach unten auf das Druckbett. Die abgeschrägte Seite sollte nach oben zeigen.
* **Stützstrukturen:** **Nicht erforderlich.**

---

### 2. Bohrlehre für Parasitärelemente
* **Bauteil:**
    * `element_drill_jig.step`
* **Zweck:** Wird zum Bohren aller anderen parasitären Elemente (Reflektoren und Direktoren) verwendet.
* **Hinweis:** Diese Lehre ist für die Verwendung mit einer Bohrbuchse ausgelegt, um den Druck vor Verschleiß zu schützen, da sie sehr oft verwendet wird.

#### Empfohlene Druckeinstellungen

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

#### Ausrichtung & Stützstrukturen
* **Ausrichtung:** Legen Sie die geschlitzte Seite nach unten auf das Druckbett. Die Senkbohrung für die Bohrbuchse sollte nach oben zeigen.
* **Stützstrukturen:** **Nicht erforderlich.**

---
---

## 日本語 (Japanese)

このディレクトリには2種類のドリルジグ（穿孔治具）が含まれています。
1.  **給電素子用ドリルジグ:** `driven_element_drill_jig_upper.step` & `driven_element_drill_jig_lower.step`
2.  **無給電素子用ドリルジグ:** `element_drill_jig.step`

各パーツに適した設定を使用してください。

### 1. 給電素子用ドリルジグ
* **パーツ:**
    * `driven_element_drill_jig_upper.step`
    * `driven_element_drill_jig_lower.step`
* **目的:** これら2つ（上部と下部）のパーツは、曲げ加工済みの給電素子を挟み込むためにペアで使用されます。穿孔する際、万力（バイス）で強く固定されます。
* **注意:** これらのパーツは万力によって大きな圧力を受けます。

#### 推奨印刷設定

| パラメータ      | 値                    |
|:-----------|:---------------------|
| **素材**     | PETG                 |
| **ノズル径**   | 0.4mm                |
| **積層ピッチ**  | 0.2mm                |
| **壁の厚さ**   | 4 層                  |
| **上部レイヤー** | 3 層                  |
| **底部レイヤー** | 3 層                  |
| **充填密度**   | 25%                  |
| **充填パターン** | クロスハッチ (Cross Hatch) |

#### 配置とサポート
* **配置:** 大きな平らな面をプリントベッド側（下）に向け、傾斜している面を上に向けてください。
* **サポート:** **不要です。**

---

### 2. 無給電素子用ドリルジグ
* **パーツ:**
    * `element_drill_jig.step`
* **目的:** 他のすべての無給電素子（反射器および導波器）の穿孔に使用します。
* **注意:** このジグは非常に多く使用されるため、ドリルブッシュ（ドリルガイド）を装着して印刷部品を摩耗から保護するように設計されています。

#### 推奨印刷設定

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

#### 配置とサポート
* **配置:** スリット（開口部）のある面をプリントベッド側（下）に向け、ドリルブッシュ用の皿穴（沈み穴）が上を向くように配置してください。
* **サポート:** **不要です。**