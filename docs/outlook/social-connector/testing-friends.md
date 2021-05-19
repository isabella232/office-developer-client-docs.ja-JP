---
title: 友だちのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のデータを適切に返すのを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433669"
---
# <a name="testing-friends"></a><span data-ttu-id="3d63a-103">友だちのテスト</span><span class="sxs-lookup"><span data-stu-id="3d63a-103">Testing friends</span></span>

<span data-ttu-id="3d63a-104">このトピックでは、Outlook Social Connector (OSC) プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のデータを適切に返すのを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode supported by the provider.</span></span>

<span data-ttu-id="3d63a-105"><a name="olosc_TestingFriends_CachedSync"> </a></span><span class="sxs-lookup"><span data-stu-id="3d63a-105"><a name="olosc_TestingFriends_CachedSync"> </a></span></span>

## <a name="cached-synchronization"></a><span data-ttu-id="3d63a-106">キャッシュされた同期</span><span class="sxs-lookup"><span data-stu-id="3d63a-106">Cached synchronization</span></span>

<span data-ttu-id="3d63a-107">OSC プロバイダーは [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)を実装します。これは、プロバイダーが友人のデータのキャッシュ同期をサポートするかどうかを判断するために OSC が呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-107">An OSC provider implements [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), which the OSC calls to determine whether the provider supports cached synchronization of friends' data.</span></span> <span data-ttu-id="3d63a-108">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出した後、OSC は、返されたフレンドのデータを、ログオンしているユーザーの既定の Outlook ストアのソーシャル ネットワークに固有の連絡先フォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-108">After calling [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), the OSC stores the returned friends' data in a contacts folder specific to the social network in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="3d63a-109">また、OSC は [ISocialSession::GetPerson](isocialsession-getperson.md) と [ISocialPerson::GetPicture](isocialperson-getpicture.md) を呼び出して、各フレンドのプロファイル画像を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-109">The OSC also calls [ISocialSession::GetPerson](isocialsession-getperson.md) and [ISocialPerson::GetPicture](isocialperson-getpicture.md) to obtain a profile picture for each friend.</span></span> 
  
### <a name="initiate-synchronization"></a><span data-ttu-id="3d63a-110">同期の開始</span><span class="sxs-lookup"><span data-stu-id="3d63a-110">Initiate synchronization</span></span>

<span data-ttu-id="3d63a-111">同期を開始するには、Fluent ユーザー インターフェイスのリボンコンポーネントでデバッグ ボタン [連絡先の同期] をオンMicrosoft Office使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-111">To initiate synchronization, you can turn on and use the debug button **Sync Contacts** in the ribbon component of the Microsoft Office Fluent user interface.</span></span> <span data-ttu-id="3d63a-112">OSC デバッグ ボタンの詳細については [、「Debuging a Provider 」を参照してください](debugging-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3d63a-112">For more information about OSC debug buttons, see [Debugging a Provider](debugging-a-provider.md).</span></span> 
  
### <a name="test-scenarios"></a><span data-ttu-id="3d63a-113">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="3d63a-113">Test scenarios</span></span>

<span data-ttu-id="3d63a-114">次の項目をテストして、フレンドのデータが正しくキャッシュされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-114">Test the following items to verify that friends' data is cached correctly.</span></span>
  
