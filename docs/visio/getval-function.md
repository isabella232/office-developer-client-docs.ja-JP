---
title: GETVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
ms.localizationpriority: medium
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: セルの値を取得し、セルの値が変更された場合、数式は再計算されません。
ms.openlocfilehash: fe5af032eae84612963913a23f94e65708e5ec8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582667"
---
# <a name="getval-function"></a>GETVAL 関数

セルの値を取得し、セルの値が変更された場合、数式は再計算されません。
  
## <a name="syntax"></a>構文

GETVAL(** *cellname* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |必須  <br/> |**String** <br/> |値を取得するセルの名前を指定します。  <br/> |
   
## <a name="example"></a>例

GETVAL(PinX) + GETVAL(PinY) + Width 
  
[PinX]、[PinY]、[Width] の各セルの値の合計を返します。 
  

