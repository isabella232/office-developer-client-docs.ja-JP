---
title: BOUNDINGBOXDIST 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: 図形の境界ボックスの、指定した部分の測定値を返します。
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428278"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST 関数

図形の境界ボックスの、指定した部分の測定値を返します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

BOUNDINGBOXDIST (* * *Index* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |必須  <br/> |**数値** <br/> |図形の境界ボックスの、測定して返す部分。 使用可能な値については備考を参照してください。  <br/> |
   
### <a name="return-value"></a>戻り値

 **数値**
  
## <a name="remarks"></a>注釈

 *Index*には、次のいずれかの値を指定できます。 
  
|**Item**|**値**|
|:-----|:-----|
|Width  <br/> |.0  <br/> |
|Height  <br/> |1   <br/> |
|左端から図形のピンまでの距離  <br/> |2   <br/> |
|図形のピンから右端までの距離  <br/> |3   <br/> |
|図形のピンから上端までの距離  <br/> |4   <br/> |
|下端から図形のピンまでの距離  <br/> |5   <br/> |
|境界ボックスの中心から PinX までの距離  <br/> |6   <br/> |
|境界ボックスの中心から PinY までの距離  <br/> |7   <br/> |
   

