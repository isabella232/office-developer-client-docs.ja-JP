---
title: SEGMENTCOUNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: パスを形成する線分の数を返します。
ms.openlocfilehash: 0250c6c9a88f1de121a5cd8e930158203537c229
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553936"
---
# <a name="segmentcount-function"></a>SEGMENTCOUNT 関数

パスを形成する線分の数を返します。
  
## <a name="syntax"></a>構文

SEGMENTCOUNT(** *pathRef* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

飛び越し点は、返される線分の合計数には含まれません。
  

