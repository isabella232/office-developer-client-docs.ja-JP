---
title: 機能のための XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (OSC) プロバイダーの XML スキーマ内の機能要素では、OSC プロバイダーの機能を指定することができます。 このような機能には次のものが含まれています。
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804461"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="371b4-104">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="371b4-104">XML for capabilities</span></span>

<span data-ttu-id="371b4-105">(OSC) プロバイダーの XML スキーマ内の**機能**要素では、OSC プロバイダーの機能を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="371b4-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="371b4-106">このような機能には次のものが含まれています。</span><span class="sxs-lookup"><span data-stu-id="371b4-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="371b4-107">かどうかを取得する、キャッシュ、または動的に友人や活動を検索、ソーシャル ネットワークからプロバイダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="371b4-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="371b4-108">方法、OSC では、特定のログオン ユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="371b4-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="371b4-109">かどうか、OSC はフォーム ベース認証を使用して、または、ソーシャル ネットワーク上のユーザーに、ソーシャル ネットワークとログを自動的に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="371b4-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="371b4-110">**機能**の XML スキーマは、プロバイダーがサポートする機能が、OSC に特定されるために重要です。</span><span class="sxs-lookup"><span data-stu-id="371b4-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="371b4-111">OSC プロバイダーでは、_結果_の文字列を返す[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="371b4-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="371b4-112">OSC では、**機能**要素の XML スキーマ定義に準拠している_結果_の文字列の OSC プロバイダーの機能に関する情報を取得する**ISocialProvider::GetCapabilities**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="371b4-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="371b4-113">この情報は、それ以降、OSC から OSC プロバイダーが正常に動作するを使用できます。</span><span class="sxs-lookup"><span data-stu-id="371b4-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="371b4-114">OSC プロバイダーの機能を**ISocialProvider::GetCapabilities**メソッドの出力パラメーターとして指定するには、OSC プロバイダーの拡張機能の XML スキーマに準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="371b4-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="371b4-115">**機能**の XML データ構造を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="371b4-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="371b4-116">**図 1 です。\<機能\>[XML データ構造**</span><span class="sxs-lookup"><span data-stu-id="371b4-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="371b4-118">**機能**要素の子要素の詳細な説明については、[機能の XML 要素](capabilities-xml-elements.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="371b4-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="371b4-119">XML の**機能**の使用例は、[機能の XML の例](capabilities-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="371b4-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="371b4-120">のどの要素には、必須またはオプションを含む、OSC プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="371b4-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="371b4-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="371b4-121">See also</span></span>

- [<span data-ttu-id="371b4-122">機能の XML の例</span><span class="sxs-lookup"><span data-stu-id="371b4-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="371b4-123">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="371b4-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="371b4-124">友人の XML</span><span class="sxs-lookup"><span data-stu-id="371b4-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="371b4-125">活動の XML</span><span class="sxs-lookup"><span data-stu-id="371b4-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="371b4-126">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="371b4-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

