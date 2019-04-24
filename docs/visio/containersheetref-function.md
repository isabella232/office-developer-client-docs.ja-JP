---
title: CONTAINERSHEETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: 図形を含む、指定されたコンテナーのシート参照を返します。
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318985"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF 関数

図形を含む、指定されたコンテナーのシート参照を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

CONTAINERSHEETREF (* * *index* * * * * *[, category]* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |コンテナーの 1 から始まるインデックス。 詳細については、「備考」を参照してください。  <br/> |
| _項目_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |コンテナーのカテゴリ。 詳細については、「備考」を参照してください。  <br/> |
   
### <a name="return-value"></a>戻り値

シェイプシート参照
  
## <a name="remarks"></a>解説

コンテナーの Z オーダー (前面から背面) を基に計算されるコンテナーのインデックス。
  
 *カテゴリ*は、図形の分類に使用できるユーザー定義の文字列です。 カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。 1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。 
  
図形がコンテナーのメンバーではない場合、または指定されたインデックス番号とカテゴリの両方に一致するコンテナーがない場合、CONTAINERSHEETREF は #REF! を返します。
  
## <a name="example"></a>例

CONTAINERSHEETREF (1)!寸法 
  
図形が属しているページの最前面にあるコンテナーの [Height] セルの値を返します。 
  

