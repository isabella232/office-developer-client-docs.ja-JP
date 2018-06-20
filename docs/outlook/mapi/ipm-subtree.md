---
title: IPM サブツリー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801117"
---
# <a name="ipm-subtree"></a>IPM サブツリー

  
  
**適用されます**: Outlook 
  
MAPI は、メッセージの送信し、コンピューターでの受信者ではなく、人間からのメッセージを受信するすべてのクライアントのメッセージ ストアのルート フォルダーの下にフォルダーのツリーを作成します。 人の受信者間で交換されるメッセージは、個人間のメッセージと呼ばれていて、このツリーは、既知の個人間のメッセージでは、IPM とサブツリーです。 
  
IPM サブツリーの配信ストアで構成されています、少なくとも次のフォルダー。
  
- 受信トレイ
    
- 送信トレイ
    
- 送信済みアイテム
    
- 削除済みアイテム
    
これらは、既定の名前とこれらのフォルダーのそれぞれの役割クライアントは、既定の名前が適切でない場合に独自の名前を指定できます。 MAPI には、既定の名前とこれらのクライアントがメッセージの受信側のフォルダーを設定しなかった場合に誤って消失からのメッセージを保持するフォルダーの関連付けが割り当てられます。 
  
コンテキストでは、Microsoft Office Outlook、IPM サブツリーは、追加の既定フォルダーの予定表、連絡先、タスク、メモ、および仕訳帳の。
  
受信トレイは通常、受信メッセージを保持し、送信トレイに送信メッセージ (つまり、送信待ちメッセージ) が保持しています。 送信済みアイテム フォルダーは、クライアントがこのフォルダーのエントリ id を**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定した場合に、送信済みのメッセージのコピーを保持します。 削除済みアイテム フォルダーには、削除用にマークされたメッセージが含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

