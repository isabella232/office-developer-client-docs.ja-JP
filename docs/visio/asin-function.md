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
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293507"
---
# <a name="asin-function"></a>ASIN 関数

数値のアークサイン (正弦が  *数値*  である角度など) を返します。 
  
## <a name="syntax"></a>構文

アークサイン (***数値*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |角度のサインを指定します。  <br/> |
   
## <a name="remarks"></a>解説

入力値は、-1 <=  *数値*  <= 1、または #NUM である必要があります。 エラーを返します。 その結果、角度は-π/2 <=  *angle*  <= π/2 ラジアン (-90 <=  *角度*  <= 90 度) になります。 
  
## <a name="example"></a>例

アークサイン (1)
  
90°を返します
  

