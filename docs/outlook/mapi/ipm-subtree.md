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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421222"
---
# <a name="ipm-subtree"></a>IPM サブツリー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、コンピューターの受信者ではなく、人間にメッセージを送受信するすべてのクライアントのメッセージ ストアのルート フォルダーの下にフォルダーのツリーを作成します。 人間の受信者間で交換されるメッセージは対人メッセージと呼び、このツリーは対人間メッセージ (IPM) サブツリーと呼ばれる。 
  
配信ストアの IPM サブツリーは、少なくとも次のフォルダーで構成されます。
  
- 受信トレイ
    
- 送信トレイ
    
- 送信済みアイテム
    
- 削除済みアイテム
    
これらは、これらの各フォルダーの既定の名前と役割です。既定の名前が適切ではない場合、クライアントは独自の名前を指定できます。 MAPI は、クライアントがメッセージの受信フォルダーの確立を怠った場合に、メッセージが誤って消えてしまうのを回避するために、これらのフォルダーの既定の名前と関連付けを割り当てします。 
  
このコンテキストMicrosoft Office Outlook IPM サブツリーは、予定表、連絡先、タスク、メモ、およびジャーナル用の追加の既定のフォルダーで構成されます。
  
受信トレイには通常、受信メッセージが保持され、送信トレイには送信メッセージ (つまり、送信待ちメッセージ) が保持されます。 クライアントが **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティをこのフォルダーのエントリ識別子に設定している場合は、送信された各メッセージのコピーが送信されたアイテム フォルダーに保持されます。 [削除済みアイテム] フォルダーには、削除のマークが付いたメッセージが含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

