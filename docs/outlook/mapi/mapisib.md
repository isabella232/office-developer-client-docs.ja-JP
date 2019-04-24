---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270211"
---
# <a name="mapisib"></a>MAPISIB

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造体は、 [imapisync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)で使用されます。
  
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

 **ulsize**
  
> 構造体のサイズ。
    
 **ulFlags**
  
> 同期の種類を示すフラグ。次のいずれかの値であることが必要です。
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |メッセージをサーバーに送信します (現在は使用されていません)。  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |サーバーに対して階層の変更を行います。  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |サーバーから階層の変更を取得します。  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |メッセージの変更をサーバーにプッシュします。  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |サーバーからメッセージの変更を取得します。  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |同期はユーザーによって開始され、より高い優先度である必要があります。  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |完全な本文ではなく、ヘッダーのみを同期する必要があります。  <br/> |
   
 **p' sync**
  
> 順番MAPI セッションへのポインター。
    
 **punkCallBack**
  
> 順番進行状況を提供するインターフェイスへのポインター。 [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)のインターフェイスを照会するために使用できます。
    
 **\*phsyncdoneevent**
  
> 読み上げ作成されたスレッドが完了したときに発生するイベント。 このポインターは、イベントが含まれるため、有効である必要があります。
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

