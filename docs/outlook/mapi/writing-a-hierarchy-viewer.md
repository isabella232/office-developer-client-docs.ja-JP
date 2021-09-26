---
title: 階層ビューアーの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 462d3ca97dacd231c167fb4834008f4ff79f5c08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619457"
---
# <a name="writing-a-hierarchy-viewer"></a>階層ビューアーの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
階層ビューアーは、フォルダーおよびアドレス帳コンテナー階層テーブルの表示に使用されるユーザー インターフェイス コンポーネントです。 階層ビューアーは、階層のメンバーを異なるレベルで表示し、各レベルをオンデマンドで拡張および契約できます。
  
container プロパティ **(PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)は、階層メンバーが表示されるレベルを制御します。 トップ レベルのアドレス帳コンテナーまたはフォルダーを表すエントリのプロパティPR_DEPTH **0** に設定されます。 このプロパティの値は、順次レベルのエントリに対して順次増分されます。 つまり、ユーザーが展開するトップ レベル のコンテナーを選択すると、すべてのコンテナーが1 に設定PR_DEPTH表示されます。 ユーザーがこれらのサブコンテナーの 1 **つ** を展開すると、コンテナーを 2 PR_DEPTHに設定して表示します。 
  
階層ビューアーは、さまざまな範囲の深度をサポートします。 閲覧者を 1 つまたは 2 つのレベルに制限するか、階層の拡大が優先される場合は複数のレベルをサポートできます。 
  
アドレス帳は、アドレス帳内のトップ レベル コンテナーの階層ビューアーを提供します。 
  
 **アドレス帳階層テーブルにアクセスするには**
  
1. [IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し、null エントリ識別子を渡して、アドレス帳のルート コンテナーを開きます。
    
2. MAPI アドレス帳の階層テーブルにアクセスするには、ルート コンテナーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出します。 
    
 **既定のメッセージ ストアの階層テーブルにアクセスするには**
  
1. [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出して、メッセージ ストア テーブルにアクセスします。 
    
2. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して制限を作成し、テーブルを PR_DEFAULT_STORE ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが **TRUE** に設定されている行にのみ制限します。 
    
3. [IMAPITable::FindRow](imapitable-findrow.md)を呼び出し **、SPropertyRestriction** を渡して、既定のメッセージ ストアを表す行を探します。 
    
4. [IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出し **、PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティをメッセージ ストア テーブルの既定のメッセージ ストアの行から渡します。
    
5. メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_IPM_SUBTREE_ENTRYID **(** [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。
    
6. メッセージ ストアの [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出し **、PR_IPM_SUBTREE_ENTRYID** プロパティを渡して、メッセージ ストアの IPM サブツリーのルート フォルダーを開きます。 
    
7. IPM ルート フォルダーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、その階層テーブルにアクセスします。 
    

