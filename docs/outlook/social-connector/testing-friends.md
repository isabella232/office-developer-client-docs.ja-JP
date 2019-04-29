---
title: 友だちのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、プロバイダーがサポートする同期モードに応じて、Outlook Social Connector (.osc) プロバイダーが友人および友人以外のデータを適切に返すことを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433669"
---
# <a name="testing-friends"></a><span data-ttu-id="855de-103">友だちのテスト</span><span class="sxs-lookup"><span data-stu-id="855de-103">Testing friends</span></span>

<span data-ttu-id="855de-104">このトピックでは、プロバイダーがサポートする同期モードに応じて、Outlook Social Connector (.osc) プロバイダーが友人および友人以外のデータを適切に返すことを確認するテストとシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="855de-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode supported by the provider.</span></span>

<span data-ttu-id="855de-105"><a name="olosc_TestingFriends_CachedSync"> </a></span><span class="sxs-lookup"><span data-stu-id="855de-105"></span></span>

## <a name="cached-synchronization"></a><span data-ttu-id="855de-106">キャッシュされた同期</span><span class="sxs-lookup"><span data-stu-id="855de-106">Cached synchronization</span></span>

<span data-ttu-id="855de-107">.osc プロバイダーは、 [isocialprovider:: getcapabilities](isocialprovider-getcapabilities.md)を実装します。この関数は、プロバイダーがフレンドのデータのキャッシュ同期をサポートしているかどうかを判断するために、.osc 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="855de-107">An OSC provider implements [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), which the OSC calls to determine whether the provider supports cached synchronization of friends' data.</span></span> <span data-ttu-id="855de-108">[iGetFriendsAndColleagues alperson::](isocialperson-getfriendsandcolleagues.md)を呼び出すと、.osc は、ログオンユーザーの既定の Outlook ストアで、返されたフレンドのデータをソーシャルネットワーク固有の連絡先フォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="855de-108">After calling [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), the OSC stores the returned friends' data in a contacts folder specific to the social network in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="855de-109">また、次のようにして、各フレンドのプロファイル画像を取得するために、 [isocialsession:: getperson](isocialsession-getperson.md)および[iな alperson:: getperson](isocialperson-getpicture.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="855de-109">The OSC also calls [ISocialSession::GetPerson](isocialsession-getperson.md) and [ISocialPerson::GetPicture](isocialperson-getpicture.md) to obtain a profile picture for each friend.</span></span> 
  
### <a name="initiate-synchronization"></a><span data-ttu-id="855de-110">同期を開始する</span><span class="sxs-lookup"><span data-stu-id="855de-110">Initiate synchronization</span></span>

<span data-ttu-id="855de-111">同期を開始するには、Microsoft Office Fluent ユーザーインターフェイスのリボンコンポーネントで [デバッグ] ボタンをオンにして、その**連絡先**を使用します。</span><span class="sxs-lookup"><span data-stu-id="855de-111">To initiate synchronization, you can turn on and use the debug button **Sync Contacts** in the ribbon component of the Microsoft Office Fluent user interface.</span></span> <span data-ttu-id="855de-112">[デバッグ] ボタンの詳細については、「[プロバイダーをデバッグする](debugging-a-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="855de-112">For more information about OSC debug buttons, see [Debugging a Provider](debugging-a-provider.md).</span></span> 
  
### <a name="test-scenarios"></a><span data-ttu-id="855de-113">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="855de-113">Test scenarios</span></span>

<span data-ttu-id="855de-114">次の項目をテストして、友人のデータが正しくキャッシュされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="855de-114">Test the following items to verify that friends' data is cached correctly.</span></span>
  
|<span data-ttu-id="855de-115">**テストするアイテム**</span><span class="sxs-lookup"><span data-stu-id="855de-115">**Item to test**</span></span>|<span data-ttu-id="855de-116">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="855de-116">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="855de-117">連絡先フォルダー</span><span class="sxs-lookup"><span data-stu-id="855de-117">Contacts folder</span></span>  <br/> |<span data-ttu-id="855de-118">ソーシャルネットワーク固有の連絡先フォルダーは、ユーザーの既定の Outlook ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="855de-118">The social network-specific contacts folder exists in the user's default Outlook store.</span></span>  <br/> |
|<span data-ttu-id="855de-119">iGetFriendsAndColleagues によって返されるフレンドのデータ **::**</span><span class="sxs-lookup"><span data-stu-id="855de-119">Friends' data returned by **ISocialPerson::GetFriendsAndColleagues**</span></span> <br/> |<span data-ttu-id="855de-120">各フレンドは、ネットワーク固有の連絡先フォルダー内の連絡先に対応します。</span><span class="sxs-lookup"><span data-stu-id="855de-120">Each friend corresponds to a contact in the network-specific contacts folder.</span></span>  <br/> |
|<span data-ttu-id="855de-121">Friends のデータ</span><span class="sxs-lookup"><span data-stu-id="855de-121">Friends' data</span></span>  <br/> |<span data-ttu-id="855de-122">各フレンドの連絡先フィールドに適切なデータがあります。</span><span class="sxs-lookup"><span data-stu-id="855de-122">Contact fields for each friend have the correct data.</span></span>  <br/> |
|<span data-ttu-id="855de-123">i入力されたユーザーによって返される友人のプロファイル画像 **:: getpicture**</span><span class="sxs-lookup"><span data-stu-id="855de-123">Friends' profile pictures returned by **ISocialPerson::GetPicture**</span></span> <br/> |<span data-ttu-id="855de-124">各フレンドの連絡先アイテムには、プロフィール画像が含まれています。</span><span class="sxs-lookup"><span data-stu-id="855de-124">The contact item for each friend contains the profile picture.</span></span>  <br/> |

<span data-ttu-id="855de-125"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="855de-125"></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="855de-126">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="855de-126">On-demand synchronization</span></span>

<span data-ttu-id="855de-127">.osc プロバイダーは、 **isocialprovider:: getcapabilities**を実装します。この関数は、プロバイダーが友人および非友人のオンデマンド同期をサポートしているかどうかを判断するために、.osc を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="855de-127">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of friends and non-friends.</span></span> <span data-ttu-id="855de-128">[Outlook People] ウィンドウに表示される人物については、.osc は SMTP アドレスを取得してハッシュし、 [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、これらのユーザーに対して返されるデータを (メモリ内に) 保存します。</span><span class="sxs-lookup"><span data-stu-id="855de-128">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), and stores (in memory) the data returned for these persons.</span></span> 
  
### <a name="determining-friends-and-non-friends"></a><span data-ttu-id="855de-129">友人と非友人を決定する</span><span class="sxs-lookup"><span data-stu-id="855de-129">Determining friends and non-friends</span></span>

<span data-ttu-id="855de-130">**GetPeopleDetails**に渡されるハッシュされた SMTP アドレスは、ユーザーがフレンドであるか友人であるかを判断するための鍵となります。</span><span class="sxs-lookup"><span data-stu-id="855de-130">The hashed SMTP addresses passed to **GetPeopleDetails** are the key to determining whether a person is a friend or non-friend.</span></span> <span data-ttu-id="855de-131">自分のソーシャルネットワークアカウントにその SMTP アドレスが含まれていない場合や、その人物がソーシャルネットワーク上の別の電子メールアドレスによって友人である場合でも、 **GetPeopleDetails**は、 \*\*\*\* **その人物に対して非フレンドをfriendStatus**は、_個人コレクション_のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="855de-131">If a person does not include that SMTP address in his or her social network account, or even if that person is a friend by a different email address on the social network, **GetPeopleDetails** still returns **nonfriend** for that person as the **friendStatus** in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="855de-132">また、友人以外のユーザーがソーシャルネットワークアカウントで SMTP アドレスを指定している場合、返されるデータには、そのユーザーのプライバシー設定によって許可されている場合に、フレンド以外に対して使用可能なもののみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="855de-132">Also, for a person who is not a friend but specifies the SMTP address in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="855de-133">友人および非友人のテスト対象を作成する</span><span class="sxs-lookup"><span data-stu-id="855de-133">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="855de-134">友人のテスト件名を作成するには、そのアドレスをソーシャルネットワークアカウントに含めるユーザーの SMTP アドレスを識別し、そのネットワークでログオンしているユーザーのフレンド状態を持っているユーザーを特定します。</span><span class="sxs-lookup"><span data-stu-id="855de-134">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="855de-135">その SMTP アドレスを含む電子メールメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="855de-135">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="855de-136">同様に、フレンド以外のテスト件名を作成するには、そのアドレスによってログオンしているユーザーのフレンドではないユーザーの SMTP アドレスを識別します。さらに、そのユーザーのプライバシー設定で指定されているユーザーが、自分のプライバシー設定で、そのユーザーのアクティビティをソーシャル networ で表示できないようにします。万.</span><span class="sxs-lookup"><span data-stu-id="855de-136">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and yet who has specified in his or her privacy settings to allow non-friends to view their activities on the social network.</span></span> <span data-ttu-id="855de-137">その SMTP アドレスを含む電子メールメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="855de-137">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="855de-138">Outlook エクスプローラーで、友達 (または友人以外) を含む電子メールメッセージを選択すると、[人] ウィンドウに受信者が表示されます。</span><span class="sxs-lookup"><span data-stu-id="855de-138">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="855de-139">[人] ウィンドウで友人 (または友人以外) を選択すると、プロバイダーがその人物に関する情報を提供しているかどうかをテストできます。</span><span class="sxs-lookup"><span data-stu-id="855de-139">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="855de-140">テスト シナリオ</span><span class="sxs-lookup"><span data-stu-id="855de-140">Test scenarios</span></span>

<span data-ttu-id="855de-141">プロバイダーが友人や友人以外に関する情報を適切に提供しているかどうかを確認するには、次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="855de-141">To verify that your provider is providing information about friends and non-friends appropriately, test for the following scenarios.</span></span>
  
|<span data-ttu-id="855de-142">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="855de-142">**Scenario**</span></span>|<span data-ttu-id="855de-143">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="855de-143">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="855de-144">[人] ウィンドウで選択されたユーザーは、ソーシャルネットワーク上でログオンしているユーザーと友人になります。</span><span class="sxs-lookup"><span data-stu-id="855de-144">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="855de-145">[人] ウィンドウには、ソーシャルネットワーク上のその人物の活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="855de-145">The People Pane displays that person's activities on the social network.</span></span>  <br/> |
|<span data-ttu-id="855de-146">People ウィンドウで選択されたユーザーは、ソーシャルネットワーク上のログオンしているユーザーのフレンドではありませんが、自分のアクティビティを友人以外のユーザーに表示することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="855de-146">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her activities to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="855de-147">[人] ウィンドウには、ソーシャルネットワーク上のその人物の活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="855de-147">The People Pane displays that person's activities on the social network.</span></span>  <br/> |

<span data-ttu-id="855de-148"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="855de-148"></span></span>

## <a name="hybrid-synchronization"></a><span data-ttu-id="855de-149">ハイブリッド同期</span><span class="sxs-lookup"><span data-stu-id="855de-149">Hybrid synchronization</span></span>

<span data-ttu-id="855de-150">.osc プロバイダーが友人と友人以外のハイブリッド同期をサポートしている場合、.osc は次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="855de-150">If an OSC provider supports hybrid synchronization of friends and non-friends, the OSC does the following:</span></span> 
  
- <span data-ttu-id="855de-151">.osc は、ログオンしているユーザーのフレンドの情報をソーシャルネットワーク固有の連絡先フォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="855de-151">The OSC stores information for friends of the logged-on user in the social network-specific contact folder.</span></span>
    
- <span data-ttu-id="855de-152">.osc は、ソーシャルネットワークから非友人の情報を取得し、それをフォルダー内に格納するのではなく、メモリのみに格納します。</span><span class="sxs-lookup"><span data-stu-id="855de-152">The OSC retrieves information for non-friends on-demand from the social network, and stores it only in memory, but not in a folder.</span></span>
    
<span data-ttu-id="855de-153">ハイブリッド同期をテストするには、友人のキャッシュされた[同期](#olosc_TestingFriends_CachedSync)セクションのテスト提案と、非友人の場合は「[オンデマンド同期](#olosc_TestingFriends_OnDemandSync)」セクションのテスト候補に従います。</span><span class="sxs-lookup"><span data-stu-id="855de-153">To test hybrid synchronization, follow the testing suggestions in the [Cached Synchronization](#olosc_TestingFriends_CachedSync) section for friends, and those in the [On-Demand Synchronization](#olosc_TestingFriends_OnDemandSync) section for non-friends.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="855de-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="855de-154">See also</span></span>

- [<span data-ttu-id="855de-155">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="855de-155">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="855de-156">Friends の XML</span><span class="sxs-lookup"><span data-stu-id="855de-156">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="855de-157">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="855de-157">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

