---
title: MAPI スプーラーの操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432150"
---
# <a name="interacting-with-the-mapi-spooler"></a>MAPI スプーラーの操作

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IXPLogon : IUnknown](ixplogoniunknown.md)インターフェイスのメソッドは、トランスポート プロバイダーを呼び出す際に MAPI スプーラーによって使用されます。 ほとんどの種類のトランスポート プロバイダーがこれらのメソッドのほとんどを実装して、これらのメソッドを迅速に返す必要があります。 これは、メソッドが返すのに長い時間がかかる場合は、他のタスクの CPU を解放するために MAPI スプーラーへの呼び出しで分解する必要があります。 
  
MAPI スプーラーは、その作業を実行し、フォアグラウンド アプリケーションがアイドル状態のときにトランスポート プロバイダーへの呼び出しを行います。 必要に応じて、トランスポート プロバイダーが最初にログオンするときにダイアログ ボックスを表示した後 (MAPI からトランスポート プロバイダーに渡されるフラグによって管理されます)、送信キューと受信キューをフラッシュするクライアントによって呼び出されない限り、トランスポート プロバイダーはバックグラウンドで動作します。 キューのフラッシュは、トランスポート プロバイダーが CPU を解放する必要が生じない唯一の時間であり、その後、潜在的に長いアクションが進行中である可能性があるという通知をユーザーに通知された場合にのみ行います。 MAPI スプーラーは通常、ユーザーの操作に応じてトランスポート プロバイダーがキューをフラッシュする要求を行うので、通常、トランスポート プロバイダーはユーザーに通知を受け取る必要はありません。
  
トランスポート プロバイダーは、キューをフラッシュし、状態行の PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの **STATUS_INBOUND_FLUSH** ビットと STATUS_OUTBOUND_FLUSH ビットを使用して、ジョブを完了するために MAPI スプーラーに注意を払う必要があることを通知します。 状態行は [、IMAPISupport::ModifyStatusRow メソッドを使用して更新](imapisupport-modifystatusrow.md) されます。 この場合、トランスポート プロバイダーは、長いアクションが発生しているユーザーに通知する進行状況インジケーターまたは他のインターフェイスを表示する必要があります。 
  
多くの場合、ネットワーク アクティビティには 0.2 秒以上かかるので、可能な限り、トランスポート プロバイダーは非同期ネットワーク要求を使用する必要があります。 これにより、要求を開始し、MAPI スプーラーに呼び出して CPU を解放し、MAPI スプーラーが再び制御を与え、ネットワーク要求が完了したのか確認できます。 まだ完了していない場合は [、IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) メソッドを使用して MAPI スプーラーに呼び出して、CPU を再び解放します。 
  
メッセージの処理中 [、IXPLogon::SubmitMessage](ixplogon-submitmessage.md) と [IXPLogon::EndMessage](ixplogon-endmessage.md) の間、 [および IXPLogon::StartMessage](ixplogon-startmessage.md)の間に、トランスポート プロバイダーは通常、MAPI スプーラーによって公開されるオブジェクトに対して多くの呼び出しを行います。 MAPI スプーラーは、これらのオブジェクトの処理の一環として、必要に応じて独自の処理を行って、トランスポート プロバイダーがバックグラウンド プロセスとして適切に動作するのに役立ちます。 タイム クリティカルな処理を必要とするトランスポート プロバイダーは [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) サポート オブジェクト メソッドを使用して、MAPI スプーラーに重要なセクションを宣言できます。 この場合、トランスポート プロバイダーがスプーラーNotify への別の呼び出しでクリティカル セクション処理を終了するまで、トランスポート プロバイダーによる明示的なスプーラー **Yield** 呼び出しでのみ CPU **が解放されます**。
  
> [!NOTE]
> これは、Win32 の重要なセクションと同じではありません。 これは、トランスポート プロバイダーが FAX 回線から受信データを読み取るなどの外部リソースをリアルタイムで制御する必要がある場合にのみ行う必要があります。 これにより、MAPI スプーラー プロセスの優先度が上がり、操作中にワークステーションが応答しなくなる可能性があるので、潜在的に長いアクションが進行中であるユーザーに通知し、可能であれば進行状況インジケーターを提供すると良い考えです。 
  

