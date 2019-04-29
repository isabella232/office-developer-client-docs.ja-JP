---
title: StopMacro マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: StopMacro/マクロの中止アクションを使用すると、現在実行中のマクロを中止できます。
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429496"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="2e14e-103">StopMacro マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="2e14e-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2e14e-104">" **StopMacro/マクロの中止** " アクションを使用すると、現在実行中のマクロを中止できます。</span><span class="sxs-lookup"><span data-stu-id="2e14e-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2e14e-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="2e14e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2e14e-107">設定</span><span class="sxs-lookup"><span data-stu-id="2e14e-107">Setting</span></span>

<span data-ttu-id="2e14e-108">**StopMacro** アクションには引数はありません。</span><span class="sxs-lookup"><span data-stu-id="2e14e-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2e14e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="2e14e-109">Remarks</span></span>

<span data-ttu-id="2e14e-p102">通常、このアクションは、条件に応じてマクロを中止する必要がある場合に使用します。たとえば、現在のビューに入力された日付に受けた注文の合計を表示するビューを開くユーザー インターフェイス (UI) マクロを作成するとします。条件式を使用して、ダイアログ ボックスの [注文日] コントロールに入力された日付が有効であるかどうかを確認できます。有効でない場合は、 **MessageBox** アクションでエラー メッセージを表示し、 **StopMacro** アクションでこの UI マクロを中止できます。</span><span class="sxs-lookup"><span data-stu-id="2e14e-p102">You typically use this action when a condition makes it necessary to stop the macro. For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view. You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date. If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

