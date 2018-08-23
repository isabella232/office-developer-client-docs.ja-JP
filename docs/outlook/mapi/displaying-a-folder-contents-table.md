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
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799944"
---
# <a name="displaying-a-folder-contents-table"></a>フォルダーの内容のテーブルを表示します。

**適用対象**: Outlook 
  
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
    

