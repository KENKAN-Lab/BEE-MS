.. |m2| replace:: m\ :sup:`2` \


****************************************************
Natural Room Temprature Simulation Tool (NRTS)
****************************************************

Introduction
============

This tool is the tool for simulating natural air temperature in a room.
In this tool, the room temperature is simulated by the heat balance of heat transmitted loss through the envelope to the outdoor air, solar heat gain, inside heat generation from the humans, lightings, appliances and cooking, and heat loss of the ventilation.

本ツールは1部屋の自然室温を計算するツールです。
本ツールによって、部屋の温度は、外気との躯体の貫流熱損失、日射による取得熱、人体・照明・家電・調理による内部発熱、換気による熱損失による熱バランスを考慮して室温が計算されます。

Description
=======================

This tool is the tool for simulating natural air temperature in a given room.

本ツールは1部屋における自然室温を計算するツールです。

In this tool, the room temperature is simulated by,

- the heat balance of heat transmitted loss through the envelope to the outdoor air
- solar heat gain,
- inside heat generation from the humans,
- heat generation from lightings, appliances and cooking,
- and heat loss of the ventilation.

本ツールでは以下の要素により室温が計算されます。

- 外気との躯体の熱貫流損失
- 日射による熱取得
- 人体・照明・家電・調理による内部発熱
- 換気による熱損失

The heat transmitted loss through the envelope to the outdoor air is caluclated by multiplying the q-value by the temperature difference between the inside air temperature and the outside air temperature.

外気への躯体を通じた貫流熱損失はq値に内外室間温度差を乗じて計算されます。

q_vaue is declined below:

q値は以下のように定められます。

.. math::
  q = U \times A.

:math:`q`
  | q_value, W / K
  | q値, W / K
:math:`U`
  | U_value,  W / |m2| K
  | U値, W / |m2| K
:math:`A`
  | Area of envelope, |m2|
  | 外皮の面積, |m2|

The heat transmitted loss through the envelope to the outdoor air is calculated below:

外気への躯体を通じた貫流熱損失は以下のように計算されます。

.. math::
  q_{env} = q \times ( \theta_i - \theta_o ).

:math:`q_{env}`
  | Heat transmitted loss through the envelope to the outdoor air, W
  | 室外への外皮を通じた熱損失, W
:math:`\theta_i`
  | Inside temperature, degree C
  | 室内温度, ℃
:math:`\theta_o`
  | Outside temperature, degree C
  | 室外温度, ℃

Derivation
============

No description.
