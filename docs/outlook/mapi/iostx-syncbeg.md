---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b35d5a55a61620cbc829da2640c3a3f588584b84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613899"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の状態での同期のためにローカル ストアを準備し、レプリケートに必要な情報を取得します。
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>パラメーター

 _uiSync_
  
>  [in]ローカル ストアが入力する状態。 状態の identifers の一覧を次に示します。 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
>  [in]/[out] 入力する状態に対応するデータ構造へのポインター。 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>注釈

クライアントは **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** を呼び出して同期の結果を設定し、その状態を終了するために **[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出します。 クライアントは、状態が正常にレプリケートされたかどうかを判断するために **、IOSTX::SyncBeg** への各呼び出しに対して **[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出す必要があります。 これが決定された後、Outlook状態のクリーンアップを開始できます。 
  
これらの構造の大部分には [out]/[in] 情報が含まれているため、Outlook はクライアントに情報を渡し、クライアントは情報をクライアントに渡Outlook。 クライアントが **IOSTX::SyncBeg** を呼び出す場合、Outlookは特定の状態のデータ構造を割り当て、その状態の情報を使用して初期化します。 これは [out] 情報です。 状態の間、クライアントは、その状態に対応するデータ構造を更新します。 これは [in] 情報です。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

