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
description: テキスト文字列の一部を別の文字列に置き換えます。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643214"
---
# <a name="substitute-function"></a>SUBSTITUTE 関数

テキスト文字列の一部を別の文字列に置き換えます。 
  
## <a name="syntax"></a>構文

 代用 (* **テキスト** *、* **文字列** *、* **と** * [、* **開始** *] [、* * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 置換前の文字列を含む文字列、またはその文字列を含むセルに対する参照を指定します。  <br/> |
| _文字列_ <br/> |必須  <br/> |**String** <br/> | 置換前の文字列を指定します。
  <br/> |
| _置換_ <br/> |必須  <br/> |**String** <br/> | _文字列_の置換に使用するテキストです。  <br/> |
| _start_num_opt_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |置換する文字列の出現箇所を指定します。  <br/> |
| _ignore_case_opt_ <br/> |省略可能  <br/> |**Boolean** <br/> |大文字と小文字を区別する場合は FALSE、区別しない場合は TRUE です。既定値は FALSE です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

 _Start_num_opt_を指定する場合のみ、検索_文字列_が置き換えられます。 _テキスト__文字列_に一致するすべてを変更する場合は、_置換します_。
  
テキスト文字列内の特定のテキストを置換する場合は、代替の関数を使用します。 テキスト文字列内の特定の位置にある文字列を置換する場合は、REPLACE 関数を使用します。
  
## <a name="example"></a>例

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
"1 JAN 2003" を返します。 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
「1 Jan 2003」を返します。 テキスト検索では大文字小文字を区別するため、変更は行われません。 
  

