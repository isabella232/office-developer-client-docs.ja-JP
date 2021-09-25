---
title: FIND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
ms.localizationpriority: medium
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: 別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、その文字列を含むテキスト文字列内の位置を基準に検索するテキスト文字列の開始位置を返します。
ms.openlocfilehash: 313f6b97c5aacbb83e8aeedb91b69ce28cef465a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590199"
---
# <a name="find-function"></a>FIND 関数

別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、その文字列を含むテキスト文字列内の位置を基準に検索するテキスト文字列の開始位置を返します。
  
## <a name="syntax"></a>構文

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ **** ignore_case ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |必須  <br/> |**String** <br/> |検索する文字列を指定します。  <br/> |
| _format_ <br/> |必須  <br/> |**String** <br/> |検索する文字列を含んでいる文字列を指定します。  <br/> |
| _start_num_ <br/> |オプション  <br/> |**数値** <br/> |検索を開始する文字の位置を指定します。 この値の最初  _のwithin_text_ は 1 です。 この  _start_num_ 見つからない場合は、1 と見なされます。  <br/> |
| _ignore_case_ <br/> |省略可能  <br/> |**Boolean** <br/> |既定では、FIND 関数は大文字と小文字を区別します。大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

一致する文字列が複数ある場合、FIND 関数は文字列内で最初に一致した文字列の開始位置を返します。 引数  _find_text_ は、任意の文字をワイルドカードと見なしません。 
  
次 _find_text:_
  
-  空 ("") の場合、FIND は検索文字列の最初の文字 (つまり、番号が 1 または 1)  _start_num_ 一致します。 
    
- ファイルに表示されない  _場合within_text_ FIND は、次の#VALUE。 が返されます。 
    
次 _start_num:_
  
- start_num がゼロ (0) 以下の場合、FIND は #VALUE! エラー値を返します。 
    
- 値の長さ  _より大きい_ 場合、FINDreturns within_textを返#VALUE! が返されます。 
    
## <a name="example"></a>例

FIND ("2003","January 1, 2003") 
  
12 を返します。 
  

