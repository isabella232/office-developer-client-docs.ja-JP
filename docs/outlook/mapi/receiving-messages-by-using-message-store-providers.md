---
title: メッセージストアプロバイダーを使用したメッセージの受信
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
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="b5390-103">メッセージストアプロバイダーを使用したメッセージの受信</span><span class="sxs-lookup"><span data-stu-id="b5390-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="b5390-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5390-105">メッセージストアプロバイダーは、受信メッセージの送信をサポートする必要はありません (つまり、トランスポートプロバイダーと MAPI スプーラーがメッセージの配信ポイントとしてメッセージストアプロバイダーを使用することをサポートしています)。</span><span class="sxs-lookup"><span data-stu-id="b5390-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="b5390-106">ただし、メッセージストアプロバイダーが受信メッセージの送信をサポートしていない場合は、既定のメッセージストアとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b5390-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="b5390-107">受信メッセージの送信をサポートするために、メッセージストアプロバイダーは次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5390-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="b5390-108">クライアントアプリケーションが受信メッセージを検索できるように、 [IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)および[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b5390-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="b5390-109">[IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドをサポートします。これにより、MAPI スプーラーは、新しいメッセージが到着したことをメッセージストアプロバイダーに通知できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b5390-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="b5390-110">通知を実装して、クライアントが新しいメッセージ通知を登録できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b5390-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="b5390-111">通知はオプションですが、プロバイダーで実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5390-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="b5390-112">受信メッセージがメッセージストアに配信されるときに実行されるメソッド呼び出しのシーケンスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b5390-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="b5390-113">MAPI スプーラーは、受信トレイ[EntryID](entryid.md)を持つ[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、 [imapifolder](imapifolderimapicontainer.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5390-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="b5390-114">MAPI スプーラーは、 [imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、新しい message オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5390-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="b5390-115">MAPI スプーラーは、メッセージオブジェクトをトランスポートプロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="b5390-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="b5390-116">トランスポートプロバイダーは、メッセージのプロパティに、基になるメッセージングシステムのデータを格納し、message オブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5390-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="b5390-117">メッセージストアプロバイダーは、通知方法を使用して、登録されているクライアントに新しいメッセージが到着したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="b5390-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="b5390-118">MAPI スプーラーは、メッセージストアの[IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5390-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b5390-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5390-119">See also</span></span>



<span data-ttu-id="b5390-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="b5390-120">[Message Store Features](message-store-features.md)</span></span>

