---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c528826d8a05b6a608c0a9e50d882baf8956e682
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561657"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
キューに入っているすべての通知を強制的にディスパッチします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
## <a name="return-value"></a>戻り値

S_OK
  
> キューに登録された通知はすべてディスパッチされています。
    
MAPI_E_USER_CANCEL
  
> WM_QUIT、WM_QUERYENDSESSION、またはWM_ENDSESSION受信しました。
    
MAPI_E_NOT_INITIALIZED
  
> MAPI が初期化されていません。
    
## <a name="remarks"></a>注釈

**HrDispatchNotifications** 関数を使用すると、MAPI は、メッセージのディスパッチを待たずに、MAPI 通知エンジンに現在キューに入っているすべての通知をディスパッチします。 これは、メモリ使用率に有益な影響を与える可能性があります。 詳細については、「通知の [送信」を参照してください](forcing-a-notification.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一部のアプリケーションは、PeekMessage 関数と[DispatchMessage](https://msdn.microsoft.com/library/ms644943.aspx)関数を使用して、タイムアウト ループWindows[を待機](https://msdn.microsoft.com/library/ms644934.aspx)します。 最も高速なプラットフォームを含むすべてのプラットフォームでは、このようなアプリケーションのパフォーマンスが低下したり、通知がブロックされる可能性があります。 **HrDispatchNotifications を使用すると、コード** が減少するだけでなく、パフォーマンスが向上します。 
  

