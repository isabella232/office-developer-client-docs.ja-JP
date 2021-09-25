---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 27, 2021
ms.openlocfilehash: 922ce2f978b5ecfb6c2b34873f7b750b6022035f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564247"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019
  
MAPI を照会して、呼び出し元プロセスで現在初期化されているかどうかを判断します。

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>パラメーター
なし

## <a name="return-value"></a>戻り値
MAPI 初期化の現在の状態を示す BOOL は、値 TRUE は MAPI が初期化され、使用できる状態であることを意味し、FALSE の値は MAPI が現在初期化されていない状態で使用できる状態であることを意味します。

## <a name="remarks"></a>注釈
これは、MAPI を使用する準備ができているかどうかを判断するために使用できます。たとえば、MAPI が既に初期化されている場合にのみアプリケーションが何かを実行する場合は、オプションの作業のために MAPI をスピンアップするコストを防ぐため、バックグラウンド タスクのチェックに役立つ可能性があります。

## <a name="see-also"></a>関連項目

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
