---
title: メッセージ ストア プロバイダーを使用したメッセージの受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418730"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="93eb6-103">メッセージ ストア プロバイダーを使用したメッセージの受信</span><span class="sxs-lookup"><span data-stu-id="93eb6-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="93eb6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93eb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93eb6-105">メッセージ ストア プロバイダーは、受信メッセージの送信をサポートする必要があります (つまり、トランスポート プロバイダーと MAPI スプーラーがメッセージの配信ポイントとしてメッセージ ストア プロバイダーを使用する機能をサポートします)。</span><span class="sxs-lookup"><span data-stu-id="93eb6-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="93eb6-106">ただし、メッセージ ストア プロバイダーが受信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="93eb6-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="93eb6-107">受信メッセージの送信をサポートするには、メッセージ ストア プロバイダーが次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="93eb6-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="93eb6-108">クライアント アプリケーションが受信メッセージを検索できるよう [、IMsgStore:::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) メソッドと [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="93eb6-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="93eb6-109">MAPI スプーラーが新しいメッセージが到着したとメッセージ ストア プロバイダーに通知できるよう [、IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="93eb6-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="93eb6-110">クライアントが新しいメッセージ通知に登録できるよう、通知を実装します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="93eb6-111">通知はオプションですが、プロバイダーはそれらを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93eb6-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="93eb6-112">受信メッセージがメッセージ ストアに配信される場合に発生するメソッド呼び出しのシーケンスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="93eb6-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="93eb6-113">MAPI スプーラーは、IMAPIFolder インターフェイスを取得するために受信トレイ[エントリ ID](entryid.md)を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md) [を呼び出](imapifolderimapicontainer.md)します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="93eb6-114">MAPI スプーラーは [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) を呼び出して、新しいメッセージ オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="93eb6-115">MAPI スプーラーは、メッセージ オブジェクトをトランスポート プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="93eb6-116">トランスポート プロバイダーは、基になるメッセージング システムからのデータをメッセージのプロパティに入力し、メッセージ オブジェクトの [IMAPIProp::SaveChanges メソッドを呼び出](imapiprop-savechanges.md) します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="93eb6-117">メッセージ ストア プロバイダーは、通知メソッドを使用して、新しいメッセージが到着したと登録済みのクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="93eb6-118">MAPI スプーラーは、メッセージ ストアの [IMsgStore::NotifyNewMail メソッドを呼び出](imsgstore-notifynewmail.md) します。</span><span class="sxs-lookup"><span data-stu-id="93eb6-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="93eb6-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="93eb6-119">See also</span></span>



<span data-ttu-id="93eb6-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="93eb6-120">[Message Store Features](message-store-features.md)</span></span>

