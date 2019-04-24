---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook Social Connector (.osc) プロバイダーの XML スキーマは、ソーシャルネットワークから、ネットワークの .osc プロバイダーを経由して、.osc に渡される大量の情報の形式を定義します。
ms.openlocfilehash: 75809179131ce6c6b8bbe171d2670e59cebe3494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281077"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="91b83-103">OSC XML スキーマによるプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="91b83-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="91b83-104">Outlook Social Connector (.osc) プロバイダーの XML スキーマは、ソーシャルネットワークから、ネットワークの .osc プロバイダーを経由して、.osc に渡される大量の情報の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="91b83-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="91b83-105">XML スキーマを使用すると、.osc プロバイダーは、3つの主要な要素、**機能**、**フレンド**、および**activityfeed**、およびその子を使用して、ソーシャルネットワーク上のプロバイダー、フレンド、アクティビティフィードアイテムの機能を指定できます。elements.</span><span class="sxs-lookup"><span data-stu-id="91b83-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="91b83-106">.osc プロバイダーは、.osc プロバイダーの拡張機能にインターフェイスとそのメソッドを実装し、xml 文字列を、.osc プロバイダーの xml スキーマに準拠する出力パラメーターとして返します。</span><span class="sxs-lookup"><span data-stu-id="91b83-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="91b83-107">.osc は、これらのメソッドを呼び出して、XML スキーマで定義されているように理解できる情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="91b83-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="91b83-108">.osc プロバイダー拡張機能は`DebugProviders` `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 、レジストリキーの値を1に設定することによって、デバッグプロバイダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="91b83-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="91b83-109">プロバイダーデバッグを有効にすると、.osc は、 **xmlns** xml 属性で指定したバージョンの .osc xml スキーマに対して、プロバイダ xml を検証します。</span><span class="sxs-lookup"><span data-stu-id="91b83-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="91b83-110">Outlook Social Connector 2013 以降の .osc 1.1 およびバージョンの .osc については、次のように**xmlns**属性を指定します。`xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="91b83-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="91b83-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="91b83-111">In this section</span></span>

- <span data-ttu-id="91b83-112">[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する: 各プロバイダーが友人、友人以外、およびソーシャルネットワーク上のアクティビティを同期できるようにするさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="91b83-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="91b83-113">[.osc プロバイダ xml の例](osc-provider-xml-examples.md): .osc xml スキーマを使用して、ソーシャルネットワーク上の .osc プロバイダー、フレンド、アクティビティフィードアイテムの機能を指定する方法を示す XML の例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91b83-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="91b83-114">[機能の xml](xml-for-capabilities.md): この例で[](isocialprovider-getcapabilities.md)は、.osc が機能情報を取得するために、.osc プロバイダーから機能情報を取得する\*\*\*\* ために、.osc で使用されています。</span><span class="sxs-lookup"><span data-stu-id="91b83-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="91b83-115">このセクションでは、.osc プロバイダーの xml スキーマの xml 要素についても説明します。これにより、.osc プロバイダーは、ユーザーの認証方法やフレンドとアクティビティの同期方法などの機能を指定できます。</span><span class="sxs-lookup"><span data-stu-id="91b83-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="91b83-116">[friends の XML](xml-for-friends.md): friends が、 **friends** XML で表現される友人の情報を、.osc プロバイダーから取得するために、.osc が使用する api の例を示します。</span><span class="sxs-lookup"><span data-stu-id="91b83-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="91b83-117">このセクションでは、 **friends** XML の要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="91b83-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="91b83-118">[アクティビティ用の XML](xml-for-activities.md): アクティビティ情報を取得するために、.osc がアクティビティ情報を取得する\*\*\*\* ために使用する api の例を、.osc プロバイダーから提供します。</span><span class="sxs-lookup"><span data-stu-id="91b83-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="91b83-119">このセクションでは、.osc プロバイダーがアクティビティフィードを指定できるようにする、.osc プロバイダーの xml スキーマの xml 要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="91b83-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="91b83-120">アクティビティフィードには、アクティビティフィードのアイテムが送信されたネットワーク、各アクティビティフィードアイテムの詳細 (所有者、種類、アクティビティの発行日など)、およびアクティビティを表示するためのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="91b83-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="91b83-121">リファレンス</span><span class="sxs-lookup"><span data-stu-id="91b83-121">Reference</span></span>

- [<span data-ttu-id="91b83-122">Outlook Social Connector プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="91b83-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="91b83-123">関連情報</span><span class="sxs-lookup"><span data-stu-id="91b83-123">Related sections</span></span>

- [<span data-ttu-id="91b83-124">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="91b83-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="91b83-125">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="91b83-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="91b83-126">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="91b83-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="91b83-127">プロバイダーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="91b83-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="91b83-128">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="91b83-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="91b83-129">プロバイダーを開発するためのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="91b83-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="91b83-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="91b83-130">See also</span></span>

- [<span data-ttu-id="91b83-131">プロバイダーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="91b83-131">Debugging a Provider</span></span>](debugging-a-provider.md)

