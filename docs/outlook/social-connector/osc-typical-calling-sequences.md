---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: OSC プロバイダーの機能拡張インターフェイス、OSC プロバイダーを実装しているメンバーの Outlook ソーシャル コネクタ (OSC) 典型的な呼び出しのシーケンスを説明します。
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804451"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="ff3f2-103">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="ff3f2-103">OSC typical calling sequences</span></span>

<span data-ttu-id="ff3f2-104">OSC プロバイダーの機能拡張インターフェイス、OSC プロバイダーを実装しているメンバーの Outlook ソーシャル コネクタ (OSC) 典型的な呼び出しのシーケンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="ff3f2-105">典型的な呼び出しシーケンスは、時期と方法を示して、OSC は、このようなインターフェイスを使用し、向上できるように、メソッドがプロバイダーの機能拡張インターフェイスで特定のメンバーを実装する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="ff3f2-106">実際の呼び出しのシーケンスは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドによって返される機能によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="ff3f2-107">機能の例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="ff3f2-108">プロバイダーを取得する、キャッシュ、または動的に友人や活動を検索、ソーシャル ネットワークからのサポートします。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="ff3f2-109">ユーザー インターフェイスは、ユーザー ログオン用の OSC を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="ff3f2-110">認証の種類 (たとえば、フォーム ベース認証の場合)、OSC を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="ff3f2-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="ff3f2-111">In this section</span></span>

- <span data-ttu-id="ff3f2-112">[基本認証](basic-authentication.md): OSC プロバイダーは、基本認証をサポートしている場合は、ソーシャル ネットワークにログオンしている Office ユーザーをサポートするために OSC の典型的な呼び出しシーケンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="ff3f2-113">[フォーム ベースの認証](forms-based-authentication.md): OSC プロバイダーは、フォーム ベース認証をサポートしている場合は、ソーシャル ネットワークにログオンしている Office ユーザーをサポートするために OSC の典型的な呼び出しシーケンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="ff3f2-114">[活動を取得する](getting-activities.md): ソーシャル ネットワーク OSC プロバイダーは、アクティビティの同期をサポートしている場合は、ソーシャル ネットワーク経由で Office ユーザーの友人の動作を同期するのには OSC の典型的な呼び出しシーケンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="ff3f2-115">[フレンド情報の取得](getting-friends-information.md): ソーシャル ネットワーク OSC プロバイダーが連絡先のキャッシュの同期をサポートしている場合は、ソーシャル ネットワーク経由での Office ユーザーのフレンド リストを同期するのには OSC の典型的な呼び出しシーケンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ff3f2-116">リファレンス</span><span class="sxs-lookup"><span data-stu-id="ff3f2-116">Reference</span></span>

- [<span data-ttu-id="ff3f2-117">Outlook ソーシャル コネクタ プロバイダーの参照</span><span class="sxs-lookup"><span data-stu-id="ff3f2-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ff3f2-118">関連セクション</span><span class="sxs-lookup"><span data-stu-id="ff3f2-118">Related sections</span></span>

- [<span data-ttu-id="ff3f2-119">Outlook Social Connector プロバイダーの開発の概要(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="ff3f2-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="ff3f2-120">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="ff3f2-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ff3f2-121">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="ff3f2-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ff3f2-122">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="ff3f2-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ff3f2-123">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="ff3f2-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ff3f2-124">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="ff3f2-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ff3f2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff3f2-125">See also</span></span>

- [<span data-ttu-id="ff3f2-126">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="ff3f2-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

