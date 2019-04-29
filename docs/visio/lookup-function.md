---
title: LOOKUP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: リスト内のサブ文字列キーの位置を示す0から始まるインデックスを返します。または、対象の文字列に区切り文字が含まれている場合は-1 を返します。
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410330"
---
# <a name="lookup-function"></a>LOOKUP 関数

_リスト_内のサブ文字列_キー_の位置を示す0から始まるインデックスを返します。または、対象の文字列に_区切り文字_が含まれている場合は-1 を返します。
  
## <a name="syntax"></a>構文

LOOKUP ("* * *key* * *", "* * *list* * *" [, "* * *delimiter* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |必須  <br/> |**String** <br/> |検索する文字列を指定します。  <br/> |
| _list_ <br/> |必須  <br/> |**String** <br/> | 検索するリストを指定します。  <br/> |
| _delimiter_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | _リスト_内で区切り文字として使用する文字列。 _区切り_文字には、複数の文字の長さを指定できます。また、マルチバイト文字を含めることもできます。 既定値はセミコロンです。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

LOOKUP 関数による検索では、大文字と小文字は区別されません。リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。 
  
すべての引数には、文字列を指定するか、文字列に変換できる式を指定する必要があります。それ以外の引数を指定した場合は、不正な引数が空の文字列に置き換わります。 
  
## <a name="example-1"></a>例 1

参照 ("rat", "cat; rat;;goat ")
  
1 を返します。
  
## <a name="example-2"></a>例 2

LOOKUP ("", "; cat; rat;;goat ")
  
0 を返します。
  
## <a name="example-3"></a>例 3

LOOKUP ("t", "cat; rat;;goat "," a ")
  
3 を返します。
  

