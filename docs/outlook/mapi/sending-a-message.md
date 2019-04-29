---
title: メッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423623"
---
# <a name="sending-a-message"></a><span data-ttu-id="d61b3-103">メッセージを送信する</span><span class="sxs-lookup"><span data-stu-id="d61b3-103">Sending a Message</span></span>

  
  
<span data-ttu-id="d61b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d61b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d61b3-105">メッセージを送信する準備ができたら、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="d61b3-106">**submitmessage**は、メッセージを送信キューに配置し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに MSGFLAG_SUBMIT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d61b3-107">メッセージストアプロバイダーは、トランスポートプロバイダーと密に結び付けられている場合、メッセージをメッセージングシステムに配信するトランスポートに直接付与します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="d61b3-108">密結合されていない場合、メッセージストアプロバイダーは、送信キューが変更されたことを mapi スプーラーに通知し、mapi スプーラーは適切なトランスポートプロバイダーにメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="d61b3-109">ユーザーが送信操作を取り消すことができるようにする場合は、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)を呼び出してこの機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="d61b3-110">**abortsubmit**は、発信キューからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="d61b3-111">ユーザーは、メッセージが基になるメッセージングシステムに渡されるまで、送信を停止することを許可できます。</span><span class="sxs-lookup"><span data-stu-id="d61b3-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="d61b3-112">**submitmessage**が MAPI_E_CORRUPT_DATA を返す場合は、送信されるデータが失われたと仮定します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="d61b3-113">2回目の送信を試行する前に、 [imapiprop:: setprops](imapiprop-setprops.md)と[imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出して、メッセージを再度書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d61b3-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="d61b3-114">これらの**imapiprop**の呼び出しが失敗するか、または**submitmessage**が2回目に失敗した場合は、ユーザーにエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="d61b3-115">**submitmessage**を正常に呼び出した後、受信者リストに割り当てられているメモリを解放し、メッセージとその添付ファイルを解放します。</span><span class="sxs-lookup"><span data-stu-id="d61b3-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="d61b3-116">メッセージが送信されると、MAPI では、これらのオブジェクトのポインターに対して他の操作は許可されません。</span><span class="sxs-lookup"><span data-stu-id="d61b3-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="d61b3-117">1つの例外は、 **IUnknown:: Release**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="d61b3-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="d61b3-118">多くのメッセージストアプロバイダーは、送信されたメッセージのエントリ id を無効にするため、他の通話は許可されません。</span><span class="sxs-lookup"><span data-stu-id="d61b3-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

