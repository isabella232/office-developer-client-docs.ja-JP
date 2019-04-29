---
title: MAPI スプーラーとの対話
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
# <a name="interacting-with-the-mapi-spooler"></a>MAPI スプーラーとの対話

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IXPLogon: IUnknown](ixplogoniunknown.md)インターフェイスのメソッドは、トランスポートプロバイダーを呼び出すときに MAPI スプーラーによって使用されます。 ほとんどの種類のトランスポートプロバイダーでは、これらのメソッドのほとんどを実装して迅速に返すことができます。 これは、メソッドが戻るまでに長い時間がかかる場合は、MAPI スプーラーに戻って他のタスクに対する CPU を解放する必要があるため、この方法が適しています。 
  
フォアグラウンドアプリケーションがアイドル状態のときに MAPI スプーラーは動作を行い、トランスポートプロバイダーに呼び出しを行います。 トランスポートプロバイダーが最初にログオンしたときにダイアログボックスを表示する (MAPI からトランスポートプロバイダーに渡されるフラグによって制御される) 場合、トランスポートプロバイダーは、送信キューと受信キューをフラッシュするためにクライアントによって呼び出されない限り、バックグラウンドで動作します。 キューのフラッシュは、トランスポートプロバイダーが CPU を解放する必要がない唯一の時間で、ユーザーが長いアクションが進行中であることが通知されている場合に限られます。 通常、MAPI スプーラーは、トランスポートプロバイダーがユーザーの操作への応答としてキューをフラッシュすることを要求するので、通常、トランスポートプロバイダーは、ユーザーに通知されるようにするために何もする必要はありません。
  
トランスポートプロバイダーは、キューをフラッシュして、その状態行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティにある STATUS_INBOUND_FLUSH および STATUS_OUTBOUND_FLUSH ビットを使用して、必要な MAPI スプーラーに通知することができます。アテンションを使用して、ジョブを完了できるようにします。 状態行は、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを使用して更新されます。 この場合、トランスポートプロバイダーは、長いアクションが発生していることをユーザーに通知するための進行状況インジケーターまたはその他のインターフェイスを表示する必要があります。 
  
ネットワークアクティビティは、多くの場合、0.2 秒以上かかります。可能な場合は、トランスポートプロバイダーが非同期ネットワーク要求を使用する必要があります。 これにより、要求を開始し、mapi スプーラーにコールバックして CPU を解放することができます。また、mapi スプーラーがそれらを再度制御できるようになると、ネットワーク要求が完了したかどうかを確認することができます。 まだ完了していない場合は、 [imapisupport:: SpoolerYield](imapisupport-spooleryield.md)メソッドを使用して MAPI スプーラーにコールバックして、再度 CPU を解放します。 
  
メッセージ処理の間、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)と[IXPLogon:: endmessage](ixplogon-endmessage.md)と[IXPLogon:: startmessage](ixplogon-startmessage.md)の間のトランスポートプロバイダーは、通常、MAPI スプーラーによって公開されたオブジェクトに対して多数の呼び出しを行います。 これらのオブジェクトの処理の一部として、MAPI スプーラーは、トランスポートプロバイダーが必要に応じて独自に実行することにより、バックグラウンドプロセスとして適切に動作するのに役に立ちます。 時間が重要な処理を必要とするトランスポートプロバイダーは、 [imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md) support オブジェクトメソッドを使用して、MAPI スプーラーにクリティカルセクションを宣言できます。 この場合、トランスポートプロバイダーが**SpoolerNotify**への別の呼び出しで重要なセクション処理を終了するまで、トランスポートプロバイダーによる明示的な**SpoolerYield**呼び出しにのみ CPU がリリースされます。
  
> [!NOTE]
> これは、Win32 のクリティカルセクションと同じではありません。 これは、fax 回線からの受信データの読み取りなど、トランスポートプロバイダーが外部リソースをリアルタイムで制御する必要がある場合にのみ実行するようにしてください。 これにより MAPI スプーラープロセスの優先度が高くなり、操作中にワークステーションが応答しなくなる可能性があるため、ユーザーに対して長時間のアクションが進行中であることを通知し、可能な場合は進行状況のインジケーターを提供することをお勧めします。 
  

