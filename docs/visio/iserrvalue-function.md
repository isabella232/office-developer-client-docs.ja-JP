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
description: 'cellreference の値が error type #VALUE の場合は TRUE を返します。数式の引数の型が正しくありません。 iserrvalue 関数は、別のセルを参照する論理式で使用します。'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404429"
---
# <a name="iserrvalue-function"></a>ISERRVALUE 関数

_cellreference_の値が error type #VALUE の場合は TRUE を返します。数式の引数の型が正しくありません。 iserrvalue 関数は、別のセルを参照する論理式で使用します。 
  
## <a name="syntax"></a>構文

iserrvalue (* * *cellreference* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。 
  
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の X1  <br/> |= "House"  <br/> |#VALUE!  <br/> |
|最初の A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2   <br/> |
   
戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**戻り値**|
|:-----|:-----|:-----|
|最初の A1  <br/> |="5 +7"  <br/> |5 + 7  <br/> |
|最初の B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。
  

