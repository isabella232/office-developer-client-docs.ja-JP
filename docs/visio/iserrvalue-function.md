---
title: ISERRVALUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
ms.localizationpriority: medium
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: セル参照の値がエラー型の場合は true を#VALUE式の引数が間違った型です。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。
ms.openlocfilehash: 0186b0b51e89fad3106bb1df034615ce9e512060
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574098"
---
# <a name="iserrvalue-function"></a>ISERRVALUE 関数

セル参照の値がエラー型の場合は true を#VALUE式の引数が間違った型です。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。 
  
## <a name="syntax"></a>構文

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**String** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。 
  
## <a name="example-1"></a>例 1

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= "House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。
  
## <a name="example-2"></a>例 2

|**Cell**|**式**|**戻り値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 +7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。
  

