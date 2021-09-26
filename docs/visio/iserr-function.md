---
title: ISERR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
ms.localizationpriority: medium
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: cellreference の値がエラーの種類である場合は TRUE を返します(#N/A を除く)。それ以外の場合は、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: bb724fdb753ada86baf6cb421a2fa758620317ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612611"
---
# <a name="iserr-function"></a>ISERR 関数

セル参照の値がエラーの  _種類である場合_ は TRUE を返します(#N/A を除く)。それ以外の場合は、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。
  
## <a name="example-2"></a>例 2

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。
  

