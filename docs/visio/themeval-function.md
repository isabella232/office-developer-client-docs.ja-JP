---
title: THEMEVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: 使用中のテーマから値を取得します。
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415755"
---
# <a name="themeval-function"></a>THEMEVAL 関数

使用中のテーマから値を取得します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **評価**([ _"theme_value"_] [, _default_]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |値を取得するテーマの定義内のセルの名前。  <br/> |
| _default_ <br/> |省略可能  <br/> |各種  <br/> |ドキュメントにテーマがない (テーマの定義がない) 場合の既定値。  <br/> |
   
## <a name="remarks"></a>注釈

関数**eval**関数が引数を受け取っていない場合は、host セルのテーマ付きの値が返されます。 これは、現在のテーマの定義に格納されている値です。 ホストセルは、値を返すようにテーマ指定できる必要があります。セルにテーマが設定されていない場合、 **eval**はエラーを返します。 
  
引数が 1 つ設定されている場合、**THEMEVAL** 関数は、引数として渡されたテーマの定義から値を取得します。 最初のパラメーターのために渡される引数は、整数、または以下の表に一覧表示された正確な文字列でなければなりません。 
  
また、**THEMEVAL** 関数は、最初のパラメーターに 1 から 8 までの値として整数を受け入れます。 整数値を使用すると、インデックスによってテーマの配色から色を取得します。 このため、' 1 ' の値はテーマから "暗い" 色を返し、' 2 ' は "明" の色を返し、' 3 ' は "アクセント 1" の色などを返します。 
  
**THEMEVAL** 関数に 2 つの引数が設定されている場合、最初の引数として渡されたテーマの定義から値を取得します。 ただし、ドキュメントに適用されるテーマがない場合は、**THEMEVAL** 関数は 2 つ目の引数に指定された値を使用します。 
  
**"theme_value" パラメーターに指定できる引数**

|**値**|**説明**|
|:-----|:-----|
|対角線  <br/> |テーマの定義から暗い RGB カラーを取得します。  <br/> |
|(  <br/> |テーマの定義から明るい RGB カラーを取得します。  <br/> |
|背景  <br/> |テーマの定義から Background RGB 色を取得します。  <br/> |
|"アクセント"  <br/> |テーマの定義から Accent1 RGB 色を取得します。  <br/> |
|"AccentColor2"  <br/> |テーマの定義から Accent2 RGB 色を取得します。  <br/> |
|"AccentColor3"  <br/> |テーマの定義から Accent3 RGB 色を取得します。  <br/> |
|"AccentColor4"  <br/> |テーマの定義から Accent4 RGB 色を取得します。  <br/> |
|"AccentColor5"  <br/> |テーマの定義から Accent5 RGB 色を取得します。  <br/> |
|"AccentColor6"  <br/> |テーマの定義から Accent6 RGB 色を取得します。  <br/> |
|[linepattern]  <br/> |テーマの定義から [LinePattern] セルの値を取得します。  <br/> |
|lineweight]  <br/> |テーマの定義から [LineWeight] の値を取得します。  <br/> |
|linecolor]  <br/> |テーマの定義から [LineColor] セルの値を取得します。  <br/> |
|[linecap]  <br/> |テーマの定義から [LineCap] セルの値を取得します。  <br/> |
|"linebegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"lineend"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|[linecolortrans]  <br/> |テーマの定義から [LineColorTrans] セルの値を取得します。  <br/> |
|"LineCompoundtype"  <br/> |テーマの定義から [CompoundType] セルの値を取得します。  <br/> |
|"linebegin"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"lineend"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|"linebeginsize"  <br/> |テーマの定義から [BeginArrowSize] セルの値を取得します。  <br/> |
|"lineendsize"  <br/> |テーマの定義から [EndArrowSize] セルの値を取得します。  <br/> |
|"LineRounding"  <br/> |テーマの定義から [Rounding] セルの値を取得します。  <br/> |
|"コネクタカラー"  <br/> |テーマの定義から [LineColor] セルの値を取得します。  <br/> |
|"コネクタパターン"  <br/> |テーマの定義から [LinePattern] セルの値を取得します。  <br/> |
|"コネクタウェイト"  <br/> |テーマの定義から [LineWeight] の値を取得します。  <br/> |
|"コネクタ透過"  <br/> |テーマの定義から [LineColorTrans] セルの値を取得します。  <br/> |
|"コネクタ丸め"  <br/> |テーマの定義から [Rounding] セルの値を取得します。  <br/> |
|"コネクタ開始"  <br/> |テーマの定義から [BeginArrow] セルの値を取得します。  <br/> |
|"コネクタ終了"  <br/> |テーマの定義から [EndArrow] セルの値を取得します。  <br/> |
|"コネクタの beginsize"  <br/> |テーマの定義から [BeginArrowSize] セルの値を取得します。  <br/> |
|"コネクタの endsize"  <br/> |テーマの定義から [EndArrowSize] セルの値を取得します。  <br/> |
|FillColor  <br/> |テーマの定義から [FillForegnd] セルの値を取得します。  <br/> |
|"FillColor2"  <br/> |テーマの定義から [FillBkgnd] セルの値を取得します。  <br/> |
|"filltransparency"  <br/> |テーマの定義から [FillForegndTrans] セルの値を取得します。  <br/> |
|fillpattern]  <br/> |テーマの定義から [FillPattern] セルの値を取得します。  <br/> |
|[linegradientenabled]  <br/> |テーマの定義から [LineGradientEnabled] セルの値を取得します。  <br/> |
|[linegradientdir]  <br/> |テーマの定義から [LineGradientDir] セルの値を取得します。  <br/> |
|[linegradientangle]  <br/> |テーマの定義から [LineGradientAngle] セルの値を取得します。  <br/> |
|[fillgradientenabled]  <br/> |テーマの定義から [FillGradientEnabled] セルの値を取得します。  <br/> |
|[fillgradientdir]  <br/> |テーマの定義から [FillGradientDir] セルの値を取得します。  <br/> |
|[fillgradientangle]  <br/> |テーマの定義から [FillGradientAngle] セルの値を取得します。  <br/> |
|[rotategradientwithshape]  <br/> |テーマの定義から [RotateGradientWithShape] セルの値を取得します。  <br/> |
|[usegroupgradient]  <br/> |テーマの定義から [UseGroupGradient] セルの値を取得します。  <br/> |
|"ShadowType"  <br/> |テーマの定義から [ShapeShdwType] セルの値を取得します。  <br/> |
|"ShadowColor"  <br/> |テーマの定義から [ShdwColor] セルの値を取得します。  <br/> |
|"ShadowTransparency"  <br/> |テーマの定義から [ShdwColorTrans] セルの値を取得します。  <br/> |
|"ShadowMagnification"  <br/> |テーマの定義から [ShapeShdwScaleFactor] セルの値を取得します。  <br/> |
|"ShadowBlur"  <br/> |テーマの定義から [ShapeShdwBlur] セルの値を取得します。  <br/> |
|"ShadowXOffset"  <br/> |テーマの定義から [ShapeShdwOffsetX] セルの値を取得します。  <br/> |
|"ShadowYOffset"  <br/> |テーマの定義から [ShapeShdwOffsetY] セルの値を取得します。  <br/> |
|"ShadowDirection"  <br/> |テーマの定義から [ShapeShdwObliqueAngle] セルの値を取得します。  <br/> |
|"ShadowPattern"  <br/> |テーマの定義から [ShdwPattern] セルの値を取得します。  <br/> |
|BevelTopType  <br/> |テーマの定義から [BevelTopType] セルの値を取得します。  <br/> |
|[beveltopwidth]  <br/> |テーマの定義から [BevelTopWidth] セルの値を取得します。  <br/> |
|[beveltopheight]  <br/> |テーマの定義から [BevelTopHeight] セルの値を取得します。  <br/> |
|"傾斜 el素材"  <br/> |テーマの定義から [BevelMaterialType] セルの値を取得します。  <br/> |
|"斜め el灯"  <br/> |テーマの定義から [BevelLightingType] セルの値を取得します。  <br/> |
|[bevellightingangle]  <br/> |テーマの定義から [BevelLightingAngle] セルの値を取得します。  <br/> |
|[bevelcontourcolor]  <br/> |テーマの定義から、斜めのセル値を取得します。  <br/> |
|[bevelcontoursize]  <br/> |テーマの定義から、斜めの elouroursize セルの値を取得します。  <br/> |
|[reflectionblur]  <br/> |テーマの定義から [reflectionblur] セルの値を取得します。  <br/> |
|[reflectiondist]  <br/> |テーマの定義から [reflectiondist] セルの値を取得します。  <br/> |
|[reflectionsize]  <br/> |テーマの定義から [reflectionsize] セルの値を取得します。  <br/> |
|[reflectiontrans]  <br/> |テーマの定義から [reflectiontrans] セルの値を取得します。  <br/> |
|[softedgessize]  <br/> |テーマの定義から [softedgessize] セルの値を取得します。  <br/> |
|[glowsize]  <br/> |テーマの定義から [GlowSize] セルの値を取得します。  <br/> |
|[glowcolor]  <br/> |テーマの定義から [GlowColor] セルの値を取得します。  <br/> |
|"GlowTransparency"  <br/> |テーマの定義から [GlowColorTrans] セルの値を取得します。  <br/> |
|[sketchamount]  <br/> |テーマの定義から [sketchamount] セルの値を取得します。  <br/> |
|[sketchenabled]  <br/> |テーマの定義から [sketchenabled] セルの値を取得します。  <br/> |
|[sketchfillchange]  <br/> |テーマの定義から [sketchfillchange] セルの値を取得します。  <br/> |
|[sketchlinechange]  <br/> |テーマの定義から [sketchlinechange] セルの値を取得します。  <br/> |
|[sketchlineweight]  <br/> |テーマの定義から [sketchlineweight] セルの値を取得します。  <br/> |
|"LatinFont"  <br/> |テーマの定義から [Font] セルの値を取得します。  <br/> |
|TextColor  <br/> |テーマの定義から [Color] セルの値を取得します。  <br/> |
|スタイル  <br/> |テーマの定義から、文字スタイルセルの値を取得します。  <br/> |
|"complexfont"  <br/> |テーマの定義から [ComplexScriptFont] セルの値を取得します。  <br/> |
|[asianfont]  <br/> |テーマの定義から [AsianFont] セルの値を取得します。  <br/> |
|"fillstop [x] Color"  <br/> |テーマの定義から、行*x*の色のセルの値を取得します。  <br/> |
|"fillstop [x] 透過性"  <br/> |テーマの定義から行*x*の colortrans セルの値を取得します。  <br/> |
|"fillstop [x] Position"  <br/> |テーマの定義から、行*x*の Position セルの値を取得します。  <br/> |
|"LineStop [x] Color"  <br/> |テーマの定義から、行*x*の色のセルの値を取得します。  <br/> |
|"LineStop [x] 透過性"  <br/> |テーマの定義から行*x*の colortrans セルの値を取得します。  <br/> |
|"LineStop [x] Position"  <br/> |テーマの定義から、行*x*の Position セルの値を取得します。  <br/> |
   
## <a name="example"></a>例

 `THEMEVAL("5")`
  
テーマの定義から "アクセント 3" の色を返します。
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
テーマの定義から [lineweight]] セルの値を返します。 この関数を含む図形にテーマが適用されていない場合、この関数は ' 0.7 pt. ' を返します。
  

