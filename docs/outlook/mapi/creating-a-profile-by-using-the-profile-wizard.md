---
title: プロファイル ウィザードを使用したプロファイルの作成
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
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="67040-103">プロファイル ウィザードを使用したプロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="67040-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="67040-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67040-105">プロファイル ウィザードは、ユーザーが可能な限り簡単な方法でプロファイルを作成できる MAPI 機能です。</span><span class="sxs-lookup"><span data-stu-id="67040-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="67040-106">プロファイル ウィザードには、一連のダイアログ ボックスが表示され、メッセージ サービスを選択し、いくつかの最も重要な構成プロパティの値を入力するようユーザーに求めるプロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67040-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="67040-107">その他の必須プロパティのほとんどで、プロファイル ウィザードは指定された既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="67040-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="67040-108">プロファイル ウィザードを呼び出す場合は、LAUNCHWIZARDENTRY プロトタイプに基づく関数 **LaunchWizard**[を呼び出](launchwizardentry.md)します。</span><span class="sxs-lookup"><span data-stu-id="67040-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="67040-109">ユーザーは、プロファイル ウィザードをサポートする新しいプロファイルに、これらのメッセージ サービスとサービス プロバイダーのみを追加できます。</span><span class="sxs-lookup"><span data-stu-id="67040-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="67040-110">各メッセージ サービスでは、プロファイル ウィザードで処理できるプロパティよりも多くのプロパティを設定する必要がある場合があります。この方法を使用すると、選択したサービスまたはプロバイダーの 1 つ以上が不完全に構成される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67040-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

