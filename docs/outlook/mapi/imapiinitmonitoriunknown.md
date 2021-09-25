---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 27, 2021
ms.openlocfilehash: 5eaac9c74bc08b8525e21f805d68d8c0d4cb5072
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575996"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019

MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。 たとえば、MAPI を初期化できる複数のスレッドがある場合や、MAPI の初期化に応答してアプリケーションが何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。 初期化モニターは [、CreateMAPIInitializationMonitor オブジェクトを介してこの機能を提供](createmapiinitializationmonitor.md) します。

| クイック 情報 | result |
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> | OLMAPI32.DLL <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>Vtable の順序

| function | 説明 |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |MAPI の初期化の現在の状態を返します。  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。  INFINITE は、無限の待機に使用できます。  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |MAPI の初期化または指定した経過時間 (ミリ秒単位) の待機を開始します。 これにより、IMAPIWaitResult インターフェイスが返され、待機を開始するために "End" が呼び出される必要があります。  これにより、呼び出し元は、待機中にブロックされるスレッドを制御できます。 <br/> |

## <a name="see-also"></a>関連項目

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
