---
title: .osc プロバイダーをリリースする準備をする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、Outlook Social Connector (.osc) プロバイダーを解放する前に実行できるテストを示します。
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327154"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="ac1c7-103">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="ac1c7-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="ac1c7-104">このセクションでは、Outlook Social Connector (.osc) プロバイダーを解放する前に実行できるテストを示します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="ac1c7-105">このセクションのトピックを参照して、開発フェーズとテストフェーズでこれらのテストの一部を実行することができますが、リリースするまでにこれらのテストを完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="ac1c7-106">これらのテストは、.osc プロバイダインターフェイスの実装の基本的な機能を、.osc プロバイダーに対して指定した機能に関して確認します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="ac1c7-107">また、.osc は複数の Office クライアントアプリケーションによって共有されている機能ですが、これらのテストでは、クライアントとして Outlook を使用して基本的な機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="ac1c7-108">プロバイダー固有の機能に他のテストが必要かどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ac1c7-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="ac1c7-109">In this section</span></span>

- <span data-ttu-id="ac1c7-110">[展開のテスト](testing-deployment.md): .osc プロバイダーのインストールとアンインストールに関してテストする必要があるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="ac1c7-111">[機能、認証、および構成をテスト](testing-capabilities-authentication-and-configuration.md)する: 機能を取得するためのテスト、およびソーシャルネットワークのアカウントの構成とユーザーの認証に関するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="ac1c7-112">[フォローおよび停止し](testing-following-and-stop-following-persons.md)ているユーザーのテスト: ユーザーをフレンドとして追加したり、ソーシャルネットワークから友人を削除したりするための、.osc プロバイダーの機能をテストするシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="ac1c7-113">[友人をテスト](testing-friends.md)する: プロバイダーがサポートする同期モードに応じて、.osc プロバイダーがフレンドおよび非友人のデータを適切に返すことを確認するためのテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="ac1c7-114">[アクティビティのテスト](testing-activities.md): プロバイダーがサポートする同期モードに応じて、.osc プロバイダーがフレンドおよび非友人のアクティビティを適切に返すことを確認するためのテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ac1c7-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ac1c7-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="ac1c7-115">Reference</span></span>

- [<span data-ttu-id="ac1c7-116">Outlook Social Connector プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="ac1c7-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ac1c7-117">関連情報</span><span class="sxs-lookup"><span data-stu-id="ac1c7-117">Related sections</span></span>

- [<span data-ttu-id="ac1c7-118">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="ac1c7-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ac1c7-119">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="ac1c7-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="ac1c7-120">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="ac1c7-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ac1c7-121">プロバイダーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="ac1c7-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ac1c7-122">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="ac1c7-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

