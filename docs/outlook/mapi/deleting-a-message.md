---
title: メッセージを削除する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433165"
---
# <a name="deleting-a-message"></a>メッセージを削除する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは開いているメッセージを削除することができ、ユーザーがメッセージを読んでいるとき、または閉じているときに、ユーザーが [コンテンツ] テーブルを表示しているときに、そのメッセージを削除することができます。 ユーザーが誤ってメッセージを削除しないようにするために、MAPI はメッセージの削除を2段階の手順で定義します。
  
1. 削除済みアイテムフォルダーとして指定されているフォルダー ( **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) プロパティにエントリ識別子が格納されているフォルダー) にメッセージを移動するようにマークします。 
    
2. [imapifolder::D eletemessages](imapifolder-deletemessages.md)メソッドを呼び出して、メッセージを削除します。 
    
削除済みアイテムフォルダー以外のフォルダーにあるメッセージを削除することをユーザーが選択した場合は、削除対象としてマークします。 ユーザーが [削除済みアイテム] フォルダー内からメッセージを選択した場合にのみ、メッセージがワークステーションから物理的に削除されます。 ユーザーに本当に削除を実行しているかどうかを確認するように求めるメッセージを表示することができます。
  
 **メッセージを削除するには**
  
1. その後の削除が意図的なものであることをユーザーに確認します。
    
2. 削除するフォルダーの親を決定します。 削除済みアイテムフォルダーまたは削除済みアイテムフォルダー内のサブフォルダーである場合は、 [imapifolder::D eletemessages](imapifolder-deletemessages.md)を呼び出してメッセージを削除します。 
    
3. フォルダーが [削除済みアイテム] フォルダーに含まれていない場合は、MESSAGE_MOVE フラグが設定された[imapifolder:: copymessages](imapifolder-copymessages.md)を呼び出して、メッセージを削除済みアイテムフォルダーに移動します。 
    

