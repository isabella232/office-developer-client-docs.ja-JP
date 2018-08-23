---
title: SEGMENTCOUNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: パスを形成する線分の数を返します。
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806376"
---
# <a name="segmentcount-function"></a>SEGMENTCOUNT 関数

パスを形成する線分の数を返します。
  
## <a name="syntax"></a>構文

SEGMENTCOUNT (* * *pathRef* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |必須  <br/> |**Integer** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

飛び越し点は、返される線分の合計数には含まれません。
  

