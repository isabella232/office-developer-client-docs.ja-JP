---
title: アクティビティのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーがオンデマンド同期を使用して友人や友人以外のアクティビティを適切に返すのを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436301"
---
# <a name="testing-activities"></a><span data-ttu-id="2475b-103">アクティビティのテスト</span><span class="sxs-lookup"><span data-stu-id="2475b-103">Testing activities</span></span>

<span data-ttu-id="2475b-104">このトピックでは、Outlook Social Connector (OSC) プロバイダーがオンデマンド同期を使用して友人や友人以外のアクティビティを適切に返すのを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2475b-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider uses on-demand synchronization to appropriately return activities of friends and non-friends.</span></span>

<span data-ttu-id="2475b-105"><a name="olosc_TestingActivities_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="2475b-105"><a name="olosc_TestingActivities_OnDemandSync"> </a></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="2475b-106">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="2475b-106">On-demand synchronization</span></span>

<span data-ttu-id="2475b-107">OSC プロバイダーは **、ISocialProvider::GetCapabilities** を実装します。これは、プロバイダーが友人や友人以外のアクティビティのオンデマンド同期をサポートするかどうかを判断するために OSC が呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2475b-107">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of activities of friends and non-friends.</span></span> <span data-ttu-id="2475b-108">Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし[、ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出し、これらのユーザーに返されるアクティビティ データを (メモリ内に) 格納します。</span><span class="sxs-lookup"><span data-stu-id="2475b-108">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md), and stores (in memory) the activities data returned for these persons.</span></span> 
  
### <a name="determining-activities-to-get"></a><span data-ttu-id="2475b-109">取得するアクティビティの決定</span><span class="sxs-lookup"><span data-stu-id="2475b-109">Determining activities to get</span></span>

<span data-ttu-id="2475b-110">**GetActivitiesEx** に渡されるハッシュ化された SMTP アドレスは、OSC がフレンドまたは非フレンドのアクティビティを取得するかどうかを決定するキーです。</span><span class="sxs-lookup"><span data-stu-id="2475b-110">The hashed SMTP addresses passed to **GetActivitiesEx** are the key to determining whether the OSC will get activities for a friend or non-friend.</span></span> <span data-ttu-id="2475b-111">ユーザーが自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定した場合、OSC はユーザーのアクティビティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2475b-111">The OSC gets activities for a person if the person specifies that SMTP address in his or her social network account.</span></span> <span data-ttu-id="2475b-112">そのユーザーが自分のソーシャル ネットワーク アカウントに SMTP アドレスを含めない場合、またはそのユーザーが友人で、ソーシャル ネットワーク上の別の電子メール アドレスである場合 **、GetActivitiesEx** は、そのユーザーのアクティビティを取得できません。</span><span class="sxs-lookup"><span data-stu-id="2475b-112">If the person does not include that SMTP address in his or her social network account, or if that person is a friend but by a different email address on the social network, **GetActivitiesEx** does not get activities for that person.</span></span> <span data-ttu-id="2475b-113">また、友人ではないが、自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定している人の場合、返されるデータには、そのユーザーのプライバシー設定で許可されているフレンド以外のユーザーが使用できるデータだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2475b-113">Also, for a person who is not a friend but specifies the SMTP addresses in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="2475b-114">友人や友人以外のテスト 対象を作成する</span><span class="sxs-lookup"><span data-stu-id="2475b-114">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="2475b-115">フレンドのテスト 対象を作成するには、そのアドレスを自分のソーシャル ネットワーク アカウントに含め、そのネットワーク上のログオンユーザーとのフレンドステータスを持つユーザーの SMTP アドレスを特定します。</span><span class="sxs-lookup"><span data-stu-id="2475b-115">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="2475b-116">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="2475b-116">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="2475b-117">同様に、フレンド以外のテスト 対象を作成するには、そのアドレスでログオンしているユーザーの友人ではないユーザーの SMTP アドレスを特定し、友人以外のユーザーがソーシャル ネットワーク上で自分のプロファイルを表示するためのプライバシー設定で指定したユーザーの SMTP アドレスを特定します。</span><span class="sxs-lookup"><span data-stu-id="2475b-117">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and who has specified in his or her privacy settings to allow non-friends to view their profile on the social network.</span></span> <span data-ttu-id="2475b-118">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="2475b-118">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="2475b-119">ユーザー エクスプローラー Outlook、友人 (または非フレンド) を含む電子メール メッセージを選択すると、受信者が [ユーザー ウィンドウ] に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2475b-119">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="2475b-120">[ユーザー] ウィンドウでフレンド (またはフレンド以外) を選択すると、プロバイダーがユーザーに関する情報を提供しているのをテストできます。</span><span class="sxs-lookup"><span data-stu-id="2475b-120">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="2475b-121">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="2475b-121">Test scenarios</span></span>

<span data-ttu-id="2475b-122">友人や友人以外のユーザーに適切なアクティビティを取得しているか確認するには、次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="2475b-122">To verify that you are getting appropriate activities for friends and non-friends, test for the following scenarios.</span></span>
  
|<span data-ttu-id="2475b-123">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="2475b-123">**Scenario**</span></span>|<span data-ttu-id="2475b-124">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="2475b-124">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2475b-125">[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンユーザーとのフレンドです。</span><span class="sxs-lookup"><span data-stu-id="2475b-125">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="2475b-126">[ユーザー] ウィンドウには、ソーシャル ネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2475b-126">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
|<span data-ttu-id="2475b-127">[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンしているユーザーの非フレンドですが、自分のプロファイルを友人以外のユーザーが表示できます。</span><span class="sxs-lookup"><span data-stu-id="2475b-127">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her profile to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="2475b-128">[ユーザー] ウィンドウには、ソーシャル ネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2475b-128">The People Pane displays that person's profile and profile picture as posted on the social network.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2475b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2475b-129">See also</span></span>

- [<span data-ttu-id="2475b-130">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="2475b-130">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="2475b-131">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="2475b-131">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="2475b-132">OSC プロバイダーをリリースする準備</span><span class="sxs-lookup"><span data-stu-id="2475b-132">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

