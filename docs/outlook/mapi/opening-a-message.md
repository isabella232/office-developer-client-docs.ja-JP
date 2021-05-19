---
title: メッセージを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411093"
---
# <a name="opening-a-message"></a><span data-ttu-id="e006f-103">メッセージを開く</span><span class="sxs-lookup"><span data-stu-id="e006f-103">Opening a message</span></span>
 
<span data-ttu-id="e006f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e006f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="e006f-105">メッセージを開く方法</span><span class="sxs-lookup"><span data-stu-id="e006f-105">To open a message</span></span>
  
1. <span data-ttu-id="e006f-106">次のいずれかのソースからメッセージのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e006f-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="e006f-107">親フォルダーのコンテンツ テーブル内のメッセージを表す行。</span><span class="sxs-lookup"><span data-stu-id="e006f-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="e006f-108">フォルダー コンテンツ テーブルの操作の詳細については、「コンテンツ テーブル」 [を参照してください](contents-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="e006f-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="e006f-109">新しいメール通知で送信 [NEWMAIL_NOTIFICATION構造体の](newmail_notification.md) **lpEntryID** メンバー。</span><span class="sxs-lookup"><span data-stu-id="e006f-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="e006f-110">通知の受信と処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="e006f-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="e006f-111">メッセージの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドへの呼び出しで、PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="e006f-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="e006f-112">次のいずれかの **OpenEntry** メソッドを呼び出してメッセージを開き  _、lpEntryID_ をメッセージのエントリ識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="e006f-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="e006f-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e006f-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="e006f-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e006f-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="e006f-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e006f-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="e006f-116">最速のメソッドは受信メッセージでのみ使用できます。受信フォルダーの **IMAPIFolder::OpenEntry** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e006f-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="e006f-117">メッセージ ストアの **IMsgStore::OpenEntry** メソッドを呼び出す次の最速のメソッドは **、IMAPISession::OpenEntry** を呼び出す最も遅いメソッドと同様に、すべてのメッセージで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e006f-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e006f-118">フォルダーとそのコンテンツ テーブルは、その中から開いたメッセージに悪影響を及ぼさずに、いつでも閉じられます。</span><span class="sxs-lookup"><span data-stu-id="e006f-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="e006f-119">ディスクに保存されているメッセージを開く方法</span><span class="sxs-lookup"><span data-stu-id="e006f-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="e006f-120">**StgOpenStorage を呼** び出して **IStorage** インターフェイス ポインターを取得し _、pwcsName_ パラメーターのメッセージ ファイルの名前を渡します。</span><span class="sxs-lookup"><span data-stu-id="e006f-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="e006f-121">**OpenIMsgOnIStg を呼** び出して **、メッセージ** にアクセスする IMessage インターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="e006f-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


