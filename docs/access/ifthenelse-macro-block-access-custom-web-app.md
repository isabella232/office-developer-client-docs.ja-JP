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
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="fae85-103">もし。。。そうしたら。。。他のマクロ ブロック (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="fae85-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="fae85-104">式の値に応じた条件に基づいてアクションのグループを実行するには、 **If** マクロ ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="fae85-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="fae85-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="fae85-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fae85-107">構文</span><span class="sxs-lookup"><span data-stu-id="fae85-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="fae85-108">設定</span><span class="sxs-lookup"><span data-stu-id="fae85-108">Setting</span></span>

<span data-ttu-id="fae85-109">両方**場合**のと * * それ以外の場合 * *、次の引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="fae85-109">For both **If** and ** Else If **, the following arguments are required.</span></span> 
  
|<span data-ttu-id="fae85-110">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="fae85-110">**Action argument**</span></span>|<span data-ttu-id="fae85-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fae85-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fae85-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="fae85-112">**Expression**</span></span> <br/> |<span data-ttu-id="fae85-p102">テストする条件です。True または False に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="fae85-p102">The condition that you wish to test. It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fae85-115">注釈</span><span class="sxs-lookup"><span data-stu-id="fae85-115">Remarks</span></span>

<span data-ttu-id="fae85-p103">**If** マクロ ブロックを選択するとテキスト ボックスが表示されるので、そこにテストする条件を表す式を入力します。さらに、マクロ アクションを挿入できるコンボ ボックスも表示されます。マクロ アクションの下に、"End If" というテキストが自動的に表示されます。If と End If は、アクションのグループ (ブロック) を入力できる領域を囲みます。ブロックは、入力した式が True の場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="fae85-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="fae85-p104">1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="fae85-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="fae85-123">If ブロックには、任意の数の **Else If** ブロックを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fae85-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="fae85-p105">オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fae85-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="fae85-p106">次のコード例では、1 つ目のブロックのマクロ アクションは、[Status] の値が 0 より大きい場合に実行されます。[Status] の値が 0 より大きくない場合は、 **Else If** に続く式が評価されます。 **Else If** ブロックのマクロ アクションは、[Status] の値が 0 の場合に実行されます。最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="fae85-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="fae85-131">**場合**のブロックを入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fae85-131">You can nest **If** blocks.</span></span> <span data-ttu-id="fae85-132">最初の式が True の場合に、2 番目の式を評価する場合は、 **If**ブロック内の**If**ブロックを入れ子にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fae85-132">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="fae85-133">内側の**If**ブロックで次のコード例では、[ステータス] の値が 0*と*100 を超える値を超える場合をのみ実行します。</span><span class="sxs-lookup"><span data-stu-id="fae85-133">In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

