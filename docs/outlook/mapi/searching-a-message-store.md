---
title: メッセージ ストアの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8ed987a558b90c22682fd050bf9d1e456eda964f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591172"
---
# <a name="searching-a-message-store"></a>メッセージ ストアの検索

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションは、検索条件に一致するメッセージを検索する 1 つ以上のフォルダーを検索できます。 最も簡単な検索方法は、条件を定義する制限を適用し、この検索または以前の検索用に明示的に作成された検索結果フォルダーに結果を配置する方法です。 一部のメッセージ ストアでは、この手法がサポートされている必要があります。 

使用しているメッセージ ストアが検索結果フォルダーの使用をサポートするかどうかを確認するには [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。 このフラグSTORE_SEARCH_OK設定されている場合は、検索がサポートされます。 設定されていない場合は、ターゲット フォルダーを手動で検査するなどの別の方法が必要です。
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>メッセージ ストア内の 1 つ以上のフォルダーを検索するには
  
1. 以前の検索から検索結果フォルダーがある場合は、手順 2 に進みます。 それ以外の場合は、検索結果フォルダーを作成します。
    
    1. メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出し、PR_FINDER_ENTRYID ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)を要求して、検索結果 **ルート** フォルダーのエントリ識別子を取得します。
        
    2. [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して、ユーザーが表すフォルダーを開PR_FINDER_ENTRYID。 
        
    3. フォルダーの [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) メソッドを呼び出して、検索結果フォルダーを作成し、FOLDER_SEARCH設定します。 
    
2. 検索条件を保持するための制限を作成します。 
    
3. 検索するフォルダーを表すエントリ識別子の配列を作成します。 検索結果フォルダーが以前に使用され、同じフォルダーを検索する場合は、この手順は不要です。
    
4. 検索結果フォルダーの [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドを呼び出し  _、lpContainerList_ をエントリ識別子配列に  _、lpRestriction_ を制限に指定します。 
    
5. メッセージ ストアで検索完了通知を登録している場合は、通知が届くのを待ちます。
    
6. 検索結果フォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出して、そのコンテンツ テーブルにアクセスして、検索の結果を表示します。 
    
7. コンテンツ テーブルの [IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、検索条件を満たすメッセージを取得します。 
    

