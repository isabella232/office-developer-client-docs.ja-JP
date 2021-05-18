---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlookソーシャル コネクタ (OSC) プロバイダーは、getActivities 要素と dynamicActivitiesLookupEx 要素を設定して、OSC にアクティビティ アイテムをメモリに格納できます。
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422916"
---
# <a name="guidelines-for-properly-displaying-activities"></a><span data-ttu-id="e4b9b-103">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="e4b9b-103">Guidelines for properly displaying activities</span></span>

<span data-ttu-id="e4b9b-104">Outlookソーシャル コネクタ (OSC) プロバイダーは **、getActivities** 要素と **dynamicActivitiesLookupEx** 要素を設定して、OSC にアクティビティ アイテムをメモリに格納できます。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-104">Outlook Social Connector (OSC) providers can set the **getActivities** and **dynamicActivitiesLookupEx** elements to have the OSC store activity items in memory.</span></span> <span data-ttu-id="e4b9b-105">このトピックでは、OSC プロバイダーがソーシャル ネットワークからのアクティビティ フィードの同期をサポートしている場合に、OSC がアクティビティとアクティビティ所有者の詳細を取得または更新するために呼び出す OSC プロバイダー拡張 API について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-105">This topic describes the OSC provider extensibility APIs that the OSC calls to get or refresh activities and activity owner details, if the OSC provider supports synchronizing activity feeds from the social network.</span></span> <span data-ttu-id="e4b9b-106">また、OSC プロバイダーが Office 連絡先カードまたは Outlook People Pane でアクティビティを適切に表示するために OSC プロバイダーが設定する **activityFeed** 要素のいくつかの子要素も一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-106">The topic also lists a few child elements of the **activityFeed** element that the OSC provider should set for the OSC to display activities properly in the Office Contact Card or Outlook People Pane.</span></span> 
  
- <span data-ttu-id="e4b9b-107">OSC は [、ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) メソッドを呼び出して、ログオンしているユーザーのニュース フィード フォルダーにアクティビティを取得して保存します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-107">The OSC calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method to get and store activities in the News Feed folder for the logged-on user.</span></span> <span data-ttu-id="e4b9b-108">OSC プロバイダーは **GetActivitiesEx** を実装して **、activityFeed** 要素の OSC プロバイダー XML スキーマ定義に準拠するアクティビティ XML 文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-108">The OSC provider must implement **GetActivitiesEx** to return an  _activities_ XML string that complies with the OSC provider XML schema definition of the **activityFeed** element.</span></span> 
    
- <span data-ttu-id="e4b9b-109">OSC プロバイダーは **、activityDetails** 要素の子要素である **ownerID** 要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-109">The OSC provider must set the **ownerID** element, which is a child element of the **activityDetails** element.</span></span> <span data-ttu-id="e4b9b-110">**ownerID** は、ソーシャル ネットワーク上のアクティビティの所有者を識別する不透明な文字列です。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-110">**ownerID** is an opaque string that identifies the owner of the activity on the social network.</span></span> 
    
- <span data-ttu-id="e4b9b-111">OSC プロバイダーは **、templateVariables** 要素の **publisherVariable** ノードで nameHint 要素と **emailAddress** 要素 **を設定する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-111">The OSC provider should set the **nameHint** and **emailAddress** elements in the **publisherVariable** node of the **templateVariables** element.</span></span> 
    
   <span data-ttu-id="e4b9b-112">OSC プロバイダー XML スキーマごとに **、nameHint** 要素は省略可能な要素です。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-112">Note that per the OSC provider XML schema, the **nameHint** element is an optional element.</span></span> <span data-ttu-id="e4b9b-113">OSC は、連絡先カードまたはユーザー ウィンドウで選択したユーザーの表示名と一致するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-113">The OSC uses it to match the display name of the user selected in the Contact Card or People Pane.</span></span> <span data-ttu-id="e4b9b-114">同様に **、emailAddress** 要素は XML スキーマの省略可能な要素です。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-114">Similarly, the **emailAddress** element is an optional element in the XML schema.</span></span> <span data-ttu-id="e4b9b-115">OSC は、連絡先カードまたはユーザー ウィンドウで選択したユーザーの SMTP アドレスと一致するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-115">The OSC uses it to match the SMTP address of the user selected in the Contact Card or People Pane.</span></span> 
    
   <span data-ttu-id="e4b9b-116">ownerID要素のみを指定したが **、nameHint** と **emailAddress** の一方または両方が指定されていない場合、OSC は [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドを呼び出し、次に [ISocialPerson::GetDetails](isocialperson-getdetails.md)メソッドを呼び出して **、ownerID** で識別された人物に関する詳細な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-116">If only the **ownerID** element is specified, but one or both of **nameHint** and **emailAddress** are not specified, the OSC calls the [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) method and then the [ISocialPerson::GetDetails](isocialperson-getdetails.md) method to get more information about the person identified by the **ownerID**.</span></span> <span data-ttu-id="e4b9b-117">OSC が **ISocialPerson::GetDetails** を呼び出す場合、プロバイダーは **fullName** 要素と **emailAddress** 要素を指定するユーザー **XML** を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9b-117">When the OSC calls **ISocialPerson::GetDetails**, the provider must return **person** XML that specifies the **fullName** and **emailAddress** elements.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4b9b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4b9b-118">See also</span></span>

- [<span data-ttu-id="e4b9b-119">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="e4b9b-119">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="e4b9b-120">友人のための XML</span><span class="sxs-lookup"><span data-stu-id="e4b9b-120">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="e4b9b-121">機能の XML</span><span class="sxs-lookup"><span data-stu-id="e4b9b-121">XML for Capabilities</span></span>](xml-for-capabilities.md)

