---
title: BOUNDINGBOXDIST 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: 図形の境界ボックスの、指定した部分の測定値を返します。
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804933"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST 関数

図形の境界ボックスの、指定した部分の測定値を返します。 
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

BOUNDINGBOXDIST (* **インデックス** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |必須  <br/> |**番号** <br/> |図形の一部に外接するボックスを測定し、返します。 使用可能な値については備考を参照してください。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **番号**
  
## <a name="remarks"></a>Remarks

 *インデックス*には、次の値のいずれかを指定できます。 
  
|**アイテム**|**値**|
|:-----|:-----|
|幅  <br/> |0  <br/> |
|高さ  <br/> |1  <br/> |
|左端から図形のピンまでの距離  <br/> |2  <br/> |
|図形のピンから右端までの距離  <br/> |3  <br/> |
|図形のピンから上端までの距離  <br/> |4  <br/> |
|下端から図形のピンまでの距離  <br/> |5  <br/> |
|境界ボックスの中心から PinX までの距離  <br/> |6  <br/> |
|境界ボックスの中心から PinY までの距離  <br/> |7  <br/> |
   

