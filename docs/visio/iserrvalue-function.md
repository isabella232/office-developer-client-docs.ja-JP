---
title: ISERRVALUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: Cellreference の値がエラーの場合は TRUE を返しますが、数式内の引数が間違った型である、#VALUE を入力します。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805623"
---
# <a name="iserrvalue-function"></a>ISERRVALUE 関数

_Cellreference_の値がエラーの場合は TRUE を返しますが、数式内の引数が間違った型である、#VALUE を入力します。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。 
  
## <a name="syntax"></a>構文

ISERRVALUE (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。 
  
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= "House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 +7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。
  

