---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062019"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**適用対象 :** Outlook 2016 |2019
  
MAPI の初期化または指定した経過時間 (ミリ秒単位) の待機を開始します。 これにより、IMAPIWaitResult::End を呼び出して待機を開始する必要がある **IMAPIWaitResult** インターフェイスが返されます。 これにより、呼び出し元は、待機中にブロックされるスレッドを制御できます。

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>パラメーター
_timeout_
>[in]MAPI の初期化を待機するミリ秒単位で、初期化が実行されるのを永遠に待機するために INFINITE に設定できます。

_ppResult_
>[out]新しく作成された待機インターフェイスを受け取るポインター。

## <a name="return-value"></a>戻り値
S_OK
>待機操作が正常に開始されました。

E_OUTOFMEMORY
>新しいオブジェクトを作成するのに十分なメモリがなかった

## <a name="remarks"></a>解説
この API は、呼び出し元にインターフェイス (スレッド セーフ) を提供し、MAPI 初期化のブロック待機を開始できます。 これにより、コンシューマーはアプリケーションを待つ最も良い待ち時間を取りやめできます。   IMAPIWaitResult::End を呼び出す動作は、IMAPIInitMonitor::Wait の呼び出しと同じです。

## <a name="see-also"></a>関連項目

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
