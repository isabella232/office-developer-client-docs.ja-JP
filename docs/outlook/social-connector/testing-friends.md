---
title: 友だちのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、テストおよび該当する場合、プロバイダーでサポートされている同期モードによって、Outlook ソーシャル コネクタ (OSC) プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804481"
---
# <a name="testing-friends"></a><span data-ttu-id="5a374-103">友だちのテスト</span><span class="sxs-lookup"><span data-stu-id="5a374-103">Testing friends</span></span>

<span data-ttu-id="5a374-104">このトピックでは、テストおよび該当する場合、プロバイダーでサポートされている同期モードによって、Outlook ソーシャル コネクタ (OSC) プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a374-104">This topic describes tests and scenarios to verify that the Outlook Social Connector (OSC) provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode supported by the provider.</span></span>

<span data-ttu-id="5a374-105"><a name="olosc_TestingFriends_CachedSync"> </a></span><span class="sxs-lookup"><span data-stu-id="5a374-105"></span></span>

## <a name="cached-synchronization"></a><span data-ttu-id="5a374-106">キャッシュの同期</span><span class="sxs-lookup"><span data-stu-id="5a374-106">Cached synchronization</span></span>

<span data-ttu-id="5a374-107">OSC プロバイダーは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)プロバイダーが友人のデータのキャッシュの同期をサポートしているかどうかを決定する、OSC を実装します。</span><span class="sxs-lookup"><span data-stu-id="5a374-107">An OSC provider implements [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), which the OSC calls to determine whether the provider supports cached synchronization of friends' data.</span></span> <span data-ttu-id="5a374-108">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出すと、OSC は、ソーシャル ネットワークにログオンしているユーザーの既定の Outlook ストアに特定の連絡先フォルダーに返された友人のデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="5a374-108">After calling [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), the OSC stores the returned friends' data in a contacts folder specific to the social network in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="5a374-109">OSC は、各フレンドのプロフィールの画像を取得するには、 [ISocialSession::GetPerson](isocialsession-getperson.md)と[ISocialPerson::GetPicture](isocialperson-getpicture.md)にも呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5a374-109">The OSC also calls [ISocialSession::GetPerson](isocialsession-getperson.md) and [ISocialPerson::GetPicture](isocialperson-getpicture.md) to obtain a profile picture for each friend.</span></span> 
  
### <a name="initiate-synchronization"></a><span data-ttu-id="5a374-110">同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="5a374-110">Initiate synchronization</span></span>

