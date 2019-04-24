---
title: setreturnvar マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: SetReturnVar/戻り変数の設定アクションは、戻り変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310948"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="b303d-103">setreturnvar マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="b303d-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="b303d-104">" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="b303d-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b303d-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="b303d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b303d-107">"**SetReturnVar**/戻り変数の設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b303d-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b303d-108">Setting</span><span class="sxs-lookup"><span data-stu-id="b303d-108">Setting</span></span>

<span data-ttu-id="b303d-109">"**SetReturnVar**/戻り変数の設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b303d-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="b303d-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="b303d-110">**Argument name**</span></span>|<span data-ttu-id="b303d-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="b303d-111">**Required**</span></span>|<span data-ttu-id="b303d-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="b303d-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b303d-113">_名前_</span><span class="sxs-lookup"><span data-stu-id="b303d-113">_Name_</span></span> <br/> |<span data-ttu-id="b303d-114">はい</span><span class="sxs-lookup"><span data-stu-id="b303d-114">Yes</span></span>  <br/> |<span data-ttu-id="b303d-115">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="b303d-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="b303d-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="b303d-116">_Expression_</span></span> <br/> |<span data-ttu-id="b303d-117">はい</span><span class="sxs-lookup"><span data-stu-id="b303d-117">Yes</span></span>  <br/> |<span data-ttu-id="b303d-p102">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  </span><span class="sxs-lookup"><span data-stu-id="b303d-p102">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="b303d-121">解説</span><span class="sxs-lookup"><span data-stu-id="b303d-121">Remarks</span></span>

<span data-ttu-id="b303d-122">"**SetReturnVar**/戻り変数の設定" アクションを使用して、変数の **ReturnVar** を作成できます。この変数を、"**RunDataMacro**/データマクロの実行" アクションを使用してデータ マクロを呼び出すマクロで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b303d-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="b303d-123">**returnvar**は、 **setreturnvar**アクションによって作成された後、呼び出し元のマクロが式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b303d-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="b303d-124">たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b303d-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="b303d-p104">" **SetReturnVar** /戻り変数の設定" アクションは、名前付きのデータ マクロでのみ使用できます。これを、データ マクロ イベントに接続されたデータ マクロで使用できません。</span><span class="sxs-lookup"><span data-stu-id="b303d-p104">The **SetReturnVar** action can be used only in named data macros. It is not available in data macros that are attached to a data macro event.</span></span> 
  

