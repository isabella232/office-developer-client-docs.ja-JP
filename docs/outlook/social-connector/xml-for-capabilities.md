---
title: 機能の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (OSC) プロバイダー XML スキーマの capabilities 要素を使用すると、OSC プロバイダーは機能を指定できます。 このような機能には、次の機能が含まれます。
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435006"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="c4f96-104">機能の XML</span><span class="sxs-lookup"><span data-stu-id="c4f96-104">XML for capabilities</span></span>

<span data-ttu-id="c4f96-105">(OSC) プロバイダー XML スキーマの **capabilities** 要素を使用すると、OSC プロバイダーは機能を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4f96-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="c4f96-106">このような機能には、次の機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4f96-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="c4f96-107">プロバイダーがソーシャル ネットワークからのフレンドやアクティビティの取得、キャッシュ、または動的な参照をサポートするかどうか。</span><span class="sxs-lookup"><span data-stu-id="c4f96-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="c4f96-108">OSC が特定のログオン ユーザー インターフェイスを表示する方法。</span><span class="sxs-lookup"><span data-stu-id="c4f96-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="c4f96-109">OSC がフォーム ベース認証を使用するか、ソーシャル ネットワークを自動的に構成し、ソーシャル ネットワーク上のユーザーにログオンするか。</span><span class="sxs-lookup"><span data-stu-id="c4f96-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="c4f96-110">機能の XML スキーマ **は、** プロバイダーがサポートする機能を OSC に識別するために重要です。</span><span class="sxs-lookup"><span data-stu-id="c4f96-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="c4f96-111">OSC プロバイダーは、結果文字列を返す [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドを実装する  _必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="c4f96-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="c4f96-112">OSC は **ISocialProvider::GetCapabilities** を呼び出して、結果文字列内の OSC プロバイダーの機能に関する情報を取得します。この情報は、capabilities 要素の XML スキーマ定義に準拠しています。  </span><span class="sxs-lookup"><span data-stu-id="c4f96-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="c4f96-113">この情報により、OSC から OSC プロバイダーへの後続の呼び出しが正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="c4f96-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="c4f96-114">**ISocialProvider::GetCapabilities** メソッドの出力パラメーターとして OSC プロバイダーの機能を指定するには、OSC プロバイダー拡張 XML スキーマに準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4f96-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="c4f96-115">次の図は、機能 **XML 構造を** 示しています。</span><span class="sxs-lookup"><span data-stu-id="c4f96-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="c4f96-116">**図 1. \<機能 \> XML 構造**</span><span class="sxs-lookup"><span data-stu-id="c4f96-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="c4f96-118">capabilities 要素の子要素の詳細な説明については[、「Capabilities XML Elements」を参照してください](capabilities-xml-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4f96-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="c4f96-119">機能 XML の例 **については、「Capabilities** [XML の例」を参照してください](capabilities-xml-example.md)。</span><span class="sxs-lookup"><span data-stu-id="c4f96-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="c4f96-120">OSC プロバイダー XML スキーマの完全な定義 (必須または省略可能な要素を含む) については、「ソーシャル コネクタ プロバイダー XML スキーマOutlook[を参照してください](outlook-social-connector-provider-xml-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="c4f96-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4f96-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4f96-121">See also</span></span>

- [<span data-ttu-id="c4f96-122">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="c4f96-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="c4f96-123">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="c4f96-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="c4f96-124">友人のための XML</span><span class="sxs-lookup"><span data-stu-id="c4f96-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="c4f96-125">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="c4f96-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="c4f96-126">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="c4f96-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