<span data-ttu-id="5a374-111">同期を開始するを有効にして、デバッグ] をクリックして**連絡先を同期する**Microsoft Office Fluent ユーザー インターフェイスのリボンのコンポーネントで。</span><span class="sxs-lookup"><span data-stu-id="5a374-111">To initiate synchronization, you can turn on and use the debug button **Sync Contacts** in the ribbon component of the Microsoft Office Fluent user interface.</span></span> <span data-ttu-id="5a374-112">OSC デバッグ ボタンの詳細については[、プロバイダーをデバッグ](debugging-a-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a374-112">For more information about OSC debug buttons, see [Debugging a Provider](debugging-a-provider.md).</span></span> 
  
### <a name="test-scenarios"></a><span data-ttu-id="5a374-113">シナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="5a374-113">Test scenarios</span></span>

<span data-ttu-id="5a374-114">友人のデータのキャッシュが正しくことを確認するのには、次の項目をテストします。</span><span class="sxs-lookup"><span data-stu-id="5a374-114">Test the following items to verify that friends' data is cached correctly.</span></span>
  
|<span data-ttu-id="5a374-115">**項目をテストするには**</span><span class="sxs-lookup"><span data-stu-id="5a374-115">**Item to test**</span></span>|<span data-ttu-id="5a374-116">**予想される動作**</span><span class="sxs-lookup"><span data-stu-id="5a374-116">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a374-117">[連絡先] フォルダー</span><span class="sxs-lookup"><span data-stu-id="5a374-117">Contacts folder</span></span>  <br/> |<span data-ttu-id="5a374-118">ソーシャル ネットワークの特定の連絡先フォルダーは、ユーザーの既定の Outlook ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="5a374-118">The social network-specific contacts folder exists in the user's default Outlook store.</span></span>  <br/> |
|<span data-ttu-id="5a374-119">友人のデータを**ISocialPerson::GetFriendsAndColleagues**によって返される</span><span class="sxs-lookup"><span data-stu-id="5a374-119">Friends' data returned by **ISocialPerson::GetFriendsAndColleagues**</span></span> <br/> |<span data-ttu-id="5a374-120">各友人は、特定のネットワークの連絡先フォルダーの連絡先に対応しています。</span><span class="sxs-lookup"><span data-stu-id="5a374-120">Each friend corresponds to a contact in the network-specific contacts folder.</span></span>  <br/> |
|<span data-ttu-id="5a374-121">友人のデータ</span><span class="sxs-lookup"><span data-stu-id="5a374-121">Friends' data</span></span>  <br/> |<span data-ttu-id="5a374-122">各友人の連絡先のフィールドには、正しいデータが存在します。</span><span class="sxs-lookup"><span data-stu-id="5a374-122">Contact fields for each friend have the correct data.</span></span>  <br/> |
|<span data-ttu-id="5a374-123">友人のプロフィールの画像が**ISocialPerson::GetPicture**によって返される</span><span class="sxs-lookup"><span data-stu-id="5a374-123">Friends' profile pictures returned by **ISocialPerson::GetPicture**</span></span> <br/> |<span data-ttu-id="5a374-124">各友人の連絡先アイテムには、プロフィールの画像が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a374-124">The contact item for each friend contains the profile picture.</span></span>  <br/> |

<span data-ttu-id="5a374-125"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="5a374-125"></span></span>

## <a name="on-demand-synchronization"></a><span data-ttu-id="5a374-126">オンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="5a374-126">On-demand synchronization</span></span>

<span data-ttu-id="5a374-127">OSC プロバイダーは、 **ISocialProvider::GetCapabilities**プロバイダーがオンデマンドの同期や友人の友人ではないをサポートするかどうかを確認するのには、OSC の呼び出しを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a374-127">An OSC provider implements **ISocialProvider::GetCapabilities**, which the OSC calls to determine whether the provider supports on-demand synchronization of friends and non-friends.</span></span> <span data-ttu-id="5a374-128">Outlook 人物情報ウィンドウに表示されている方のため、OSC を取得、これらの方のために返されるハッシュの SMTP アドレスを[ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出して、(メモリ) にデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="5a374-128">For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), and stores (in memory) the data returned for these persons.</span></span> 
  
### <a name="determining-friends-and-non-friends"></a><span data-ttu-id="5a374-129">友人と友人ではないを決定します。</span><span class="sxs-lookup"><span data-stu-id="5a374-129">Determining friends and non-friends</span></span>

<span data-ttu-id="5a374-130">ハッシュされた SMTP アドレスが**GetPeopleDetails**に渡されますが、人が友人や友人ではないかどうかを判断するキーです。</span><span class="sxs-lookup"><span data-stu-id="5a374-130">The hashed SMTP addresses passed to **GetPeopleDetails** are the key to determining whether a person is a friend or non-friend.</span></span> <span data-ttu-id="5a374-131">人に自分のソーシャル ネットワーク アカウントの SMTP アドレスが含まれていない場合、またはその人がソーシャル ネットワーク上の別の電子メール アドレスで友人の場合でも、 **GetPeopleDetails**も**nonfriend**その人のとして返します、 **friendStatus** 、 _personsCollection_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="5a374-131">If a person does not include that SMTP address in his or her social network account, or even if that person is a friend by a different email address on the social network, **GetPeopleDetails** still returns **nonfriend** for that person as the **friendStatus** in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="5a374-132">また、フレンドではありませんが、自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定したユーザーでは、返されたデータが含まれています以外の友人にその人のプライバシーの設定で許可された使用可能なのみです。</span><span class="sxs-lookup"><span data-stu-id="5a374-132">Also, for a person who is not a friend but specifies the SMTP address in his or her social network account, the data returned includes only what is available to a non-friend as allowed by the privacy settings of that person.</span></span> 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a><span data-ttu-id="5a374-133">友人と友人ではないテストの情報カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a374-133">Creating test subjects for friends and non-friends</span></span>

<span data-ttu-id="5a374-134">友人のテストの対象を作成するには、自分のソーシャル ネットワーク アカウントでそのアドレスを含むユーザーと、そのネットワークにログオン中のユーザーとフレンドのステータスを持つユーザーの SMTP アドレスを識別します。</span><span class="sxs-lookup"><span data-stu-id="5a374-134">To create a test subject for a friend, identify the SMTP address of a person who includes that address in his or her social network account and who has a friend status with the logged-on user on that network.</span></span> <span data-ttu-id="5a374-135">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a374-135">Create an email message that includes that SMTP address.</span></span> <span data-ttu-id="5a374-136">同様に、以外の友人のテストの対象を作成するには、ユーザーの SMTP アドレスを識別する人はそのアドレスでは、ログオン中のユーザーのフレンドではありませんし、まだ、ソーシャル ネットワーク上での活動を表示するのにはフレンド以外を使用するのには自分のプライバシーの設定で指定しました。k です。</span><span class="sxs-lookup"><span data-stu-id="5a374-136">Similarly, to create a test subject for a non-friend, identify the SMTP address of a person who is not a friend of the logged-on user by that address, and yet who has specified in his or her privacy settings to allow non-friends to view their activities on the social network.</span></span> <span data-ttu-id="5a374-137">その SMTP アドレスを含む電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a374-137">Create an email message that includes that SMTP address.</span></span> 
  
<span data-ttu-id="5a374-138">Outlook エクスプ ローラーで、友人 (または友人ではない) を含む電子メール メッセージを選択すると、人物情報ウィンドウは、受信者を表示します。</span><span class="sxs-lookup"><span data-stu-id="5a374-138">In the Outlook explorer, when you select the email message that includes a friend (or non-friend), the People Pane displays the recipients.</span></span> <span data-ttu-id="5a374-139">人物情報ウィンドウで、友人、友人ではない) を選択すると、テストするのにはプロバイダーが個人情報を提供することできます。</span><span class="sxs-lookup"><span data-stu-id="5a374-139">Selecting the friend (or non-friend) in the People Pane allows you to test that the provider is providing information about the person.</span></span>
  
