---
title: GETVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: セルの値を取得し、セルの値が変更されたとき、数式を再計算しません。
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805472"
---
# <a name="getval-function"></a>GETVAL 関数

セルの値を取得し、セルの値が変更されたとき、数式を再計算しません。
  
## <a name="syntax"></a>構文

GETVAL (* * *cellname* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |値を取得するセルの名前を指定します。  <br/> |
   
## <a name="example"></a>例

GETVAL(PinX) + GETVAL(PinY) + Width 
  
[PinX]、[PinY]、[Width] の各セルの値の合計を返します。 
  

