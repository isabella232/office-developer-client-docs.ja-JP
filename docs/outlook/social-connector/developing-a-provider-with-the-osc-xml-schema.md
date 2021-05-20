---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook ソーシャル コネクタ (OSC) プロバイダー XML スキーマは、ネットワークの OSC プロバイダーを介してソーシャル ネットワークから OSC に渡される大量の情報の形式を定義します。
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539256"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="82be8-103">OSC XML スキーマによるプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="82be8-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="82be8-104">Outlook ソーシャル コネクタ (OSC) プロバイダー XML スキーマは、ネットワークの OSC プロバイダーを介してソーシャル ネットワークから OSC に渡される大量の情報の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="82be8-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="82be8-105">XML スキーマを使用すると、OSC プロバイダーは、3 つの主要な要素、機能、フレンド、activityFeed、および子要素を使用して、ソーシャルネットワーク上のプロバイダー、フレンド、アクティビティ フィード アイテムの機能を指定できます。</span><span class="sxs-lookup"><span data-stu-id="82be8-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="82be8-106">OSC プロバイダーは、OSC プロバイダーの機能拡張にインターフェイスとそのメソッドを実装し、OSC プロバイダー XML スキーマに準拠する出力パラメーターとして XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="82be8-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="82be8-107">OSC は、これらのメソッドを呼び出して、XML スキーマで定義されている情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="82be8-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82be8-108">OSC プロバイダーの機能拡張は、レジストリ キーの値を 1 に設定することで、デバッグ プロバイダー `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` をサポートします。</span><span class="sxs-lookup"><span data-stu-id="82be8-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="82be8-109">プロバイダーのデバッグを有効にした場合、OSC は **xmlns** XML 属性で指定した OSC XML スキーマのバージョンに対してプロバイダー XML を検証します。</span><span class="sxs-lookup"><span data-stu-id="82be8-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="82be8-110">ソーシャル コネクタ 2013 以降の OSC 1.1 およびバージョンOutlook **xmlns** 属性を次のように指定します。`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="82be8-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="82be8-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="82be8-111">In this section</span></span>

- <span data-ttu-id="82be8-112">[フレンドとアクティビティの同期](synchronizing-friends-and-activities.md): OSC プロバイダーがフレンド、フレンド以外、ソーシャル ネットワーク上のアクティビティを同期できるさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="82be8-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="82be8-113">[OSC プロバイダー XML](osc-provider-xml-examples.md)の例 : OSC XML スキーマを使用して、ソーシャル ネットワーク上の OSC プロバイダー、フレンド、およびアクティビティ フィード アイテムの機能を指定する方法を示す XML 例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82be8-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="82be8-114">[機能の XML](xml-for-capabilities.md): OSC が OSC プロバイダーから機能 **XML** で表される機能情報を取得するために使用する - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="82be8-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="82be8-115">このセクションでは、OSC プロバイダーがユーザーを認証し、友人やアクティビティを同期する方法など、OSC プロバイダーが機能を指定できる OSC プロバイダー XML スキーマの XML 要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="82be8-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="82be8-116">[[フレンド用 XML]:](xml-for-friends.md)OSC がフレンド **XML** で表されるフレンドの情報を OSC プロバイダーから取得するために使用する API の例を示します。</span><span class="sxs-lookup"><span data-stu-id="82be8-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="82be8-117">このセクションでは、フレンド XML の要素について **説明** します。</span><span class="sxs-lookup"><span data-stu-id="82be8-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="82be8-118">[アクティビティの XML](xml-for-activities.md): OSC プロバイダーから **activityFeed** XML で表されるアクティビティ情報を取得するために OSC が使用する API の例を示します。</span><span class="sxs-lookup"><span data-stu-id="82be8-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="82be8-119">このセクションでは、OSC プロバイダーがアクティビティ フィードを指定できる OSC プロバイダー XML スキーマの XML 要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="82be8-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="82be8-120">アクティビティ フィードには、アクティビティ フィード アイテムが発生したネットワーク、各アクティビティ フィード アイテムの詳細 (アクティビティの所有者、種類、発行日など)、アクティビティを表示するテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="82be8-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="82be8-121">参照</span><span class="sxs-lookup"><span data-stu-id="82be8-121">Reference</span></span>

- [<span data-ttu-id="82be8-122">Outlookソーシャル コネクタ プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="82be8-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="82be8-123">関連情報</span><span class="sxs-lookup"><span data-stu-id="82be8-123">Related sections</span></span>

- [<span data-ttu-id="82be8-124">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="82be8-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="82be8-125">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="82be8-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="82be8-126">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="82be8-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="82be8-127">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="82be8-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="82be8-128">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="82be8-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="82be8-129">プロバイダーの開発に関するベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="82be8-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="82be8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="82be8-130">See also</span></span>

- [<span data-ttu-id="82be8-131">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="82be8-131">Debugging a Provider</span></span>](debugging-a-provider.md)

