---
title: MAPI スプーラーとの対話
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: faf3d48b63d1858a2b91f66c83d9ce08e9daa02b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801069"
---
# <a name="interacting-with-the-mapi-spooler"></a>MAPI スプーラーとの対話

  
  
**適用されます**: Outlook 
  
内のメソッド、 [IXPLogon: IUnknown](ixplogoniunknown.md)トランスポート プロバイダーを呼び出すときに、MAPI スプーラーによってインターフェイスを使用します。 すばやく戻ることができるように、これらのメソッドのほとんどを実装するトランスポート プロバイダーのほとんどの種類の可能性がある場合があります。 メソッドで取得するのには時間がかかる場合、分解 MAPI スプーラーに呼び出しを他のタスクの CPU を解放するにこれは望ましいことです。 
  
MAPI スプーラー機能の動作し、フォア グラウンド アプリケーションがアイドル状態のときに、プロバイダーをトランスポートするための呼び出しを行います。 トランスポート プロバイダーは、最初のログオン (MAPI からトランスポート プロバイダーに渡されるフラグによって制御される) ときにダイアログ ボックスの表示オプションで後のトランスポート プロバイダーはクライアントへのフラッシュの送信および受信キューで呼び出されない限り、バック グラウンドで動作します。 フラッシュのキューは、トランスポート プロバイダーが必要な CPU を解放されないことだけにし、長い可能性のあるアクションが、進行状況にあるユーザーに通知される場合のみです。 MAPI スプーラーは、通常、トランスポート プロバイダーがユーザーに通知されることを確認するのには何もする必要はありません通常、トランスポート プロバイダーがユーザー アクションへの応答として、キューをフラッシュするを要求します。
  
トランスポート プロバイダーは、個別に決定できます、キューをフラッシュし、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティの [状態] 行で STATUS_INBOUND_FLUSH と STATUS_OUTBOUND_FLUSH のビットを使用して、MAPI スプーラーを無効にしようとしているを通知します注意のことが作業を行えるようにします。 [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを使用して、[状態] 行が更新されます。 ここでは、進行状況インジケーターまたはその他のインタ フェースの長いアクションが発生しているかをユーザーに通知するためにトランスポート プロバイダーは、可能性があります表示します。 
  
ネットワークのアクティビティでは、0.2 秒以上の多くの場合はため、トランスポート プロバイダーは、可能な限りを使用して、非同期ネットワーク要求。 これにより、要求を開始、MAPI スプーラー再度がそれらを確認するかどうかは、ネットワーク要求が完了するのには、コントロールと、MAPI スプーラーを呼び出すことで、CPU を解放することができます。 それがまだ完了していない場合、もう一度リリース、CPU を呼び出すことで、MAPI スプーラーを無効に[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)メソッドを使用しています。 
  
メッセージ処理、および[IXPLogon::StartMessage](ixplogon-startmessage.md)、 [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)と[IXPLogon::EndMessage](ixplogon-endmessage.md)の間でトランスポート プロバイダーは、通常は多数の呼び出し、MAPI スプーラーに公開されるオブジェクトにします。 これらのオブジェクトの処理の一部として、MAPI スプーラーを無効には、該当する場合、独自に生成することによって、バック グラウンド プロセスとして適切に動作するトランスポート プロバイダーことができます。 タイム クリティカルな処理を必要とするトランスポート プロバイダーは、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)のサポート オブジェクトのメソッドを使用して MAPI スプーラーにクリティカル セクションを宣言できます。 この例では、CPU により解放された**SpoolerYield**の明示的な呼び出しでのみトランスポート プロバイダーは、トランスポート プロバイダーは、 **SpoolerNotify**に対して別の呼び出しを処理するクリティカル セクションを終了するまでです。
  
> [!NOTE]
> これは Win32 のクリティカル セクションと同じです。 これはのみ、トランスポート プロバイダーは、fax 回線からの着信データの読み取りなどの外部リソースのリアルタイム制御を必要なときに行ってください。 MAPI スプーラ プロセスの優先順位が発生し、操作の間のスレッドが横取りされますワークステーションが発生することができます、ためにが長い可能性のある操作が進行中であるユーザーに通知し、可能な場合は、進行状況インジケーターを提供することをお勧めします。 
  

