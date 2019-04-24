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
description: ユーザーインターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326006"
---
# <a name="setatrefexpr-function"></a>SETATREFEXPR 関数

ユーザーインターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。
  
## <a name="syntax"></a>構文

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |省略可能  <br/> |**さまざま** <br/> |SETATREF 関数で参照先のセルに割り当てられる値または式によって置き換えられる式を指定します。 指定しない場合、初期値は 0 (ゼロ) になります。  <br/> |
   
## <a name="remarks"></a>解説

SETATREFEXPR 式の値は、SETATREFEXPR 式を含むセルを参照する別のセルの SETATREF 関数から設定することもできます。 
  
SETATREF 関数のパラメーターとして SETATREFEXPR 関数を使用することに制限はありません。 
  
## <a name="example-1"></a>例 1

次の例では、SETATREFEXPR 関数を使用して、図形の幅がそのテキストの幅と同じであることを確認します。
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>例 2

次の例では、SETATREFEXPR 関数を使用して、図形をカスタム グリッドにスナップする方法を示します。SETATREFEXPR 数式は  [PinX] および [PinY] セルに設定され、図形のピンは [User.GridX] および [User.GridY] で定義されたグリッドにスナップします。 
  
User.GridX =2 in
  
User.GridY =2 in
  
PinX = INT (SETATREFEXPR ()/User.GridX + .5)\*GridX
  
PinY = INT (SETATREFEXPR ()/User.GridY + .5)\*ユーザー. GridY
  
## <a name="example-3"></a>例 3

SETATREFEXPR 関数を SETATREF 関数と共に使用する例については、[SETATREF](setatref-function.md) 関数を参照してください。 
  

