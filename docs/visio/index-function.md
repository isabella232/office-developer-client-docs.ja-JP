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
description: 区切り記号で区切られたリスト内の位置を示す 0 から始まるインデックス位置の部分文字列を返します。 または、インデックスが範囲を返しますが空の文字列、または errorvalue 引数として提供されている場合。
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805575"
---
# <a name="index-function"></a>INDEX 関数

_区切り記号_で区切られた_リスト_内の位置の 0 から始まる_インデックス_位置の部分文字列を返します。 または、インデックスが範囲を返しますが空の文字列、または*errorvalue*引数として提供されている場合。 
  
## <a name="syntax"></a>構文

インデックス (* **インデックス** *、"* **リスト** *] [、[* **区切り記号** *] [、[* * *errorvalue* * *]]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |必須  <br/> |**番号** <br/> |検索する位置を指定します。  <br/> |
| _リスト_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |検索するリストを指定します。  <br/> |
| _delimiter_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | _リスト_内の区切り文字として使用する文字列です。 _区切り記号_文字列は、1 つ以上の文字し、マルチバイト文字が含まれます。 既定値は、セミコロンです。  <br/> |
| _errorvalue_ <br/> |省略可能  <br/> |**番号** <br/> | インデックスが範囲外の場合に返す、ユーザー指定の値です。既定では、空の文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

リストの先頭または終わりが区切り文字の場合、リストの前または後に NULL 文字列があると見なされます。リストに区切り文字を連続して指定すると、その間に NULL 文字列があることを意味します。 
  
インデックスが範囲外にある場合は、Visio は、空の文字列、または*errorvalue*引数として指定された省略可能なトークンを返します。 
  
## <a name="example-1"></a>例 1

INDEX(3,"cat;rat;;goat")
  
"goat" を返します。
  
## <a name="example-2"></a>例 2

INDEX(54,";1;2;3;",,"ERROR")
  
「エラー」を返します。
  

