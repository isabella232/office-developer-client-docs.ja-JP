---
title: ISERRNA 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Cellreference の値が #n/a エラーの種類である場合は、TRUE を返します。 (利用できない)。それ以外の場合、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805618"
---
# <a name="iserrna-function"></a>ISERRNA 関数

_Cellreference_の値が #n/a エラーの種類である場合は、TRUE を返します。 (利用できない)。それ以外の場合、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERRNA (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |「8」  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |
   
戻り値が有効であるため、FALSE を返します。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |
   
戻り値がエラー タイプ #N/A! であるため、TRUE を返します。
  

