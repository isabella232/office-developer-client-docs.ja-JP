---
title: メッセージを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0701e64469576a8241002a6ff11299d1c343556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582981"
---
# <a name="opening-a-message"></a><span data-ttu-id="5a81f-103">メッセージを開く</span><span class="sxs-lookup"><span data-stu-id="5a81f-103">Opening a message</span></span>
 
<span data-ttu-id="5a81f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a81f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="5a81f-105">メッセージを開く</span><span class="sxs-lookup"><span data-stu-id="5a81f-105">To open a message</span></span>
  
1. <span data-ttu-id="5a81f-106">以下のいずれかからのメッセージのエントリ id を取得します。</span><span class="sxs-lookup"><span data-stu-id="5a81f-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="5a81f-107">親フォルダーの内容のテーブル内のメッセージを表す行です。</span><span class="sxs-lookup"><span data-stu-id="5a81f-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="5a81f-108">フォルダー コンテンツ テーブルの操作に関する詳細については、[内容のテーブル](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a81f-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="5a81f-109">**LpEntryID** 、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体のメンバーで新着メールの通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="5a81f-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="5a81f-110">受信と処理の通知の詳細については、[通知の処理](handling-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a81f-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="5a81f-111">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを要求するメッセージの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="5a81f-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="5a81f-112">次のいずれかの**OpenEntry**を開くには、メッセージ、メッセージのエントリ id を設定_lpEntryID_を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5a81f-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="5a81f-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5a81f-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="5a81f-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5a81f-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="5a81f-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5a81f-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="5a81f-116">最も速い方法は、受信メッセージに対してのみ使用可能な受信フォルダーの**IMAPIFolder::OpenEntry**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a81f-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="5a81f-117">メッセージ ストアの**IMsgStore::OpenEntry**メソッドを呼び出して、次の最も高速な方法は**IMAPISession::OpenEntry**を呼び出して、最も低速な方法は、すべてのメッセージに対して使用可能。</span><span class="sxs-lookup"><span data-stu-id="5a81f-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5a81f-118">フォルダーとその内容のテーブルは、その中から開かれているメッセージのいずれかの影響を及ぼすことがなくいつでも終了できます。</span><span class="sxs-lookup"><span data-stu-id="5a81f-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="5a81f-119">ディスクに保存されているメッセージを開く</span><span class="sxs-lookup"><span data-stu-id="5a81f-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="5a81f-120">_PwcsName_パラメーターのメッセージ ファイルの名前を渡して、 **IStorage**インターフェイス ポインターを取得するために**StgOpenStorage**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5a81f-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="5a81f-121">メッセージへのアクセス、 **IMessage**インターフェイス ポインターを取得するために**OpenIMsgOnIStg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5a81f-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


