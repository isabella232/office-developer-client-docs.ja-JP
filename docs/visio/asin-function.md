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
description: 数値のアークサイン (たとえば、サインが数値の角度) を返します。
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293507"
---
# <a name="asin-function"></a>ASIN 関数

数値のアークサイン (たとえば、サインが数値の角度) を返  *します*  。 
  
## <a name="syntax"></a>構文

ASIN(***number*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |角度のサインを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

入力値は、-1 の範囲で指定する必要< *=*  <= 1、または #NUM! エラーを返します。 結果の角度は、-PI/2 <=  *角度*  <= PI/2 ラジアン (-90 < *=*  角度 <= 90 度) です。 
  
## <a name="example"></a>例

ASIN(1)
  
90°を返します
  

