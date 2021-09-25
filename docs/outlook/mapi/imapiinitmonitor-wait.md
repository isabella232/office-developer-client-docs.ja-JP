---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 27, 2021
ms.openlocfilehash: 98111b27b09082c6730b42b0f9d10bdd56d5614c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604909"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019
  
このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。 INFINITE は、無限の待機に使用できます。

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>パラメーター
_timeout_
> [in]MAPI が初期化されるのを待つミリ秒単位で、INFINITE (0xFFFFFFFF) を渡して永遠に待機できます。

## <a name="return-value"></a>戻り値

S_OK
> MAPI が正常に初期化されました。

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> 無限でないタイムアウトが与えられた場合、これは MAPI が初期化されていない期間を示します。

## <a name="see-also"></a>関連項目

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
