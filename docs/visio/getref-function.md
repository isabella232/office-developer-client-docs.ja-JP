---
title: GETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
ms.localizationpriority: medium
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: セルを参照し、参照先のセルが変更しても数式は再計算されません。
ms.openlocfilehash: b2331b18ed78583e745472b02736bd21fb45a104
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628291"
---
# <a name="getref-function"></a>GETREF 関数

セルを参照し、参照先のセルが変更しても数式は再計算されません。
  
## <a name="syntax"></a>構文

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |必須  <br/> |**String** <br/> |参照を取得するセルの名前。  <br/> |
   
## <a name="example"></a>例

SETF(GETREF(PinX),5.1) 
  
[PinX] セルの数式を 5.1 に設定します。 
  

