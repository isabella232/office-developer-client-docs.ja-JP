---
title: FlushQueues メソッドの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 01296995adbca2640c8da42b4d06c1c749be3266
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582414"
---
# <a name="implementing-the-flushqueues-method"></a>FlushQueues メソッドの実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI スプーラーでは、 [IXPLogon::FlushQueues](ixplogon-flushqueues.md)メソッドを使用して、ダウンロードして、トランスポート プロバイダーとの間に、保留中のメッセージをアップロードします。 通常、MAPI スプーラーはすべてトランスポート プロバイダーは、セッションにログオンするユーザーのプロファイルのトランスポートの順序] セクションで設定されている最初のトランスポート プロバイダーを開始のキューをフラッシュします。 キューのフラッシュは、ほとんどの場合、ユーザーが直接要求の結果ですので送信側と受信メッセージ キューがフラッシュされるときに、MAPI スプーラーを同期。 これらの呼び出しは同期であるため、トランスポート プロバイダーは、処理して、できるだけ早くします。 
  
トランスポート プロバイダーは、適切なメッセージ処理を有効にして、MAPI スプーラーの一部として、他のトランスポート プロバイダーが使用するモデムなどの外部リソースを有効にするのには、次の一連の手順で説明したように**FlushQueues**呼び出しを処理する必要があります。**FlushQueues**操作です。 
  
