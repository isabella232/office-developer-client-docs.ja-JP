---
title: RunDataMacro マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: RunDataMacro/データマクロの実行アクションを使用して、スタンドアロンデータ マクロを実行できます。
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304243"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="a8e62-103">RunDataMacro マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="a8e62-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a8e62-104">" **RunDataMacro/データマクロの実行** " アクションを使用して、スタンドアロンデータ マクロを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a8e62-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a8e62-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="a8e62-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a8e62-107">設定</span><span class="sxs-lookup"><span data-stu-id="a8e62-107">Setting</span></span>

<span data-ttu-id="a8e62-108">"RunDataMacro/データマクロの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a8e62-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="a8e62-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="a8e62-109">**Action argument**</span></span>|<span data-ttu-id="a8e62-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8e62-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a8e62-111">_Macro Name/マクロ名_</span><span class="sxs-lookup"><span data-stu-id="a8e62-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="a8e62-112">実行するデータ マクロの名前</span><span class="sxs-lookup"><span data-stu-id="a8e62-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8e62-113">解説</span><span class="sxs-lookup"><span data-stu-id="a8e62-113">Remarks</span></span>

<span data-ttu-id="a8e62-p102">マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8e62-p102">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters. If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="a8e62-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span><span class="sxs-lookup"><span data-stu-id="a8e62-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

