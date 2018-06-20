---
title: SETATREFEXPR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: ユーザー インターフェイス (UI) またはオートメーションでのアクションによって設定される値を格納します。
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806388"
---
# <a name="setatrefexpr-function"></a>SETATREFEXPR 関数

ユーザー インターフェイス (UI) またはオートメーションでのアクションによって設定される値を格納します。
  
## <a name="syntax"></a>構文

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |省略可能  <br/> |**によって異なります** <br/> |値または SETATREF 関数で参照されているセルに代入される式によって置き換えられる式です。 指定されていない場合、初期値は 0 (ゼロ) にします。  <br/> |
   
## <a name="remarks"></a>注釈

SETATREFEXPR 式の値は、SETATREFEXPR 式を含むセルを参照する別のセルの SETATREF 関数から設定することもできます。 
  
SETATREFEXPR 関数を SETATREF 関数にパラメーターとして使用するのには制限されません。 
  
## <a name="example-1"></a>例 1

次の例では、SETATREFEXPR 関数を使用して、図形の幅がそのテキストの幅と同じであることを確認します。
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>例 2

次の例では、SETATREFEXPR 関数を使用して、図形をカスタム グリッドにスナップする方法を示します。SETATREFEXPR 数式は  [PinX] および [PinY] セルに設定され、図形のピンは [User.GridX] および [User.GridY] で定義されたグリッドにスナップします。 
  
User.GridX =2 in
  
User.GridY =2 in
  
[Pinx] = INT (SETATREFEXPR ()/User.GridX +.5)\*User.GridX
  
[Piny] = INT (SETATREFEXPR ()/User.GridY +.5)\*User.GridY
  
## <a name="example-3"></a>例 3

SETATREFEXPR 関数を SETATREF 関数の使用例は、 [SETATREF](setatref-function.md)関数を参照してください。 
  

