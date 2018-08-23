---
title: EVALCELL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: (オプション) 引数としてユーザー定義関数に渡す 1 つ以上の名前/値ペアと同様に、カスタム関数を含むセルへの参照を受け取ります。 指定した引数と値を指定するユーザー定義関数の計算結果を返します。
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805319"
---
# <a name="evalcell-function"></a>EVALCELL 関数

(オプション) 引数としてユーザー定義関数に渡す 1 つ以上の名前/値ペアと同様に、カスタム関数を含むセルへの参照を受け取ります。 指定した引数と値を指定するユーザー定義関数の計算結果を返します。
  
## <a name="syntax"></a>構文

EVALCELL (* * *cellRef* * *、[* * *arg1Name、arg1* * *]、[* * *arg2Name、arg2* * *],...) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |カスタム関数を含むセルへの参照。 シート間の参照は許可されています。  <br/> |
| _arg1Name_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |ユーザー設定関数に渡す 1 番目の引数の名前です。スペースを使用できます。  <br/> |
| _arg1_ <br/> |省略可能  <br/> |**多様** <br/> |_Arg1_パラメーターの値です。  <br/> |
| _arg2Name_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |ユーザー定義関数に渡される 2 番目の引数の名前。 スペースを使用します。  <br/> |
| _arg2_ <br/> |省略可能  <br/> |**多様** <br/> |_Arg2_パラメーターの値です。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

呼び出し元のセルは、ユーザー設定関数が使用する引数をすべて指定する必要はありません。 
  
## <a name="example"></a>例

次の例は、3 つの値の集合から中央値を検索するために、ARG 関数と共に EVALCELL 関数を使用する方法を示しています。 
  
式セルに、ユーザー設定関数を定義する次のコードを配置します。 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

呼び出しセルに、ユーザー設定関数を呼び出す次のコードを配置します。
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


