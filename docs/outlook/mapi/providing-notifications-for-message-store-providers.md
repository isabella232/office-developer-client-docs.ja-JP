---
title: メッセージ ストア プロバイダーへの通知の提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419934"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="a722b-103">メッセージ ストア プロバイダーへの通知の提供</span><span class="sxs-lookup"><span data-stu-id="a722b-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="a722b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a722b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a722b-105">通知はオプションですが、優れたメッセージ ストア プロバイダーの非常に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="a722b-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="a722b-106">クライアント アプリケーションと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知に依存して、送信メッセージの送信時や受信メッセージの受信時に優れたパフォーマンスを得る。</span><span class="sxs-lookup"><span data-stu-id="a722b-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="a722b-107">クライアントと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知を受信せずに機能できますが、メッセージ ストア内の変更をユーザーに通知する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a722b-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="a722b-108">通常、これは、クライアントが次にメッセージ ストアの受信フォルダーを開くまで、新しいメッセージが届いたのをユーザーが確認できないという意味です。</span><span class="sxs-lookup"><span data-stu-id="a722b-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="a722b-109">クライアントは [、IMsgStore::Advise](imsgstore-advise.md) メソッドを呼び出して通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="a722b-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="a722b-110">クライアントは [、IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)インターフェイス、クライアントが受信に関心を持つ通知の種類を示すビットマスク、およびメッセージ ストア内の Advise 要求が適用されるオブジェクトを示す **EntryID** を渡します。</span><span class="sxs-lookup"><span data-stu-id="a722b-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="a722b-111">関連するイベントがオブジェクトで発生した場合 (たとえば、メッセージ ストアの受信フォルダーに新しいメッセージが到着した場合)、メッセージ ストア プロバイダーまたはオブジェクト自体は、そのイベントの種類に登録されている[IMAPIAdviseSink オブジェクトのすべてについて IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="a722b-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="a722b-112">メッセージ ストア プロバイダーがメッセージ ストア内の変更を他の MAPI コンポーネントに通知しない場合でも **、IMsgStore::Advise** を実装してメッセージ ストアを返す必要MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="a722b-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="a722b-113">これにより、メッセージ ストア プロバイダーからの通知を期待しない他のコンポーネントに通知されます。</span><span class="sxs-lookup"><span data-stu-id="a722b-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a722b-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a722b-114">See also</span></span>



<span data-ttu-id="a722b-115">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="a722b-115">[Message Store Features](message-store-features.md)</span></span>

