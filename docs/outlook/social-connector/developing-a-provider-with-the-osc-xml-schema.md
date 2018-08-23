---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook ソーシャル コネクタ (OSC) プロバイダーの XML スキーマでは、膨大な OSC をソーシャル ネットワークからネットワークの OSC プロバイダーを通じて渡される情報の形式を定義します。
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804346"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="69eef-103">OSC XML スキーマによるプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="69eef-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="69eef-104">Outlook ソーシャル コネクタ (OSC) プロバイダーの XML スキーマでは、膨大な OSC をソーシャル ネットワークからネットワークの OSC プロバイダーを通じて渡される情報の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="69eef-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="69eef-105">XML スキーマでは、プロバイダー、友人、またはアクティビティ フィードのアイテムの 3 つの主要な要素、**機能**、**友人**、および**activityFeed**、およびその子を使用して、ソーシャル ネットワーク上の機能を指定するのには、OSC プロバイダー要素です。</span><span class="sxs-lookup"><span data-stu-id="69eef-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="69eef-106">OSC プロバイダーにより、OSC プロバイダーの機能拡張のインターフェイスとそのメソッドを実装 OSC プロバイダーの XML スキーマに準拠している出力パラメーターとしての XML 文字列を返すことが実現します。</span><span class="sxs-lookup"><span data-stu-id="69eef-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="69eef-107">OSC では、XML スキーマで定義されていることが理解できる情報を取得するこれらのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="69eef-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="69eef-108">OSC プロバイダーの拡張機能を設定してプロバイダーのデバッグをサポートする、`DebugProviders`の値、`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`レジストリ キーを 1 にします。</span><span class="sxs-lookup"><span data-stu-id="69eef-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="69eef-109">プロバイダーのデバッグを有効にすると、OSC は、 **xmlns**の XML 属性で指定した OSC の XML スキーマのバージョンとプロバイダーの XML を検証します。</span><span class="sxs-lookup"><span data-stu-id="69eef-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="69eef-110">OSC 1.1 とバージョンの Outlook ソーシャル コネクタ 2013 以降の OSC は、次のように、 **xmlns**属性を指定します。`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="69eef-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="69eef-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="69eef-111">In this section</span></span>

- <span data-ttu-id="69eef-112">[同期の友人と活動](synchronizing-friends-and-activities.md): OSC プロバイダーが友人、友人以外の場合、およびソーシャル ネットワーク上のアクティビティを同期できること、さまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="69eef-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="69eef-113">[OSC プロバイダーの XML の例](osc-provider-xml-examples.md): を含む XML の例を示します、OSC プロバイダー、友人、およびアクティビティの機能を指定するのにはソーシャル ネットワークの OSC の XML スキーマを使用してアイテムをフィードします。</span><span class="sxs-lookup"><span data-stu-id="69eef-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="69eef-114">[機能のための XML](xml-for-capabilities.md): 説明 - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) OSC を使用するメソッド**の機能**、XML から OSC プロバイダーで表される機能情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="69eef-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="69eef-115">OSC プロバイダーなど、どのようにユーザーを認証して、友人との活動を同期化の機能を指定できるように、OSC プロバイダーの XML スキーマ内の XML 要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="69eef-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="69eef-116">[友人の XML](xml-for-friends.md): OSC を使用して**友人**、XML OSC プロバイダーからで表される、友人の情報を取得する Api の例を紹介します。</span><span class="sxs-lookup"><span data-stu-id="69eef-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="69eef-117">**友人**XML 内の要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="69eef-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="69eef-118">[アクティビティ用の XML](xml-for-activities.md): OSC を使用してアクティビティについては、 **activityFeed** XML、OSC プロバイダーからの表現を取得する Api の例を紹介します。</span><span class="sxs-lookup"><span data-stu-id="69eef-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="69eef-119">OSC プロバイダー、アクティビティ フィードを指定できるように、OSC プロバイダーの XML スキーマ内の XML 要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="69eef-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="69eef-120">アクティビティ フィードには、ネットワーク アクティビティが発生した場合、アイテムをフィードごとのアクティビティ フィードのアイテムの詳細が含まれています (などの所有者は、入力、発行とアクティビティの日付)、および活動を表示するテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="69eef-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="69eef-121">リファレンス</span><span class="sxs-lookup"><span data-stu-id="69eef-121">Reference</span></span>

- [<span data-ttu-id="69eef-122">Outlook ソーシャル コネクタ プロバイダーの参照</span><span class="sxs-lookup"><span data-stu-id="69eef-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="69eef-123">関連情報</span><span class="sxs-lookup"><span data-stu-id="69eef-123">Related sections</span></span>

- [<span data-ttu-id="69eef-124">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="69eef-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="69eef-125">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="69eef-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="69eef-126">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="69eef-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="69eef-127">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="69eef-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="69eef-128">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="69eef-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="69eef-129">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="69eef-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="69eef-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="69eef-130">See also</span></span>

- [<span data-ttu-id="69eef-131">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="69eef-131">Debugging a Provider</span></span>](debugging-a-provider.md)

