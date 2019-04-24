---
title: setlocalvar マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: SetLocalVar/ローカル変数の設定アクションは、一時変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310945"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="146dd-103">setlocalvar マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="146dd-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="146dd-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span><span class="sxs-lookup"><span data-stu-id="146dd-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="146dd-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="146dd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="146dd-107">"**SetLocalVar/ローカル変数の設定**" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="146dd-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="146dd-108">Setting</span><span class="sxs-lookup"><span data-stu-id="146dd-108">Setting</span></span>

<span data-ttu-id="146dd-109">"SetLocalVar/ローカル変数の設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="146dd-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="146dd-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="146dd-110">**Argument name**</span></span>|<span data-ttu-id="146dd-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="146dd-111">**Required**</span></span>|<span data-ttu-id="146dd-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="146dd-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="146dd-113">**名前**</span><span class="sxs-lookup"><span data-stu-id="146dd-113">**Name**</span></span> <br/> |<span data-ttu-id="146dd-114">はい</span><span class="sxs-lookup"><span data-stu-id="146dd-114">Yes</span></span>  <br/> |<span data-ttu-id="146dd-115">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="146dd-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="146dd-116">**Expression**</span><span class="sxs-lookup"><span data-stu-id="146dd-116">**Expression**</span></span> <br/> |<span data-ttu-id="146dd-117">はい</span><span class="sxs-lookup"><span data-stu-id="146dd-117">Yes</span></span>  <br/> |<span data-ttu-id="146dd-p102">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  </span><span class="sxs-lookup"><span data-stu-id="146dd-p102">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  </span></span><br/> |
   

