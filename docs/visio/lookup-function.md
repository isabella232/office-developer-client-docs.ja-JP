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
description: リスト内の部分文字列のキーの場所または対象の文字列に区切り文字が含まれている場合は-1 を返しますを示す 0 から始まるインデックスを返します。
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805800"
---
# <a name="lookup-function"></a>LOOKUP 関数

_リスト_内の部分文字列_キー_の場所または対象の文字列に_区切り記号_が含まれている場合は-1 を返しますを示す 0 から始まるインデックスを返します。
  
## <a name="syntax"></a>構文

参照 ("* **キー* * *」、「* **リスト** * [、* **区切り記号** *」]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _キー_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |検索する文字列を指定します。  <br/> |
| _リスト_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 検索するリストを指定します。  <br/> |
| _delimiter_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | _リスト_内の区切り文字として使用する文字列です。 _区切り記号_文字列は 1 文字以上の長さし、マルチバイト文字を含めることがあります。 既定値は、セミコロンです。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値型 (Numeric)
  
## <a name="remarks"></a>注釈

LOOKUP 関数による検索では、大文字と小文字は区別されません。リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。 
  
すべての引数には、文字列を指定するか、文字列に変換できる式を指定する必要があります。それ以外の引数を指定した場合は、不正な引数が空の文字列に置き換わります。 
  
## <a name="example-1"></a>例 1

LOOKUP("rat","cat;rat;;goat")
  
1 を返します。
  
## <a name="example-2"></a>例 2

LOOKUP("",";cat;rat;;goat")
  
0 を返します。
  
## <a name="example-3"></a>例 3

LOOKUP("t","cat;rat;;goat","a")
  
3 を返します。
  

