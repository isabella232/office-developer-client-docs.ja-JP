---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: このセクションでは、OSC プロバイダー Outlook実装する OSC プロバイダー拡張インターフェイスのメンバーの Outlook ソーシャル コネクタ (OSC) の一般的な呼び出しシーケンスについて説明します。
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413613"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="fd1e8-103">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="fd1e8-103">OSC typical calling sequences</span></span>

<span data-ttu-id="fd1e8-104">このセクションでは、OSC プロバイダー Outlook実装する OSC プロバイダー拡張インターフェイスのメンバーの Outlook ソーシャル コネクタ (OSC) の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="fd1e8-105">一般的な呼び出しシーケンスは、OSC がこのようなインターフェイスとメソッドを使用する方法と時間を示し、プロバイダー拡張インターフェイスに特定のメンバーを実装する方法をより適切に決定できます。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="fd1e8-106">実際の呼び出しシーケンスは [、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドによって返される機能によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="fd1e8-107">機能の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="fd1e8-108">ソーシャル ネットワークからフレンドやアクティビティを取得、キャッシュ、または動的に参照するプロバイダーのサポート。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="fd1e8-109">ユーザー ログオンのために OSC が表示するユーザー インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="fd1e8-110">OSC で使用する認証の種類 (フォーム ベース認証など)。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="fd1e8-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="fd1e8-111">In this section</span></span>

- <span data-ttu-id="fd1e8-112">[基本認証](basic-authentication.md): OSC プロバイダーが基本認証をサポートしている場合に、ソーシャル ネットワークにログオンしている Office ユーザーをサポートする OSC の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="fd1e8-113">[フォーム ベース認証](forms-based-authentication.md): OSC プロバイダーがフォーム ベース認証をサポートしている場合に、ソーシャル ネットワークにログオンしている Office ユーザーをサポートする OSC の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="fd1e8-114">[Getting Activities](getting-activities.md): ソーシャル ネットワーク OSC プロバイダーがアクティビティの同期をサポートしている場合に、Office ユーザーのフレンドのアクティビティをソーシャル ネットワークから同期する OSC の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="fd1e8-115">[フレンド情報の](getting-friends-information.md)取得 : ソーシャル ネットワーク OSC プロバイダーが連絡先のキャッシュ同期をサポートしている場合に、ソーシャル ネットワークから Office ユーザーのフレンド リストを同期する OSC の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1e8-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="fd1e8-116">参照</span><span class="sxs-lookup"><span data-stu-id="fd1e8-116">Reference</span></span>

- [<span data-ttu-id="fd1e8-117">Outlookソーシャル コネクタ プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="fd1e8-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="fd1e8-118">関連情報</span><span class="sxs-lookup"><span data-stu-id="fd1e8-118">Related sections</span></span>

- [<span data-ttu-id="fd1e8-119">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="fd1e8-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="fd1e8-120">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="fd1e8-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="fd1e8-121">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="fd1e8-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="fd1e8-122">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="fd1e8-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="fd1e8-123">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="fd1e8-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="fd1e8-124">プロバイダーの開発に関するベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="fd1e8-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="fd1e8-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd1e8-125">See also</span></span>

- [<span data-ttu-id="fd1e8-126">機能の XML</span><span class="sxs-lookup"><span data-stu-id="fd1e8-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