|**手順**|**コンポーネント**|**実装**|
|:-----|:-----|:-----|
|1。  <br/> |MAPI スプーラー  <br/> |_UlFlags_パラメーターで要求されたフラグを渡すこと、最初のトランスポート プロバイダーのユーザーのプロファイルでは、トランスポートの順番に記載されているため、 **FlushQueues**メソッドを呼び出します。 **FlushQueues**は、全体のアップロードとダウンロード操作のすべてのフラグが設定された 1 回だけ呼び出されます。  <br/> |
|2。  <br/> |トランスポート プロバイダー  <br/> |**FlushQueues**の呼び出しから戻る前にさまざまな処理を行う必要があります。 以前に提出メッセージが遅延している場合は、NOTIFY_SENT_DEFERRED フラグを設定して、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。 MAPI スプーラーを無効にするトランスポート プロバイダーは、前に延期されたメッセージをキャンセルすることには、メッセージの処理を完了することがあります。  <br/> トランスポート プロバイダーは、モデムなどの外部リソースを使用する場合、外部リソースへの接続を確立する必要があります。  <br/> [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを使用して、STATUS_OUTBOUND_FLUSH、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))、トランスポート プロバイダーの状態の行のプロパティ内のビットを設定しなければなりません。  <br/> トランスポート プロバイダーは、 **FlushQueues**呼び出しの S_OK を返す必要があります。  <br/> |
|3。  <br/> |MAPI スプーラー  <br/> |STATUS_OUTBOUND_FLUSH ビットのトランスポート プロバイダーの状態の行をチェックし、キューの最初のメッセージの[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を呼び出します。  <br/> |
|4。  <br/> |トランスポート プロバイダー  <br/> |メッセージを処理し、 **SubmitMessage**の呼び出しから返されます。  <br/> |
|5。  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーでは、 **SubmitMessage**から S_OK が返された場合、MAPI スプーラーを無効の場合と通常のメッセージを送信するメッセージの[IXPLogon::EndMessage](ixplogon-endmessage.md)を呼び出します。  <br/> トランスポート プロバイダーでは、 **SubmitMessage**から S_OK 以外の値が返された場合、MAPI スプーラーは、 **EndMessage**を呼び出す前に、またはもう一度**SubmitMessage**を呼び出す前に適切に値を処理します。  <br/> |
|6。  <br/> |トランスポート プロバイダー  <br/> |**EndMessage**からそのメッセージの処理、 _lpulFlags_パラメーターのステータスを返します。  <br/> |
|7。  <br/> |MAPI スプーラーとトランスポート プロバイダー  <br/> |**SubmitMessage**- **EndMessage**ループがキュー内のすべてのメッセージのダウンロードが完了するまで続行します。  <br/> |
|8。  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーは、NOTIFY_END_OUTBOUND_FLUSH フラグを設定して、トランスポート プロバイダーの[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出して、メッセージのダウンロードが完了したことを通知します。  <br/> |
|9。  <br/> |トランスポート プロバイダー  <br/> |キューをフラッシュするその他のトランスポート プロバイダーによって使用できるように、送信メッセージを送信することで使用されている外部リソースを解放します。  <br/> **ModifyStatusRow**では、ビットのトランスポート プロバイダーは、[状態] 行の**PR_STATUS_CODE**プロパティに STATUS_INBOUND_FLUSH を設定しなければなりません。  <br/> |
|10。  <br/> |MAPI スプーラー  <br/> |STATUS_INBOUND_FLUSH ビットのトランスポート プロバイダーの状態の行をチェックし、設定されている場合に[IXPLogon::StartMessage](ixplogon-startmessage.md)を呼び出します。  <br/> |
|11。  <br/> |トランスポート プロバイダー  <br/> |メッセージを処理し、 **StartMessage**から返されます。 トランスポート プロバイダーにアップロードするには、他のメッセージがある場合は、NOTIFY_NEWMAIL フラグを設定して**SpoolerNotify**を呼び出す必要があること。  <br/> アップロード メッセージ トランスポート プロバイダーがない場合は、MAPI スプーラーが**StartMessage**に渡され、返すメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出す必要があること。  <br/> |
|12。  <br/> |MAPI スプーラー  <br/> |メッセージに**SaveChanges**が呼び出されるまで、 **StartMessage**を呼び出すことが続行されます。 トランスポート プロバイダーは、アップロードが終了したら、MAPI スプーラーは、NOTIFY_END_INBOUND_FLUSH フラグを設定して**TransportNotify**を呼び出します。  <br/> |
|13 です。  <br/> |トランスポート プロバイダー  <br/> |STATUS_INBOUND_FLUSH の他のトランスポート プロバイダーによって**ModifyStatusRow**と使用して、すべての外部リソースを利用できるようにリリースを使用して、[状態] 行の**PR_STATUS_CODE**プロパティでビットをクリアします。  <br/> |
|14。  <br/> |MAPI スプーラー  <br/> |ユーザーのプロファイルのトランスポートの順番に記載されている次のトランスポート プロバイダーの**FlushQueues**が呼び出されます。  <br/> |
   
トランスポート プロバイダーの状態のオブジェクトをクライアント アプリケーションが[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)場合、トランスポート プロバイダーは、 **ModifyStatusRow**のステータス行の適切なビットを設定する必要があります。 MAPI スプーラー メソッドを呼び出して、トランスポート プロバイダーの**IXPLogon::FlushQueues** MAPI スプーラーでの利便性のために。 トランスポート プロバイダーの**IXPLogon::FlushQueues**メソッドが呼び出されたとき、クライアント アプリケーションの**IMAPIStatus::FlushQueues**の呼び出しの結果としてクライアント アプリケーションに非同期操作が発生しました。 それ以外の場合**IXPLogon::FlushQueues**は、MAPI スプーラーでは同期的に動作します。 
  
パフォーマンス上の理由から、MAPI スプーラーがのみメソッドを呼び出す、トランスポート プロバイダーの**FlushQueues**トランスポート プロバイダーの [状態] 行で、STATUS_INBOUND_FLUSH と STATUS_OUTBOUND_FLUSH のフラグが設定されている場合。 その結果、トランスポート プロバイダーのステータス行に STATUS_OUTBOUND_FLUSH と STATUS_INBOUND_FLUSH のフラグをオフにしてはいつでも**FlushQueues**の操作を停止できます。 MAPI スプーラーをシャット ダウンして、 **FlushQueues**の操作を終了する必要がある場合は、NOTIFY_END_INBOUND_FLUSH と NOTIFY_END_OUTBOUND_FLUSH の両方のフラグのセットを使用して**TransportNotify**を呼び出します。 トランスポート プロバイダーはすべての外部リソースを解放する必要があり、返します。 
  

