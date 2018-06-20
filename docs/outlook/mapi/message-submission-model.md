---
title: メッセージ送信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801654"
---
# <a name="message-submission-model"></a>メッセージ送信モデル

  
  
**適用されます**: Outlook 
  
メッセージの送信は、一連の MAPI スプーラーからトランスポート プロバイダーへの呼び出しによって実行されます。 呼び出しは次のように順序付けられました。
  
1. MAPI スプーラーが[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を渡すことを呼び出し、 [IMessage: IMAPIProp](imessageimapiprop.md)インスタンスは、プロセスを開始します。 
    
2. トランスポート プロバイダーは、参照の値を配置し、-将来的にこのメッセージへの参照に使用されるトランスポート定義の識別子、 **SubmitMessage**で参照されている場所にします。
    
3. トランスポート プロバイダーは、渡された**IMessage**のインスタンスを使用してメッセージ データにアクセスします。 各受信者について責任を受け入れることを渡された**IMessage**で、トランスポート プロバイダーは**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、返します。
    
4. または標準的な配信レポートを作成するには、配信できないすべての受信者を認識しているかどうかを示すために、トランスポート プロバイダーは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用できます。 **StatusRecips**は、利便性のため、一部の受信者に配信できないと判断したトランスポート プロバイダーのユーザーまたはクライアント アプリケーション可能性がありますが、基になるメッセージング システムからの配信情報を受信するか便利です。 
    
5. [IXPLogon::EndMessage](ixplogon-endmessage.md) MAPI スプーラーでの呼び出しは、トランスポート プロバイダーにメッセージを MAPI スプーラーから最終的な責任の手からです。 
    
6. MAPI スプーラーは、メッセージを**SubmitMessage**または**EndMessage**の呼び出し中に処理をキャンセルするのには[IXPLogon::TransportNotify](ixplogon-transportnotify.md)を使用できます。 
    

