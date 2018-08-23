---
title: メッセージの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 68a842ccfdaea8ecdb975e1c510711b0e43fd576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803842"
---
# <a name="sending-a-message"></a><span data-ttu-id="78b54-103">メッセージの送信</span><span class="sxs-lookup"><span data-stu-id="78b54-103">Sending a Message</span></span>

  
  
<span data-ttu-id="78b54-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78b54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78b54-105">メッセージを送信する準備ができたら、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="78b54-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="78b54-106">**SubmitMessage**では、発信キューにメッセージを配置し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティで、MSGFLAG_SUBMIT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="78b54-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="78b54-107">メッセージ ストア プロバイダーでは、トランスポート プロバイダーでは、密に結合されている場合は、メッセージング システムに配信するトランスポートに直接メッセージを示します。</span><span class="sxs-lookup"><span data-stu-id="78b54-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="78b54-108">されていない場合は、発信キューが変更された MAPI スプーラー通知メッセージ ストア プロバイダーを組み合わせることで、緊密にし MAPI スプーラーは、適切なトランスポート プロバイダーにメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="78b54-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="78b54-109">送信操作をキャンセルするユーザーを許可する場合は、この機能を実装するために[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="78b54-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="78b54-110">**AbortSubmit**では、発信キューからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="78b54-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="78b54-111">ユーザーは、基になるメッセージング システムにメッセージが指定されるまでに発生してから、送信を停止するのにはできることができます。</span><span class="sxs-lookup"><span data-stu-id="78b54-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="78b54-112">**SubmitMessage**では、MAPI_E_CORRUPT_DATA が返された場合を想定しています送信されるデータが失われるようになりました。</span><span class="sxs-lookup"><span data-stu-id="78b54-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="78b54-113">2 番目の時間を送信する前に、 [IMAPIProp::SetProps](imapiprop-setprops.md)と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すことによって、メッセージを再書き込みします。</span><span class="sxs-lookup"><span data-stu-id="78b54-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="78b54-114">**IMAPIProp**のこれらの呼び出しが失敗した場合、または**SubmitMessage**には、2 回目が失敗した場合は、ユーザーにエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="78b54-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="78b54-115">**SubmitMessage**を正常に呼び出し、受信者の一覧に割り当てられたメモリをすべて解放し、メッセージとその添付ファイルを解放します。</span><span class="sxs-lookup"><span data-stu-id="78b54-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="78b54-116">メッセージが送信されると、MAPI にはこれらのオブジェクトのポインターをその他の操作はできません。</span><span class="sxs-lookup"><span data-stu-id="78b54-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="78b54-117">1 つの例外が**リ ス**を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="78b54-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="78b54-118">多くのメッセージ ストア プロバイダーに送信されたメッセージのエントリ id が無効になるために、他の呼び出しは許可されません。</span><span class="sxs-lookup"><span data-stu-id="78b54-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

