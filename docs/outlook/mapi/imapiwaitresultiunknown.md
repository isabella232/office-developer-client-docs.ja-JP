---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062040"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019

このインターフェイスは、IMAPIInitMonitor のコンシューマーが待機の発生場所を制御するために使用します。 これにより、オブジェクトを 1 つのスレッドに作成し、別のスレッドに移動して実際の待機を実行できます。

## <a name="vtable-order"></a>Vtable の順序

| function | 説明 |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|呼び出されたスレッドでブロック待機を開始するために呼び出されます *。IMAPIInitMonitor::BeginWait* と呼ばれるスレッドとは異なっている必要があります。|

| クイック 情報 | result |
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> |  OLMAPI32.DLL<br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIWaitResult  <br/> |

## <a name="see-also"></a>関連項目

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIInitMonitor : IUnknown](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
