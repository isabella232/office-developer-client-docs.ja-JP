---
title: STRSAMEEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: 2 つの文字列が同じかどうかを判断します。
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806589"
---
# <a name="strsameex-function"></a>STRSAMEEX 関数

2 つの文字列が同じかどうかを判断します。
  
## <a name="syntax"></a>構文

場合は、STRSAMEEX ("* * *string1* * *「,」* **文字列 2* * *」、* **ロケール Id* * *、* **フラグ** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _文字列 1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |比較する最初の文字列を指定します。  <br/> |
| _文字列 2_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 比較する 2 番目の文字列を指定します。  <br/> |
| _ロケール Id_ <br/> |必須  <br/> |**数値** <br/> |ロケールの ID を示すコードを指定します。  <br/> |
| _フラグ_ <br/> |必須  <br/> |**数値** <br/> | 比較の種類を示すビットを指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

ブール型
  
## <a name="remarks"></a>Remarks

両方の入力文字列が同じ場合は TRUE と FALSE を指定するとされていない場合は、STRSAMEEX を返します。 マルチバイト文字列を比較する、または特定のロケールの規則を使用する比較を行うには、この関数を使用します。
  
STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。
  
|**Flag**|**説明**|
|:-----|:-----|
|1  <br/> |大文字/小文字を区別しません。  <br/> |
|2  <br/> |間隔のない文字を無視します。  <br/> |
|4  <br/> |記号を無視します。  <br/> |
|4096  <br/> |句読点を記号として扱います。  <br/> |
|65536  <br/> |ひらがなとカタカナを区別しません。  <br/> |
|131072  <br/> |半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。  <br/> |
   

