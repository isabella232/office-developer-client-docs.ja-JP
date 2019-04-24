---
title: PATHSEGMENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: 指定したパーセント記号に沿った、指定されたパスにある1から始まるセグメント番号を返します。
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344451"
---
# <a name="pathsegment-function"></a>PATHSEGMENT 関数

指定したパーセント記号に沿った、指定されたパスにある1から始まるセグメント番号を返します。
  
## <a name="syntax"></a>構文

pathsegment (* **セクション** *、* **トラベル** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _travel_ <br/> |必須  <br/> |**Double** <br/> |スキャンするパスの始点から終点までの割合。 0 ～ 1 の値を指定する必要があります。  <br/> |
   
### <a name="return-value"></a>戻り値

整数型 (Integer)
  

