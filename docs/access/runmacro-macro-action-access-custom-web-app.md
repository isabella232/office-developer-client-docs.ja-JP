---
title: RunMacro マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: RunMacro /マクロの実行アクションを使用すると、ユーザー インターフェイス (UI) マクロを実行できます。
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798731"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="41175-103">RunMacro マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="41175-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="41175-104">" **RunMacro** /マクロの実行" アクションを使用すると、ユーザー インターフェイス (UI) マクロを実行できます。</span><span class="sxs-lookup"><span data-stu-id="41175-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="41175-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="41175-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="41175-107">設定</span><span class="sxs-lookup"><span data-stu-id="41175-107">Setting</span></span>

<span data-ttu-id="41175-108">**RunMacro** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="41175-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="41175-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="41175-109">**Action argument**</span></span>|<span data-ttu-id="41175-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="41175-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41175-111">**Macro Name/マクロ名**</span><span class="sxs-lookup"><span data-stu-id="41175-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="41175-112">実行する UI マクロの名前。</span><span class="sxs-lookup"><span data-stu-id="41175-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41175-113">注釈</span><span class="sxs-lookup"><span data-stu-id="41175-113">Remarks</span></span>

<span data-ttu-id="41175-p102">" **RunMacro** /マクロの実行" アクションを含む UI マクロを実行し、" **RunMacro** /マクロの実行" アクションに到達すると、呼び出された UI マクロが実行されます。呼び出された UI マクロの実行が終了すると、元の UI マクロに戻り、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="41175-p102">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro. When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

