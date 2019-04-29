---
title: もし。。。そうしたら。。。Else マクロブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: 式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434495"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="29ac9-103">もし。。。そうしたら。。。Else マクロブロック (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="29ac9-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="29ac9-104">式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="29ac9-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="29ac9-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="29ac9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="29ac9-107">構文</span><span class="sxs-lookup"><span data-stu-id="29ac9-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="29ac9-108">Setting</span><span class="sxs-lookup"><span data-stu-id="29ac9-108">Setting</span></span>

<span data-ttu-id="29ac9-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span><span class="sxs-lookup"><span data-stu-id="29ac9-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="29ac9-110">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="29ac9-110">**Action argument**</span></span>|<span data-ttu-id="29ac9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="29ac9-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29ac9-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="29ac9-112">**Expression**</span></span> <br/> |<span data-ttu-id="29ac9-113">テストする条件です。</span><span class="sxs-lookup"><span data-stu-id="29ac9-113">The condition that you wish to test.</span></span> <span data-ttu-id="29ac9-114">真または偽のいずれかに評価できる式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="29ac9-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ac9-115">注釈</span><span class="sxs-lookup"><span data-stu-id="29ac9-115">Remarks</span></span>

<span data-ttu-id="29ac9-p103">
            \*\*If\*\* マクロブロックを選択すると、テキストボックスが表示され、テストする条件を示す式を入力することができます。さらにコンボ ボックスが表示され、マクロ アクションを入力できます。その下に、"End If" というテキストが自動的に表示されます。If と End If が囲む領域の中で、一連のアクション (ブロック) を指定します。入力した式が真である場合にのみ、そのブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="29ac9-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="29ac9-p104">1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="29ac9-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="29ac9-123">If ブロックには **Else If** ブロックをいくつでも追加できます。</span><span class="sxs-lookup"><span data-stu-id="29ac9-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="29ac9-p105">オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。</span><span class="sxs-lookup"><span data-stu-id="29ac9-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="29ac9-p106">次のコード例では、1 つ目のブロックのマクロ アクションは、[Status] の値が 0 より大きい場合に実行されます。[Status] の値が 0 より大きくない場合は、 **Else If** に続く式が評価されます。 **Else If** ブロックのマクロ アクションは、[Status] の値が 0 の場合に実行されます。最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="29ac9-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="29ac9-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span><span class="sxs-lookup"><span data-stu-id="29ac9-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

