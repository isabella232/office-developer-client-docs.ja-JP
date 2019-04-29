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
  
トランスポートプロバイダーへの MAPI スプーラーアクセスを提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|公開者:  <br/> |トランスポートログオンオブジェクト  <br/> |
|実装元:  <br/> |トランスポートプロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI スプーラー  <br/> |
|インターフェイス識別子:  <br/> |IID_IXPLogon  <br/> |
|ポインターの種類:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |トランスポートプロバイダーが処理する受信者の種類を返します。  <br/> |
|**registeroptions** <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[transportnotify](ixplogon-transportnotify.md) <br/> |トランスポートプロバイダーが通知を要求したイベントが発生したことを通知します。  <br/> |
|[アイドル](ixplogon-idle.md) <br/> |システムがアイドル状態であることを示します。これにより、トランスポートプロバイダーは優先度の低い操作を実行できるようになります。  <br/> |
|[transportlogoff](ixplogon-transportlogoff.md) <br/> |ログオフプロセスを開始します。  <br/> |
|[submitmessage](ixplogon-submitmessage.md) <br/> |トランスポートプロバイダーが配信するメッセージを MAPI スプーラーに指定します。  <br/> |
|[endmessage](ixplogon-endmessage.md) <br/> |MAPI スプーラーが送信メッセージの処理を完了したことをトランスポートプロバイダーに通知します。  <br/> |
|[間隔](ixplogon-poll.md) <br/> |トランスポートプロバイダーが1つ以上の受信メッセージを受信したかどうかを示します。  <br/> |
|[startmessage](ixplogon-startmessage.md) <br/> |トランスポートプロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。  <br/> |
|[openstatusentry](ixplogon-openstatusentry.md) <br/> |トランスポートプロバイダーの状態オブジェクトを開きます。  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |トランスポートプロバイダーの外部の状態を確認します。  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |保留中の受信または送信メッセージをすべてトランスポートプロバイダーが直ちに配信するよう要求します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

