---
title: メッセージ受信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8fbc09d9d79f88ef783b8effe7a24e4b35564cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570374"
---
# <a name="message-reception-model"></a>メッセージ受信モデル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーは、かどうか、MAPI スプーラーを無効する必要がありますポーリング受信メール用、または新着メールが届いたときに MAPI スプーラーに呼び出しを実行してかどうかを制御します。 トランスポート プロバイダーは、ポーリングを要求する[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)すると、SP_LOGON_POLL フラグを設定します。 それ以外の場合、トランスポート プロバイダーは、受信メールがある場合、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)を使用します。 、受信メールが利用できることを学習した後 MAPI スプーラー新しいメッセージを開き、メッセージを受信したメッセージのプロパティを格納するトランスポート プロバイダーを確認します。 
  
このプロセスは、次のように動作します。
  
1. 使用可能なメッセージは、トランスポート プロバイダーは、 **IMAPISupport::SpoolerNotify**を呼び出すことによって、または[IXPLogon::Poll](ixplogon-poll.md)を呼び出して、MAPI スプーラーによって示されます。
    
2. MAPI スプーラーは、プロセスを開始するのには[IXPLogon::StartMessage](ixplogon-startmessage.md)を呼び出します。 
    
3. トランスポート プロバイダーは、 **StartMessage**で参照されている場所の参照値を配置します。 これらの参照の値を提供する複数のメッセージがある場合にどのようなメッセージが処理されているを追跡するには、トランスポート プロバイダーと MAPI スプーラーを使用できます。
    
4. トランスポート プロバイダーに渡されたメッセージ データを格納する[IMessage: IMAPIProp](imessageimapiprop.md)インスタンス。 
    
5. トランスポート プロバイダーは、 **IMessage**のインスタンスの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すし、 **StartMessage**からを返します。
    
6. MAPI スプーラーは、メッセージの配信を停止する必要がある場合に[IXPLogon::TransportNotify](ixplogon-transportnotify.md)を呼び出します。 
    
> [!NOTE]
> トランスポート プロバイダーが多数のメッセージを配信する必要がありますトランスポート プロバイダーは、使用している場合**IMAPISupport::SpoolerNotify** **IXPLogon::Poll**ではなく、注意が必要ない順序で**SpoolerNotify**をあまり頻繁に電話するにはCPU 時間の場合は、他のトランスポート プロバイダーを占有します。 MAPI スプーラーは、問題を認識できなくためのロジックを持つが、一般に**SpoolerNotify**の呼び出し間隔が 1 つのメッセージを処理するトランスポート プロバイダーが必要な時間よりも長いにする必要があります。 > また、MAPI スプーラー可能性がありますいない受信メッセージをすぐに処理。 MAPI スプーラーを無効なトランスポート プロバイダーは、着信メッセージを受信する前に、他のタスクを実行するでしょう。 
  

