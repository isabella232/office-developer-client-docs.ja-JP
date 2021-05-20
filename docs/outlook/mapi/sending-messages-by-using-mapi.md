---
title: MAPI を使用したメッセージの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438723"
---
# <a name="sending-messages-by-using-mapi"></a>MAPI を使用したメッセージの送信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションは [、IMessage::SubmitMessage](imessage-submitmessage.md) メソッドを呼び出してメッセージを送信します。 **SubmitMessage は** [IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出して、MAPI スプーラーまたはトランスポート プロバイダーに直接コントロールを転送する前にメッセージを保存します。 
  
MAPI スプーラーは、次の場合にメッセージを受信します。
  
- メッセージ ストア プロバイダーとトランスポート プロバイダーは密に結合されません。
    
- メッセージには前処理が必要です。
    
- 密に結合されたメッセージ ストアとトランスポートは、メッセージの宛先であるすべての受信者を処理できません。
    
緊密に結合されたメッセージ ストアは、トランスポート プロバイダーにダウンロードする MAPI スプーラーにメッセージを表示する前に、メッセージの状態を考慮する必要があります。 メッセージが MAPI スプーラーを必要とすると思える場合がありますが、MAPI スプーラーは実際には関与しない必要があります。
  
たとえば、ユーザーが受信トレイからメッセージを送信する状況を考え出します。 クライアントは緊密に結合されたストアとトランスポートを使用しています。 密結合されたメッセージ ストアが、MAPI スプーラーがメッセージを処理できるかどうかを決定する唯一の基準としてメッセージの場所を使用する場合、MAPI スプーラーは常にメッセージを受信します。 この種の問題を回避するには、緊密に結合されたメッセージ ストアで、メッセージの場所に加えてメッセージの状態を確認する必要があります。 具体的には、トランスポート プロバイダーは、MAPI スプーラーがアクティブに送信されたメッセージをダウンロードする必要があります。
  
メッセージ送信プロセスには、メッセージ ストア プロバイダー、1 つ以上のトランスポート プロバイダー、MAPI が含まれています。 このセクションのトピックでは、メッセージ送信プロセスにおける特定の役割に関する詳細情報を提供します。
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

