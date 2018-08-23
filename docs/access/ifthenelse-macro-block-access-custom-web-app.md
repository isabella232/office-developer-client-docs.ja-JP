---
title: もし。。。そうしたら。。。他のマクロ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: 式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798588"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>もし。。。そうしたら。。。他のマクロ ブロック (カスタム web アプリケーションのアクセス)

式の値に応じた条件に基づいてアクションのグループを実行するには、 **If** マクロ ブロックを使用します。 
  
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

両方**場合**のと * * それ以外の場合 * *、次の引数が必要です。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
|**Expression** <br/> |テストする条件です。True または False に評価される式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

**If** マクロ ブロックを選択するとテキスト ボックスが表示されるので、そこにテストする条件を表す式を入力します。さらに、マクロ アクションを挿入できるコンボ ボックスも表示されます。マクロ アクションの下に、"End If" というテキストが自動的に表示されます。If と End If は、アクションのグループ (ブロック) を入力できる領域を囲みます。ブロックは、入力した式が True の場合にのみ実行されます。 
  
1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。 
  
If ブロックには、任意の数の **Else If** ブロックを追加できます。 
  
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

**場合**のブロックを入れ子にすることができます。 最初の式が True の場合に、2 番目の式を評価する場合は、 **If**ブロック内の**If**ブロックを入れ子にする必要があります。 内側の**If**ブロックで次のコード例では、[ステータス] の値が 0*と*100 を超える値を超える場合をのみ実行します。 
  

