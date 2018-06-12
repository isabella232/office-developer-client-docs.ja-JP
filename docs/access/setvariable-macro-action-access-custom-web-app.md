---
title: SetVariable マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a4ffbd02-eed7-43ed-9da2-f0d1ff5d8014
description: SetVariable /変数の設定アクションを使用すると、一時変数を作成して特定の値に設定できます。作成した変数は、後続のアクションで条件や引数として使用したり、別のユーザー インターフェイス (UI) マクロで使用したりできます。
ms.openlocfilehash: 28daa4e8de247fbe4ca0d7a3fa8a908f6d7d885d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798733"
---
# <a name="setvariable-macro-action-access-custom-web-app"></a><span data-ttu-id="9443c-104">SetVariable マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="9443c-104">SetVariable Macro Action (Access custom web app)</span></span>

<span data-ttu-id="9443c-p102">" **SetVariable** /変数の設定" アクションを使用すると、一時変数を作成して特定の値に設定できます。作成した変数は、後続のアクションで条件や引数として使用したり、別のユーザー インターフェイス (UI) マクロで使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="9443c-p102">You can use the **SetVariable** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9443c-p103">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="9443c-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="9443c-109">設定</span><span class="sxs-lookup"><span data-stu-id="9443c-109">Setting</span></span>

<span data-ttu-id="9443c-110">**SetVariable** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9443c-110">The **SetVariable** action has the following arguments.</span></span> 
  
|<span data-ttu-id="9443c-111">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="9443c-111">**Action argument**</span></span>|<span data-ttu-id="9443c-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="9443c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9443c-113">**変数**</span><span class="sxs-lookup"><span data-stu-id="9443c-113">**Variable**</span></span> <br/> |<span data-ttu-id="9443c-114">一時変数の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9443c-114">Enter the name of the temporary variable.</span></span>  <br/> |
|<span data-ttu-id="9443c-115">**値 =**</span><span class="sxs-lookup"><span data-stu-id="9443c-115">**Value =**</span></span> <br/> |<span data-ttu-id="9443c-116">この一時変数の値を設定するために使用する式を入力します。</span><span class="sxs-lookup"><span data-stu-id="9443c-116">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="9443c-117">等号を含む式の前の操作を行います (**=** ) 記号。</span><span class="sxs-lookup"><span data-stu-id="9443c-117">Do not precede the expression with the equal (**=** ) sign.</span></span> <span data-ttu-id="9443c-118">この引数を設定するのには、式ビルダーを使用する![数式](media/buildbut_ZA06047218.gif "数式")の [**ビルド**] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="9443c-118">You can click the **Build** button ![Formula](media/buildbut_ZA06047218.gif "Formula") to use the Expression Builder to set this argument.</span></span>  <br/> |
   

