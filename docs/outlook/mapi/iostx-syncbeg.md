---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801085"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**適用対象**: Outlook 
  
特定の状態の同期をローカル ストアを準備し、複製に必要な情報を取得します。
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>パラメーター

 _uiSync_
  
>  [in]ローカル ストアが入力されている状態です。 状態識別子の一覧は次のとおりです。 
    
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
  
>  [内] と [出力] を入力する状態に対応するデータ構造へのポインター。 
    
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

クライアントでは、同期の結果を設定するのには**[IOSTX::SetSyncResult](iostx-setsyncresult.md)** を呼び出すし、その状態を終了するのには**[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出します。 クライアントは、状態が正常にレプリケートされたかどうかを判断するために**IOSTX::SyncBeg**が呼び出されるたびに、 **[IOSTX::SyncEnd](iostx-syncend.md)** を呼び出す必要があります。 これが判明すると、Outlook の内部の状態をクリーンアップするのには開始できます。 
  
[Out] これらの構造体の大部分が含まれている/[in] については、Outlook が Outlook に情報を渡すには、クライアント、およびクライアントに情報を渡すことを許可します。 クライアントは、 **IOSTX::SyncBeg**を呼び出して、Outlook は特定の状態のデータ構造体を割り当てるし、その状態の情報を初期化しています。 [Out] の情報です。 、状態のときに、クライアントは、対応するデータ構造体をその状態を更新します。 [In] これは、情報です。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

