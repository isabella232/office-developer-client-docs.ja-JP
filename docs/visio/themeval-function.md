---
title: THEMEVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: 使用中のテーマから値を取得します。
ms.openlocfilehash: af46d000c8a7513cf961573d20d71e28c1c66915
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597850"
---
# <a name="themeval-function"></a>THEMEVAL 関数

使用中のテーマから値を取得します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **THEMEVAL**([ _"theme_value"_][, _default_]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |省略可能  <br/> |**String** <br/> |値を取得するテーマの定義内のセルの名前。  <br/> |
| _default_ <br/> |オプション  <br/> |各種  <br/> |ドキュメントにテーマがない (テーマの定義がない) 場合の既定値。  <br/> |
   
## <a name="remarks"></a>注釈

引数が設定されていない場合、**THEMEVAL** 関数はホスト セルのテーマの値を返します。これは、現在のテーマの定義に格納されている値です。ホスト セルは、値を返すためにテーマを適用できる必要があります。このセルにテーマを適用できない場合、**THEMEVAL** はエラーを返します。 
  
引数が 1 つ設定されている場合、**THEMEVAL** 関数は、引数として渡されたテーマの定義から値を取得します。最初のパラメーターのために渡される引数は、整数、または以下の表に一覧表示された正確な文字列でなければなりません。 
  
また、**THEMEVAL** 関数は、最初のパラメーターに 1 から 8 までの値として整数を受け入れます。 整数値を使用すると、インデックスによってテーマの配色から色を取得します。 したがって、値 '1' はテーマから "Dark" 色を返し、'2' は "Light" 色を返し、'3' は "アクセント 1" の色などを返します。 
  
**THEMEVAL** 関数に 2 つの引数が設定されている場合、最初の引数として渡されたテーマの定義から値を取得します。ただし、ドキュメントに適用されるテーマがない場合は、**THEMEVAL** 関数は 2 つ目の引数に指定された値を使用します。 
  
**"theme_value" パラメーター theme_value引数**

|**値**|**説明**|
|:-----|:-----|
|"Dark"  <br/> |テーマ定義から暗い RGB 色を取得します。  <br/> |
|"Light"  <br/> |テーマ定義から明るい RGB 色を取得します。  <br/> |
|"BackgroundColor"  <br/> |テーマの定義から Background RGB 色を取得します。  <br/> |
|"AccentColor"  <br/> |テーマの定義から Accent1 RGB 色を取得します。  <br/> |
|"AccentColor2"  <br/> |テーマの定義から Accent2 RGB 色を取得します。  <br/> |
|"AccentColor3"  <br/> |テーマの定義から Accent3 RGB 色を取得します。  <br/> |
|"AccentColor4"  <br/> |テーマの定義から Accent4 RGB 色を取得します。  <br/> |
|"AccentColor5"  <br/> |テーマの定義から Accent5 RGB 色を取得します。  <br/> |
|"AccentColor6"  <br/> |テーマの定義から Accent6 RGB 色を取得します。  <br/> |
|"LinePattern"  <br/> |テーマの定義から [LinePattern] セルの値を取得します。  <br/> |
|"LineWeight"  <br/> |テーマの定義から [LineWeight] の値を取得します。  <br/> |
|"LineColor"  <br/> |テーマの定義から [LineColor] セルの値を取得します。  <br/> |
|"LineCap"  <br/> |テーマの定義から [LineCap] セルの値を取得します。  <br/> |
|"LineBegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"LineEnd"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|"LineColorTrans"  <br/> |テーマの定義から [LineColorTrans] セルの値を取得します。  <br/> |
|"LineCompoundtype"  <br/> |テーマの定義から [CompoundType] セルの値を取得します。  <br/> |
|"LineBegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"LineEnd"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
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
|"FillColor"  <br/> |テーマの定義から [FillForegnd] セルの値を取得します。  <br/> |
|"FillColor2"  <br/> |テーマの定義から [FillBkgnd] セルの値を取得します。  <br/> |
|"FillTransparency"  <br/> |テーマの定義から [FillForegndTrans] セルの値を取得します。  <br/> |
|"FillPattern"  <br/> |テーマの定義から [FillPattern] セルの値を取得します。  <br/> |
|"LineGradientEnabled"  <br/> |テーマの定義から [LineGradientEnabled] セルの値を取得します。  <br/> |
|"LineGradientDir"  <br/> |テーマの定義から [LineGradientDir] セルの値を取得します。  <br/> |
|"LineGradientAngle"  <br/> |テーマの定義から [LineGradientAngle] セルの値を取得します。  <br/> |
|"FillGradientEnabled"  <br/> |テーマの定義から [FillGradientEnabled] セルの値を取得します。  <br/> |
|"FillGradientDir"  <br/> |テーマの定義から [FillGradientDir] セルの値を取得します。  <br/> |
|"FillGradientAngle"  <br/> |テーマの定義から [FillGradientAngle] セルの値を取得します。  <br/> |
|"RotateGradientWithShape"  <br/> |テーマの定義から [RotateGradientWithShape] セルの値を取得します。  <br/> |
|"UseGroupGradient"  <br/> |テーマの定義から [UseGroupGradient] セルの値を取得します。  <br/> |
|"ShadowType"  <br/> |テーマの定義から [ShapeShdwType] セルの値を取得します。  <br/> |
|"ShadowColor"  <br/> |テーマの定義から [ShdwColor] セルの値を取得します。  <br/> |
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
|"BevelContourColor"  <br/> |テーマ定義から BevelContourColor セルの値を取得します。  <br/> |
|"BevelContourSize"  <br/> |テーマ定義から BevelContourSize セル値を取得します。  <br/> |
|"ReflectionBlur"  <br/> |テーマ定義から ReflectionBlur セル値を取得します。  <br/> |
|"ReflectionDist"  <br/> |テーマ定義から ReflectionDist セル値を取得します。  <br/> |
|"ReflectionSize"  <br/> |テーマ定義から ReflectionSize セルの値を取得します。  <br/> |
|"ReflectionTrans"  <br/> |テーマ定義から ReflectionTrans セルの値を取得します。  <br/> |
|"SoftEdgesSize"  <br/> |テーマ定義から SoftEdgesSize セル値を取得します。  <br/> |
|"GlowSize"  <br/> |テーマの定義から [GlowSize] セルの値を取得します。  <br/> |
|"GlowColor"  <br/> |テーマの定義から [GlowColor] セルの値を取得します。  <br/> |
|"GlowTransparency"  <br/> |テーマの定義から [GlowColorTrans] セルの値を取得します。  <br/> |
|"SketchAmount"  <br/> |テーマ定義から SketchAmount セル値を取得します。  <br/> |
|"SketchEnabled"  <br/> |テーマ定義から SketchEnabled セル値を取得します。  <br/> |
|"SketchFillChange"  <br/> |テーマ定義から SketchFillChange セルの値を取得します。  <br/> |
|"SketchLineChange"  <br/> |テーマ定義から SketchLineChange セル値を取得します。  <br/> |
|"SketchLineWeight"  <br/> |テーマ定義から SketchLineWeight セルの値を取得します。  <br/> |
|"LatinFont"  <br/> |テーマの定義から [Font] セルの値を取得します。  <br/> |
|"TextColor"  <br/> |テーマの定義から [Color] セルの値を取得します。  <br/> |
|"TextStyle"  <br/> |テーマ定義から Character.Style セル値を取得します。  <br/> |
|"ComplexFont"  <br/> |テーマの定義から [ComplexScriptFont] セルの値を取得します。  <br/> |
|"AsianFont"  <br/> |テーマの定義から [AsianFont] セルの値を取得します。  <br/> |
|"FillStop[x]Color"  <br/> |テーマ定義から行  *x*  の [色] セルの値を取得します。  <br/> |
|"FillStop[x]Transparency"  <br/> |テーマ定義から行  *x*  の ColorTrans セル値を取得します。  <br/> |
|"FillStop[x]Position"  <br/> |テーマ定義から行  *x*  の [位置] セルの値を取得します。  <br/> |
|"LineStop[x]Color"  <br/> |テーマ定義から行  *x*  の [色] セルの値を取得します。  <br/> |
|"LineStop[x]Transparency"  <br/> |テーマ定義から行  *x*  の ColorTrans セル値を取得します。  <br/> |
|"LineStop[x]Position"  <br/> |テーマ定義から行  *x*  の [位置] セルの値を取得します。  <br/> |
   
## <a name="example"></a>例

 `THEMEVAL("5")`
  
テーマ定義から "アクセント 3" の色を返します。
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
テーマ定義の [LineWeight] セルの値を返します。 この関数を含む図形にテーマが適用されている場合、関数は '0.7 pt.' を返します。
  

