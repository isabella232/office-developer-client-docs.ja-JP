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
# <a name="opening-a-message"></a>メッセージを開く
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>メッセージを開くには
  
1. 次のいずれかのソースからメッセージのエントリ id を取得します。
    
   - 親フォルダーの contents テーブル内のメッセージを表す行。 folder contents テーブルを使用した作業の詳細については、「 [contents Tables](contents-tables.md)」を参照してください。
    
   - 新しいメール通知と共に送信される[NEWMAIL_NOTIFICATION](newmail_notification.md)構造の**lて tryid**メンバ。 通知の受信および処理の詳細については、「[通知の処理](handling-notifications.md)」を参照してください。
    
   - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求しているメッセージの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドへの呼び出し。 
    
2. メッセージを開くには、次のいずれかの**openentry**メソッドを呼び出します。メッセージのエントリ識別子に_lな tryid_を設定します。 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  最も高速なメソッドは、受信メッセージに対してのみ使用できます。また、受信フォルダーの**imapifolder:: openentry**メソッドを呼び出す必要があります。 次の最も高速な方法は、メッセージストアの**IMsgStore:: openentry**メソッドを呼び出すのと同じように、 **imapisession:: openentry**を呼び出すことにより、すべてのメッセージで使用できます。
    
> [!NOTE]
> フォルダーとその内容テーブルは、いつでも、その中から開いたメッセージに悪影響を与えることなく閉じることができます。 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>ディスクに保存されているメッセージを開くには
  
1. **StgOpenStorage**を呼び出して、 **IStorage**インターフェイスポインターを取得し、 _pwcsName_パラメーターのメッセージファイルの名前を渡します。 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. **OpenIMsgOnIStg**を呼び出して、メッセージにアクセスするための**IMessage**インターフェイスポインターを取得します。 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


