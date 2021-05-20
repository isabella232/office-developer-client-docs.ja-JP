---
title: INDEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: 区切り記号で区切られたリスト内の 0 から始る位置インデックスの部分文字列を返します。 または、インデックスが範囲を外している場合は、空の文字列または errorvalue 引数として指定されたオプションのトークンを返します。
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431576"
---
# <a name="index-function"></a>INDEX 関数

区切り記号で区切られたリスト内の 0 から始る位置インデックス _の部分文字列_ を返 _します_。 または、インデックスが範囲を外している場合は、空の文字列または errorvalue 引数として指定されたオプションの  *トークンを返*  します。 
  
## <a name="syntax"></a>構文

INDEX(** *index* **," ** *list* ** "[,** *区切* り文字 ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |必須  <br/> |**数値** <br/> |検索する位置を指定します。  <br/> |
| _リスト_ <br/> |必須  <br/> |**String** <br/> |検索するリストを指定します。  <br/> |
| _delimiter_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | リスト内で区切り文字として使用する  _文字列_ です。 区切  _り文字_ は、長さが 1 文字以上で、マルチバイト文字を含めることができます。 既定値はセミコロンです。  <br/> |
| _errorvalue_ <br/> |省略可能  <br/> |**数値** <br/> | インデックスが範囲外の場合に返す、ユーザー指定の値です。既定では、空の文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。 
  
インデックスが範囲を外している場合、Visio引数 errorvalue として指定された空の文字列またはオプションの *トークンを返* します。 
  
## <a name="example-1"></a>例 1

INDEX(3,"cat;rat;;ヤギ")
  
"goat" を返します。
  
## <a name="example-2"></a>例 2

INDEX(54,";1;2;3;",,"ERROR")
  
"ERROR" を返します。
  

