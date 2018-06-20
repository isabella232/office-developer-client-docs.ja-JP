---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801524"
---
# <a name="mapisib"></a>MAPISIB

  
  
**適用されます**: Outlook 
  
この構造体は、 [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md)で使用されます。
  
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

## <a name="members"></a>メンバー

 **ulSize**
  
> 構造体のサイズです。
    
 **ulFlags**
  
> 同期の種類を示すフラグ。次の値のいずれかを指定する必要があります。
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |(使用) では現在のサーバーにメッセージを送信します。  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |階層の変更内容をサーバーにプッシュします。  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |階層の変更内容をサーバーから取得します。  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |メッセージの変更をサーバーにプッシュします。  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |メッセージの変更をサーバーから取得します。  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000 を設定  <br/> |同期では、ユーザーによって開始され、優先順位が高い必要があります。  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |ヘッダーと本文のない完全同期させるだけ必要があります。  <br/> |
   
 **psesSync**
  
> [IN]MAPI セッションへのポインター。
    
 **punkCallBack**
  
> [IN]進行状況を提供するインターフェイスへのポインター。 インターフェイスを照会するために使用できる[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)。
    
 **\*phSyncDoneEvent**
  
> [OUT]作成されたスレッドが完了したときに発生するイベントです。 イベントが含まれているために、ポインターは有効である必要があります。
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync: IUnknown](imapisynciunknown.md)

