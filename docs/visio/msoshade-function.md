---
title: MSOSHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: 指定された割合で明度を減らして色を変更します。
ms.openlocfilehash: 76ba30f977b9a08916ba158f474f57dbf2d9a7a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563043"
---
# <a name="msoshade-function"></a>MSOSHADE 関数

指定された割合で明度を減らして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

MSOSHADE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _-deltaLum_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |パーセンテージは、色の値から白 (-100%) または黒 (100%) に  _変_ わります。  <br/> |
   
## <a name="remarks"></a>注釈

色の値  _が_ 白または黒に近いほど、特定の -deltaLum 値によって生成される網掛け  _への変更が小さ_ になります。 
  

