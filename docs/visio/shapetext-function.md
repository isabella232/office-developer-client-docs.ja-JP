---
title: SHAPETEXT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: 図形からテキストを取得します。
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806439"
---
# <a name="shapetext-function"></a>SHAPETEXT 関数

図形からテキストを取得します。 
  
## <a name="syntax"></a>構文

SHAPETEXT (* **なります。[Thetext]* * * * * *[] フラグ** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _なります!テキスト_ <br/> |必須  <br/> ||セルへの参照では、接続先の図形の [thetext] という名前です。  _なります!_ テキストを取得する図形の名前です。  <br/> |
| _フラグ_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |テキストの書式を示すビットを指定します。既定のフラグ (0) は、図形に表示されるとおりにテキストを返します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

SHAPETEXT 関数では、次のフラグを任意に組み合わせて使用できます。
  
|**Flag**|**説明**|
|:-----|:-----|
|0  <br/> |図形に表示されているとおりにテキストを返します。  <br/> |
|1  <br/> |任意のハイフンを含みます。  <br/> |
|2  <br/> |フィールドの拡張テキストは除外されます。  <br/> |
|4  <br/> |タブを単一のスペースに変換します。  <br/> |
|8  <br/> |タブを複数のスペースに変換します。  <br/> |
|16  <br/> |改行文字と行送りをスペースに変換します。  <br/> |
|32  <br/> |印刷用の引用符を通常の引用符に変換します。  <br/> |
|64  <br/> |隣接した余白を単一のスペースに変換します。  <br/> |
   
## <a name="example-1"></a>例 1

SHAPETEXT(sheetN!theText)
  
図形に表示されているとおりに、sheetN という図形のテキストを返します。
  
## <a name="example-2"></a>例 2

SHAPETEXT(theText)
  
図形に表示されているとおりに、現在の図形のテキストを返します。
  
## <a name="example-3"></a>例 3

SHAPETEXT(theText, 84)
  
現在の図形のテキストを返します。隣接した余白から単一のスペースへの変換 (64)、改行文字と行送りのスペースへの変換 (16)、およびタブの単一のスペースへの変換 (4) も行います。これらのフラグの合計は 84 です。
  

