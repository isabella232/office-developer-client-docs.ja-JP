---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックは、Outlook ソーシャル コネクタ (OSC) プロバイダーの開発について学習するのにはいくつかの手順をお勧めします。
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804458"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="2e98b-103">プロバイダー開発方法を学習するためのクイック手順</span><span class="sxs-lookup"><span data-stu-id="2e98b-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="2e98b-104">OSC プロバイダーを開発するには、次の一般的な手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e98b-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="2e98b-105">4 つの必須のインターフェイスを実装する: [ISocialProvider](isocialprovideriunknown.md)、 [ISocialSession](isocialsessioniunknown.md)、 [ISocialProfile](isocialprofileisocialperson.md)、および[ISocialPerson](isocialpersoniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="2e98b-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="2e98b-106">ソーシャル ネットワーク、または動的に同期の友人との活動では、[次のユーザーのログオン資格情報をキャッシュするためのソーシャル ネットワークのサポートによって[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2e98b-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="2e98b-107">インターフェイスを実装すると、並列でテストし、OSC プロバイダーをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="2e98b-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="2e98b-108">OSC プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="2e98b-109">リリース前に、の最終テストを行います。</span><span class="sxs-lookup"><span data-stu-id="2e98b-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="2e98b-110">手順 a: 実装インターフェイスします。</span><span class="sxs-lookup"><span data-stu-id="2e98b-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="2e98b-111">OSC プロバイダーはインターフェイスを実装する、OSC や OSC プロバイダーを通じて、ソーシャル ネットワークから、必要な情報を入手するのにはこれらのインタ フェースを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2e98b-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="2e98b-112">このような情報には次のものが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e98b-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="2e98b-113">アカウントの [ログオン] ダイアログ ボックスをユーザーに提示する方法です。</span><span class="sxs-lookup"><span data-stu-id="2e98b-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="2e98b-114">かどうか、プロバイダーをサポートしている表示されている友人や活動ソーシャル ネットワークに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e98b-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="2e98b-115">友人や活動を連絡先カードまたは Outlook 人物情報ウィンドウに表示する方法です。</span><span class="sxs-lookup"><span data-stu-id="2e98b-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="2e98b-116">連絡先カードまたは人物情報ウィンドウの友人や活動の情報を更新する場合。</span><span class="sxs-lookup"><span data-stu-id="2e98b-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="2e98b-117">情報は、インターフェイス メソッドの出力パラメーターとしての XML 文字列の形式で、OSC を通常、プロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="2e98b-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="2e98b-118">OSC と OSC プロバイダーの両方は、OSC プロバイダーの XML スキーマに準拠します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="2e98b-119">したがって、インターフェイスを実装する過程で XML スキーマを使用するも上記の情報を指定する方法を十分に理解が必要。</span><span class="sxs-lookup"><span data-stu-id="2e98b-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="2e98b-120">次のリソースには、プロバイダーの機能、友人、および活動の XML を指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="2e98b-121">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="2e98b-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="2e98b-122">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="2e98b-123">機能の XML の例</span><span class="sxs-lookup"><span data-stu-id="2e98b-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="2e98b-124">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="2e98b-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="2e98b-125">友人の XML の例</span><span class="sxs-lookup"><span data-stu-id="2e98b-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="2e98b-126">友人の XML</span><span class="sxs-lookup"><span data-stu-id="2e98b-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="2e98b-127">アクティビティ フィードの XML の例</span><span class="sxs-lookup"><span data-stu-id="2e98b-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="2e98b-128">活動の XML</span><span class="sxs-lookup"><span data-stu-id="2e98b-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="2e98b-129">実装を開始する前にも後のデバッグ プロセスで時間を節約するには、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e98b-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="2e98b-130">技術的な要件</span><span class="sxs-lookup"><span data-stu-id="2e98b-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="2e98b-131">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="2e98b-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="2e98b-132">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="2e98b-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="2e98b-133">手順 b: デバッグ</span><span class="sxs-lookup"><span data-stu-id="2e98b-133">Step B: Debugging</span></span>

<span data-ttu-id="2e98b-134">トピックは[、プロバイダーのデバッグ](debugging-a-provider.md)OSC プロバイダーを開発する際に使用することができますプロシージャのデバッグをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2e98b-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="2e98b-135">開発しているときに、[準備 OSC プロバイダーを解放する](getting-ready-to-release-an-osc-provider.md)(たとえば、基本的なとフォーム ベース認証) は、特定のシナリオで予想される動作の理解を参照することも。</span><span class="sxs-lookup"><span data-stu-id="2e98b-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="2e98b-136">手順 c: を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-136">Step C: Deploying</span></span>

<span data-ttu-id="2e98b-137">展開の要件の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e98b-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="2e98b-138">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="2e98b-139">プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="2e98b-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="2e98b-140">インストールのチェックリスト</span><span class="sxs-lookup"><span data-stu-id="2e98b-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="2e98b-141">手順 d: の最終リリース前にテスト</span><span class="sxs-lookup"><span data-stu-id="2e98b-141">Step D: Final testing before release</span></span>

<span data-ttu-id="2e98b-142">ソーシャル ネットワーク、OSC プロバイダーによっては、プロバイダーをリリースする前に実行する必要があります通常は、プロバイダー固有のテストがあります。</span><span class="sxs-lookup"><span data-stu-id="2e98b-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="2e98b-143">テストの候補の一覧[を取得する準備ができて OSC プロバイダーを解放する](getting-ready-to-release-an-osc-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e98b-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e98b-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e98b-144">See also</span></span>

- [<span data-ttu-id="2e98b-145">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="2e98b-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

