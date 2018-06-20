---
title: 階層ビューアーを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804241"
---
# <a name="writing-a-hierarchy-viewer"></a>階層ビューアーを作成します。

  
  
**適用されます**: Outlook 
  
階層ビューアーは、フォルダーとアドレス帳コンテナーの階層テーブルを表示するために使用されるユーザー インターフェイス コンポーネントです。 階層ビューアーでは、さまざまなレベル、オン ・ デマンドでの各レベルを変更することで、階層のメンバーを表示できます。
  
コンテナーのプロパティ、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) は、階層のメンバーを表示するレベルを制御します。 最上位のアドレス帳コンテナーまたはフォルダーを表すエントリがある、 **PR_DEPTH**プロパティを 0 に設定します。 このプロパティの値は連続したレベルにあるエントリを順に増加します。 ユーザーが最上位のコンテナーを展開し、表示するを選択すると**PR_DEPTH**を持つすべてのコンテナーは 1 に設定します。 ユーザーには、これらのサブコンテナーのいずれかが拡張されと 2、 **PR_DEPTH**のセットを使用してコンテナーを表示するように。 
  
階層ビューアーでは、深さの別の範囲をサポートします。 ビューアーに 1 つまたは 2 つのレベルを制限することや、複数のレベルをサポートするには、優先度、拡張性のある階層を表示する場合。 
  
アドレス帳には、アドレス帳内の最上位のコンテナーの階層ビューアーが用意されています。 
  
 **アドレス帳の階層テーブルにアクセスするには**
  
1. [アドレス帳コンテナー](iaddrbook-openentry.md)を null のエントリの識別子を渡すことを開くには、アドレス帳のルート コンテナーを呼び出します。
    
2. MAPI アドレス帳の階層テーブルにアクセスするためのルート コンテナーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出します。 
    
 **既定のメッセージ ストアの階層テーブルにアクセスするには**
  
1. メッセージ ストアにアクセスする[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出します。 
    
2. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが TRUE に設定を持つ行のみのテーブルを制限する制約を作成します。 
    
3. [IMAPITable::FindRow](imapitable-findrow.md)を渡すことを**SPropertyRestriction**既定のメッセージ ストアを表す行を検索するを呼び出します。 
    
4. [IMAPISession::OpenEntry](imapisession-openentry.md)既定のメッセージ ストアのテーブルの行のメッセージ ストアから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティに渡すことを呼び出します。
    
5. **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。
    
6. メッセージ ストアの IPM サブツリーのルート フォルダーを開く、 **PR_IPM_SUBTREE_ENTRYID**プロパティを渡すメッセージ ストアの[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出します。 
    
7. 階層テーブルにアクセスするための IPM のルート フォルダーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出します。 
    

