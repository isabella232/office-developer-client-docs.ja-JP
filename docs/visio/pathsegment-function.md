---
title: PATHSEGMENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: 指定したパスに沿って、指定したパーセントマークで 1 から基準のセグメント番号を返します。
ms.openlocfilehash: 8ad574a112202c2f02fce3731a470960413d3042
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554216"
---
# <a name="pathsegment-function"></a>PATHSEGMENT 関数

指定したパスに沿って、指定したパーセントマークで 1 から基準のセグメント番号を返します。
  
## <a name="syntax"></a>構文

PATHSEGMENT(** *section* **, ** *travel* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
   
### <a name="return-value"></a>戻り値

整数型 (Integer)
  

