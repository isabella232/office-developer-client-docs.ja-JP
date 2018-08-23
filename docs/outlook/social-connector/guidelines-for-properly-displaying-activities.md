---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook ソーシャル コネクタ (OSC) プロバイダーには、OSC の活動項目をメモリに格納する getActivities と dynamicActivitiesLookupEx の要素を設定できます。
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804331"
---
# <a name="guidelines-for-properly-displaying-activities"></a><span data-ttu-id="39cfb-103">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="39cfb-103">Guidelines for properly displaying activities</span></span>

<span data-ttu-id="39cfb-104">Outlook ソーシャル コネクタ (OSC) のプロバイダーは、 **getActivities**を設定でき、OSC に**dynamicActivitiesLookupEx**要素は、活動項目をメモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-104">Outlook Social Connector (OSC) providers can set the **getActivities** and **dynamicActivitiesLookupEx** elements to have the OSC store activity items in memory.</span></span> <span data-ttu-id="39cfb-105">OSC プロバイダーは、同期アクティビティをサポートしている場合を取得またはアクティビティおよびアクティビティの所有者の詳細を更新するには、OSC を呼び出す Api のフィードをソーシャル ネットワークから、OSC プロバイダーの機能拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-105">This topic describes the OSC provider extensibility APIs that the OSC calls to get or refresh activities and activity owner details, if the OSC provider supports synchronizing activity feeds from the social network.</span></span> <span data-ttu-id="39cfb-106">OSC プロバイダーは、連絡先カードの Office または Outlook 人物情報ウィンドウでのアクティビティを正しく表示するための OSC の設定をする必要があります**activityFeed**要素のいくつかの子要素についても説明します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-106">The topic also lists a few child elements of the **activityFeed** element that the OSC provider should set for the OSC to display activities properly in the Office Contact Card or Outlook People Pane.</span></span> 
  
- <span data-ttu-id="39cfb-107">OSC では、取得し、ニュース フィードのフォルダーにログオンしているユーザーのアクティビティを格納する[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-107">The OSC calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method to get and store activities in the News Feed folder for the logged-on user.</span></span> <span data-ttu-id="39cfb-108">OSC プロバイダーは、OSC プロバイダーの**activityFeed**要素の XML スキーマ定義に準拠している_アクティビティ_の XML 文字列を返すには、 **GetActivitiesEx**を実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="39cfb-108">The OSC provider must implement **GetActivitiesEx** to return an  _activities_ XML string that complies with the OSC provider XML schema definition of the **activityFeed** element.</span></span> 
    
- <span data-ttu-id="39cfb-109">OSC プロバイダーでは、 **activityDetails**要素の子要素である、 **ownerID**要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39cfb-109">The OSC provider must set the **ownerID** element, which is a child element of the **activityDetails** element.</span></span> <span data-ttu-id="39cfb-110">**ownerID**は、不透明なソーシャル ネットワーク上の活動の所有者を識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="39cfb-110">**ownerID** is an opaque string that identifies the owner of the activity on the social network.</span></span> 
    
- <span data-ttu-id="39cfb-111">OSC プロバイダーは、 **templateVariables**要素の [ **publisherVariable** ] ノードで、 **nameHint**と**emailAddress**要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39cfb-111">The OSC provider should set the **nameHint** and **emailAddress** elements in the **publisherVariable** node of the **templateVariables** element.</span></span> 
    
   <span data-ttu-id="39cfb-112">OSC プロバイダーの XML スキーマでは、各**nameHint**の要素が省略可能な要素に注意してください。</span><span class="sxs-lookup"><span data-stu-id="39cfb-112">Note that per the OSC provider XML schema, the **nameHint** element is an optional element.</span></span> <span data-ttu-id="39cfb-113">OSC では、連絡先カードまたは人物情報ウィンドウで選択したユーザーの表示名を一致するようにそれを使用します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-113">The OSC uses it to match the display name of the user selected in the Contact Card or People Pane.</span></span> <span data-ttu-id="39cfb-114">同様に、 **emailAddress**要素は、XML スキーマに省略可能な要素です。</span><span class="sxs-lookup"><span data-stu-id="39cfb-114">Similarly, the **emailAddress** element is an optional element in the XML schema.</span></span> <span data-ttu-id="39cfb-115">OSC では、連絡先カードまたは人物情報ウィンドウで選択したユーザーの SMTP アドレスと一致するのに、それを使用します。</span><span class="sxs-lookup"><span data-stu-id="39cfb-115">The OSC uses it to match the SMTP address of the user selected in the Contact Card or People Pane.</span></span> 
    
   <span data-ttu-id="39cfb-116">[ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドとし、 [ISocialPerson::GetDetails](isocialperson-getdetails.md) OSC を呼び出す場合だけ**ownerID**要素を指定すると、 **nameHint**および**emailAddress**の一方または両方が指定されていない、**ownerID**によって識別されるユーザーに関する詳細情報を取得するメソッドです。</span><span class="sxs-lookup"><span data-stu-id="39cfb-116">If only the **ownerID** element is specified, but one or both of **nameHint** and **emailAddress** are not specified, the OSC calls the [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) method and then the [ISocialPerson::GetDetails](isocialperson-getdetails.md) method to get more information about the person identified by the **ownerID**.</span></span> <span data-ttu-id="39cfb-117">OSC が**ISocialPerson::GetDetails**を呼び出すと、プロバイダーは**人****氏名**と**emailAddress**要素を指定する XML を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="39cfb-117">When the OSC calls **ISocialPerson::GetDetails**, the provider must return **person** XML that specifies the **fullName** and **emailAddress** elements.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="39cfb-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="39cfb-118">See also</span></span>

- [<span data-ttu-id="39cfb-119">活動の XML</span><span class="sxs-lookup"><span data-stu-id="39cfb-119">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="39cfb-120">友人の XML</span><span class="sxs-lookup"><span data-stu-id="39cfb-120">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="39cfb-121">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="39cfb-121">XML for Capabilities</span></span>](xml-for-capabilities.md)

