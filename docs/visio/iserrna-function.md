---
title: ISERRNA 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
ms.localizationpriority: medium
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: cellreference の値がエラー型の場合は TRUE を#N/A! (使用できません)。それ以外の場合は、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: ad39cc4fb96600f90ff24673e591fbc409ae4d77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612597"
---
# <a name="iserrna-function"></a>ISERRNA 関数

cellreference の値が  _エラー型の場合_ は TRUE を#N/A! (使用できません)。それ以外の場合は、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERRNA(** *cellreference* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |
   
戻り値が有効であるため、FALSE を返します。
  
## <a name="example-2"></a>例 2

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |
   
戻り値がエラー タイプ #N/A! であるため、TRUE を返します。
  

