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
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806593"
---
# <a name="substitute-function"></a>SUBSTITUTE 関数

テキスト文字列の一部を別の文字列に置き換えます。 
  
## <a name="syntax"></a>構文

 代用 (* **テキスト** *、* **文字列** *、* **と** * [、* **開始** *] [、* * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 置換前の文字列を含む文字列、またはその文字列を含むセルに対する参照を指定します。  <br/> |
| _文字列_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 置換するテキストです。  <br/> |
| _置換_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | _文字列_の置換に使用するテキストです。  <br/> |
| _start_num_opt_ <br/> |省略可能  <br/> |**数値** <br/> |何番目の old_text を置換するかを指定します。  <br/> |
| _ignore_case_opt_ <br/> |省略可能  <br/> |**ブール型 (Boolean)** <br/> |大文字と小文字を区別する場合は FALSE、区別しない場合は TRUE です。既定値は FALSE です。  <br/> |
   
### <a name="return-value"></a>�߂�l

String
  
## <a name="remarks"></a>Remarks

 _Start_num_opt_を指定する場合のみ、検索_文字列_が置き換えられます。 _テキスト__文字列_に一致するすべてを変更する場合は、_置換します_。
  
テキスト文字列内の特定のテキストを置換する場合は、代替の関数を使用します。 テキスト文字列内の特定の位置にある文字列を置換する場合は、REPLACE 関数を使用します。
  
## <a name="example"></a>例

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
"1 JAN 2003" を返します。 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
「1 Jan 2003」を返します。 テキスト検索では大文字小文字を区別するため、変更は行われません。 
  

