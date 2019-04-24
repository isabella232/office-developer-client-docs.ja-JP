---
title: IPM サブツリー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317109"
---
# <a name="ipm-subtree"></a>IPM サブツリー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、メッセージをコンピューターや受信者ではなく、人間との間で送受信するすべてのクライアントに対して、メッセージストアのルートフォルダーの下にフォルダーのツリーを作成します。 人間の受信者間で交換されるメッセージは、個人間メッセージと呼ばれ、このツリーは個人間メッセージ (IPM、サブツリー) と呼ばれます。 
  
配信ストアの IPM サブツリーは、少なくとも次のフォルダーで構成されます。
  
- Inbox
    
- 送信トレイ
    
- 送信済みアイテム
    
- 削除済みアイテム
    
これらの各フォルダーの既定の名前とロールは次のとおりです。クライアントは、既定の名前が適切でない場合、独自の名前を指定できます。 MAPI では、クライアント戻さがメッセージの受信フォルダーを確立するときに、メッセージが誤って消失しないようにするために、これらのフォルダーに既定の名前と関連付けが割り当てられます。 
  
Microsoft Office Outlook のコンテキストでは、IPM サブツリーは、予定表、連絡先、タスク、メモ、およびジャーナルの追加の既定のフォルダーで構成されます。
  
通常、受信トレイは受信メッセージを保持し、送信トレイは送信メッセージを保持します (つまり、送信を待機しているメッセージ)。 クライアントが**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティをこのフォルダーのエントリ識別子に設定している場合、送信済みアイテムフォルダーには、送信された各メッセージのコピーが保持されます。 削除済みアイテムフォルダーには、削除のマークが付いたメッセージが含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

