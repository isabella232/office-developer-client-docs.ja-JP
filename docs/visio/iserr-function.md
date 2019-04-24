---
title: ISERR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'cellreference の値が #N/a 以外のエラーの種類の場合は TRUE を返します。それ以外の場合は、FALSE を返します。 iserr 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297250"
---
# <a name="iserr-function"></a>ISERR 関数

_cellreference_の値が #N/a 以外のエラーの種類の場合は TRUE を返します。それ以外の場合は、FALSE を返します。 iserr 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

iserr (* * *cellreference* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|最初の B1  <br/> |= iserr (A1)  <br/> |FALSE  <br/> |
   
ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の X1  <br/> |= "House"  <br/> |#VALUE!  <br/> |
|最初の A1  <br/> |= iserr (最初の X1)  <br/> |TRUE  <br/> |
   
ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。
  

