---
title: RunDataMacro マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: RunDataMacro/データマクロの実行アクションを使用して、スタンドアロンデータ マクロを実行できます。
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798726"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="cbcbd-103">RunDataMacro マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="cbcbd-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="cbcbd-104">" **RunDataMacro/データマクロの実行** " アクションを使用して、スタンドアロンデータ マクロを実行できます。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cbcbd-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="cbcbd-107">設定</span><span class="sxs-lookup"><span data-stu-id="cbcbd-107">Setting</span></span>

<span data-ttu-id="cbcbd-108">" **RunDataMacro/データマクロの実行** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="cbcbd-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="cbcbd-109">**Action argument**</span></span>|<span data-ttu-id="cbcbd-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="cbcbd-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cbcbd-111">_Macro Name/マクロ名_</span><span class="sxs-lookup"><span data-stu-id="cbcbd-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="cbcbd-112">実行するデータ マクロの名前</span><span class="sxs-lookup"><span data-stu-id="cbcbd-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbcbd-113">解説</span><span class="sxs-lookup"><span data-stu-id="cbcbd-113">Remarks</span></span>

<span data-ttu-id="cbcbd-p102">マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-p102">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters. If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="cbcbd-116">**RunDataMacro**アクションを含むマクロを実行するし、 **RunDataMacro**アクションに到達して、data という名前のマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="cbcbd-117">Data という名前のマクロが完了したら、アクセスが元に戻りし、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="cbcbd-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

