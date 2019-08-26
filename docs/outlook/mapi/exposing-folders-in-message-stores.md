---
title: メッセージ ストアのフォルダーの公開
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341350"
---
# <a name="exposing-folders-in-message-stores"></a>メッセージ ストアのフォルダーの公開

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのメッセージ ストア プロバイダーは、クライアント アプリケーションに最上位の [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスを提示する必要があります。最上位フォルダーは、メッセージ ストア全体に対応し、メッセージ ストアの内容としてユーザーに表示されるフォルダーへのアクセスを提供します。さらに、最上位フォルダーは、IPC メッセージの既定の受信フォルダーや、既読レポートが送信されるフォルダーとしてもよく使用されます。メッセージ ストア プロバイダーはまた、クライアント アプリケーションに IPM メッセージの格納に使用する一連のフォルダーである、IPM サブツリーも提示する必要があります。 
  
クライアント アプリケーションは、_cbEntryId_、_lpEntryId_ パラメーターにそれぞれ 0、Null 値を指定して [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出し、最上位フォルダーを開くことができます。ただし、ほとんどの場合、クライアント アプリケーションは IPM メッセージが格納された一連のフォルダーを開きます。 
  
メッセージ ストアの IPM フォルダー ツリーにあるフォルダーのリストを取得するには、次のプロシージャを使用します。
  
1. MAPI セッションを使って、[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出します。 
    
2. 結果として得られたメッセージ データベースのポインターを使って、**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出します。
    
3. エントリ識別子付きの [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出して、**IMAPIFolder** ポインターを取得します。 
    
4. [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、フォルダーの目次を取得します。 
    
5. [IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、最上位フォルダー内のフォルダーを一覧表示します。 
    
MAPI クライアントは、これらのフォルダーを使用して、メッセージ ストア内の他のフォルダー オブジェクトやメッセージ オブジェクトにアクセスします。**IMAPIFolder** とその親インターフェイスである [IMAPIContainer](imapicontainerimapiprop.md) には、メッセージ ストア プロバイダーがフォルダーにメッセージ オブジェクトを追加し、クライアントの要求に応えてメッセージを処理するうえで、実装する必要のあるメソッドが含まれています。
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのフォルダーの実装](implementing-folders-in-message-stores.md)

