---
title: ISERROR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: セル参照の値がエラーの種類の場合は TRUE を返します。それ以外の場合は、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421544"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR 関数 (VisioShapeSheet)

セル参照の値がエラーの種類  _の場合は_ TRUE を返します。それ以外の場合は、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERROR(** *cellreference* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.A1)  <br/> |TRUE  <br/> |
   
ISERROR 関数は #N/A! エラーを認識するため、TRUE を返します。#N/A! エラー以外のすべてのエラー タイプを検出する場合は、ISERR を使用できます。
  
## <a name="example-2"></a>例 2

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |
   
ISERROR 関数は #VALUE! エラーを認識するため、TRUE を返します。#VALUE! エラーを基に式を作成するには、ISERRVALUE 関数を使用します。
  

