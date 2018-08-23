---
title: HASCATEGORY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: 指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805519"
---
# <a name="hascategory-function"></a>HASCATEGORY 関数

指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

HASCATEGORY (* **カテゴリ** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |検索するカテゴリ。  <br/> |
   
### <a name="return-value"></a>戻り値

 **ブール型 (Boolean)**
  
## <a name="remarks"></a>注釈

 *カテゴリ*は、図形を分類するために使用できるユーザー定義の文字列です。 User.msvShapeCategories 図形のシェイプ シート セルでは、カテゴリを定義することができます。 カテゴリをセミコロンで区切ると、図形の複数のカテゴリを定義できます。 
  

