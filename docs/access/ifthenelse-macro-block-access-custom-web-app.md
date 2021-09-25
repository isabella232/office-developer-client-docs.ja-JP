---
title: もし。。。そうしたら。。。Else マクロ ブロック (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: 式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。
ms.openlocfilehash: b7e86cd3db73d77cafcb128aee0f8c2a1a0fa991
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614816"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>もし。。。そうしたら。。。Else マクロ ブロック (Access カスタム Web アプリ)

式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a>設定

For both **If** and ** Else If **, the following arguments are required. 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
|**Expression** <br/> |テストする条件です。True または False に評価される式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈


            **If** マクロブロックを選択すると、テキストボックスが表示され、テストする条件を示す式を入力することができます。さらにコンボ ボックスが表示され、マクロ アクションを入力できます。その下に、"End If" というテキストが自動的に表示されます。If と End If が囲む領域の中で、一連のアクション (ブロック) を指定します。入力した式が真である場合にのみ、そのブロックが実行されます。 
  
1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。 
  
If ブロックには **Else If** ブロックをいくつでも追加できます。 
  
オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。 
  
次のコード例では、1 つ目のブロックのマクロ アクションは、[Status] の値が 0 より大きい場合に実行されます。[Status] の値が 0 より大きくない場合は、 **Else If** に続く式が評価されます。 **Else If** ブロックのマクロ アクションは、[Status] の値が 0 の場合に実行されます。最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100. 
  

