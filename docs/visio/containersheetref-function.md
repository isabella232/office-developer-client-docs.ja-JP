---
title: CONTAINERSHEETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: 図形を含む、指定されたコンテナーのシート参照を返します。
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805111"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF 関数

図形を含む、指定されたコンテナーのシート参照を返します。
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

CONTAINERSHEETREF (* **インデックス** * * * *[] カテゴリ** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |必須  <br/> |**Integer** <br/> |コンテナーの 1 から始まるインデックス。詳細については、「備考」を参照してください。  <br/> |
| _category_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |コンテナーのカテゴリ。詳細については、「備考」を参照してください。  <br/> |
   
### <a name="return-value"></a>�߂�l

シェイプシート参照
  
## <a name="remarks"></a>注釈

コンテナーの Z オーダー (前面から背面) を基に計算されるコンテナーのインデックス。
  
 *カテゴリ*は、図形を分類するために使用できるユーザー定義の文字列です。 User.msvShapeCategories 図形のシェイプ シート セルでは、カテゴリを定義することができます。 カテゴリをセミコロンで区切ると、図形の複数のカテゴリを定義できます。 
  
図形がコンテナーのメンバーではない場合、または指定されたインデックス番号とカテゴリの両方に一致するコンテナーがない場合、CONTAINERSHEETREF は #REF! を返します。
  
## <a name="example"></a>例

CONTAINERSHEETREF(1)!Height 
  
図形が属しているページの最前面にあるコンテナーの [Height] セルの値を返します。 
  

