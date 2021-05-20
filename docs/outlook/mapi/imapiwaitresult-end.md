---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062033"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**適用対象 :** Outlook 2013 |Outlook 2016 |2019

このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。 INFINITE は、無限の待機に使用できます。

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>パラメーター

_timeout_
> [in]MAPI が初期化されるのを待つミリ秒単位で、INFINITE (0xFFFFFFFF) を渡して永遠に待機できます。

## <a name="return-value"></a>戻り値

S_OK
> MAPI が正常に初期化されました

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> 無限でないタイムアウトが与えられた場合、これは MAPI が初期化されていない期間を示します。

## <a name="remarks"></a>注釈
この API は [、IMAPInitMonitor::Wait とまったく同じ動作をします](imapiinitmonitor-wait.md)。
  
## <a name="see-also"></a>関連項目

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
