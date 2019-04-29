---
title: フォローおよびフォロー停止のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: このトピックでは、Outlook social Connector (.osc) プロバイダーが友人をフォローする機能をテストし、ソーシャルネットワークで友人のフォローを停止するシナリオについて説明します。
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432451"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="02212-103">フォローおよびフォロー停止のテスト</span><span class="sxs-lookup"><span data-stu-id="02212-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="02212-104">このトピックでは、Outlook social Connector (.osc) プロバイダーが友人をフォローする機能をテストし、ソーシャルネットワークで友人のフォローを停止するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="02212-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="02212-105">ユーザーのフォロー</span><span class="sxs-lookup"><span data-stu-id="02212-105">Following a person</span></span>

<span data-ttu-id="02212-106">ユーザーをフォローするには、選択された Outlook アイテムによって提供される SMTP アドレスを使用して、ソーシャルネットワーク上にその人物を友人として追加します。</span><span class="sxs-lookup"><span data-stu-id="02212-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="02212-107">ソーシャルネットワーク上のユーザーをフォローするには、通常、その SMTP アドレス宛ての電子メールによってその送信者からのアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="02212-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="02212-108">アクセス許可を付与するには、その smtp アドレスがソーシャルネットワークアカウントに既に含まれているか、ソーシャルネットワークアカウントに smtp を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02212-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="02212-109">次の各シナリオをテストして、.osc プロバイダーが正しく動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="02212-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="02212-110">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="02212-110">**Scenario**</span></span>|<span data-ttu-id="02212-111">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="02212-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02212-112">ソーシャルネットワーク上に存在するソーシャルネットワーク上のユーザーのフォローを試みます。</span><span class="sxs-lookup"><span data-stu-id="02212-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="02212-113">ユーザーからアクセス許可を必要としないソーシャルネットワークの場合、ソーシャルネットワークはすぐにその人物をフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="02212-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="02212-114">その人物からのアクセス許可を必要とするネットワークの場合、ソーシャルネットワークは通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="02212-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="02212-115">Outlook の [ユーザー] ウィンドウに、その人物の保留中のアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02212-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="02212-116">ソーシャルネットワーク上に存在しないソーシャルネットワーク上のユーザーのフォローを試行しています。</span><span class="sxs-lookup"><span data-stu-id="02212-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="02212-117">.osc プロバイダーは、 [iISocialSession2 alsession::](isocialsession-followperson.md)という名前の適切なエラー [](isocialsession2-followpersonex.md)を表示します。</span><span class="sxs-lookup"><span data-stu-id="02212-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="02212-118">ソーシャルネットワークで友人をフォローする。</span><span class="sxs-lookup"><span data-stu-id="02212-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="02212-119">[ユーザー] ウィンドウで選択されたフレンドについては、ソーシャルネットワークのバッジとそのソーシャルネットワークのフレンドのプロフィール画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02212-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="02212-120">フレンドのプロファイルページへのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="02212-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="02212-121">ソーシャルネットワーク上のフレンドのページが、ログオンしているユーザーの既定のブラウザーで開きます。</span><span class="sxs-lookup"><span data-stu-id="02212-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="02212-122">ユーザーのフォローを停止する</span><span class="sxs-lookup"><span data-stu-id="02212-122">Stop following a person</span></span>

<span data-ttu-id="02212-123">ユーザーのフォローを停止するには、ソーシャルネットワーク上でその人物を友人として削除します。</span><span class="sxs-lookup"><span data-stu-id="02212-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="02212-124">次のシナリオをテストして、.osc プロバイダーがユーザーの適切なフォローを停止することを確認します。</span><span class="sxs-lookup"><span data-stu-id="02212-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="02212-125">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="02212-125">**Scenario**</span></span>|<span data-ttu-id="02212-126">**予期される動作**</span><span class="sxs-lookup"><span data-stu-id="02212-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02212-127">ソーシャルネットワーク上のフレンドとして個人を削除しようとしています。</span><span class="sxs-lookup"><span data-stu-id="02212-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="02212-128">ソーシャルネットワークには、ログオンしているユーザーのアカウントのフレンドとしてそのユーザーが表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="02212-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02212-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="02212-129">See also</span></span>

- [<span data-ttu-id="02212-130">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="02212-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

