---
title: MSOTINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 指定した割合で明度を増やして色を変更します。
ms.openlocfilehash: 6d263872f10971d913938370f580e95fe5d743fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608222"
---
# <a name="msotint-function"></a>MSOTINT 関数

指定した割合で明度を増やして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

MSOTINT(** *color* **, ** *deltaLum* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _deltaLum_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |パーセンテージは、色の値から白 (-100%) または黒 (100%) に  _変_ わります。  <br/> |
   
## <a name="remarks"></a>注釈

色の値  _が_ 白または黒に近いほど、特定の deltaLum 値によって生成される色合いへの変更  _が小さ_ になります。 
  

