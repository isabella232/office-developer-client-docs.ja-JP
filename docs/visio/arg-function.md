---
title: ARG 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: 呼び出し元のセルは、既定値がユーザー定義関数によって返されるかどうか呼び出し元のセルが渡されない値の引数と同様のカスタム関数に渡すことができる引数を指定します。 呼び出し元のセルと一致する argName パラメーターで指定された値を返します。
ms.openlocfilehash: 3d0e126e0fa075ff2a07773197c1973e6b0249d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804805"
---
# <a name="arg-function"></a>ARG 関数

呼び出し元のセルは、既定値がユーザー定義関数によって返されるかどうか呼び出し元のセルが渡されない値の引数と同様のカスタム関数に渡すことができる引数を指定します。 呼び出し元のセルと一致する argName パラメーターで指定された値を返します。
  
## <a name="syntax"></a>構文

ARG (* * *argName* * *、[* **既定値** *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |呼び出し元のセルが関数に渡すことができる引数の名前です。  <br/> |
| _既定値_ <br/> |省略可能  <br/> |**数値** <br/> |呼び出し元のセルは_argName_パラメーターの値で合格しなかった場合は、引数によって返される値です。  <br/> |
   
## <a name="remarks"></a>注釈

図形の開発者と同様に、1 つのセルに式を記述し、その式を 1 つまたは複数の別のセルから呼び出すことによって、ユーザー設定関数を作成できます。式には、リテラル文字列、シェイプシートの関数、およびセル参照を入れることができます。また、呼び出し元のセルによって渡される特定の引数を入れることも可能です。 
  
呼び出し元のセルは、関数に渡す必要があるすべての引数と同様に、カスタム関数を含むセルを指定します。 式のセルが評価され、呼び出し元のセルに結果が返されます。
  
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

