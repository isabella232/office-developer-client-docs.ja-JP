---
title: CONTAINERSHEETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: 図形を含む、指定されたコンテナーのシート参照を返します。
ms.openlocfilehash: 59d820760d09d56bdbc47ef2a56252d6214c6278
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559991"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF 関数

図形を含む、指定されたコンテナーのシート参照を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

CONTAINERSHEETREF(** *index* ** ** *[, category]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |コンテナーの 1 から始まるインデックス。詳細については、「備考」を参照してください。  <br/> |
| _category_ <br/> |省略可能  <br/> |**String** <br/> |コンテナーのカテゴリ。詳細については、「備考」を参照してください。  <br/> |
   
### <a name="return-value"></a>戻り値

シェイプシート参照
  
## <a name="remarks"></a>注釈

コンテナーの Z オーダー (前面から背面) を基に計算されるコンテナーのインデックス。
  
 *カテゴリ*  は、図形を分類するために使用できるユーザー定義の文字列です。 カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。 1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。 
  
図形がコンテナーのメンバーではない場合、または指定されたインデックス番号とカテゴリの両方に一致するコンテナーがない場合、CONTAINERSHEETREF は #REF! を返します。
  
## <a name="example"></a>例

CONTAINERSHEETREF(1)!Height 
  
図形が属しているページの最前面にあるコンテナーの [Height] セルの値を返します。 
  

