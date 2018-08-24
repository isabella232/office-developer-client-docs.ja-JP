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
# <a name="opening-a-message"></a>メッセージを開く
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>メッセージを開く
  
1. 以下のいずれかからのメッセージのエントリ id を取得します。
    
   - 親フォルダーの内容のテーブル内のメッセージを表す行です。 フォルダー コンテンツ テーブルの操作に関する詳細については、[内容のテーブル](contents-tables.md)を参照してください。
    
   - **LpEntryID** 、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体のメンバーで新着メールの通知が送信されます。 受信と処理の通知の詳細については、[通知の処理](handling-notifications.md)を参照してください。
    
   - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを要求するメッセージの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出す。 
    
2. 次のいずれかの**OpenEntry**を開くには、メッセージ、メッセージのエントリ id を設定_lpEntryID_を呼び出します。 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  最も速い方法は、受信メッセージに対してのみ使用可能な受信フォルダーの**IMAPIFolder::OpenEntry**メソッドを呼び出す必要があります。 メッセージ ストアの**IMsgStore::OpenEntry**メソッドを呼び出して、次の最も高速な方法は**IMAPISession::OpenEntry**を呼び出して、最も低速な方法は、すべてのメッセージに対して使用可能。
    
> [!NOTE]
> フォルダーとその内容のテーブルは、その中から開かれているメッセージのいずれかの影響を及ぼすことがなくいつでも終了できます。 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>ディスクに保存されているメッセージを開く
  
1. _PwcsName_パラメーターのメッセージ ファイルの名前を渡して、 **IStorage**インターフェイス ポインターを取得するために**StgOpenStorage**を呼び出します。 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. メッセージへのアクセス、 **IMessage**インターフェイス ポインターを取得するために**OpenIMsgOnIStg**を呼び出します。 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


