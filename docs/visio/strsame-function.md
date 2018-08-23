---
title: STRSAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: 文字列が同じかどうかを判断します。 値が同じ場合に TRUE を返します false の場合は、します。
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806567"
---
# <a name="strsame-function"></a>STRSAME 関数

文字列が同じかどうかを判断します。 値が同じ場合に TRUE を返します false の場合は、します。 
  
## <a name="syntax"></a>構文

STRSAME ("* * *string1* * *「,」* **文字列 2* * *」、* * *ignoreCase* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _文字列 1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |比較する最初の文字列を指定します。  <br/> |
| _文字列 2_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |比較する 2 番目の文字列を指定します。  <br/> |
| _ignoreCase_ <br/> |省略可能  <br/> |**ブール型 (Boolean)** <br/> |大文字/小文字を区別しない場合は TRUE を、大文字/小文字を区別する場合は FALSE を指定します。既定値は FALSE です。  <br/> |
   
### <a name="return-value"></a>戻り値

ブール型
  
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
  

