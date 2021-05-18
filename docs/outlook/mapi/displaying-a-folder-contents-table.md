---
title: フォルダー コンテンツ テーブルの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412395"
---
# <a name="displaying-a-folder-contents-table"></a>フォルダー コンテンツ テーブルの表示

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーのコンテンツ テーブルには、すべてのメッセージに関する概要情報が含まれます。 新しい受信メッセージに関する概要情報が、メッセージ クラスの受信フォルダーのコンテンツ テーブルに表示されます。 この情報をユーザーが利用するには、テーブルを取得し、必要に応じて列と行を表示します。
  
**フォルダーの内容テーブルを表示するには**
  
1. [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出し、テーブルを含むフォルダーのエントリ識別子を渡します。
    
2. フォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出して、そのコンテンツ テーブルを開きます。 
    
3. テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md) メソッドを呼び出して特定の列を指定することで、必要に応じてコンテンツ テーブルのビューを制限します。 
    
4. テーブルの [IMAPITable::Restrict](imapitable-restrict.md) メソッドを呼び出して特定の行をフィルター処理することで、必要に応じてコンテンツ テーブルのビューを制限します。 たとえば、まだ読み取っていない特定のメッセージ クラスを持つメッセージのみを表示する場合は、次の処理を行います。 
    
    1. 目的のメッセージ クラスと PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティと一致する [SPropertyRestriction](spropertyrestriction.md)構造体にプロパティ制限を作成します。 
        
    2. プロパティ タグとして PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) を使用し、マスクとして **MSGFLAG_UNREAD** 値を使用する [SBitMaskRestriction](sbitmaskrestriction.md)構造体にビットマスク制限を作成します。
        
    3. プロパティとビットマスク [の制限に参加する SAndRestriction](sandrestriction.md) 構造体に制限を作成します。 
    
5. 必要に応じて、テーブルの [IMAPITable::SortTable](imapitable-sorttable.md) メソッドを呼び出して、コンテンツ テーブルを並べ替えてください。 
    
6. [IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出して、処理のためにコンテンツ テーブルからすべての行を取得します。 
    

