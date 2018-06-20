---
title: MAPI を使用してメッセージを送信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803866"
---
# <a name="sending-messages-by-using-mapi"></a>MAPI を使用してメッセージを送信します。

  
  
**適用されます**: Outlook 
  
クライアント アプリケーションは、メッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。 **SubmitMessage**では、MAPI スプーラーを無効にするか、コントロールを転送する前に、またはトランスポート プロバイダーに直接メッセージを保存するのには[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出します。 
  
MAPI スプーラーは、次のいずれかが発生した場合に、メッセージを受け取ります。
  
- メッセージ ストア プロバイダーおよびトランスポート プロバイダーが密に結合されていません。
    
- メッセージには、前処理が必要です。
    
- 密結合のメッセージ ・ ストアおよびトランスポートは、メッセージの宛先は、受信者のすべてで処理できません。
    
密結合のメッセージ ・ ストアする必要があります考慮に入れるメッセージのステータス、MAPI スプーラーを無効にするトランスポート プロバイダーをダウンロードするのにはその前に。 状況で、MAPI スプーラーを要求するメッセージが表示される場合がありますが、MAPI スプーラーを無効する必要があります実際には関与しません。
  
たとえば、ユーザーが受信トレイからメッセージを送信する場合があるとします。 密結合のストアおよびトランスポート、クライアントが使用します。 密結合のメッセージ ・ ストアでは、唯一の条件としてメッセージの場所を使用して、メッセージを処理するために、MAPI スプーラーを許可するかどうかを決定するため、MAPI スプーラーは常にメッセージが表示されます。 この種の問題を避けるためには、密結合のメッセージ ・ ストアは、メッセージの場所だけでなくメッセージ状態を確認する必要があります。 具体的には、トランスポート プロバイダーを要求しないでください、MAPI スプーラーが積極的に送信されるすべてのメッセージをダウンロードします。
  
メッセージ ストア プロバイダー、1 つまたは複数のトランスポート プロバイダー、および MAPI メッセージの送信プロセスが含まれます。 このセクションのトピックでは、メッセージ転送のプロセスで特定の役割に関する詳細情報を提供します。
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

