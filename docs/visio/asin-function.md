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
description: そのサインが number である角度など、数値のアークサインを返します。
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804808"
---
# <a name="asin-function"></a>ASIN 関数

そのサインが*数値*である角度など、数値のアークサインを返します。 
  
## <a name="syntax"></a>構文

ASIN (* **番号** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |角度のサインを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

入力値が-1 の範囲である必要があります < =*数*< = 1、または、#NUM! エラーが返されます。 結果として得られる角度は -π/2 の範囲で、< =*角度*< = π/2 ラジアン (-90 < =*角度*< = 90 °)。 
  
## <a name="example"></a>例

ASIN(1)
  
90°を返します
  

