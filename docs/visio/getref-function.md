---
title: GETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: セルを参照し、参照先のセルが変更されたとき、数式を再計算しません。
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805470"
---
# <a name="getref-function"></a>GETREF 関数

セルを参照し、参照先のセルが変更されたとき、数式を再計算しません。
  
## <a name="syntax"></a>構文

GETREF (* * *cellname* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |参照を取得するセルの名前です。  <br/> |
   
## <a name="example"></a>例

SETF(GETREF(PinX),5.1) 
  
[PinX] セルの数式を 5.1 に設定します。 
  

