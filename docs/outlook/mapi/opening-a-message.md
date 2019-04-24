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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348609"
---
# <a name="opening-a-message"></a><span data-ttu-id="ffddc-103">メッセージを開く</span><span class="sxs-lookup"><span data-stu-id="ffddc-103">Opening a message</span></span>
 
<span data-ttu-id="ffddc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="ffddc-105">メッセージを開くには</span><span class="sxs-lookup"><span data-stu-id="ffddc-105">To open a message</span></span>
  
1. <span data-ttu-id="ffddc-106">次のいずれかのソースからメッセージのエントリ id を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffddc-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="ffddc-107">親フォルダーの contents テーブル内のメッセージを表す行。</span><span class="sxs-lookup"><span data-stu-id="ffddc-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="ffddc-108">folder contents テーブルを使用した作業の詳細については、「 [contents Tables](contents-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffddc-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="ffddc-109">新しいメール通知と共に送信される[NEWMAIL_NOTIFICATION](newmail_notification.md)構造の**lて tryid**メンバ。</span><span class="sxs-lookup"><span data-stu-id="ffddc-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="ffddc-110">通知の受信および処理の詳細については、「[通知の処理](handling-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffddc-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="ffddc-111">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求しているメッセージの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドへの呼び出し。</span><span class="sxs-lookup"><span data-stu-id="ffddc-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="ffddc-112">メッセージを開くには、次のいずれかの**openentry**メソッドを呼び出します。メッセージのエントリ識別子に_lな tryid_を設定します。</span><span class="sxs-lookup"><span data-stu-id="ffddc-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="ffddc-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ffddc-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="ffddc-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ffddc-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="ffddc-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ffddc-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="ffddc-116">最も高速なメソッドは、受信メッセージに対してのみ使用できます。また、受信フォルダーの**imapifolder:: openentry**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffddc-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="ffddc-117">次の最も高速な方法は、メッセージストアの**IMsgStore:: openentry**メソッドを呼び出すのと同じように、 **imapisession:: openentry**を呼び出すことにより、すべてのメッセージで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffddc-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ffddc-118">フォルダーとその内容テーブルは、いつでも、その中から開いたメッセージに悪影響を与えることなく閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="ffddc-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="ffddc-119">ディスクに保存されているメッセージを開くには</span><span class="sxs-lookup"><span data-stu-id="ffddc-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="ffddc-120">**StgOpenStorage**を呼び出して、 **IStorage**インターフェイスポインターを取得し、 _pwcsName_パラメーターのメッセージファイルの名前を渡します。</span><span class="sxs-lookup"><span data-stu-id="ffddc-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="ffddc-121">**OpenIMsgOnIStg**を呼び出して、メッセージにアクセスするための**IMessage**インターフェイスポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="ffddc-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


