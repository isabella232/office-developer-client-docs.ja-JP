---
title: SETF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: セルの数式を設定します。
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425975"
---
# <a name="setf-function"></a>SETF 関数

セルの数式を設定します。 
  
## <a name="syntax"></a>構文

setf (getref (* * *cell* * *), * * *formula* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セル_ <br/> |必須  <br/> |**String** <br/> |数式を設定するセルを指定します。  <br/> |
| _formula_ <br/> |必須  <br/> |**String** <br/> |使用する数式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

評価された場合、_数式_の式の結果は、_セル_の新しい数式になります。 _数式_が引用符で囲まれている場合は、引用符で囲まれた式が_セル_に書き込まれます。 _セル_を文字列に設定するには、_数式_を3組の引用符で囲みます。 
  
循環処理を避けるために、ターゲット セルは、GETREF() による参照を使用して指定するか、または文字列として指定する必要があります。Microsoft Visio では、図形を別の図面に移動したときに参照が調整されるので、GETREF を使用することをお勧めします。
  
getref または文字列として_セル_が指定されていない場合、関数はエラーを返し、セルの数式は変更されません。 _数式_に構文エラーがある場合、関数はエラーを返し、_セル_の数式は変更されません。 
  
## <a name="example-1"></a>例 1

setf (getref (A1)、1.5 の場合は\* 6 + 1 ft)
  
Scratch.A1 の数式を 21 インチに設定します。
  
## <a name="example-2"></a>例 2

setf (getref (A1)、"1.5 in \* 6+ 1 ft")
  
最初の数式を設定します。 A1 を 6 + 1 ft\*の式1.5 に指定します。
  
## <a name="example-3"></a>例 3

SETF( GETREF(Scratch.A1), """Say """"ahh""""""")
  
Scratch.A1 の数式を、文字列 "Say ""ahh""" に設定します。これは "Say "ahh"" と表示されます。
  

