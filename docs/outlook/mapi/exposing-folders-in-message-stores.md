---
title: ���b�Z�[�W�̃X�g�A��̃t�H���_�[����J���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb6134d462dbe7541e7672b5a684bc6af51a0d86
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596485"
---
# <a name="exposing-folders-in-message-stores"></a>メッセージ ストアのフォルダーの公開

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications. 
  
クライアント アプリケーションは、_cbEntryId_、_lpEntryId_ パラメーターにそれぞれ 0、Null 値を指定して [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出し、最上位フォルダーを開くことができます。ただし、ほとんどの場合、クライアント アプリケーションは IPM メッセージが格納された一連のフォルダーを開きます。 
  
To get a list of folders in the message store's IPM folder tree, use the following procedure:
  
1. MAPI セッションを使って、[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出します。 
    
2. 結果として得られたメッセージ データベースのポインターを使って、**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出します。
    
3. エントリ識別子付きの [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出して、**IMAPIFolder** ポインターを取得します。 
    
4. �t�H���_�[�̓�e�̃e�[�u����擾����[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)���\�b�h��Ăяo���܂��B 
    
5. Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder. 
    
MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのフォルダーの実装](implementing-folders-in-message-stores.md)

