---
title: BOUNDINGBOXRECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: 図形の境界ボックスの、指定した端の座標を返します。
ms.openlocfilehash: da94210970e1c3331380e1ee319b0ba59230ea68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598718"
---
# <a name="boundingboxrect-function"></a>BOUNDINGBOXRECT 関数

図形の境界ボックスの、指定した端の座標を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

BOUNDINGBOXRECT(** *Index* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |座標を取得する図形の境界ボックスの端。使用可能な値については、「備考」を参照してください。  <br/> |
   
### <a name="return-value"></a>戻り値

 **数値**
  
## <a name="remarks"></a>注釈

 *Index*  には、次のいずれかの値を指定できます。 
  
|**項目**|**値**|
|:-----|:-----|
|左端  <br/> |0  <br/> |
|右端  <br/> |1  <br/> |
|上端  <br/> |2  <br/> |
|下端  <br/> |3  <br/> |
   
図形に親がある場合、戻り値は親の座標系になります。
  

