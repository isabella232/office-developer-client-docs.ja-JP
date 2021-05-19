---
title: アカウント
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d539f38419a8eaac60cd3054da6283a49bf4cc00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331186"
---
# <a name="accounts"></a><span data-ttu-id="fc6ab-102">アカウント</span><span class="sxs-lookup"><span data-stu-id="fc6ab-102">Accounts</span></span> 

<span data-ttu-id="fc6ab-103">このセクションでは、電子メール アカウントに関連するサンプル タスクを示します。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-103">This section provides sample tasks that involve email accounts.</span></span> <span data-ttu-id="fc6ab-104">電子メール アカウントの例は、Microsoft Exchange Server、Post Office Protocol 3 (POP3)、Internet Message Access Protocol (IMAP)、および Hypertext Transfer Protocol (HTTP) のアカウントです。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-104">Examples of email accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="fc6ab-105">現在のプロファイルのアカウントは、[Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) オブジェクトによって表されます。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="fc6ab-106">トピック</span><span class="sxs-lookup"><span data-stu-id="fc6ab-106">Topic</span></span>|<span data-ttu-id="fc6ab-107">説明</span><span class="sxs-lookup"><span data-stu-id="fc6ab-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="fc6ab-108">アカウント情報を取得する</span><span class="sxs-lookup"><span data-stu-id="fc6ab-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="fc6ab-109">信頼されている Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) オブジェクトを入力引数として受け取り、 **Account** オブジェクトを使用して、現在の Outlook プロファイルで使用できる各アカウントの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="fc6ab-110">現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="fc6ab-110">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="fc6ab-111">送信可能な電子メール アイテムと会議出席依頼を作成する方法と、それらを現在のフォルダーに基づく特定のアカウントを使用して送信する方法を示す 2 つのコード例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-111">Contains two code examples that show how to create a sendable email item and meeting request, and then send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="fc6ab-112">フォルダーのアカウントを取得する</span><span class="sxs-lookup"><span data-stu-id="fc6ab-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="fc6ab-113">現在のセッションで特定のフォルダーに関連付けられているアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="fc6ab-114">複数のアカウントの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="fc6ab-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="fc6ab-115">現在のプロファイルの各アカウントの情報を取得して表示します。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|[<span data-ttu-id="fc6ab-116">Hotmail アカウントを使用してメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="fc6ab-116">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | <span data-ttu-id="fc6ab-117">[SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) プロパティを使用し、Windows Live Hotmail アカウントを使用して、メール アイテムを送信します。</span><span class="sxs-lookup"><span data-stu-id="fc6ab-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="fc6ab-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc6ab-118">See also</span></span>

- [<span data-ttu-id="fc6ab-119">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="fc6ab-119">Exchange users</span></span>](exchange-users.md)
- [<span data-ttu-id="fc6ab-120">メール</span><span class="sxs-lookup"><span data-stu-id="fc6ab-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="fc6ab-121">受信者</span><span class="sxs-lookup"><span data-stu-id="fc6ab-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="fc6ab-122">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="fc6ab-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

