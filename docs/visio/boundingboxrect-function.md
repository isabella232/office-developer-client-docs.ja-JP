---
title: BOUNDINGBOXRECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: 図形の境界ボックスの、指定した端の座標を返します。
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418072"
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
  