|<span data-ttu-id="3d63a-115">**テストするアイテム**</span><span class="sxs-lookup"><span data-stu-id="3d63a-115">**Item to test**</span></span>|<span data-ttu-id="3d63a-116">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="3d63a-116">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d63a-117">連絡先フォルダー</span><span class="sxs-lookup"><span data-stu-id="3d63a-117">Contacts folder</span></span>  <br/> |<span data-ttu-id="3d63a-118">ソーシャル ネットワーク固有の連絡先フォルダーは、ユーザーの既定の連絡先ストアにOutlookされます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-118">The social network-specific contacts folder exists in the user's default Outlook store.</span></span>  <br/> |
|<span data-ttu-id="3d63a-119">ISocialPerson によって返されるフレンドのデータ **::GetFriendsAndColleagues**</span><span class="sxs-lookup"><span data-stu-id="3d63a-119">Friends' data returned by **ISocialPerson::GetFriendsAndColleagues**</span></span> <br/> |<span data-ttu-id="3d63a-120">各フレンドは、ネットワーク固有の連絡先フォルダー内の連絡先に対応します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-120">Each friend corresponds to a contact in the network-specific contacts folder.</span></span>  <br/> |
|<span data-ttu-id="3d63a-121">フレンドのデータ</span><span class="sxs-lookup"><span data-stu-id="3d63a-121">Friends' data</span></span>  <br/> |<span data-ttu-id="3d63a-122">各フレンドの連絡先フィールドに正しいデータがあります。</span><span class="sxs-lookup"><span data-stu-id="3d63a-122">Contact fields for each friend have the correct data.</span></span>  <br/> |
|<span data-ttu-id="3d63a-123">ISocialPerson によって返されるフレンドのプロフィール **写真::GetPicture**</span><span class="sxs-lookup"><span data-stu-id="3d63a-123">Friends' profile pictures returned by **ISocialPerson::GetPicture**</span></span> <br/> |<span data-ttu-id="3d63a-124">各フレンドの連絡先アイテムには、プロファイル画像が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3d63a-124">The contact item for each friend contains the profile picture.</span></span>  <br/> |

<span data-ttu-id="3d63a-125"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="3d63a-125"><a name="olosc_TestingFriends_OnDemandSync"> </a></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="3d63a-126">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="3d63a-126">On-demand synchronization</span></span>

<span data-ttu-id="3d63a-127">OSC プロバイダーは **ISocialProvider::GetCapabilities** を実装します。これは、プロバイダーが友人と友人以外のオンデマンド同期をサポートするかどうかを判断するために OSC が呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-127">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of friends and non-friends.</span></span> <span data-ttu-id="3d63a-128">Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし[、ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、これらのユーザーに返されるデータを (メモリ内に) 格納します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-128">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), and stores (in memory) the data returned for these persons.</span></span> 
  
### <a name="determining-friends-and-non-friends"></a><span data-ttu-id="3d63a-129">フレンドと非フレンドを決定する</span><span class="sxs-lookup"><span data-stu-id="3d63a-129">Determining friends and non-friends</span></span>

<span data-ttu-id="3d63a-130">**GetPeopleDetails** に渡されるハッシュ化された SMTP アドレスは、人が友人か非友人かを判断するキーです。</span><span class="sxs-lookup"><span data-stu-id="3d63a-130">The hashed SMTP addresses passed to **GetPeopleDetails** are the key to determining whether a person is a friend or non-friend.</span></span> <span data-ttu-id="3d63a-131">ユーザーが自分のソーシャル ネットワーク アカウントに SMTP アドレスを含めない場合、またはそのユーザーがソーシャル ネットワーク上の別の電子メール アドレスの友人である場合でも **、GetPeopleDetails** は _personsCollection_ パラメーターの **friendStatus** としてそのユーザーの非フレンドを返します。 </span><span class="sxs-lookup"><span data-stu-id="3d63a-131">If a person does not include that SMTP address in his or her social network account, or even if that person is a friend by a different email address on the social network, **GetPeopleDetails** still returns **nonfriend** for that person as the **friendStatus** in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="3d63a-132">また、友人ではないが、自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定している人の場合、返されるデータには、そのユーザーのプライバシー設定で許可されているフレンド以外のユーザーが使用できるデータだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-132">Also, for a person who is not a friend but specifies the SMTP address in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="3d63a-133">友人や友人以外のテスト 対象を作成する</span><span class="sxs-lookup"><span data-stu-id="3d63a-133">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="3d63a-134">フレンドのテスト 対象を作成するには、そのアドレスを自分のソーシャル ネットワーク アカウントに含め、そのネットワーク上のログオンユーザーとのフレンドステータスを持つユーザーの SMTP アドレスを特定します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-134">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="3d63a-135">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-135">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="3d63a-136">同様に、フレンド以外のテスト 対象を作成するには、ログオンしているユーザーの友人ではないユーザーの SMTP アドレスをそのアドレスで特定し、まだ友人以外のユーザーがソーシャル ネットワーク上で自分のアクティビティを表示するためのプライバシー設定を指定しているユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-136">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and yet who has specified in his or her privacy settings to allow non-friends to view their activities on the social network.</span></span> <span data-ttu-id="3d63a-137">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-137">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="3d63a-138">ユーザー エクスプローラー Outlook、友人 (または非フレンド) を含む電子メール メッセージを選択すると、受信者が [ユーザー ウィンドウ] に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-138">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="3d63a-139">[ユーザー] ウィンドウでフレンド (またはフレンド以外) を選択すると、プロバイダーがユーザーに関する情報を提供しているのをテストできます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-139">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="3d63a-140">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="3d63a-140">Test scenarios</span></span>

