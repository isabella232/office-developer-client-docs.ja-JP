---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Social Connector (.osc) プロバイダーは、getactivities および dynamicActivitiesLookupEx 要素が、.osc store アクティビティアイテムをメモリに保持するように設定できます。
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422916"
---
# <a name="guidelines-for-properly-displaying-activities"></a><span data-ttu-id="5bc8c-103">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="5bc8c-103">Guidelines for properly displaying activities</span></span>

<span data-ttu-id="5bc8c-104">Outlook Social Connector (.osc) プロバイダーは、 **getactivities**および**dynamicActivitiesLookupEx**要素が、.osc store アクティビティアイテムをメモリに保持するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-104">Outlook Social Connector (OSC) providers can set the **getActivities** and **dynamicActivitiesLookupEx** elements to have the OSC store activity items in memory.</span></span> <span data-ttu-id="5bc8c-105">このトピックでは、.osc プロバイダーがソーシャルネットワークからのアクティビティフィードの同期をサポートしている場合に、アクティビティとアクティビティ所有者の詳細を取得または更新するために、.osc が呼び出すプロバイダー拡張 api について説明します。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-105">This topic describes the OSC provider extensibility APIs that the OSC calls to get or refresh activities and activity owner details, if the OSC provider supports synchronizing activity feeds from the social network.</span></span> <span data-ttu-id="5bc8c-106">また、このトピックには、.osc に対して .osc プロバイダーで設定する必要がある**activityfeed**要素のいくつかの子要素が表示されます。これにより、Office の連絡先カードまたは Outlook の [ユーザー] ウィンドウにアクティビティが適切に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-106">The topic also lists a few child elements of the **activityFeed** element that the OSC provider should set for the OSC to display activities properly in the Office Contact Card or Outlook People Pane.</span></span> 
  
- <span data-ttu-id="5bc8c-107">.osc は、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出して、ログオンしているユーザーのニュースフィードフォルダーにアクティビティを取得して保存します。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-107">The OSC calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method to get and store activities in the News Feed folder for the logged-on user.</span></span> <span data-ttu-id="5bc8c-108">.osc プロバイダーは、 **GetActivitiesEx**を実装して、 **activityfeed**要素の .osc プロバイダ xml スキーマ定義に準拠した_アクティビティ_xml 文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-108">The OSC provider must implement **GetActivitiesEx** to return an  _activities_ XML string that complies with the OSC provider XML schema definition of the **activityFeed** element.</span></span> 
    
- <span data-ttu-id="5bc8c-109">.osc プロバイダーは、 **activitydetails**要素の子要素である**ownerID**要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-109">The OSC provider must set the **ownerID** element, which is a child element of the **activityDetails** element.</span></span> <span data-ttu-id="5bc8c-110">**ownerID**は、ソーシャルネットワーク上のアクティビティの所有者を識別する非透過文字列です。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-110">**ownerID** is an opaque string that identifies the owner of the activity on the social network.</span></span> 
    
- <span data-ttu-id="5bc8c-111">.osc プロバイダーは、 **templateVariables**要素の**publisherVariable**ノードで**namehint**および**emailAddress**要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-111">The OSC provider should set the **nameHint** and **emailAddress** elements in the **publisherVariable** node of the **templateVariables** element.</span></span> 
    
   <span data-ttu-id="5bc8c-112">.osc プロバイダーの XML スキーマの場合、 **namehint**要素は省略可能な要素であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-112">Note that per the OSC provider XML schema, the **nameHint** element is an optional element.</span></span> <span data-ttu-id="5bc8c-113">.osc は、これを使用して、連絡先カードまたは [ユーザー] ウィンドウで選択したユーザーの表示名と照合します。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-113">The OSC uses it to match the display name of the user selected in the Contact Card or People Pane.</span></span> <span data-ttu-id="5bc8c-114">同様に、 **emailAddress**要素は、XML スキーマの省略可能な要素です。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-114">Similarly, the **emailAddress** element is an optional element in the XML schema.</span></span> <span data-ttu-id="5bc8c-115">.osc は、連絡先カードまたはユーザーウィンドウで選択したユーザーの SMTP アドレスと一致するように使用します。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-115">The OSC uses it to match the SMTP address of the user selected in the Contact Card or People Pane.</span></span> 
    
   <span data-ttu-id="5bc8c-116">**ownerID**要素のみが指定されていて、 **namehint**と**emailAddress**の一方または両方が指定されていない場合、.osc は[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドを呼び出した後、 [i alperson:: getdetails](isocialperson-getdetails.md)を呼び出します。メソッドを使って、 **ownerID**によって識別される個人に関する詳細情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-116">If only the **ownerID** element is specified, but one or both of **nameHint** and **emailAddress** are not specified, the OSC calls the [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) method and then the [ISocialPerson::GetDetails](isocialperson-getdetails.md) method to get more information about the person identified by the **ownerID**.</span></span> <span data-ttu-id="5bc8c-117">.osc が iemailAddress **alperson:: getdetails**を呼び出した場合、プロバイダーは**fullName**要素と\*\*\*\* 要素を指定する**person** XML を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc8c-117">When the OSC calls **ISocialPerson::GetDetails**, the provider must return **person** XML that specifies the **fullName** and **emailAddress** elements.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5bc8c-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bc8c-118">See also</span></span>

- [<span data-ttu-id="5bc8c-119">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="5bc8c-119">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="5bc8c-120">Friends の XML</span><span class="sxs-lookup"><span data-stu-id="5bc8c-120">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="5bc8c-121">機能の XML</span><span class="sxs-lookup"><span data-stu-id="5bc8c-121">XML for Capabilities</span></span>](xml-for-capabilities.md)

