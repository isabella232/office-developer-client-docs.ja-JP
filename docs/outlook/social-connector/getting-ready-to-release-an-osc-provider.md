---
title: OSC プロバイダーをリリースする準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、ソーシャル コネクタ (OSC) プロバイダーをリリースする前Outlookテストについて説明します。
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414663"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="87c68-103">OSC プロバイダーをリリースする準備</span><span class="sxs-lookup"><span data-stu-id="87c68-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="87c68-104">このセクションでは、ソーシャル コネクタ (OSC) プロバイダーをリリースする前Outlookテストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="87c68-105">このセクションのトピックの参照を開始し、開発およびテストの段階でこれらのテストの一部を実行できますが、リリース時にはこれらのテストを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="87c68-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="87c68-106">これらのテストでは、OSC プロバイダーに指定する機能に関して、OSC プロバイダー インターフェイスの実装の基本的な機能を確認します。</span><span class="sxs-lookup"><span data-stu-id="87c68-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="87c68-107">また、OSC は複数の Office クライアント アプリケーションで共有される機能ですが、これらのテストでは、Outlook をクライアントとして使用して、基本的な機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="87c68-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="87c68-108">プロバイダー固有の機能に他のテストが必要かどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87c68-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="87c68-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="87c68-109">In this section</span></span>

- <span data-ttu-id="87c68-110">[展開の](testing-deployment.md)テスト: OSC プロバイダーのインストールとアンインストールについてテストする必要があるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="87c68-111">[機能、認証、](testing-capabilities-authentication-and-configuration.md)および構成のテスト: 機能を取得するためのテストと、アカウントの構成とソーシャル ネットワークのユーザー認証に関するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="87c68-112">[[次のユーザーStop-Followingテスト](testing-following-and-stop-following-persons.md)]: OSC プロバイダーがユーザーを友人として追加したり、ソーシャル ネットワークから友人を削除したりする機能をテストするシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="87c68-113">[友人の](testing-friends.md)テスト: OSC プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合はフレンドとフレンド以外のデータが適切に返されるのを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="87c68-114">[テストアクティビティ](testing-activities.md): OSC プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のアクティビティが適切に返されるのを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87c68-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="87c68-115">参照</span><span class="sxs-lookup"><span data-stu-id="87c68-115">Reference</span></span>

- [<span data-ttu-id="87c68-116">Outlookソーシャル コネクタ プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="87c68-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="87c68-117">関連情報</span><span class="sxs-lookup"><span data-stu-id="87c68-117">Related sections</span></span>

- [<span data-ttu-id="87c68-118">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="87c68-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="87c68-119">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="87c68-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="87c68-120">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="87c68-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="87c68-121">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="87c68-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="87c68-122">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="87c68-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

