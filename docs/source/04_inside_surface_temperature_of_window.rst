.. |m2| replace:: m\ :sup:`2` \


******************************************************************
Inside Surface Temperature of Window Simulation Tool (ISTWST)
******************************************************************

Introduction
============

This tool provides the surface temperature of window.
The surface temperature is calculated based on U value of the glass or the flame.
This tool also provedes the inside surface temperature of the inside attachment such as Shoji, inside blind.

本ツールは窓の表面温度を提供します。
表面温度はガラスまたはフレームのU値に基づいて計算されます。
本ツールは障子や室内側ブラインドのような室内側付属部材の室内側表面温度の計算も提供します。

How to Use
==================

Input

- U value of the glass or the flame of the window, W / |m2| K
- Outside air temperature, degree C
- Inside surface thermal resistane, |m2| K / W
- Thermal resistance of the inside attachment (optional), |m2| K / W

入力

- 窓のガラスまたはフレームのU値, W / |m2| K
- 室外側空気温度, ℃
- 室内側表面熱伝達抵抗, |m2| K / W
- 室内側付属部材の熱伝達抵抗（オプション）, |m2| K / W

U values of the glass are described in the Japanese energy efficiency standard.
The U values in the case with 6 mm of the width of air layer are shown below.

ガラスのU値は日本の省エネ基準において定められています。空気層厚さ6mmの場合のみのU値を以下に示します。

.. csv-table:: Solar Heat Gain Example
   :header: "Spec.", "Value"
   :widths: 15, 15

   "Triple glass (double low-e and insulation gas)", 1.4
   "Triple glass (double low-e)", 1.7
   "Triple glass (single low-e and insulation gas)", 1.7
   "Triple glass (single low-e)", 2.0
   "Triple glass", 2.3
   "Double glass (low-e and insulation gas)", 2.2
   "Double glass (low-e)", 2.6
   "Double glass", 3.3
   "Sigle glass", 6.0

These values can be calculated based on JIS R3107 and ISO 10292.

これらの値はJIS R3107 及び ISO 10292 により計算されます。

U values of the flame are declined in the Japanese energy efficiency standard as below:

フレームのU値は日本の省エネルギー基準において以下のように決められています。

.. csv-table:: Solar Heat Gain Example
   :header: "Spec.", "Value"
   :widths: 15, 15

   "Wood", 2.379
   "Resin", 2.379
   "Complex of Wood and Metal", 4.367
   "Complex of Resin and Metal", 4.367
   "Metal", 7.349

Examples of the outside temperature designed for the heating season are below.

暖房期の設計外気温度の例を以下に示します。

.. csv-table::
  :header: "Region", "Temperature, degree C"
  :widths: 15, 15

  "Semi Cold (Morioka)", -3.1
  "Warm (Utsunomiya)", -1.1
  "Semi Hot (Miyazaki)", 2.9

Inside surface thermal resistance of the vertical window is decided to be 0.11 |m2| K / W in Japnaese energy efficiency standard.

垂直の窓の室内側表面熱伝達抵抗は日本の省エネルギー基準では、0.11 |m2| K / W と決められています。

The thermal resistance of Shoji, one of the inside attachments, is 0.18 |m2| K / W.

例えば室内側付属部材の一つである障子の熱抵抗は 0.18 |m2| K / W です。


Image
============

You can calculate the surface temperature by plotting the thermal resistances on the horizontal axis and the inside and outside temperatures on the vertical axis.

縦軸に熱抵抗、横軸に室内外温度をとることで、表面温度を計算することができます。

.. figure:: ./_static/fig/surface_temperature_diagram_1.png
    :align: center
    :scale: 30 %

    Surface Temperature Diagram

.. figure:: ./_static/fig/surface_temperature_diagram_2.png
    :align: center
    :scale: 30 %

    Surface Temperature Diagram (Attachment)

Description
=======================

The inside surface temperature of the glass or the fralme of the window is calculated by:

窓のガラスまたはフレームの室内側表面温度は以下のように計算できます。

Without attachment:

付属部材が無い場合:

.. math::
  \theta_{s,w} = \theta_i - U \cdot ( \theta_i - \theta_o ) \cdot R_i

With attachemt:

付属部材がある場合:

.. math::
  \theta_{s,a} = \theta_i - U \cdot ( \theta_i - \theta_o ) \cdot R_i

.. math::
  \theta_{s,w} = \theta_i - U \cdot ( \theta_i - \theta_o ) \cdot ( R_i + R_a )

:math:`\theta_{s,w}`
  | Inside surface temperature of glass or frame of window, degree C
  | 窓のガラスまたはフレームの室内側表面温度, ℃
:math:`\theta_{s,a}`
  | Inside surface temperature of attachment, degree C
  | 付属部材の室内側表面温度, ℃
:math:`\theta_i`
  | Indoor temperature, degree C
  | 室内温度, ℃
:math:`\theta_o`
  | Outdoor Temperature, degree C
  | 外気温度, ℃
:math:`U`
  | U value of glass or frame of window, W / |m2| K
  | 窓のガラスまたはフレームのU値, W / |m2| K
:math:`R_i`
  | Inside surface thermal resistance, |m2| K / W
  | 室内側表面熱伝達抵抗, |m2| K / W
:math:`R_a`
  | Thermal resistance of attachment, |m2| K / W
  | 付属部材の熱抵抗, |m2| K / W


Derivation
============

No description.
