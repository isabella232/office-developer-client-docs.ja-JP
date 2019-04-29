---
title: プロファイルウィザードを使用してプロファイルを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411737"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="570c0-103">プロファイルウィザードを使用してプロファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="570c0-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="570c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="570c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="570c0-105">プロファイルウィザードは、ユーザーが最も簡単な方法でプロファイルを作成できる MAPI の機能です。</span><span class="sxs-lookup"><span data-stu-id="570c0-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="570c0-106">プロファイルウィザードには一連のダイアログボックスが表示され、メッセージサービスを選択して、いくつかの最も重要な構成プロパティの値を入力するようにユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="570c0-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="570c0-107">その他の必要なプロパティのほとんどについて、プロファイルウィザードは提供されている既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="570c0-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="570c0-108">プロファイルウィザードを起動するには、 [launchwizardentry](launchwizardentry.md) prototype に基づく関数として、 **launchwizard**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="570c0-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="570c0-109">ユーザーは、プロファイルウィザードをサポートする新しいプロファイルに、これらのメッセージサービスとサービスプロバイダーのみを追加できます。</span><span class="sxs-lookup"><span data-stu-id="570c0-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="570c0-110">各メッセージサービスでは、プロファイルウィザードで処理できるよりも多くのプロパティを設定する必要がある場合があるため、この方法を使用する場合は、1つ以上の選択されたサービスまたはプロバイダーが不完全に構成される可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="570c0-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

