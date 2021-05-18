---
title: 管理メッセージは POP3 アカウントをダウンロードします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: このセクションでは、 Outlookの POP3 プロバイダーでの使用方法の固有 ID リスト (UIDL) 履歴、POP3 アカウントのプロバイダーがダウンロードまたは複数回、同じメッセージのダウンロードを避けるために、POP3 サーバーから削除するメッセージを識別するについて説明します。
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322247"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a><span data-ttu-id="26dfa-103">管理メッセージは POP3 アカウントをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="26dfa-103">Managing message downloads for POP3 accounts</span></span>

<span data-ttu-id="26dfa-104">このセクションでは、 Outlookの POP3 プロバイダーでの使用方法の固有 ID リスト (UIDL) 履歴、POP3 アカウントのプロバイダーがダウンロードまたは複数回、同じメッセージのダウンロードを避けるために、POP3 サーバーから削除するメッセージを識別するについて説明します。</span><span class="sxs-lookup"><span data-stu-id="26dfa-104">This section describes how the POP3 provider of Outlook uses the Unique ID Listing (UIDL) history on a POP3 account to identify messages that the provider has downloaded or deleted from the POP3 server, to avoid downloading the same message more than once.</span></span>
  
## <a name="introduction-to-pop"></a><span data-ttu-id="26dfa-105">ポップアップの概要</span><span class="sxs-lookup"><span data-stu-id="26dfa-105">Introduction to POP</span></span>

<span data-ttu-id="26dfa-p101">ポスト Office プロトコル (POP) は、電子メール クライアントがメール サーバーから電子メール メッセージをダウンロードするOutlookなどのアプリケーション層プロトコルを指定します。ユーザーにサーバー上のコピーをローカル デバイス (スマート フォン、コンピューター)、し、いずれかのままにする、電子メール メッセージのコピーをダウンロードしたり、削除したりできます。プロトコルは、メールボックスに同時に接続する 1 つのメール クライアントをサポートします。それを取得する必要がなく、メール サーバーから電子メール メッセージを送信する方法のみを指定します。POP を使用する場合メール クライアント通常新しい電子メール メッセージをチェックするには、だけの時間と新着メールの通知を取得するのには、サーバーへの接続を維持しませんが、新しいメッセージをダウンロードするには、メール サーバーに接続します。POP は、電子メールにカプセル化しない限り、電子メール メッセージだけがいない項目など他の種類の連絡先との予定をサポートします。POP3 は、プロトコルのバージョン 3 です。</span><span class="sxs-lookup"><span data-stu-id="26dfa-p101">The Post Office Protocol (POP) specifies an application layer protocol for an email client such as Outlook to download email messages from a mail server. It allows a user to download a copy of an email message to a local device (such as a smart phone or computer), and either leave a copy on the server or delete it. The protocol supports only one mail client to be connected to the mailbox at one time. It specifies only how to retrieve but not send email messages from the mail server. When using POP, a mail client typically has to check for new email messages, connects to the mail server for only the amount of time it takes to download new messages, and does not stay connected to the server to get new mail notifications. POP supports only email messages but not other item types such as contacts and appointments unless they are encapsulated in an email. POP3 is version 3 of the protocol.</span></span>
  
<span data-ttu-id="26dfa-p102">POP アカウントのメッセージは、一意の識別子 (Uid) で識別されます。電子メール クライアントがメール サーバーに残ります UIDL マップを関連付けるその UID をメールボックスに送信された各メッセージを取得するために、UIDL コマンドを使用します。クライアントはダウンロードまたはクライアント上で受信トレイを削除するメッセージの UIDL 履歴も取得します。クライアントは、UIDL 履歴に基づき、メッセージは新しいをダウンロードするかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="26dfa-p102">Messages for a POP account are identified by unique identifiers (UIDs). An email client that leaves mail on the server uses the UIDL command to retrieve the UIDL map that associates each message that has been delivered to the mailbox to its UID. The client also gets the UIDL history for messages that have been downloaded or deleted for the Inbox on that client. Based on the UIDL history, the client can determine which messages are new and should be downloaded.</span></span>

- <span data-ttu-id="26dfa-117">[POP3](locating-the-message-download-history-for-a-pop3-account.md)アカウントのメッセージダウンロード履歴を検索する : このトピックでは、メール クライアントが [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) プロパティにアクセスして、POP3 アカウントのクライアント受信トレイにあるメッセージの UIDL 履歴を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="26dfa-117">[Locating the message download history for a POP3 account](locating-the-message-download-history-for-a-pop3-account.md): This topic describes how a mail client accesses the [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) property to get the UIDL history for messages in the client Inbox of a POP3 account.</span></span> 
    
- <span data-ttu-id="26dfa-118">[POP3](parsing-the-message-download-history-for-a-pop3-account.md)アカウントのメッセージダウンロード履歴を解析する : このトピックでは、POP3 アカウントのクライアント受信トレイにあるメッセージの UIDL 履歴を表す POP3 BLOB を解析し、そのアカウントでダウンロードまたは削除されたメッセージを識別する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="26dfa-118">[Parsing the message download history for a POP3 account](parsing-the-message-download-history-for-a-pop3-account.md): This topic describes how to parse the POP3 BLOB that represents the UIDL history for messages in the client Inbox of a POP3 account, to identify the messages that have been downloaded or deleted on that account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26dfa-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="26dfa-119">See also</span></span>

- [<span data-ttu-id="26dfa-120">Outlook アカウントの管理</span><span class="sxs-lookup"><span data-stu-id="26dfa-120">Outlook account management</span></span>](outlook-account-management.md)    
- [<span data-ttu-id="26dfa-121">POP3 アカウントのメッセージのダウンロードの履歴を検索します。</span><span class="sxs-lookup"><span data-stu-id="26dfa-121">Locating the message download history for a POP3 account</span></span>](locating-the-message-download-history-for-a-pop3-account.md) 
- [<span data-ttu-id="26dfa-122">POP3 アカウントのメッセージのダウンロードの履歴の解析</span><span class="sxs-lookup"><span data-stu-id="26dfa-122">Parsing the message download history for a POP3 account</span></span>](parsing-the-message-download-history-for-a-pop3-account.md)   
- [<span data-ttu-id="26dfa-123">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="26dfa-123">PROP_POP_LEAVE_ON_SERVER</span></span>](prop_pop_leave_on_server.md)  
- [<span data-ttu-id="26dfa-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="26dfa-124">Constants (Account management API)</span></span>](constants-account-management-api.md)    
- [<span data-ttu-id="26dfa-125">プロパティ (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="26dfa-125">Properties (Account management API)</span></span>](properties-account-management-api.md)
    