<span data-ttu-id="3d63a-141">プロバイダーが友人や友人以外の情報を適切に提供しているか確認するには、次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="3d63a-141">To verify that your provider is providing information about friends and non-friends appropriately, test for the following scenarios.</span></span>
  
|<span data-ttu-id="3d63a-142">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="3d63a-142">**Scenario**</span></span>|<span data-ttu-id="3d63a-143">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="3d63a-143">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d63a-144">[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンユーザーとのフレンドです。</span><span class="sxs-lookup"><span data-stu-id="3d63a-144">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="3d63a-145">[ユーザー] ウィンドウには、そのユーザーのソーシャル ネットワーク上のアクティビティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-145">The People Pane displays that person's activities on the social network.</span></span>  <br/> |
|<span data-ttu-id="3d63a-146">[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンしているユーザーの非フレンドですが、自分のアクティビティを友人以外のユーザーが表示できます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-146">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her activities to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="3d63a-147">[ユーザー] ウィンドウには、そのユーザーのソーシャル ネットワーク上のアクティビティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d63a-147">The People Pane displays that person's activities on the social network.</span></span>  <br/> |

<span data-ttu-id="3d63a-148"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="3d63a-148"><a name="olosc_TestingFriends_OnDemandSync"> </a></span></span>

## <a name="hybrid-synchronization"></a><span data-ttu-id="3d63a-149">ハイブリッド同期</span><span class="sxs-lookup"><span data-stu-id="3d63a-149">Hybrid synchronization</span></span>

<span data-ttu-id="3d63a-150">OSC プロバイダーが友人と友人以外のハイブリッド同期をサポートしている場合、OSC は次の処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-150">If an OSC provider supports hybrid synchronization of friends and non-friends, the OSC does the following:</span></span> 
  
- <span data-ttu-id="3d63a-151">OSC は、ログオンしているユーザーの友人の情報をソーシャル ネットワーク固有の連絡先フォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="3d63a-151">The OSC stores information for friends of the logged-on user in the social network-specific contact folder.</span></span>
    
- <span data-ttu-id="3d63a-152">OSC は、フレンド以外のオンデマンドの情報をソーシャル ネットワークから取得し、メモリにのみ格納しますが、フォルダーには格納できません。</span><span class="sxs-lookup"><span data-stu-id="3d63a-152">The OSC retrieves information for non-friends on-demand from the social network, and stores it only in memory, but not in a folder.</span></span>
    
<span data-ttu-id="3d63a-153">ハイブリッド同期をテストするには、友人の [キャッシュされた[](#olosc_TestingFriends_CachedSync)同期] セクションのテストの提案に従い[](#olosc_TestingFriends_OnDemandSync)、友人以外の場合は [オンデマンド同期] セクションのテストの提案に従います。</span><span class="sxs-lookup"><span data-stu-id="3d63a-153">To test hybrid synchronization, follow the testing suggestions in the [Cached Synchronization](#olosc_TestingFriends_CachedSync) section for friends, and those in the [On-Demand Synchronization](#olosc_TestingFriends_OnDemandSync) section for non-friends.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d63a-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d63a-154">See also</span></span>

- [<span data-ttu-id="3d63a-155">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="3d63a-155">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="3d63a-156">友人のための XML</span><span class="sxs-lookup"><span data-stu-id="3d63a-156">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="3d63a-157">OSC プロバイダーをリリースする準備</span><span class="sxs-lookup"><span data-stu-id="3d63a-157">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

