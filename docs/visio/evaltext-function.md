---
title: EVALTEXT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
ms.localizationpriority: medium
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: shapename のテキストを数式として評価し、結果を返します。
ms.openlocfilehash: 2ba21cc55ea24144396fe4ef029b9a3e1014484a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574301"
---
# <a name="evaltext-function"></a>EVALTEXT 関数

shapename のテキストを  _数式_ として評価し、結果を返します。 
  
## <a name="syntax"></a>構文

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |必須  <br/> |**String** <br/> |関連付けられている図形のテキスト構成が変更されたときにトリガーされるセルを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

 _shapename_ を使用して、現在の図形以外の図形のテキストを参照できます。 
  
テキストがない場合、結果はゼロになります。テキストを評価できない場合、関数はエラーを返します。
  
## <a name="example"></a>例

EVALTEXT(Line.2!theText) 
  
[線 2] 図形に含まれているテキストを評価します。たとえば、[線 2] に "4 ft + 0.5 ft" が含まれている場合、値 4.5 ft を返します。 
  

