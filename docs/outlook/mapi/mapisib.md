---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418709"
---
# <a name="mapisib"></a>MAPISIB

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造は [IMAPISync::SyncInBackground と一緒に使用されます](imapisyncsynchronizeinbackground.md)。
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> 構造体のサイズ。
    
 **ulFlags**
  
> 同期の種類を示すフラグ。これは、次のいずれかの値である必要があります。
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |(現在使用されていない) サーバーにメッセージを送信します。  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |階層の変更をサーバーにプッシュします。  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |階層の変更をサーバーからプルします。  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |メッセージの変更をサーバーにプッシュします。  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |サーバーからメッセージの変更をプルします。  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |同期はユーザーによって開始され、優先度が高い必要があります。  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |ヘッダーのみを同期し、完全なボディを同期しない必要があります。  <br/> |
   
 **psesSync**
  
> [IN]MAPI セッションへのポインター。
    
 **punkCallBack**
  
> [IN]進行状況を提供するインターフェイスへのポインター。 [IMAPISyncProgressCallback : IUnknown のインターフェイスを照会するために使用できます](imapisyncprogresscallbackiunknown.md)。
    
 **\*phSyncDoneEvent**
  
> [OUT]作成されたスレッドが完了した場合に発生するイベント。 ポインターはイベントを含むので有効である必要があります。
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

