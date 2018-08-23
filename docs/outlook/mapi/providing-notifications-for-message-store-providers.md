---
title: メッセージ ストア プロバイダー用の通知の提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3722893ae57a108b338725e46c975e92c0f8ff72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587510"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="47c95-103">メッセージ ストア プロバイダー用の通知の提供</span><span class="sxs-lookup"><span data-stu-id="47c95-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="47c95-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c95-105">通知は省略可能ですが、適切なメッセージ ストア プロバイダーの非常に重要な含まにはれています。</span><span class="sxs-lookup"><span data-stu-id="47c95-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="47c95-106">クライアント アプリケーションと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知メッセージを送信または受信側の受信メッセージを送信するときに、良好なパフォーマンスを取得するに依存します。</span><span class="sxs-lookup"><span data-stu-id="47c95-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="47c95-107">クライアントと、MAPI スプーラーは、メッセージ ストア プロバイダーから通知を受信する前に機能できますが、変更せずにメッセージ ・ ストア内のユーザーに通知することはできません。</span><span class="sxs-lookup"><span data-stu-id="47c95-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="47c95-108">通常、ユーザーが、クライアントは、メッセージ ストアを次に開くまで、新しいメッセージが到着したことを確認することことを意味では、フォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="47c95-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="47c95-109">クライアントは、 [IMsgStore::Advise](imsgstore-advise.md)メソッドを呼び出して、通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47c95-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="47c95-110">クライアントのパスで、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェースは、クライアントが受け取るでは通知の種類を示すビットマスク、**アドバイズ**を格納、メッセージのどのオブジェクトを示す**エントリ Id**要求に適用されます。</span><span class="sxs-lookup"><span data-stu-id="47c95-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="47c95-111">オブジェクト (たとえば、メッセージ ・ ストア内の受信フォルダーに新しいメッセージが到着したときなど) に関連するイベントが発生すると、メッセージ ストア プロバイダーまたはオブジェクト自体はメソッドを呼び出す[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) **のすべてのIMAPIAdviseSink**そのイベントの種類に対して登録されているオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="47c95-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="47c95-112">場合でも、メッセージの格納プロバイダー決して通知メッセージ ・ ストア内の変更の場合は、他の MAPI コンポーネント MAPI_E_NO_SUPPORT を取得する**IMsgStore::Advise**を実装する必要がありますが、します。</span><span class="sxs-lookup"><span data-stu-id="47c95-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="47c95-113">プロバイダーを格納、メッセージからの通知が他のコンポーネントに通知されます。</span><span class="sxs-lookup"><span data-stu-id="47c95-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47c95-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="47c95-114">See also</span></span>



<span data-ttu-id="47c95-115">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="47c95-115">[Message Store Features](message-store-features.md)</span></span>

