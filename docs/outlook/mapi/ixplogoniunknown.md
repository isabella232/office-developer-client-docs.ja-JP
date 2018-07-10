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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801274"
---
# <a name="ixplogon--iunknown"></a>IXPLogon: IUnknown

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーを MAPI スプーラーのアクセスを提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって公開されます。  <br/> |トランスポート ログオン オブジェクト  <br/> |
|によって実装されます。  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI スプーラーを無効  <br/> |
|インターフェイスの識別子。  <br/> |IID_IXPLogon  <br/> |
|ポインターの型。  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |トランスポート プロバイダーを処理する受信者の種類を返します。  <br/> |
|**RegisterOptions** <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |トランスポート プロバイダーが通知を要求するイベントの発生を通知します。  <br/> |
|[アイドル](ixplogon-idle.md) <br/> |システムがアイドル状態、優先度の低い操作を実行するトランスポート プロバイダーを有効にすることを示します。  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |ログオフ処理を開始します。  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |MAPI スプーラーがメッセージを配信するトランスポート プロバイダーを持っていることを示します。  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |トランスポート プロバイダーは、MAPI スプーラーに送信メッセージの処理が完了したことを通知します。  <br/> |
|[ポール](ixplogon-poll.md) <br/> |トランスポート プロバイダーが 1 つまたは複数の受信メッセージを受信したかどうかを示します。  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始します。  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |トランスポート プロバイダーの状態のオブジェクトを開きます。  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |トランスポート プロバイダーの外部の状況をチェックします。  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |要求がトランスポート プロバイダーは、すべての保留の受信または送信メッセージを即座に配信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)
