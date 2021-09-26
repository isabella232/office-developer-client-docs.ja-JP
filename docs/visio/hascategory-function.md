---
title: HASCATEGORY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: 指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
ms.openlocfilehash: 953894bbc2914a363c4db99338528fa5f8ac7504
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598543"
---
# <a name="hascategory-function"></a>HASCATEGORY 関数

指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

HASCATEGORY(** *category* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |必須  <br/> |**String** <br/> |検索するカテゴリ。  <br/> |
   
### <a name="return-value"></a>戻り値

 **ブール型 (Boolean)**
  
## <a name="remarks"></a>注釈

 *カテゴリ*  は、図形を分類するために使用できるユーザー定義の文字列です。 カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。 1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。 
  

