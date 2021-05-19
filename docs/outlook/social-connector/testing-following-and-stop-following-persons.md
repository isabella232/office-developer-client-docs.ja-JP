---
title: フォローおよびフォロー停止のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーがフレンドをフォローする機能をテストし、ソーシャル ネットワーク上の友人のフォローを停止するシナリオについて説明します。
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432451"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="a4671-103">フォローおよびフォロー停止のテスト</span><span class="sxs-lookup"><span data-stu-id="a4671-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="a4671-104">このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーがフレンドをフォローする機能をテストし、ソーシャル ネットワーク上の友人のフォローを停止するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a4671-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="a4671-105">ユーザーの後に続く</span><span class="sxs-lookup"><span data-stu-id="a4671-105">Following a person</span></span>

<span data-ttu-id="a4671-106">人をフォローするには、選択したユーザーが提供する SMTP アドレスを使用して、ソーシャル ネットワークにフレンドとしてOutlookします。</span><span class="sxs-lookup"><span data-stu-id="a4671-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="a4671-107">通常、ソーシャル ネットワーク上のユーザーに従う場合は、その SMTP アドレスに電子メールでそのユーザーからのアクセス許可を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4671-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="a4671-108">アクセス許可を付与するには、そのユーザーは、その SMTP アドレスが既に自分のソーシャル ネットワーク アカウントに含まれているか、その SMTP をソーシャル ネットワーク アカウントに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4671-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="a4671-109">次の各シナリオをテストして、OSC プロバイダーが正しく動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4671-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="a4671-110">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="a4671-110">**Scenario**</span></span>|<span data-ttu-id="a4671-111">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="a4671-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4671-112">ソーシャル ネットワーク上に存在するソーシャル ネットワーク上のユーザーをフォローする試み。</span><span class="sxs-lookup"><span data-stu-id="a4671-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="a4671-113">ユーザーからのアクセス許可を必要としないソーシャル ネットワークの場合、ソーシャル ネットワークは即座にそのユーザーを友人として追加します。</span><span class="sxs-lookup"><span data-stu-id="a4671-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="a4671-114">そのユーザーからのアクセス許可を必要とするネットワークの場合、ソーシャル ネットワークは通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="a4671-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="a4671-115">[Outlook] ウィンドウには、そのユーザーの保留中のアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a4671-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="a4671-116">ソーシャル ネットワーク上に存在しないソーシャル ネットワーク上の人物をフォローする試み。</span><span class="sxs-lookup"><span data-stu-id="a4671-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="a4671-117">OSC プロバイダーは [、ISocialSession::FollowPerson](isocialsession-followperson.md) または [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)に適切なエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="a4671-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="a4671-118">ソーシャル ネットワーク上の友人を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a4671-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="a4671-119">[ユーザー] ウィンドウで選択したフレンドの場合、ソーシャル ネットワークのバッジと、そのソーシャル ネットワークのフレンドのプロファイル画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a4671-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="a4671-120">友人のプロファイル ページへのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a4671-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="a4671-121">ソーシャル ネットワーク上の友人のページが、ログオンしているユーザーの既定のブラウザーで開きます。</span><span class="sxs-lookup"><span data-stu-id="a4671-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="a4671-122">人の後を見るのをやめる</span><span class="sxs-lookup"><span data-stu-id="a4671-122">Stop following a person</span></span>

<span data-ttu-id="a4671-123">人の後を通すのをやめるには、その人をソーシャル ネットワーク上の友人として削除します。</span><span class="sxs-lookup"><span data-stu-id="a4671-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="a4671-124">次のシナリオをテストして、OSC プロバイダーがユーザーの後を適切に実行しなかっているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4671-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="a4671-125">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="a4671-125">**Scenario**</span></span>|<span data-ttu-id="a4671-126">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="a4671-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4671-127">ソーシャル ネットワーク上の友人としてユーザーを削除する試み。</span><span class="sxs-lookup"><span data-stu-id="a4671-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="a4671-128">ソーシャル ネットワークは、ログオンしているユーザーのアカウント上のフレンドとしてそのユーザーを一覧表示しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a4671-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4671-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4671-129">See also</span></span>

- [<span data-ttu-id="a4671-130">OSC プロバイダーをリリースする準備</span><span class="sxs-lookup"><span data-stu-id="a4671-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

