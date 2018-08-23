---
title: FIND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: 別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、それを含むテキスト文字列内の位置を基準にして検索するテキスト文字列の開始位置を返します。
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805413"
---
# <a name="find-function"></a>FIND 関数

別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、それを含むテキスト文字列内の位置を基準にして検索するテキスト文字列の開始位置を返します。
  
## <a name="syntax"></a>構文

検索 (* **文字列** *、* **対象** *、[* **開始** *]、[* * *ignore_case* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _検索文字列_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |検索する文字列を指定します。  <br/> |
| _format_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |検索する文字列を含んでいる文字列を指定します。  <br/> |
| _開始位置_ <br/> |省略可能  <br/> |**番号** <br/> |文字の検索を開始する位置。 _対象_の最初の文字は、1 です。 _開始位置_が指定されていない場合は 1 であると見なされます。  <br/> |
| _ignore_case_ <br/> |省略可能  <br/> |**ブール型 (Boolean)** <br/> |既定では、FIND 関数は大文字と小文字を区別します。大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>備考

複数の一致が見つかった場合、FIND 関数は、文字列に一致する最初の開始位置を返します。 _文字列_引数には、ワイルドカードを使用する任意の文字は考慮されません。 
  
場合_文字列を指定_します。
  
-  空 ("")、検索に一致する検索文字列の最初の文字 (つまり、文字番号_開始位置_または 1)。 
    
- ない_対象_検索、#VALUE を返します。 エラー値です。 
    
場合_開始位置_。
  
- start_num がゼロ (0) 以下の場合、FIND は #VALUE! エラー値を返します。 
    
- _対象_#VALUE を FINDreturns の長さを超える値です。 エラー値です。 
    
## <a name="example"></a>例

FIND ("2003","January 1, 2003") 
  
12 を返します。 
  

