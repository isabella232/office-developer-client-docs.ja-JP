---
title: アクティビティのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーが、オンデマンド同期を使用して友人や非友人の活動を適切に返すことを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329205"
---
# <a name="testing-activities"></a><span data-ttu-id="c1ffc-103">アクティビティのテスト</span><span class="sxs-lookup"><span data-stu-id="c1ffc-103">Testing activities</span></span>

<span data-ttu-id="c1ffc-104">このトピックでは、Outlook Social Connector (.osc) プロバイダーが、オンデマンド同期を使用して友人や非友人の活動を適切に返すことを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider uses on-demand synchronization to appropriately return activities of friends and non-friends.</span></span>

<span data-ttu-id="c1ffc-105"><a name="olosc_TestingActivities_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="c1ffc-105"></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="c1ffc-106">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="c1ffc-106">On-demand synchronization</span></span>

<span data-ttu-id="c1ffc-107">.osc プロバイダーは、 **isocialprovider:: getcapabilities**を実装します。この関数は、プロバイダーが友人および非友人のアクティビティのオンデマンド同期をサポートしているかどうかを判断するために、.osc を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-107">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of activities of friends and non-friends.</span></span> <span data-ttu-id="c1ffc-108">[Outlook People] ウィンドウに表示される人物については、.osc は SMTP アドレスを取得してハッシュし、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出します。また、これらのユーザーに対して返されるアクティビティデータをメモリ内に格納します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-108">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md), and stores (in memory) the activities data returned for these persons.</span></span> 
  
### <a name="determining-activities-to-get"></a><span data-ttu-id="c1ffc-109">取得するアクティビティの決定</span><span class="sxs-lookup"><span data-stu-id="c1ffc-109">Determining activities to get</span></span>

<span data-ttu-id="c1ffc-110">**GetActivitiesEx**に渡されるハッシュされた SMTP アドレスは、.osc がフレンドまたはフレンド以外のアクティビティを取得するかどうかを判断するための鍵となります。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-110">The hashed SMTP addresses passed to **GetActivitiesEx** are the key to determining whether the OSC will get activities for a friend or non-friend.</span></span> <span data-ttu-id="c1ffc-111">.osc は、ユーザーがソーシャルネットワークアカウントでその SMTP アドレスを指定した場合に、そのユーザーのアクティビティを取得します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-111">The OSC gets activities for a person if the person specifies that SMTP address in his or her social network account.</span></span> <span data-ttu-id="c1ffc-112">その SMTP アドレスが自分のソーシャルネットワークアカウントに含まれていない場合、またはそのユーザーがソーシャルネットワーク上の他の電子メールアドレスで友人である場合、 **GetActivitiesEx**はその人物のアクティビティを取得しません。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-112">If the person does not include that SMTP address in his or her social network account, or if that person is a friend but by a different email address on the social network, **GetActivitiesEx** does not get activities for that person.</span></span> <span data-ttu-id="c1ffc-113">また、友人以外のユーザーがソーシャルネットワークアカウントの SMTP アドレスを指定している場合、返されるデータには、そのユーザーのプライバシー設定によって許可されている場合に、フレンド以外に対して使用可能なもののみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-113">Also, for a person who is not a friend but specifies the SMTP addresses in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="c1ffc-114">友人および非友人のテスト対象を作成する</span><span class="sxs-lookup"><span data-stu-id="c1ffc-114">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="c1ffc-115">友人のテスト件名を作成するには、そのアドレスをソーシャルネットワークアカウントに含めるユーザーの SMTP アドレスを識別し、そのネットワークでログオンしているユーザーのフレンド状態を持っているユーザーを特定します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-115">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="c1ffc-116">その SMTP アドレスを含む電子メールメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-116">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="c1ffc-117">同様に、フレンド以外のテスト件名を作成するには、そのアドレスによってログオンしているユーザーのフレンドではないユーザーの SMTP アドレスを識別し、自分のプライバシー設定で指定したユーザーがソーシャルネットワークで自分のプロファイルを表示できないようにします。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-117">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and who has specified in his or her privacy settings to allow non-friends to view their profile on the social network.</span></span> <span data-ttu-id="c1ffc-118">その SMTP アドレスを含む電子メールメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-118">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="c1ffc-119">Outlook エクスプローラーで、友達 (または友人以外) を含む電子メールメッセージを選択すると、[人] ウィンドウに受信者が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-119">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="c1ffc-120">[人] ウィンドウで友人 (または友人以外) を選択すると、プロバイダーがその人物に関する情報を提供しているかどうかをテストできます。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-120">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="c1ffc-121">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="c1ffc-121">Test scenarios</span></span>

<span data-ttu-id="c1ffc-122">友人や友人以外の適切な活動を取得していることを確認するには、次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-122">To verify that you are getting appropriate activities for friends and non-friends, test for the following scenarios.</span></span>
  
|<span data-ttu-id="c1ffc-123">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="c1ffc-123">**Scenario**</span></span>|<span data-ttu-id="c1ffc-124">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="c1ffc-124">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1ffc-125">[人] ウィンドウで選択されたユーザーは、ソーシャルネットワーク上でログオンしているユーザーと友人になります。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-125">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="c1ffc-126">[人] ウィンドウには、ソーシャルネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-126">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
|<span data-ttu-id="c1ffc-127">People ウィンドウで選択されたユーザーは、ソーシャルネットワーク上のログオンしているユーザーのフレンドではありませんが、自分のプロファイルを友人以外に表示することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-127">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her profile to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="c1ffc-128">[人] ウィンドウには、ソーシャルネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1ffc-128">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1ffc-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1ffc-129">See also</span></span>

- [<span data-ttu-id="c1ffc-130">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="c1ffc-130">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="c1ffc-131">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="c1ffc-131">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="c1ffc-132">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="c1ffc-132">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

