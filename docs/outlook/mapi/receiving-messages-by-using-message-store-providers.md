---
title: メッセージ ストア プロバイダーを使用したメッセージ受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590191"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="ed91e-103">メッセージ ストア プロバイダーを使用したメッセージ受信</span><span class="sxs-lookup"><span data-stu-id="ed91e-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="ed91e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed91e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed91e-105">メッセージ ストア プロバイダーは、受信メッセージの送信をサポートする必要はありません (メッセージを使用するには、トランスポート プロバイダーおよび MAPI スプーラーは、メッセージの配信場所としてプロバイダーを格納するは、機能をサポートする)。</span><span class="sxs-lookup"><span data-stu-id="ed91e-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="ed91e-106">ただし、メッセージ ストア プロバイダーが受信したメッセージの送信をサポートしていない場合、既定のメッセージ ストアとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="ed91e-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="ed91e-107">受信メッセージの送信をサポートするために、メッセージ ストア プロバイダーは、次の。</span><span class="sxs-lookup"><span data-stu-id="ed91e-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="ed91e-108">クライアント アプリケーションが受信メッセージを見つけることができますので、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドと[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed91e-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="ed91e-109">[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドをサポートして、MAPI スプーラーが新しいメッセージが到着したメッセージ ストア プロバイダーに通知できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ed91e-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="ed91e-110">通知を実装するは、クライアントが新しいメッセージの通知を登録できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ed91e-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="ed91e-111">通知はオプションですが、プロバイダーが実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed91e-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="ed91e-112">メッセージ ・ ストアに受信メッセージが配信されるときに発生する一連のメソッド呼び出しは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ed91e-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="ed91e-113">MAPI スプーラーは、 [IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを取得するのには [受信トレイ] の[エントリ Id](entryid.md)を持つ[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="ed91e-114">MAPI スプーラーは、新しいメッセージ オブジェクトを取得する[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="ed91e-115">MAPI スプーラーは、トランスポート プロバイダーへのメッセージ オブジェクトを渡します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="ed91e-116">トランスポート プロバイダーは、基になるメッセージング システムからのデータをメッセージのプロパティを格納し、メッセージ オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="ed91e-117">メッセージ ストア プロバイダーは、新しいメッセージが到着した登録済みのクライアントに通知するのには、通知方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="ed91e-118">MAPI スプーラーでは、メッセージ ストアの[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ed91e-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ed91e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed91e-119">See also</span></span>



<span data-ttu-id="ed91e-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="ed91e-120">[Message Store Features](message-store-features.md)</span></span>

