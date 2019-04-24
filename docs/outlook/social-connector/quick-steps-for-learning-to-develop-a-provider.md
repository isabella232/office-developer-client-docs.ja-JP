---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーの開発について学ぶためのいくつかの手順について説明します。
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="7a6c0-103">プロバイダー開発方法を学習するためのクイック手順</span><span class="sxs-lookup"><span data-stu-id="7a6c0-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="7a6c0-104">.osc プロバイダーを開発するには、次の一般的な手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="7a6c0-105">次の4つの必須インターフェイスを実装します。 [i、alprovider](isocialprovideriunknown.md)、 [i入力 alsession](isocialsessioniunknown.md)、 [i入力 alprofile](isocialprofileisocialperson.md)、および iな省略[alperson](isocialpersoniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="7a6c0-106">ソーシャルネットワークがログオン資格情報のキャッシュ、ソーシャルネットワーク上のユーザーのフォロー、またはフレンドとそのアクティビティの動的な同期をサポートしているかどうかに応じて、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="7a6c0-107">インターフェイスの実装と並行して、.osc プロバイダーをテストしてデバッグします。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="7a6c0-108">.osc プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="7a6c0-109">最終的なテストは、リリース前に行います。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="7a6c0-110">手順 A: インターフェイスを実装する</span><span class="sxs-lookup"><span data-stu-id="7a6c0-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="7a6c0-111">.osc プロバイダーはインターフェイスを実装するので、.osc はこれらのインターフェイスを使用して、.osc プロバイダーを経由して、ソーシャルネットワークに関する必要な情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="7a6c0-112">このような情報には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="7a6c0-113">[アカウントログオン] ダイアログボックスをユーザーに表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="7a6c0-114">ソーシャルネットワークに表示されているように、プロバイダーが友人または活動を表示するかどうか。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="7a6c0-115">連絡先カードまたは Outlook の [ユーザー] ウィンドウで友人や活動を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="7a6c0-116">連絡先カードまたはユーザーウィンドウのフレンドまたは活動情報を更新するタイミング。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="7a6c0-117">通常、この情報は、プロバイダーから .osc に渡され、インターフェイスメソッドの出力パラメーターとして XML 文字列の形式になります。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="7a6c0-118">.osc プロバイダーと .osc プロバイダーの両方が、.osc プロバイダ XML スキーマに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="7a6c0-119">そのため、インターフェイスを実装するときに、XML スキーマによって、上記のように情報を指定する方法を十分に理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="7a6c0-120">以下のリソースでは、プロバイダーの機能、フレンド、およびアクティビティの XML を指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="7a6c0-121">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="7a6c0-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="7a6c0-122">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="7a6c0-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="7a6c0-123">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="7a6c0-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="7a6c0-124">機能の XML</span><span class="sxs-lookup"><span data-stu-id="7a6c0-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="7a6c0-125">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="7a6c0-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="7a6c0-126">Friends の XML</span><span class="sxs-lookup"><span data-stu-id="7a6c0-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="7a6c0-127">アクティビティフィード XML の例</span><span class="sxs-lookup"><span data-stu-id="7a6c0-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="7a6c0-128">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="7a6c0-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="7a6c0-129">実装を開始する前に、次のトピックを参照して、後からデバッグプロセスで時間を節約してください。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="7a6c0-130">技術的な要件</span><span class="sxs-lookup"><span data-stu-id="7a6c0-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="7a6c0-131">プロバイダーを開発するためのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="7a6c0-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="7a6c0-132">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="7a6c0-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="7a6c0-133">手順 B: デバッグ</span><span class="sxs-lookup"><span data-stu-id="7a6c0-133">Step B: Debugging</span></span>

<span data-ttu-id="7a6c0-134">「[プロバイダーをデバッグ](debugging-a-provider.md)する」では、.osc プロバイダーの開発時に使用できるデバッグ手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="7a6c0-135">開発中に、特定のシナリオで想定される動作をより深く理解するために、 [.osc プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)をすることもできます (たとえば、基本認証とフォームベース認証)。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="7a6c0-136">手順 C: 展開</span><span class="sxs-lookup"><span data-stu-id="7a6c0-136">Step C: Deploying</span></span>

<span data-ttu-id="7a6c0-137">展開の要件については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="7a6c0-138">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="7a6c0-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="7a6c0-139">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="7a6c0-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="7a6c0-140">インストールチェックリスト</span><span class="sxs-lookup"><span data-stu-id="7a6c0-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="7a6c0-141">手順 D: リリース前の最終テスト</span><span class="sxs-lookup"><span data-stu-id="7a6c0-141">Step D: Final testing before release</span></span>

<span data-ttu-id="7a6c0-142">ソーシャルネットワークと .osc プロバイダーによっては、プロバイダーをリリースする前に実行する必要があるプロバイダー固有のテストが通常あります。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="7a6c0-143">推奨されるテストの一覧については、「 [.osc プロバイダーを解放する準備](getting-ready-to-release-an-osc-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a6c0-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a6c0-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a6c0-144">See also</span></span>

- [<span data-ttu-id="7a6c0-145">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="7a6c0-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

