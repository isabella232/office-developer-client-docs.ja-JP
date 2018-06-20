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
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806373"
---
# <a name="setf-function"></a>SETF 関数

セルの数式を設定します。 
  
## <a name="syntax"></a>構文

SETF (GETREF (* **セル** *)、* **式** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セル_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルの数式を設定するのには。  <br/> |
| _formula_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |使用する数式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

評価するときは、_セル_に新しい数式が_数式_内の式の結果になります。 _数式_は、引用符で囲まれたが、引用符で囲まれた式が_セル_に書き込まれます。 _セル_を文字列に設定するには、3 つの引用符 () で_数式_を囲みます。 
  
循環処理を避けるために、ターゲット セルは、GETREF() による参照を使用して指定するか、または文字列として指定する必要があります。Microsoft Visio では、図形を別の図面に移動したときに参照が調整されるので、GETREF を使用することをお勧めします。
  
_セル_が GETREF を使用して指定されていない場合、または文字列として、関数には、エラーが返され、ないセルの数式を変更します。 _数式_に構文エラーが含まれている場合、関数はエラーを返し、_セル_の数式は変更されません。 
  
## <a name="example-1"></a>例 1

SETF (GETREF(Scratch.A1)、1.5 で\*6 + 1 ft)
  
Scratch.A1 の数式を 21 インチに設定します。
  
## <a name="example-2"></a>例 2

SETF (GETREF(Scratch.A1)、"の 1.5 \* 6 + 1 フィート」)
  
最初の数式を設定します。 A1 に、式 1.5\*6 + 1 フィートです。
  
## <a name="example-3"></a>例 3

SETF( GETREF(Scratch.A1), """Say """"ahh""""""")
  
Scratch.A1 の数式を、文字列 "Say ""ahh""" に設定します。これは "Say "ahh"" と表示されます。
  

