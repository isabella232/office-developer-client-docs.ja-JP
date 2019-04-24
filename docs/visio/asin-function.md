---
title: ASIN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: 数値のアークサイン (正弦が数値である角度など) を返します。
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341525"
---
# <a name="asin-function"></a>ASIN 関数

数値のアークサイン (正弦が*数値*である角度など) を返します。 
  
## <a name="syntax"></a>構文

アークサイン (* **数値** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |角度のサインを指定します。  <br/> |
   
## <a name="remarks"></a>解説

入力値は、-1 < = *number* < = 1、または #NUM の範囲内である必要があります。 エラーを返します。 結果の角度は、-pi/2 < = *angle* < = π/2 ラジアン (-90 < = *angle* < = 90 °) の範囲になります。 
  
## <a name="example"></a>例

アークサイン (1)
  
90°を返します
  

