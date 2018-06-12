---
title: BOUNDINGBOXRECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: 図形の境界ボックスの、指定した端の座標を返します。
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804928"
---
# <a name="boundingboxrect-function"></a>BOUNDINGBOXRECT 関数

図形の境界ボックスの、指定した端の座標を返します。
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

BOUNDINGBOXRECT (* **インデックス** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |必須  <br/> |**Integer** <br/> |座標を取得する図形の境界ボックスの端。使用可能な値については、「備考」を参照してください。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **番号**
  
## <a name="remarks"></a>Remarks

 *インデックス*には、次の値のいずれかを指定できます。 
  
|**アイテム**|**値**|
|:-----|:-----|
|左端  <br/> |0  <br/> |
|右端  <br/> |1  <br/> |
|上端  <br/> |2  <br/> |
|下端  <br/> |3  <br/> |
   
図形に親がある場合、戻り値はその親の座標系では。
  

