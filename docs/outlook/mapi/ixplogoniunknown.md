---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432535"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーにトランスポート プロバイダーへのアクセス権を与えます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|次のユーザーによって公開されます。  <br/> |トランスポート ログオン オブジェクト  <br/> |
|実装元:  <br/> |トランスポート プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI スプーラー  <br/> |
|インターフェイス識別子:  <br/> |IID_IXPLogon  <br/> |
|ポインターの種類:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |トランスポート プロバイダーが処理する受信者の種類を返します。  <br/> |
|**RegisterOptions** <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |トランスポート プロバイダーが通知を要求したイベントの発生を通知します。  <br/> |
|[アイドル状態](ixplogon-idle.md) <br/> |システムがアイドル状態で、トランスポート プロバイダーが優先度の低い操作を実行できる状態を示します。  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |ログオフ プロセスを開始します。  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |MAPI スプーラーにトランスポート プロバイダーが配信するメッセージが含まれています。  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |MAPI スプーラーが送信メッセージの処理を完了したとトランスポート プロバイダーに通知します。  <br/> |
|[Poll](ixplogon-poll.md) <br/> |トランスポート プロバイダーが 1 つ以上の受信メッセージを受信したかどうかを示します。  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |トランスポート プロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |トランスポート プロバイダーの状態オブジェクトを開きます。  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |トランスポート プロバイダーの外部状態を確認します。  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |トランスポート プロバイダーが保留中のすべての受信メッセージまたは送信メッセージを直ちに配信する要求。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

