---
title: MAPI を使用してメッセージを送信する
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
# <a name="sending-messages-by-using-mapi"></a>MAPI を使用してメッセージを送信する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションは、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出して、メッセージを送信します。 **submitmessage**呼び出し[imapiprop:: SaveChanges](imapiprop-savechanges.md)は、コントロールを MAPI スプーラーまたはトランスポートプロバイダーに直接転送する前にメッセージを保存します。 
  
MAPI スプーラーは、次のいずれかが発生した場合にメッセージを受信します。
  
- メッセージストアプロバイダーとトランスポートプロバイダーは密接に結合されていません。
    
- メッセージには前処理が必要です。
    
- 密結合メッセージストアとトランスポートは、メッセージの宛先になっているすべての受信者を処理できません。
    
密結合メッセージストアは、メッセージの状態を、MAPI スプーラーに送信してトランスポートプロバイダーにダウンロードする前に、そのメッセージの状態を考慮する必要があります。 mapi スプーラーを必要とするメッセージが表示される場合がありますが、mapi スプーラーは実際には関係ありません。
  
たとえば、ユーザーが受信トレイからメッセージを送信する状況を考えてみます。 クライアントは、密結合ストアとトランスポートを使用しています。 密結合メッセージストアがメッセージの場所を使用して、mapi スプーラーによるメッセージの処理を許可するかどうかを決定するための唯一の条件として、mapi スプーラーは常にメッセージを受信します。 この種の問題を回避するには、密結合のメッセージストアで、メッセージの場所に加えてメッセージの状態を確認する必要があります。 具体的には、トランスポートプロバイダーは、MAPI スプーラーが送信中のメッセージをダウンロードすることを要求してはなりません。
  
メッセージ転送プロセスには、メッセージストアプロバイダー、1つ以上のトランスポートプロバイダー、MAPI が含まれます。 このセクションのトピックでは、メッセージ送信プロセスにおける特定の役割について詳しく説明します。
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

