---
title: メッセージの削除
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
# <a name="deleting-a-message"></a>メッセージの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、メッセージが開いているときに、ユーザーがメッセージを読み取る場合、またはメッセージが閉じ、ユーザーがコンテンツ テーブルを表示している場合に削除できます。 ユーザーが誤ってメッセージを削除することを保護するために、MAPI はメッセージの削除を 2 つの手順プロセスとして定義します。
  
1. 削除済みアイテム フォルダーとして指定されているフォルダー (エントリ識別子が **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)プロパティに格納されているフォルダー) に移動して、削除メッセージをマークします。 
    
2. [IMAPIFolder::D eleteMessages メソッドを呼び出して、メッセージを削除](imapifolder-deletemessages.md)します。 
    
ユーザーが [削除済みアイテム] フォルダー以外のフォルダー内のメッセージを削除する場合は、削除のマークを付きます。 ユーザーが削除済みアイテム フォルダー内からメッセージを選択した場合にのみ、メッセージをワークステーションから物理的に削除する必要があります。 ユーザーに対して、削除を実際に実行する意図を確認するように求めるメッセージを表示できます。
  
 **メッセージを削除するには**
  
1. 差し迫った削除が意図的な場合は、ユーザーに確認します。
    
2. 削除するフォルダーの親を決定します。 削除済みアイテム フォルダーまたは削除済みアイテム フォルダー内のサブフォルダーである場合は [、IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) を呼び出してメッセージを削除します。 
    
3. フォルダーが削除済みアイテム フォルダー内に含まれている場合は、メッセージを削除済みアイテム フォルダーに再配置するために、MESSAGE_MOVE フラグが設定された [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) を呼び出します。 
    

