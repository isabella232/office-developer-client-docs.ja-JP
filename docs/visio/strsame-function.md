---
title: STRSAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
ms.localizationpriority: medium
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: 文字列が同じかどうかを判断します。 同じ場合は TRUE、同じでない場合は FALSE を返します。
ms.openlocfilehash: 502d1b782c900d872b95a790cad38416b8d851dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603439"
---
# <a name="strsame-function"></a>STRSAME 関数

文字列が同じかどうかを判断します。 同じ場合は TRUE、同じでない場合は FALSE を返します。 
  
## <a name="syntax"></a>構文

STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |必須  <br/> |**String** <br/> |比較する最初の文字列を指定します。  <br/> |
| _string2_ <br/> |必須  <br/> |**String** <br/> |比較する 2 番目の文字列を指定します。  <br/> |
| _ignoreCase_ <br/> |省略可能  <br/> |**Boolean** <br/> |大文字/小文字を区別しない場合は TRUE を、大文字/小文字を区別する場合は FALSE を指定します。既定値は FALSE です。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>注釈

マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合は、STRSAMEEX 関数を使用します。
  
## <a name="example-1"></a>例 1

STRSAME("cat","dog")
  
FALSE を返します。
  
## <a name="example-2"></a>例 2

STRSAME("cat","cat")
  
TRUE を返します。
  
## <a name="example-3"></a>例 3

STRSAME("cat","cat", TRUE)
  
TRUE を返します。
  
## <a name="example-4"></a>例 4

STRSAME("cat","CAT")
  
FALSE を返します。
  
## <a name="example-5"></a>例 5

STRSAME("cat","CAT", TRUE)
  
TRUE を返します。
  
## <a name="example-6"></a>例 6

STRSAME("cät,"CAT", TRUE)
  
FALSE を返します。
  
## <a name="example-7"></a>例 7

STRSAME("cät,"CÄT", TRUE)
  
TRUE を返します。
  

