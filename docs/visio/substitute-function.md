---
title: SUBSTITUTE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: 文字列の一部を別の文字列に置き換えます。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346824"
---
# <a name="substitute-function"></a>SUBSTITUTE 関数

文字列の一部を別の文字列に置き換えます。 
  
## <a name="syntax"></a>構文

 代替 (* * *text* * *, * **文字列** *, * **置換** * [, * **開始位置** *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 文字を置換する文字列または文字列を含むセルへの参照を指定します。  <br/> |
| _文字列_ <br/> |必須  <br/> |**String** <br/> | 置換する文字列を指定します。  <br/> |
| _文字列_ <br/> |必須  <br/> |**String** <br/> | 文字列を置換するために使用する__ 文字列を指定します。  <br/> |
| _start_num_opt_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |置換する文字列の出現を指定します。  <br/> |
| _ignore_case_opt_ <br/> |省略可能  <br/> |**Boolean** <br/> |大文字と小文字を区別する場合は FALSE。それ以外の場合は TRUE。 既定値は "FALSE" です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

 _start_num_opt_を指定すると、指定した_文字列_だけが置き換えられます。 それ以外の場合は__ 、_テキスト_内のすべての検索文字列が置換文字列に変更され_ます。_
  
文字列内の特定のテキストを置換する場合は、代替関数を使用します。 文字列内の特定の位置にある文字列を置換する場合は、replace 関数を使用します。
  
## <a name="example"></a>例

代用 ("1 年1月 2003", "january", "JAN", "JAN") 
  
"1 JAN 2003" を返します。 
  
代替 ("1 月 2003"、"january"、"JAN", "JAN") 
  
"1 January 2003" を返します。 テキスト検索では大文字と小文字が区別されるため、変更は行われません。 
  

