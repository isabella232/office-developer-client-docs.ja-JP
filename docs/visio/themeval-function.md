---
title: THEMEVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: '使用中のテーマから値を取得します。 '
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806654"
---
# <a name="themeval-function"></a>THEMEVAL 関数

使用中のテーマから値を取得します。  
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **THEMEVAL**([ _"theme_value"_] [、_既定値_]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |値を取得するテーマの定義内のセルの名前。  <br/> |
| _default_ <br/> |省略可能  <br/> |各種  <br/> |ドキュメントにテーマがない (テーマの定義がない) 場合の既定値。  <br/> |
   
## <a name="remarks"></a>Remarks

引数が設定されていない場合、**THEMEVAL** 関数はホスト セルのテーマの値を返します。これは、現在のテーマの定義に格納されている値です。ホスト セルは、値を返すためにテーマを適用できる必要があります。このセルにテーマを適用できない場合、**THEMEVAL** はエラーを返します。 
  
引数が 1 つ設定されている場合、**THEMEVAL** 関数は、引数として渡されたテーマの定義から値を取得します。最初のパラメーターのために渡される引数は、整数、または以下の表に一覧表示された正確な文字列でなければなりません。 
  
**THEMEVAL**関数は、1 から 8 までの値として、最初のパラメーターの整数値を受け入れることができるも。 整数値を使用して、テーマの配色パターンのインデックスを使用して色を取得します。 したがって、'1' の値は、テーマから「濃い」色を返す、'2' は、「明るい」色を返します、[アクセント 1] の色 '3' を返します。 
  
**THEMEVAL** 関数に 2 つの引数が設定されている場合、最初の引数として渡されたテーマの定義から値を取得します。ただし、ドキュメントに適用されるテーマがない場合は、**THEMEVAL** 関数は 2 つ目の引数に指定された値を使用します。 
  
**"Theme_value"のパラメーターの使用可能な引数**

|**値**|**説明**|
|:-----|:-----|
|「濃い」  <br/> |テーマの定義から、濃い色の RGB カラーを取得します。  <br/> |
|「ライト」  <br/> |テーマの定義からのライトの RGB カラーを取得します。  <br/> |
|「背景色」  <br/> |テーマの定義から Background RGB 色を取得します。  <br/> |
|"AccentColor"  <br/> |テーマの定義から Accent1 RGB 色を取得します。  <br/> |
|"AccentColor2"  <br/> |テーマの定義から Accent2 RGB 色を取得します。  <br/> |
|"AccentColor3"  <br/> |テーマの定義から Accent3 RGB 色を取得します。  <br/> |
|"AccentColor4"  <br/> |テーマの定義から Accent4 RGB 色を取得します。  <br/> |
|"AccentColor5"  <br/> |テーマの定義から Accent5 RGB 色を取得します。  <br/> |
|"AccentColor6"  <br/> |テーマの定義から Accent6 RGB 色を取得します。  <br/> |
|[LinePattern]  <br/> |テーマの定義から [LinePattern] セルの値を取得します。  <br/> |
|[LineWeight]  <br/> |テーマの定義から [LineWeight] の値を取得します。  <br/> |
|「線の色]  <br/> |テーマの定義から [LineColor] セルの値を取得します。  <br/> |
|「[Linecap]」  <br/> |テーマの定義から [LineCap] セルの値を取得します。  <br/> |
|"LineBegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|「行末文字」  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|[LineColorTrans]  <br/> |テーマの定義から [LineColorTrans] セルの値を取得します。  <br/> |
|"LineCompoundtype"  <br/> |テーマの定義から [CompoundType] セルの値を取得します。  <br/> |
|"LineBegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|「行末文字」  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|"LineBeginSize"  <br/> |テーマの定義から [BeginArrowSize] セルの値を取得します。  <br/> |
|"LineEndSize"  <br/> |テーマの定義から [EndArrowSize] セルの値を取得します。  <br/> |
|"LineRounding"  <br/> |テーマの定義から [Rounding] セルの値を取得します。  <br/> |
|"ConnectorColor"  <br/> |テーマの定義から [LineColor] セルの値を取得します。  <br/> |
|"ConnectorPattern"  <br/> |テーマの定義から [LinePattern] セルの値を取得します。  <br/> |
|"ConnectorWeight"  <br/> |テーマの定義から [LineWeight] の値を取得します。  <br/> |
|"ConnectorTransparency"  <br/> |テーマの定義から [LineColorTrans] セルの値を取得します。  <br/> |
|"ConnectorRounding"  <br/> |テーマの定義から [Rounding] セルの値を取得します。  <br/> |
|"ConnectorBegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"ConnectorEnd"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|"ConnectorBeginSize"  <br/> |テーマの定義から [BeginArrowSize] セルの値を取得します。  <br/> |
|"ConnectorEndSize"  <br/> |テーマの定義から [EndArrowSize] セルの値を取得します。  <br/> |
|「れた」  <br/> |テーマの定義から [FillForegnd] セルの値を取得します。  <br/> |
|"FillColor2"  <br/> |テーマの定義から [FillBkgnd] セルの値を取得します。  <br/> |
|"FillTransparency"  <br/> |テーマの定義から [FillForegndTrans] セルの値を取得します。  <br/> |
|[FillPattern]  <br/> |テーマの定義から [FillPattern] セルの値を取得します。  <br/> |
|"LineGradientEnabled"  <br/> |テーマの定義から [LineGradientEnabled] セルの値を取得します。  <br/> |
|"LineGradientDir"  <br/> |テーマの定義から [LineGradientDir] セルの値を取得します。  <br/> |
|"LineGradientAngle"  <br/> |テーマの定義から [LineGradientAngle] セルの値を取得します。  <br/> |
|"FillGradientEnabled"  <br/> |テーマの定義から [FillGradientEnabled] セルの値を取得します。  <br/> |
|"FillGradientDir"  <br/> |テーマの定義から [FillGradientDir] セルの値を取得します。  <br/> |
|"FillGradientAngle"  <br/> |テーマの定義から [FillGradientAngle] セルの値を取得します。  <br/> |
|"RotateGradientWithShape"  <br/> |テーマの定義から [RotateGradientWithShape] セルの値を取得します。  <br/> |
|"UseGroupGradient"  <br/> |テーマの定義から [UseGroupGradient] セルの値を取得します。  <br/> |
|「ShadowType」  <br/> |テーマの定義から [ShapeShdwType] セルの値を取得します。  <br/> |
|「ShadowColor」  <br/> |テーマの定義から [ShdwColor] セルの値を取得します。  <br/> |
|"ShadowTransparency"  <br/> |テーマの定義から [ShdwColorTrans] セルの値を取得します。  <br/> |
|"ShadowMagnification"  <br/> |テーマの定義から [ShapeShdwScaleFactor] セルの値を取得します。  <br/> |
|"ShadowBlur"  <br/> |テーマの定義から [ShapeShdwBlur] セルの値を取得します。  <br/> |
|"ShadowXOffset"  <br/> |テーマの定義から [ShapeShdwOffsetX] セルの値を取得します。  <br/> |
|"ShadowYOffset"  <br/> |テーマの定義から [ShapeShdwOffsetY] セルの値を取得します。  <br/> |
|"ShadowDirection"  <br/> |テーマの定義から [ShapeShdwObliqueAngle] セルの値を取得します。  <br/> |
|"ShadowPattern"  <br/> |テーマの定義から [ShdwPattern] セルの値を取得します。  <br/> |
|"BevelTopType"  <br/> |テーマの定義から [BevelTopType] セルの値を取得します。  <br/> |
|"BevelTopWidth"  <br/> |テーマの定義から [BevelTopWidth] セルの値を取得します。  <br/> |
|"BevelTopHeight"  <br/> |テーマの定義から [BevelTopHeight] セルの値を取得します。  <br/> |
|"BevelMaterial"  <br/> |テーマの定義から [BevelMaterialType] セルの値を取得します。  <br/> |
|"BevelLighting"  <br/> |テーマの定義から [BevelLightingType] セルの値を取得します。  <br/> |
|"BevelLightingAngle"  <br/> |テーマの定義から [BevelLightingAngle] セルの値を取得します。  <br/> |
|"BevelContourColor"  <br/> |テーマの定義から BevelContourColor のセルの値を取得します。  <br/> |
|"BevelContourSize"  <br/> |テーマの定義から BevelContourSize のセルの値を取得します。  <br/> |
|"ReflectionBlur"  <br/> |テーマの定義から ReflectionBlur のセルの値を取得します。  <br/> |
|"ReflectionDist"  <br/> |テーマの定義から ReflectionDist のセルの値を取得します。  <br/> |
|"ReflectionSize"  <br/> |テーマの定義から ReflectionSize のセルの値を取得します。  <br/> |
|"ReflectionTrans"  <br/> |テーマの定義から ReflectionTrans のセルの値を取得します。  <br/> |
|"SoftEdgesSize"  <br/> |テーマの定義から SoftEdgesSize のセルの値を取得します。  <br/> |
|"GlowSize"  <br/> |テーマの定義から [GlowSize] セルの値を取得します。  <br/> |
|"GlowColor"  <br/> |テーマの定義から [GlowColor] セルの値を取得します。  <br/> |
|"GlowTransparency"  <br/> |テーマの定義から [GlowColorTrans] セルの値を取得します。  <br/> |
|"SketchAmount"  <br/> |テーマの定義から SketchAmount のセルの値を取得します。  <br/> |
|"SketchEnabled"  <br/> |テーマの定義から SketchEnabled のセルの値を取得します。  <br/> |
|"SketchFillChange"  <br/> |テーマの定義から SketchFillChange のセルの値を取得します。  <br/> |
|"SketchLineChange"  <br/> |テーマの定義から SketchLineChange のセルの値を取得します。  <br/> |
|"SketchLineWeight"  <br/> |テーマの定義から SketchLineWeight のセルの値を取得します。  <br/> |
|"LatinFont"  <br/> |テーマの定義から [Font] セルの値を取得します。  <br/> |
|「TextColor」  <br/> |テーマの定義から [Color] セルの値を取得します。  <br/> |
|「テキスト スタイル」  <br/> |テーマの定義から Character.Style のセルの値を取得します。  <br/> |
|"ComplexFont"  <br/> |テーマの定義から [ComplexScriptFont] セルの値を取得します。  <br/> |
|「[Asianfont]」  <br/> |テーマの定義から [AsianFont] セルの値を取得します。  <br/> |
|「FillStop [x] 色」  <br/> |テーマの定義から、 *x*の行の色のセルの値を取得します。  <br/> |
|「FillStop [x] 透明性」  <br/> |ColorTrans *x*の行のセルの値は、テーマの定義から取得します。  <br/> |
|「FillStop [x] の位置」  <br/> |テーマの定義から、 *x*の行の位置のセルの値を取得します。  <br/> |
|「LineStop [x] 色」  <br/> |テーマの定義から、 *x*の行の色のセルの値を取得します。  <br/> |
|「LineStop [x] 透明性」  <br/> |ColorTrans *x*の行のセルの値は、テーマの定義から取得します。  <br/> |
|「LineStop [x] の位置」  <br/> |テーマの定義から、 *x*の行の位置のセルの値を取得します。  <br/> |
   
## <a name="example"></a>例

 `THEMEVAL("5")`
  
テーマの定義からは、[アクセント 3] の色を返します。
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
テーマの定義から [LineWeight] セルの値を返します。 この関数が含まれている図形に適用されているテーマをなしがある場合は、' 0.7 pt。 ' を返します。
  