### <a name="test-scenarios"></a><span data-ttu-id="5a374-140">シナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="5a374-140">Test scenarios</span></span>

<span data-ttu-id="5a374-141">プロバイダーが友人と友人ではないについての情報を適切に提供していることを確認するには、次のシナリオでテストします。</span><span class="sxs-lookup"><span data-stu-id="5a374-141">To verify that your provider is providing information about friends and non-friends appropriately, test for the following scenarios.</span></span>
  
|<span data-ttu-id="5a374-142">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="5a374-142">**Scenario**</span></span>|<span data-ttu-id="5a374-143">**予想される動作**</span><span class="sxs-lookup"><span data-stu-id="5a374-143">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a374-144">人物情報ウィンドウで選択したユーザーは、ソーシャル ネットワークにログオン中のユーザーのフレンドです。</span><span class="sxs-lookup"><span data-stu-id="5a374-144">Person selected in the People Pane is a friend with the logged-on user on the social network.</span></span>  <br/> |<span data-ttu-id="5a374-145">人物情報ウィンドウには、ソーシャル ネットワーク上の人の活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a374-145">The People Pane displays that person's activities on the social network.</span></span>  <br/> |
|<span data-ttu-id="5a374-146">人物情報ウィンドウで選択されている人は、ソーシャル ネットワークにログオン中のユーザーの非友人が、友人で非表示に自分の活動が可能に。</span><span class="sxs-lookup"><span data-stu-id="5a374-146">Person selected in the People Pane is a non-friend of the logged-on user on the social network, but has allowed his or her activities to be viewed by non-friends.</span></span>  <br/> |<span data-ttu-id="5a374-147">人物情報ウィンドウには、ソーシャル ネットワーク上の人の活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a374-147">The People Pane displays that person's activities on the social network.</span></span>  <br/> |

<span data-ttu-id="5a374-148"><a name="olosc_TestingFriends_OnDemandSync"> </a></span><span class="sxs-lookup"><span data-stu-id="5a374-148"></span></span>

## <a name="hybrid-synchronization"></a><span data-ttu-id="5a374-149">ハイブリッド同期</span><span class="sxs-lookup"><span data-stu-id="5a374-149">Hybrid synchronization</span></span>

<span data-ttu-id="5a374-150">OSC プロバイダーでは、友人や友人ではないのハイブリッド同期をサポートする場合、OSC は、次を行います。</span><span class="sxs-lookup"><span data-stu-id="5a374-150">If an OSC provider supports hybrid synchronization of friends and non-friends, the OSC does the following:</span></span> 
  
- <span data-ttu-id="5a374-151">OSC では、ソーシャル ネットワークに固有の連絡先フォルダーにログオンしているユーザーの友人の情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="5a374-151">The OSC stores information for friends of the logged-on user in the social network-specific contact folder.</span></span>
    
- <span data-ttu-id="5a374-152">OSC では、ソーシャル ネットワークからオン ・ デマンドの友人ではないの情報を取得し、メモリ内のみではなくフォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="5a374-152">The OSC retrieves information for non-friends on-demand from the social network, and stores it only in memory, but not in a folder.</span></span>
    
<span data-ttu-id="5a374-153">ハイブリッド同期をテストするには、[キャッシュの同期](#olosc_TestingFriends_CachedSync)で、友人のテストの推奨事項とその友人ではないの[オンデマンド同期](#olosc_TestingFriends_OnDemandSync)のセクションに従います。</span><span class="sxs-lookup"><span data-stu-id="5a374-153">To test hybrid synchronization, follow the testing suggestions in the [Cached Synchronization](#olosc_TestingFriends_CachedSync) section for friends, and those in the [On-Demand Synchronization](#olosc_TestingFriends_OnDemandSync) section for non-friends.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a374-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a374-154">See also</span></span>

- [<span data-ttu-id="5a374-155">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="5a374-155">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="5a374-156">友人の XML</span><span class="sxs-lookup"><span data-stu-id="5a374-156">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="5a374-157">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="5a374-157">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

