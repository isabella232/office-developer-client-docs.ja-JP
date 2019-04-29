---
title: メッセージ ストアの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426038"
---
# <a name="searching-a-message-store"></a>メッセージ ストアの検索

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションは、検索条件に一致するメッセージを検索するために、1つまたは複数のフォルダーを検索できます。 最も単純な検索手法では、条件を定義し、その結果を検索結果フォルダーに格納する制限を適用して、この検索または以前の検索に対して明示的に作成します。 すべてのメッセージストアがこの手法をサポートするわけではありません。 

使用しているメッセージストアが検索結果フォルダーの使用をサポートしているかどうかを判断するには、 **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得するのには、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出します。 STORE_SEARCH_OK フラグが設定されている場合は、検索がサポートされます。 設定されていない場合は、ターゲットフォルダーを手動で検査するなどの別の方法が必要になります。
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>メッセージストア内の1つまたは複数のフォルダーを検索するには
  
1. 以前の検索からの検索結果フォルダーがある場合は、手順2に進みます。 それ以外の場合は、検索結果フォルダーを作成します。
    
    1. メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を要求することにより、検索結果のルートフォルダーのエントリ識別子を取得します。
        
    2. [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、PR_FINDER_ENTRYID によって表されるフォルダーを開きます。 
        
    3. フォルダーの[imapifolder:: CreateFolder](imapifolder-createfolder.md)メソッドを呼び出して、FOLDER_SEARCH フラグが設定された検索結果フォルダーを作成します。 
    
2. 検索条件を保持する制限を作成します。 
    
3. 検索するフォルダーを表すエントリ識別子の配列を作成します。 検索結果フォルダーが以前に使用されていて、同じフォルダーを検索する場合は、この手順は必要ありません。
    
4. 検索結果フォルダーの[IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出し、 _lpContainerList_をエントリ識別子の配列に、lpRestriction を制限に__ します。 
    
5. メッセージストアで検索完了通知を登録している場合は、通知が到着するまで待機します。
    
6. 検索結果フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、そのコンテンツテーブルにアクセスし、検索結果を表示します。 
    
7. コンテンツテーブルの[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、検索条件に一致するメッセージを取得します。 
    

