---
title: 機能の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (.osc) プロバイダ XML スキーマの capabilities 要素を使用すると、.osc プロバイダーはその機能を指定できます。 そのような機能は次のとおりです。
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356447"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="78d91-104">機能の XML</span><span class="sxs-lookup"><span data-stu-id="78d91-104">XML for capabilities</span></span>

<span data-ttu-id="78d91-105">(.osc) プロバイダ XML スキーマの**capabilities**要素を使用すると、.osc プロバイダーはその機能を指定できます。</span><span class="sxs-lookup"><span data-stu-id="78d91-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="78d91-106">そのような機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="78d91-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="78d91-107">プロバイダーがソーシャルネットワークからのフレンドやアクティビティを取得、キャッシュ、または動的に検索することをサポートしているかどうか。</span><span class="sxs-lookup"><span data-stu-id="78d91-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="78d91-108">.osc で特定のログオンユーザーインターフェイスを表示する方法。</span><span class="sxs-lookup"><span data-stu-id="78d91-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="78d91-109">.osc がフォームベース認証を使用するか、ソーシャルネットワーク上のユーザーに対してソーシャルネットワークとログを自動的に構成するか。</span><span class="sxs-lookup"><span data-stu-id="78d91-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="78d91-110">**機能**の XML スキーマは、プロバイダーによってサポートされている機能を詳細に示すために重要です。</span><span class="sxs-lookup"><span data-stu-id="78d91-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="78d91-111">.osc プロバイダーは、_結果_の文字列を返す[imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78d91-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="78d91-112">.osc は**iな alprovider:: getcapabilities**を呼び出して、_結果_文字列の .osc プロバイダーの機能に関する情報を取得します。これは、 **capabilities**要素の XML スキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="78d91-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="78d91-113">この情報によって、.osc から .osc プロバイダーへの後続の呼び出しが正しく動作するようになります。</span><span class="sxs-lookup"><span data-stu-id="78d91-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="78d91-114">.osc プロバイダーの機能を**imethod alprovider:: getcapabilities**メソッドの出力パラメーターとして指定するには、.osc プロバイダ拡張 XML スキーマに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="78d91-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="78d91-115">次の図は、**機能**の XML データ構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="78d91-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="78d91-116">**図1。\<機能\> XML データ構造**</span><span class="sxs-lookup"><span data-stu-id="78d91-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="78d91-118">**capabilities**要素の子要素の詳細については、「[機能 XML 要素](capabilities-xml-elements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78d91-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="78d91-119">**機能**xml の例については、「 [capabilities xml の例](capabilities-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78d91-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="78d91-120">必要な要素やオプションの要素を含む、.osc プロバイダ XML スキーマの完全な定義については、「 [Outlook Social Connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78d91-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78d91-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="78d91-121">See also</span></span>

- [<span data-ttu-id="78d91-122">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="78d91-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="78d91-123">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="78d91-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="78d91-124">Friends の XML</span><span class="sxs-lookup"><span data-stu-id="78d91-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="78d91-125">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="78d91-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="78d91-126">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="78d91-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

