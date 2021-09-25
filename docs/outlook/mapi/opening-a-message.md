---
title: メッセージを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d74e26f2968758f31a410a428bd75b70803e5141
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555952"
---
# <a name="opening-a-message"></a>メッセージを開く
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>メッセージを開く方法
  
1. 次のいずれかのソースからメッセージのエントリ識別子を取得します。
    
   - 親フォルダーのコンテンツ テーブル内のメッセージを表す行。 フォルダー コンテンツ テーブルの操作の詳細については、「コンテンツ テーブル」 [を参照してください](contents-tables.md)。
    
   - 新しいメール通知で送信 [NEWMAIL_NOTIFICATION構造体の](newmail_notification.md) **lpEntryID** メンバー。 通知の受信と処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。
    
   - メッセージの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドへの呼び出しで、PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求します。 
    
2. 次のいずれかの **OpenEntry** メソッドを呼び出してメッセージを開き  _、lpEntryID_ をメッセージのエントリ識別子に設定します。 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  最速のメソッドは受信メッセージでのみ使用できます。受信フォルダーの **IMAPIFolder::OpenEntry** メソッドを呼び出す必要があります。 メッセージ ストアの **IMsgStore::OpenEntry** メソッドを呼び出す次の最速のメソッドは **、IMAPISession::OpenEntry** を呼び出す最も遅いメソッドと同様に、すべてのメッセージで使用できます。
    
> [!NOTE]
> フォルダーとそのコンテンツ テーブルは、その中から開いたメッセージに悪影響を及ぼさずに、いつでも閉じられます。 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>ディスクに保存されているメッセージを開く方法
  
1. **StgOpenStorage を呼** び出して **IStorage** インターフェイス ポインターを取得し _、pwcsName_ パラメーターのメッセージ ファイルの名前を渡します。 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. **OpenIMsgOnIStg を呼** び出して **、メッセージ** にアクセスする IMessage インターフェイス ポインターを取得します。 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


