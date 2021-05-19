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
description: テキスト文字列の一部を別のテキスト文字列に置き換える。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346824"
---
# <a name="substitute-function"></a>SUBSTITUTE 関数

テキスト文字列の一部を別のテキスト文字列に置き換える。 
  
## <a name="syntax"></a>構文

 SUBSTITUTE (** *text* **, ** *old_text* **, **** new_text ** [, **** start_num ** **, **** ignore_case_opt ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 文字を置き換えるテキストを含むセルへのテキストまたは参照。  <br/> |
| _old_text_ <br/> |必須  <br/> |**String** <br/> | 置換するテキスト。  <br/> |
| _new_text_ <br/> |必須  <br/> |**String** <br/> | 文字列を置換するために使用 _するold_text。_  <br/> |
| _start_num_opt_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |置換するファイルのold_text指定します。  <br/> |
| _ignore_case_opt_ <br/> |省略可能  <br/> |**Boolean** <br/> |大文字と小文字を区別する場合は FALSE。それ以外の場合は TRUE。 既定値は "FALSE" です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

 この値を  _指定start_num_opt、_ その  _出現回数old_text_ 置き換えられる。 それ以外の場合は、_テキストold_text__の出現_ 回数が 1 回 _にnew_text。_
  
テキスト文字列内の特定のテキストを置き換える場合は、SUBSTITUTE 関数を使用します。 テキスト文字列内の特定の場所で発生するテキストを置き換える場合は、REPLACE 関数を使用します。
  
## <a name="example"></a>例

SUBSTITUTE ("2003 年 1 月 1 日"、"1 月"、"JAN") 
  
"1 JAN 2003" を返します。 
  
SUBSTITUTE ("2003 年 1 月 1 日","1 月","JAN") 
  
"2003 年 1 月 1 日" を返します。 テキスト検索では大文字と小文字が区別されるので、変更は行なされません。 
  

