---
title: フォルダーの内容のテーブルを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580797"
---
# <a name="displaying-a-folder-contents-table"></a>フォルダーの内容のテーブルを表示します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーの内容のテーブルには、そのメッセージのすべてについての概要情報が含まれています。 メッセージ クラスに対応する受信フォルダーの内容のテーブルで、新しい着信メッセージについての概要情報が表示されます。 この情報をユーザーが利用できるように、テーブルを取得し、適切な列と行を表示します。
  
**フォルダーの内容のテーブルを表示するには**
  
1. [IMsgStore::OpenEntry](imsgstore-openentry.md)テーブルを含むフォルダーのエントリ id を渡すことを呼び出します。
    
2. その内容のテーブルを開くにはフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出します。 
    
3. 特定の列を指定するテーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、必要な場合は、内容のテーブルの表示を制限します。 
    
4. 特定の行をフィルター選択するテーブルの[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出して、必要な場合は、内容のテーブルの表示を制限します。 場合は、たとえば、読み取ることがまだ設定されて、特定のメッセージ クラスのメッセージだけを表示するのには。 
    
    1. **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、目的のメッセージ クラス プロパティに一致する[SPropertyRestriction](spropertyrestriction.md)構造体にプロパティ制約を作成します。 
        
    2. プロパティ タグと MSGFLAG_UNREAD の値として**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) をマスクとして使用する[SBitMaskRestriction](sbitmaskrestriction.md)構造体では、ビットマスクの制限を作成します。
        
    3. プロパティは、ビットマスクの制限を結合する[SAndRestriction](sandrestriction.md)構造に制約を作成します。 
    
5. テーブルの[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出して、必要な場合は、内容のテーブルを並べ替えます。 
    
6. 処理の内容のテーブルからすべての行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 
    

