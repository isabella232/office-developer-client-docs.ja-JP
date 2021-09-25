---
title: メッセージ受信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48cd642cf72a04764c17be5480b10036f61142d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592040"
---
# <a name="message-reception-model"></a>メッセージ受信モデル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーは、MAPI スプーラーが受信メールをポーリングする必要があるかどうか、または新しいメールが届いたときに MAPI スプーラーへの呼び出しを実行するかどうかを制御します。 トランスポート プロバイダーは [、IXPProvider::TransportLogon](ixpprovider-transportlogon.md) からポーリングを要求するときに、SP_LOGON_POLL フラグを設定します。 それ以外の場合、トランスポート プロバイダーは [受信メールが使用可能なときに IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) を使用します。 受信メールが利用できると確認した後、MAPI スプーラーは新しいメッセージを開き、受信したメッセージのプロパティをメッセージに格納するトランスポート プロバイダーに依頼します。 
  
このプロセスは次のように動作します。
  
1. 使用可能なメッセージは **、IMAPISupport::SpoolerNotify** を呼び出すトランスポート プロバイダー、または [IXPLogon::P oll](ixplogon-poll.md)を呼び出す MAPI スプーラーによって示されます。
    
2. MAPI スプーラーは [IXPLogon::StartMessage](ixplogon-startmessage.md) を呼び出してプロセスを開始します。 
    
3. トランスポート プロバイダーは、StartMessage で参照されている場所に参照値 **を設定します**。 これらの参照値を使用すると、トランスポート プロバイダーと MAPI スプーラーは、配信するメッセージが複数ある場合に処理されているメッセージを追跡できます。
    
4. トランスポート プロバイダーは、渡された [IMessage : IMAPIProp インスタンスにメッセージ データを格納](imessageimapiprop.md) します。 
    
5. トランスポート プロバイダーは **、IMessage** インスタンスで [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出し **、StartMessage から返します**。
    
6. MAPI スプーラーは、メッセージ配信を停止する必要がある場合に [IXPLogon::TransportNotify](ixplogon-transportnotify.md) を呼び出します。 
    
> [!NOTE]
> トランスポート プロバイダーが多数のメッセージを配信する必要がある場合に、トランスポート プロバイダーが **IXPLogon::P oll** の代わりに **IMAPISupport::SpoolerNotify** を使用している場合は、CPU 時間の他のトランスポート プロバイダーを奪い取らなくするために、スプーラー **Notify** を呼び出さなすぎに注意する必要があります。 MAPI スプーラーには、このような処理を防止するロジックがありますが、一般に、 **スプーラーNotify** 呼び出しの間隔は、トランスポート プロバイダーが 1 つのメッセージを処理するのにかかる時間よりも長くする必要があります。 > MAPI スプーラーは、受信メッセージを直ちに処理しない場合があります。 MAPI スプーラーは、受信メッセージを受信する前に、トランスポート プロバイダーに他のタスクの実行を求める場合があります。 
  

