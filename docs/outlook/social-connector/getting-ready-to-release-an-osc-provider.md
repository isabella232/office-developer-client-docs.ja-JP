---
title: OSC プロバイダーをリリースする準備をします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、Outlook ソーシャル コネクタ (OSC) は、プロバイダーをリリースする前に行うことができますテストをお勧めします。
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804338"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="88e9c-103">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="88e9c-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="88e9c-104">このセクションでは、Outlook ソーシャル コネクタ (OSC) は、プロバイダーをリリースする前に行うことができますテストをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88e9c-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="88e9c-105">このセクションのトピックを参照するを起動し、開発とテストのフェーズの中にいくつかのこれらのテストを実行しますが、リリースした時点でこれらのテストを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88e9c-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="88e9c-106">OSC プロバイダーを指定する機能に関して、OSC プロバイダーのインターフェイスの実装の基本的な機能を検証します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="88e9c-107">また、複数の Office クライアント アプリケーションで共有する機能ですが、OSC、これらのテスト Outlook を使用クライアントとして基本的な機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="88e9c-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="88e9c-108">その他のテストは、プロバイダーに固有の機能に必要かどうかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88e9c-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="88e9c-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="88e9c-109">In this section</span></span>

- <span data-ttu-id="88e9c-110">[展開テスト](testing-deployment.md): をインストールすると、OSC プロバイダーをアンインストールするをテストする必要があるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="88e9c-111">[機能のテスト、認証、および構成](testing-capabilities-authentication-and-configuration.md): 機能、およびアカウントの構成とソーシャル ネットワークのユーザーの認証のシナリオを取得するためのテストを説明します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="88e9c-112">[次のテストと停止次の人](testing-following-and-stop-following-persons.md): 友人としてユーザーを追加する機能やソーシャル ネットワークからフレンドを削除するのには、OSC プロバイダーの機能をテストするシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="88e9c-113">[友人のテスト](testing-friends.md): テストおよび該当する場合、プロバイダーがサポートする同期モードに応じて、OSC プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="88e9c-114">[活動のテスト](testing-activities.md): テストおよび該当する場合、プロバイダーがサポートする同期モードに応じて、OSC プロバイダーがその友人や、友人以外の活動を適切に返すことを確認するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="88e9c-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="88e9c-115">Reference</span></span>

- [<span data-ttu-id="88e9c-116">Outlook ソーシャル コネクタ プロバイダーの参照</span><span class="sxs-lookup"><span data-stu-id="88e9c-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="88e9c-117">関連セクション</span><span class="sxs-lookup"><span data-stu-id="88e9c-117">Related sections</span></span>

- [<span data-ttu-id="88e9c-118">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="88e9c-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="88e9c-119">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="88e9c-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="88e9c-120">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="88e9c-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="88e9c-121">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="88e9c-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="88e9c-122">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="88e9c-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

