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
description: ユーザー インターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439052"
---
# <a name="setatrefexpr-function"></a>SETATREFEXPR 関数

ユーザー インターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。
  
## <a name="syntax"></a>構文

SETATREFEXPR ([ **** expr_opt ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |省略可能  <br/> |**さまざま** <br/> |SETATREF 関数で参照先のセルに割り当てられる値または式によって置き換えられる式を指定します。 指定されていない場合、その初期値は 0 (ゼロ) です。  <br/> |
   
## <a name="remarks"></a>注釈

SETATREFEXPR 式の値は、SETATREFEXPR 式を含むセルを参照する別のセルの SETATREF 関数から設定することもできます。 
  
SETATREFEXPR 関数を SETATREF 関数のパラメーターとして使用する場合に限る必要はありません。 
  
## <a name="example-1"></a>例 1

次の例では、SETATREFEXPR 関数を使用して、図形の幅がそのテキストの幅と同じであることを確認します。
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>例 2

次の例では、SETATREFEXPR 関数を使用して、図形をカスタム グリッドにスナップする方法を示します。SETATREFEXPR 数式は  [PinX] および [PinY] セルに設定され、図形のピンは [User.GridX] および [User.GridY] で定義されたグリッドにスナップします。 
  
User.GridX =2 in
  
User.GridY =2 in
  
PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX
  
PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY
  
## <a name="example-3"></a>例 3

SETATREFEXPR 関数を SETATREF 関数と共に使用する例については、[SETATREF](setatref-function.md) 関数を参照してください。 
  

