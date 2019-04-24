---
title: MSOTINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 指定した割合で明度を増やして色を変更します。
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335197"
---
# <a name="msotint-function"></a>MSOTINT 関数

指定した割合で明度を増やして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

msotint (* * *color* * *, * * *deltaLum* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _deltaLum_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |パーセンテージを白に変更します (-100%)または黒 (100%)_色_の値から。  <br/> |
   
## <a name="remarks"></a>解説

_色_の値が白または黒に近いほど、特定の_deltaLum_値によって生成される濃淡に対する変更が小さくなります。 
  

