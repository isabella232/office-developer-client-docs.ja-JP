---
title: メッセージの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad891a9884e72aa352dc114232cd5951c590272f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585102"
---
# <a name="deleting-a-message"></a>メッセージの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが閉じていると、ユーザーがコンテンツのテーブルを表示するときに開いているし、ユーザーが読み取りまたはメッセージを削除できます。 メッセージを誤って削除してからユーザーを保護するためには、MAPI は、2 段階の処理としてメッセージの削除を定義します。
  
1. 削除済みアイテム フォルダーとして指定されているフォルダーに移動することによってメッセージに削除のマークを付ける: **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) のプロパティの識別子を持つエントリが格納されているフォルダーです。 
    
2. [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)メソッドを呼び出してメッセージを削除します。 
    
削除済みアイテム フォルダー以外のフォルダーにメッセージを削除するときに、削除対象としてマークします。 ユーザーが削除済みアイテム フォルダー内からメッセージを選択した場合にのみ、メッセージに物理的にから削除するかワークステーションです。 ユーザーが実際に削除を実行することを確認するプロンプトを表示できます。
  
 **メッセージを削除するのには**
  
1. ユーザーに間もなく削除は意図的なことを確認します。
    
2. 削除するフォルダーの親を決定します。 削除済みアイテム フォルダーまたは削除済みアイテム フォルダー内にサブフォルダーがある場合は、メッセージを削除するのには[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)を呼び出します。 
    
3. 削除済みアイテム フォルダー内のフォルダーが含まれていない場合、は、メッセージを削除済みアイテム フォルダーに移動するのには、MESSAGE_MOVE フラグを設定して[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)を呼び出します。 
    

