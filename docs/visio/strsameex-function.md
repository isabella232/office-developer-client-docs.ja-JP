---
title: STRSAMEEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
ms.localizationpriority: medium
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: 2 つの文字列が同じかどうかを判断します。
ms.openlocfilehash: ab5d1a4b1a2005014ca6386ef21e18f10b042588
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549484"
---
# <a name="strsameex-function"></a>STRSAMEEX 関数

2 つの文字列が同じかどうかを判断します。
  
## <a name="syntax"></a>構文

STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |必須  <br/> |**String** <br/> |比較する最初の文字列を指定します。  <br/> |
| _string2_ <br/> |必須  <br/> |**String** <br/> | 比較する 2 番目の文字列を指定します。  <br/> |
| _localeID_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |ロケールの ID を示すコードを指定します。  <br/> |
| _flag_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> | 比較の種類を示すビットを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>注釈

STRSAMEEX は、2 つの入力文字列が同じ場合は TRUE を、異なる場合は FALSE を返します。マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合に、この関数を使用します。
			

  
STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。
  
|**Flag**|**説明**|
|:-----|:-----|
|1  <br/> |大文字/小文字を区別しません。  <br/> |
|2  <br/> |間隔のない文字を無視します。  <br/> |
|4   <br/> |記号を無視します。  <br/> |
|4096  <br/> |句読点を記号として扱います。  <br/> |
|65536  <br/> |ひらがなとカタカナを区別しません。  <br/> |
|131072  <br/> |半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。  <br/> |
   

