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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339936"
---
# <a name="displaying-a-folder-contents-table"></a>フォルダー コンテンツ テーブルの表示

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの contents テーブルには、すべてのメッセージに関する概要情報が含まれています。 新しい受信メッセージに関する概要情報は、メッセージクラスの受信フォルダーのコンテンツテーブルに表示されます。 ユーザーがこの情報を使用できるようにするには、テーブルを取得し、必要に応じて列と行を表示します。
  
**フォルダコンテンツテーブルを表示するには**
  
1. [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出し、テーブルを含むフォルダーのエントリ識別子を渡します。
    
2. フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、そのコンテンツテーブルを開きます。 
    
3. 必要に応じて、テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して特定の列を指定することによって、contents テーブルの表示を制限します。 
    
4. 必要に応じて、テーブルの[IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出して、特定の行をフィルター処理することによって、contents テーブルの表示を制限します。 たとえば、まだ読まれていない特定のメッセージクラスを持つメッセージのみを表示する場合は、次のようにします。 
    
    1. **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティと目的のメッセージクラスを一致させるプロパティ制限を[spropertyrestriction](spropertyrestriction.md)構造で作成します。 
        
    2. **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) をプロパティタグとして使用し、MSGFLAG_UNREAD 値をマスクとして使用する[sbitmaskrestriction](sbitmaskrestriction.md)構造で、ビットマスク制限を作成します。
        
    3. プロパティとビットマスク制限を結合する[SAndRestriction](sandrestriction.md)構造で制限を作成します。 
    
5. 必要に応じて、テーブルの[IMAPITable:: sorttable](imapitable-sorttable.md)メソッドを呼び出して、コンテンツテーブルを並べ替えます。 
    
6. 処理のために contents テーブルからすべての行を取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。 
    

