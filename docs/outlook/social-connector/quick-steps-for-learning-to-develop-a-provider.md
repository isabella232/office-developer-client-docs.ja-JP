---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックでは、ソーシャル コネクタ (OSC) プロバイダーの開発についてOutlook手順を示します。
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424218"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="bdbad-103">プロバイダー開発方法を学習するためのクイック手順</span><span class="sxs-lookup"><span data-stu-id="bdbad-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="bdbad-104">OSC プロバイダーを開発するには、次の一般的な手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbad-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="bdbad-105">[ISocialProvider、ISocialSession、ISocialProfile、](isocialprovideriunknown.md)[および ISocialPerson](isocialprofileisocialperson.md)の 4 つの必須インターフェイスを[実装します](isocialpersoniunknown.md)。 [](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="bdbad-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="bdbad-106">ログオン資格情報のキャッシュ、ソーシャル ネットワーク上のユーザーの実行、友人とそのアクティビティの動的同期に関するソーシャル ネットワークのサポートに応じて [、ISocialSession2](isocialsession2iunknown.md) インターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="bdbad-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="bdbad-107">インターフェイスの実装と並行して、OSC プロバイダーをテストおよびデバッグします。</span><span class="sxs-lookup"><span data-stu-id="bdbad-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="bdbad-108">OSC プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="bdbad-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="bdbad-109">リリース前に最終テストを行います。</span><span class="sxs-lookup"><span data-stu-id="bdbad-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="bdbad-110">手順 A: インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="bdbad-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="bdbad-111">OSC プロバイダーは、OSC がこれらのインターフェイスを使用して、OSC プロバイダーを介してソーシャル ネットワークに関する必要な情報を取得したり、ソーシャル ネットワークから取得したりできるよう、インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="bdbad-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="bdbad-112">このような情報には、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bdbad-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="bdbad-113">ユーザーにアカウント ログオン ダイアログを表示する方法。</span><span class="sxs-lookup"><span data-stu-id="bdbad-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="bdbad-114">プロバイダーがソーシャル ネットワークに表示されるフレンドやアクティビティの表示をサポートするかどうか。</span><span class="sxs-lookup"><span data-stu-id="bdbad-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="bdbad-115">連絡先カードまたはユーザー ウィンドウにフレンドやアクティビティOutlook表示する方法。</span><span class="sxs-lookup"><span data-stu-id="bdbad-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="bdbad-116">連絡先カードまたはユーザー ウィンドウでフレンドやアクティビティの情報を更新する場合。</span><span class="sxs-lookup"><span data-stu-id="bdbad-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="bdbad-117">この情報は、通常、インターフェイス メソッドの出力パラメーターとして XML 文字列の形式でプロバイダーから OSC に渡されます。</span><span class="sxs-lookup"><span data-stu-id="bdbad-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="bdbad-118">OSC プロバイダーと OSC プロバイダーの両方が OSC プロバイダー XML スキーマに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="bdbad-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="bdbad-119">したがって、インターフェイスを実装する過程で、XML スキーマで上記のように情報を指定する方法を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbad-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="bdbad-120">次のリソースでは、プロバイダーの機能、友人、アクティビティに XML を指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bdbad-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="bdbad-121">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="bdbad-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="bdbad-122">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="bdbad-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="bdbad-123">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="bdbad-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="bdbad-124">機能の XML</span><span class="sxs-lookup"><span data-stu-id="bdbad-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="bdbad-125">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="bdbad-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="bdbad-126">友人のための XML</span><span class="sxs-lookup"><span data-stu-id="bdbad-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="bdbad-127">アクティビティ フィード XML の例</span><span class="sxs-lookup"><span data-stu-id="bdbad-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="bdbad-128">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="bdbad-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="bdbad-129">実装を開始する前に、デバッグ プロセスの後半で時間を節約するために、次のトピックも参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdbad-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="bdbad-130">技術的な要件</span><span class="sxs-lookup"><span data-stu-id="bdbad-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="bdbad-131">プロバイダーの開発に関するベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="bdbad-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="bdbad-132">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="bdbad-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="bdbad-133">手順 B: デバッグ</span><span class="sxs-lookup"><span data-stu-id="bdbad-133">Step B: Debugging</span></span>

<span data-ttu-id="bdbad-134">「 [プロバイダーのデバッグ」では、OSC](debugging-a-provider.md) プロバイダーの開発中に使用できるデバッグ手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="bdbad-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="bdbad-135">開発中は [、「OSC](getting-ready-to-release-an-osc-provider.md) プロバイダーをリリースする準備」を参照して、特定のシナリオ (基本認証やフォーム ベース認証など) で予期される動作をよりよく理解することもできます。</span><span class="sxs-lookup"><span data-stu-id="bdbad-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="bdbad-136">手順 C: 展開</span><span class="sxs-lookup"><span data-stu-id="bdbad-136">Step C: Deploying</span></span>

<span data-ttu-id="bdbad-137">展開要件の詳細については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdbad-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="bdbad-138">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="bdbad-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="bdbad-139">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="bdbad-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="bdbad-140">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="bdbad-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="bdbad-141">手順 D: リリース前の最終テスト</span><span class="sxs-lookup"><span data-stu-id="bdbad-141">Step D: Final testing before release</span></span>

<span data-ttu-id="bdbad-142">ソーシャル ネットワークと OSC プロバイダーに応じて、プロバイダーを解放する前に実行する必要があるプロバイダー固有のテストが通常行います。</span><span class="sxs-lookup"><span data-stu-id="bdbad-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="bdbad-143">テストの推奨リストについては [、「GETTING Ready to Release a OSC Provider 」を参照してください](getting-ready-to-release-an-osc-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="bdbad-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bdbad-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdbad-144">See also</span></span>

- [<span data-ttu-id="bdbad-145">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="bdbad-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

