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
description: 'cellreference の値がエラーの種類である場合は TRUE を返します #N/a! (使用できません)、それ以外の場合は、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357261"
---
# <a name="iserrna-function"></a>ISERRNA 関数

_cellreference_の値がエラーの種類である場合は TRUE を返します #N/a! (使用できません)、それ以外の場合は、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERRNA (* * *cellreference* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の A1  <br/> |="5 + 3"  <br/> |~  <br/> |
|最初の B1  <br/> |= ISERRNA (A1)  <br/> |FALSE  <br/> |
   
戻り値が有効であるため、FALSE を返します。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|最初の B1  <br/> |= ISERRNA (A1)  <br/> |TRUE  <br/> |
   
戻り値がエラー タイプ #N/A! であるため、TRUE を返します。
  

