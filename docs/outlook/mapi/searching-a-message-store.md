---
title: メッセージ ストアを検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571837"
---
# <a name="searching-a-message-store"></a>メッセージ ストアを検索

**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアント アプリケーションは、検索条件に一致するメッセージを探して、1 つまたは複数のフォルダーを検索できます。 最も簡単な検索方法は、抽出条件を定義するのには制限を適用する必要があり、または以前の検索の検索条件に明示的に作成、検索結果フォルダーに結果を配置すること。 すべてのメッセージ ストアは、この手法をサポートします。 

決定するかどうか、メッセージ ・ ストアを使用しているをサポートしている検索結果フォルダーを使用して、取得するために[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出す、 **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティです。 STORE_SEARCH_OK フラグが設定されている場合に、検索はサポートされています。 設定されていない場合は、ターゲット フォルダーを手動で検査などの別の方法をする必要があります。
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>メッセージ ストアに 1 つまたは複数のフォルダーを検索するには
  
1. 前の検索から検索結果フォルダーを使っている場合は、手順 2 に進みます。 それ以外の場合、検索結果フォルダーを作成します。
    
    1. 検索結果のルート フォルダーのエントリ id を取得するには、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を要求します。
        
    2. PR_FINDER_ENTRYID によって表されるフォルダーを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
        
    3. メソッドを呼び出してフォルダーの[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を FOLDER_SEARCH フラグを設定して、[検索結果] フォルダーを作成します。 
    
2. 検索条件を保持するために制限を作成します。 
    
3. 検索するフォルダーを表すエントリの識別子の配列を作成します。 使用されています。 検索結果のフォルダーと同じフォルダーを検索する場合、この手順は必要ではありません。
    
4. エントリの識別子の配列を制限する_lpRestriction_ _lpContainerList_を参照、検索結果フォルダーの[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。 
    
5. メッセージ ・ ストアの検索の完了通知を登録する場合は、到着を通知するため待機します。
    
6. 検索結果の内容のテーブルにアクセスするためのフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すことによって、検索結果を表示します。 
    
7. 内容の検索条件を満たすメッセージを取得するテーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。 
    

