---
title: BOUNDINGBOXDIST 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: 図形の境界ボックスの、指定した部分の測定値を返します。
ms.openlocfilehash: 7a3da5917f38596ff3d277fc01d145752b6bda32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554818"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST 関数

図形の境界ボックスの、指定した部分の測定値を返します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

BOUNDINGBOXDIST(** *Index* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |必須  <br/> |**数値** <br/> |図形の境界ボックスの一部を測定して返します。 使用可能な値については備考を参照してください。  <br/> |
   
### <a name="return-value"></a>戻り値

 **数値**
  
## <a name="remarks"></a>注釈

 *Index*  には、次のいずれかの値を指定できます。 
  
|**項目**|**値**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1  <br/> |
|左端から図形のピンまでの距離  <br/> |2  <br/> |
|図形のピンから右端までの距離  <br/> |3  <br/> |
|図形のピンから上端までの距離  <br/> |4   <br/> |
|下端から図形のピンまでの距離  <br/> |5  <br/> |
|境界ボックスの中心から PinX までの距離  <br/> |6   <br/> |
|境界ボックスの中心から PinY までの距離  <br/> |7   <br/> |
   

