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
description: 別のテキスト文字列に含まれる1つのテキスト文字列を検索し、その文字列を含む文字列の位置を基準にして、検索する文字列の開始位置を返します。
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322499"
---
# <a name="find-function"></a>FIND 関数

別のテキスト文字列に含まれる1つのテキスト文字列を検索し、その文字列を含む文字列の位置を基準にして、検索する文字列の開始位置を返します。
  
## <a name="syntax"></a>構文

find (* * ** 検索語 * *, * ** * 対象 * *, [* **開始位置** *], [* * *ignore_case* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _文字列_ <br/> |必須  <br/> |**String** <br/> |検索する文字列を指定します。  <br/> |
| _format_ <br/> |必須  <br/> |**String** <br/> |検索する文字列を含んでいる文字列を指定します。  <br/> |
| _開始_ <br/> |省略可能  <br/> |**数値** <br/> |検索を開始する文字の位置を指定します。 対象の最初の__ 文字は1です。 _開始位置_が指定されていない場合は、1と見なされます。  <br/> |
| _ignore_case_ <br/> |省略可能  <br/> |**Boolean** <br/> |既定では、FIND 関数は大文字と小文字を区別します。 大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>解説

一致する文字列が複数ある場合、FIND 関数は文字列内で最初に一致した文字列の開始位置を返します。 "検索_文字列_" 引数では、ワイルドカードとして使用する文字は考慮されません。 
  
検索_文字列_の場合:
  
-  が空 ("") の場合、FIND は検索文字列の最初の文字 (つまり、_開始位置_または1の文字) と一致します。 
    
- 対象に含まれ__ ない場合、FIND は #VALUE を返します。 が返されます。 
    
_開始位置_:
  
- start_num がゼロ (0) 以下の場合、FIND は #VALUE! エラー値を返します。 
    
- が対象の長さより大きい__ 場合、findreturns #VALUE を返します。 が返されます。 
    
## <a name="example"></a>例

FIND ("2003","January 1, 2003") 
  
12 を返します。 
  

