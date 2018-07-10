---
title: メッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 68a842ccfdaea8ecdb975e1c510711b0e43fd576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803842"
---
# <a name="sending-a-message"></a>メッセージを送信する

  
  
**適用されます**: Outlook 
  
メッセージを送信する準備ができたら、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。 **SubmitMessage**では、発信キューにメッセージを配置し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティで、MSGFLAG_SUBMIT フラグを設定します。
  
メッセージ ストア プロバイダーでは、トランスポート プロバイダーでは、密に結合されている場合は、メッセージング システムに配信するトランスポートに直接メッセージを示します。 されていない場合は、発信キューが変更された MAPI スプーラー通知メッセージ ストア プロバイダーを組み合わせることで、緊密にし MAPI スプーラーは、適切なトランスポート プロバイダーにメッセージを転送します。
  
送信操作をキャンセルするユーザーを許可する場合は、この機能を実装するために[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)を呼び出します。 **AbortSubmit**では、発信キューからメッセージを削除します。 ユーザーは、基になるメッセージング システムにメッセージが指定されるまでに発生してから、送信を停止するのにはできることができます。 
  
**SubmitMessage**では、MAPI_E_CORRUPT_DATA が返された場合を想定しています送信されるデータが失われるようになりました。 2 番目の時間を送信する前に、 [IMAPIProp::SetProps](imapiprop-setprops.md)と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すことによって、メッセージを再書き込みします。 **IMAPIProp**のこれらの呼び出しが失敗した場合、または**SubmitMessage**には、2 回目が失敗した場合は、ユーザーにエラーを表示します。 
  
**SubmitMessage**を正常に呼び出し、受信者の一覧に割り当てられたメモリをすべて解放し、メッセージとその添付ファイルを解放します。 メッセージが送信されると、MAPI にはこれらのオブジェクトのポインターをその他の操作はできません。 1 つの例外が**リ ス**を呼び出しています。 多くのメッセージ ストア プロバイダーに送信されたメッセージのエントリ id が無効になるために、他の呼び出しは許可されません。
  
