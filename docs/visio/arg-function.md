---
title: ARG 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: 呼び出し元のセルがカスタム関数に渡す引数と、呼び出し元のセルが引数の値を渡していない場合にカスタム関数によって返される既定値を指定します。 呼び出し元のセルと一致する argName パラメーターで指定された値を返します。
ms.openlocfilehash: df1e3106eb624064be48bed76201dae6fe40e3cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628858"
---
# <a name="arg-function"></a>ARG 関数

呼び出し元のセルがカスタム関数に渡す引数と、呼び出し元のセルが引数の値を渡していない場合にカスタム関数によって返される既定値を指定します。 呼び出し元のセルと一致する argName パラメーターで指定された値を返します。
  
## <a name="syntax"></a>構文

ARG(***argName** _,[ _ *_defaultValue_** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |必須  <br/> |**String** <br/> |呼び出し元のセルが関数に渡すことができる引数の名前です。  <br/> |
| _既定値_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |argName パラメーターの値を呼び出し元のセルが渡していない場合に  _ARG_ によって返される値。  <br/> |
   
## <a name="remarks"></a>注釈

図形の開発者と同様に、1 つのセルに式を記述し、その式を 1 つまたは複数の別のセルから呼び出すことによって、ユーザー設定関数を作成できます。式には、リテラル文字列、シェイプシートの関数、およびセル参照を入れることができます。また、呼び出し元のセルによって渡される特定の引数を入れることも可能です。 
  
呼び出し元のセルは、ユーザー設定関数を含むセル、およびそのセルが関数に渡す引数を指定します。 式のセルは評価され、結果が呼び出し元のセルに返されます。
  
## <a name="example"></a>例

次の例は、3 つの値の集合から中央値を検索するために、EVALCELL 関数と共に ARG 関数を使用する方法を示しています。 
  
式セルに、ユーザー設定関数を定義する次のコードを配置します。 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

呼び出しセルに、ユーザー設定関数を呼び出す次のコードを配置します。
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


