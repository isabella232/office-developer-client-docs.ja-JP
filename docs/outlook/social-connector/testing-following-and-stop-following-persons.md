---
title: フォローおよびフォロー停止のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: このトピックでは、友人に従うと、ソーシャル ネットワーク上の友人のフォローを停止する、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能をテストするシナリオについて説明します。
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804455"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="4a9e0-103">フォローおよびフォロー停止のテスト</span><span class="sxs-lookup"><span data-stu-id="4a9e0-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="4a9e0-104">このトピックでは、友人に従うと、ソーシャル ネットワーク上の友人のフォローを停止する、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能をテストするシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="4a9e0-105">次の人</span><span class="sxs-lookup"><span data-stu-id="4a9e0-105">Following a person</span></span>

<span data-ttu-id="4a9e0-106">次の人には選択したアイテムによって提供される SMTP アドレスを使用して、ソーシャル ネットワーク上の友人との人を追加します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="4a9e0-107">次の他のソーシャル ネットワークに通常では、その SMTP アドレスに電子メールでその人から許可を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="4a9e0-108">アクセス許可を付与するためにそのユーザーする必要がありますがその SMTP アドレスを自分のソーシャル ネットワーク アカウントに既に含まれているかを追加するソーシャル ネットワークのアカウントには、その SMTP です。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="4a9e0-109">OSC プロバイダーが正しく動作することを確認するのには次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="4a9e0-110">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-110">**Scenario**</span></span>|<span data-ttu-id="4a9e0-111">**予想される動作**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a9e0-112">ソーシャル ネットワーク ソーシャル ネットワーク上に存在するユーザーに次の人しようとしています。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="4a9e0-113">ユーザーからアクセス許可を必要としないソーシャル ネットワークのソーシャル ネットワークはすぐに友人としてユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="4a9e0-114">その人からのアクセス許可を必要とするネットワークでは、ソーシャル ネットワークは、通知を送ります。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="4a9e0-115">Outlook 人物情報ウィンドウには、その人の保留中アイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="4a9e0-116">ソーシャル ネットワーク ソーシャル ネットワークに存在しないユーザーに次の人しようとしています。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="4a9e0-117">OSC プロバイダーでは、 [ISocialSession::FollowPerson](isocialsession-followperson.md)または[ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)で適切なエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="4a9e0-118">ソーシャル ネットワークの友人に従います。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="4a9e0-119">人物情報ウィンドウで選択されている友人、ソーシャル ネットワークのバッジとソーシャル ネットワークの友人のプロフィールの画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="4a9e0-120">友人のプロファイルのページへのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="4a9e0-121">ソーシャル ネットワーク上の友人のページにログオンしたユーザーの既定のブラウザーで開きます。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="4a9e0-122">次の人を停止します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-122">Stop following a person</span></span>

<span data-ttu-id="4a9e0-123">次の人を停止するにはソーシャル ネットワークの友人とそのユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="4a9e0-124">OSC プロバイダーが停止する人に正しく従うことを確認するのには次のシナリオをテストします。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="4a9e0-125">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-125">**Scenario**</span></span>|<span data-ttu-id="4a9e0-126">**予想される動作**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a9e0-127">ソーシャル ネットワークで友達とユーザーを削除しようとしています。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="4a9e0-128">不要になった、ソーシャル ネットワークには、ログオンしたユーザーのアカウントのフレンドとしては、そのユーザーが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a9e0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a9e0-129">See also</span></span>

- [<span data-ttu-id="4a9e0-130">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

