---
title: USE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
ms.localizationpriority: medium
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: LinePattern、FillPattern、BeginArrow、または EndArrow セルに配置すると、名前と呼ばれる線のパターン、塗りつぶしパターン、または線の端を図形に適用します。
ms.openlocfilehash: 411193444316617e09ee947f34cc4f6a7c49d99e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622655"
---
# <a name="use-function"></a>USE 関数

LinePattern、FillPattern、BeginArrow、または EndArrow セルに配置すると、名前と呼ばれる線のパターン、塗りつぶしパターン、または線の端を図形に適用します。  
  
## <a name="syntax"></a>構文

USE(" ** *name* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |必須  <br/> |**String** <br/> |有効なマスター シェイプの名前である、任意の文字列を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

文書の文書ステンシルにマスター名が存在する場合、パターンは線のパターン、塗りつぶしパターン、開始矢印、または終了矢印として適用されます。 
  
この関数は常に 254 を返します。
  
## <a name="example"></a>例

USE("線路") 
  
"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。 
  

