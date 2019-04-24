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
description: 2つの文字列が同じかどうかを判断します。
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329793"
---
# <a name="strsameex-function"></a>STRSAMEEX 関数

2つの文字列が同じかどうかを判断します。
  
## <a name="syntax"></a>構文

strsameex ("* * *string1* * *", "* * *string2* * *", * * *localeID* * *, * * *flag* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |必須  <br/> |**String** <br/> |比較する最初の文字列を指定します。  <br/> |
| _string2_ <br/> |必須  <br/> |**String** <br/> | 比較する 2 番目の文字列を指定します。  <br/> |
| _localeID_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |ロケールの ID を示すコードを指定します。  <br/> |
| _flag_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> | 比較の種類を示すビットを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>解説

STRSAMEEX は、2 つの入力文字列が同じ場合は TRUE を、異なる場合は FALSE を返します。 マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合に、この関数を使用します。
  
STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。
  
|**Flag**|**説明**|
|:-----|:-----|
|1-d  <br/> |大文字/小文字を区別しません。  <br/> |
|pbm-2  <br/> |間隔のない文字を無視します。  <br/> |
|2/4  <br/> |記号を無視します。  <br/> |
|4096  <br/> |句読点を記号として扱います。  <br/> |
|65536  <br/> |ひらがなとカタカナを区別しません。  <br/> |
|131072  <br/> |半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。  <br/> |
   

