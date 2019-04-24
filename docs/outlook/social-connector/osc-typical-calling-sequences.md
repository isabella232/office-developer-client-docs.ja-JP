---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: このセクションでは、.osc プロバイダーが実装している、.osc プロバイダー拡張インターフェイスのメンバーの一般的な呼び出しシーケンス (.osc) について説明します。
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356267"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="c6281-103">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="c6281-103">OSC typical calling sequences</span></span>

<span data-ttu-id="c6281-104">このセクションでは、.osc プロバイダーが実装している、.osc プロバイダー拡張インターフェイスのメンバーの一般的な呼び出しシーケンス (.osc) について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6281-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="c6281-105">典型的な呼び出しシーケンスは、.osc がこのようなインターフェイスやメソッドを使用する方法とタイミングを示しており、プロバイダー拡張インターフェイスに特定のメンバーを実装する方法をより良く判断できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c6281-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="c6281-106">実際の通話シーケンスは、 [iime alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドによって返される機能によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c6281-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="c6281-107">機能の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c6281-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="c6281-108">プロバイダーは、ソーシャルネットワークからの友人やアクティビティを取得、キャッシュ、または動的に検索するためにサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c6281-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="c6281-109">ユーザーがログオンするために、.osc が表示するユーザーインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="c6281-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="c6281-110">.osc が使用する認証の種類 (フォームベース認証など)。</span><span class="sxs-lookup"><span data-stu-id="c6281-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="c6281-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="c6281-111">In this section</span></span>

- <span data-ttu-id="c6281-112">[基本認証](basic-authentication.md): .osc プロバイダーが基本認証をサポートしている場合、ソーシャルネットワークにログオンしている Office ユーザーをサポートするために、.osc の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6281-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="c6281-113">[フォームベース認証](forms-based-authentication.md): .osc プロバイダーがフォームベース認証をサポートしている場合、ソーシャルネットワークにログオンしている Office ユーザーをサポートするために、.osc の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6281-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="c6281-114">[アクティビティの取得](getting-activities.md): ソーシャルネットワークの関連プロバイダーがアクティビティの同期をサポートしている場合は、.osc の一般的な呼び出しシーケンスを、ソーシャルネットワークから同期するように記述します。</span><span class="sxs-lookup"><span data-stu-id="c6281-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="c6281-115">[フレンド情報の取得](getting-friends-information.md): ソーシャルネットワークの機能プロバイダーが連絡先のキャッシュされた同期をサポートしている場合は、アプリケーションから Office ユーザーのフレンドリストをソーシャルネットワークから同期するための、.osc の一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6281-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="c6281-116">リファレンス</span><span class="sxs-lookup"><span data-stu-id="c6281-116">Reference</span></span>

- [<span data-ttu-id="c6281-117">Outlook Social Connector プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="c6281-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="c6281-118">関連情報</span><span class="sxs-lookup"><span data-stu-id="c6281-118">Related sections</span></span>

- [<span data-ttu-id="c6281-119">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="c6281-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="c6281-120">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="c6281-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="c6281-121">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="c6281-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="c6281-122">プロバイダーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="c6281-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="c6281-123">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="c6281-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="c6281-124">プロバイダーを開発するためのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="c6281-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="c6281-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6281-125">See also</span></span>

- [<span data-ttu-id="c6281-126">機能の XML</span><span class="sxs-lookup"><span data-stu-id="c6281-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

