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
# <a name="sending-a-message"></a><span data-ttu-id="a656c-103">メッセージを送信する</span><span class="sxs-lookup"><span data-stu-id="a656c-103">Sending a Message</span></span>

  
  
<span data-ttu-id="a656c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a656c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a656c-105">メッセージを送信する準備ができたら、 [その IMessage::SubmitMessage メソッドを呼び出](imessage-submitmessage.md) します。</span><span class="sxs-lookup"><span data-stu-id="a656c-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a656c-106">**SubmitMessage** は、メッセージを送信キューに入れ、メッセージの MSGFLAG_SUBMIT **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに PR_MESSAGE_FLAGS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a656c-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a656c-107">メッセージ ストア プロバイダーは、トランスポート プロバイダーと緊密に結合されている場合、メッセージをメッセージング システムに配信するトランスポートに直接送信します。</span><span class="sxs-lookup"><span data-stu-id="a656c-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="a656c-108">密に結合されていない場合、メッセージ ストア プロバイダーは、送信キューが変更されたと MAPI スプーラーに通知し、MAPI スプーラーはメッセージを適切なトランスポート プロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="a656c-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="a656c-109">ユーザーが送信操作をキャンセルできる場合は [、IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) を呼び出してこの機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="a656c-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="a656c-110">**AbortSubmit** は、送信キューからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a656c-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="a656c-111">メッセージが基になるメッセージング システムに与えられるまで、ユーザーは送信を停止できます。</span><span class="sxs-lookup"><span data-stu-id="a656c-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="a656c-112">**SubmitMessage が** データを返MAPI_E_CORRUPT_DATA、送信されるデータが失われたと仮定します。</span><span class="sxs-lookup"><span data-stu-id="a656c-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="a656c-113">2 回目の送信を試みる前に [、IMAPIProp::SetProps](imapiprop-setprops.md) と [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを書き戻します。</span><span class="sxs-lookup"><span data-stu-id="a656c-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="a656c-114">これらの **IMAPIProp** 呼び出しが失敗した場合、または SubmitMessage が **2** 度目に失敗した場合は、ユーザーにエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="a656c-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="a656c-115">SubmitMessage の呼び **出しが成功** した後、受信者リストに割り当てられたメモリを解放し、メッセージとその添付ファイルを解放します。</span><span class="sxs-lookup"><span data-stu-id="a656c-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="a656c-116">メッセージが送信された後、MAPI は、これらのオブジェクトのポインターに対するそれ以上の操作を許可しません。</span><span class="sxs-lookup"><span data-stu-id="a656c-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="a656c-117">1 つの例外は **、IUnknown::Release を呼び出しています**。</span><span class="sxs-lookup"><span data-stu-id="a656c-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="a656c-118">多くのメッセージ ストア プロバイダーが送信されたメッセージのエントリ識別子を無効にしたため、他の呼び出しは許可されません。</span><span class="sxs-lookup"><span data-stu-id="a656c-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

