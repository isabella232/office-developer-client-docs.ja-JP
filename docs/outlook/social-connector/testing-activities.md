---
title: アクティビティをテストします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: テストおよび以外の友人や友人の活動を適切に取得するのには Outlook ソーシャル コネクタ (OSC) プロバイダーがオンデマンドの同期を使用することを確認するシナリオについて説明します。
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804466"
---
# <a name="testing-activities"></a><span data-ttu-id="81b46-103">アクティビティをテストします。</span><span class="sxs-lookup"><span data-stu-id="81b46-103">Testing activities</span></span>

<span data-ttu-id="81b46-104">テストおよび以外の友人や友人の活動を適切に取得するのには Outlook ソーシャル コネクタ (OSC) プロバイダーがオンデマンドの同期を使用することを確認するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="81b46-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider uses on-demand synchronization to appropriately return activities of friends and non-friends.</span></span>

<span data-ttu-id="81b46-105"><a name="olosc_TestingActivities_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="81b46-105"></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="81b46-106">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="81b46-106">On-demand synchronization</span></span>

<span data-ttu-id="81b46-107">OSC プロバイダーは、 **ISocialProvider::GetCapabilities**、プロバイダー以外の友人や友人の活動のオン ・ デマンドの同期をサポートしているかどうかを決定する、OSC を実装します。</span><span class="sxs-lookup"><span data-stu-id="81b46-107">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of activities of friends and non-friends.</span></span> <span data-ttu-id="81b46-108">Outlook 人物情報ウィンドウに表示されている方のため、OSC を取得、これらの方のために返されるハッシュの SMTP アドレスを[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出して、(メモリ内) のアクティビティ データを格納します。</span><span class="sxs-lookup"><span data-stu-id="81b46-108">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md), and stores (in memory) the activities data returned for these persons.</span></span> 
  
### <a name="determining-activities-to-get"></a><span data-ttu-id="81b46-109">取得するアクティビティを決定します。</span><span class="sxs-lookup"><span data-stu-id="81b46-109">Determining activities to get</span></span>

<span data-ttu-id="81b46-110">ハッシュされた SMTP アドレスが**GetActivitiesEx**に渡されますが、OSC が友人の友人ではない活動を取得するかどうかを判断するキーです。</span><span class="sxs-lookup"><span data-stu-id="81b46-110">The hashed SMTP addresses passed to **GetActivitiesEx** are the key to determining whether the OSC will get activities for a friend or non-friend.</span></span> <span data-ttu-id="81b46-111">OSC では、人が自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定する場合に、人の活動を取得します。</span><span class="sxs-lookup"><span data-stu-id="81b46-111">The OSC gets activities for a person if the person specifies that SMTP address in his or her social network account.</span></span> <span data-ttu-id="81b46-112">人には、自分のソーシャル ネットワーク アカウントでその SMTP アドレスは含まれませんか、 **GetActivitiesEx**がその人の活動を取得しませんその人が友人である場合は、ソーシャル ネットワーク上の別の電子メール アドレスで。</span><span class="sxs-lookup"><span data-stu-id="81b46-112">If the person does not include that SMTP address in his or her social network account, or if that person is a friend but by a different email address on the social network, **GetActivitiesEx** does not get activities for that person.</span></span> <span data-ttu-id="81b46-113">また、フレンドではありませんが、自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定したユーザーでは、返されたデータが含まれています以外の友人にその人のプライバシーの設定で許可された使用可能なのみです。</span><span class="sxs-lookup"><span data-stu-id="81b46-113">Also, for a person who is not a friend but specifies the SMTP addresses in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="81b46-114">友人と友人ではないテストの情報カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="81b46-114">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="81b46-115">友人のテストの対象を作成するには、自分のソーシャル ネットワーク アカウントでそのアドレスを含むユーザーと、そのネットワークにログオン中のユーザーとフレンドのステータスを持つユーザーの SMTP アドレスを識別します。</span><span class="sxs-lookup"><span data-stu-id="81b46-115">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="81b46-116">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="81b46-116">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="81b46-117">同様に、以外の友人のテストの対象を作成するには、ユーザーはそのアドレスでユーザーのログオンのフレンドではありませんし、ソーシャル ネットワーク上のプロファイルを表示するのにはフレンド以外を使用するのには自分のプライバシーの設定で指定したユーザーの SMTP アドレスを識別します。</span><span class="sxs-lookup"><span data-stu-id="81b46-117">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and who has specified in his or her privacy settings to allow non-friends to view their profile on the social network.</span></span> <span data-ttu-id="81b46-118">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="81b46-118">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="81b46-119">Outlook エクスプ ローラーで、友人 (または友人ではない) を含む電子メール メッセージを選択すると、人物情報ウィンドウは、受信者を表示します。</span><span class="sxs-lookup"><span data-stu-id="81b46-119">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="81b46-120">人物情報ウィンドウで、友人、友人ではない) を選択すると、テストするのにはプロバイダーが個人情報を提供することできます。</span><span class="sxs-lookup"><span data-stu-id="81b46-120">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="81b46-121">シナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="81b46-121">Test scenarios</span></span>

<span data-ttu-id="81b46-122">友人と友人ではない適切な活動が発生していることを確認するには、次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="81b46-122">To verify that you are getting appropriate activities for friends and non-friends, test for the following scenarios.</span></span>
  
|<span data-ttu-id="81b46-123">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="81b46-123">**Scenario**</span></span>|<span data-ttu-id="81b46-124">**予想される動作**</span><span class="sxs-lookup"><span data-stu-id="81b46-124">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81b46-125">人物情報ウィンドウで選択したユーザーは、ソーシャル ネットワークにログオン中のユーザーのフレンドです。</span><span class="sxs-lookup"><span data-stu-id="81b46-125">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="81b46-126">人物情報ウィンドウには、そのユーザーのプロファイルとソーシャル ネットワークに投稿すると、プロフィールの画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="81b46-126">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
|<span data-ttu-id="81b46-127">人物情報ウィンドウで選択されている人は、ソーシャル ネットワークにログオン中のユーザーの非友人が、友人で非表示に自分のプロファイルを許可するには。</span><span class="sxs-lookup"><span data-stu-id="81b46-127">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her profile to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="81b46-128">人物情報ウィンドウには、そのユーザーのプロファイルとソーシャル ネットワークに投稿すると、プロフィールの画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="81b46-128">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81b46-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="81b46-129">See also</span></span>

- [<span data-ttu-id="81b46-130">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="81b46-130">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="81b46-131">活動の XML</span><span class="sxs-lookup"><span data-stu-id="81b46-131">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="81b46-132">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="81b46-132">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

