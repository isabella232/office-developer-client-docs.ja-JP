---
title: Exchange ユーザー
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 775bfa2c67f3f570bddc749fb995460f6b90b18a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406989"
---
# <a name="exchange-users"></a><span data-ttu-id="15099-102">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="15099-102">Exchange Users</span></span>

<span data-ttu-id="15099-p101">このセクションでは、Microsoft Exchange メールボックス ユーザーに関連するサンプル タスクを示します。Exchange ユーザーは、Exchange Server に接続しているユーザーで、[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトで表されます。これらのオブジェクトは [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトから派生します。</span><span class="sxs-lookup"><span data-stu-id="15099-p101">This section provides sample tasks that involve Microsoft Exchange mailbox users. Exchange users are connected to an Exchange server, and are represented by [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) objects, which are derived from the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15099-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="15099-105">In this section</span></span>

|<span data-ttu-id="15099-106">トピック</span><span class="sxs-lookup"><span data-stu-id="15099-106">Topic</span></span>|<span data-ttu-id="15099-107">説明</span><span class="sxs-lookup"><span data-stu-id="15099-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="15099-108">現在のユーザーの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="15099-108">Get information about the signed in user.</span></span>](how-to-get-information-about-the-current-user.md)  |<span data-ttu-id="15099-109">名前、役職、電話番号など、現在のユーザーの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="15099-109">Gets the current user’s information, such as name, job title, and telephone number.</span></span>|
|[<span data-ttu-id="15099-110">現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="15099-110">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |<span data-ttu-id="15099-111">[GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) メソッドを使用して、現在のユーザーがメンバーになっているすべての配布リストについての情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="15099-111">Uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>|
|[<span data-ttu-id="15099-112">配布リストを作成する</span><span class="sxs-lookup"><span data-stu-id="15099-112">Create a list:</span></span>](how-to-create-a-distribution-list.md)  |<span data-ttu-id="15099-113">配布リストを作成し、それをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="15099-113">Creates a distribution list and displays it to the user.</span></span>|
[<span data-ttu-id="15099-114">Exchange 配布リストのメンバーを取得する</span><span class="sxs-lookup"><span data-stu-id="15099-114">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)  |<span data-ttu-id="15099-115">ユーザーが [ **名前の選択**] ダイアログ ボックスで Exchange 配布リストを選択できるようにして、配布リストを展開してリストのメンバーを表示します。</span><span class="sxs-lookup"><span data-stu-id="15099-115">Prompts the user to select an Exchange distribution list from the **Select Names** dialog box and expands the distribution list to display its members.</span></span>|
[<span data-ttu-id="15099-116">現在のユーザーの上司の情報を取得する</span><span class="sxs-lookup"><span data-stu-id="15099-116">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)  |<span data-ttu-id="15099-117">現在のユーザーの上司についての情報 (名前、役職、電話番号など) を取得します。</span><span class="sxs-lookup"><span data-stu-id="15099-117">Gets information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>|
[<span data-ttu-id="15099-118">Exchange ユーザーの上司の空き時間情報を取得する</span><span class="sxs-lookup"><span data-stu-id="15099-118">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  <span data-ttu-id="15099-119">ユーザーの上司の予定表で次に空いている 60 分の時間枠を表示します。</span><span class="sxs-lookup"><span data-stu-id="15099-119">Displays the next free 60-minute time slot in the calendar for a user's manager.</span></span>|
|[<span data-ttu-id="15099-120">会議出席依頼に対する上司からの返信を確認する</span><span class="sxs-lookup"><span data-stu-id="15099-120">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md) | <span data-ttu-id="15099-121">[GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドおよび [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを使用して、会議出席依頼に対する現在のユーザーの上司からの返信の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="15099-121">Uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>|
|[<span data-ttu-id="15099-122">現在のユーザーの上司の直属部下についての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="15099-122">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | <span data-ttu-id="15099-123">現在のユーザーに上司がいる場合はその上司の直属の部下を取得し、上司の各直属部下についての情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="15099-123">Gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>|

## <a name="see-also"></a><span data-ttu-id="15099-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="15099-124">See also</span></span>

- [<span data-ttu-id="15099-125">アカウント</span><span class="sxs-lookup"><span data-stu-id="15099-125">Accounts</span></span>](accounts.md)
- [<span data-ttu-id="15099-126">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="15099-126">Address Book</span></span>](address-book.md)
- [<span data-ttu-id="15099-127">ストア</span><span class="sxs-lookup"><span data-stu-id="15099-127">Stores</span></span>](stores.md)
- [<span data-ttu-id="15099-128">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="15099-128">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
