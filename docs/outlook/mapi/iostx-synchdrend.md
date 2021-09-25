---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: d246754dd0ac9b131808b05d5ac669aee0f5d542
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564079"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ヘッダーの同期を終了します。
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>パラメーター

 _pprog_
  
> [in] **[IMAPIProgress インターフェイス](imapiprogressiunknown.md)** を使用して、移動またはコピーされたメッセージの同期を行います。 **LPMAPIPROGRESS の型定義については、mapidefs.h を参照してください**。 
    
## <a name="remarks"></a>注釈

**[IOSTX::SyncBeg](iostx-syncbeg.md)** の場合、ローカル ストアはダウンロード メッセージ ヘッダー [の状態に入ります](download-message-header-state.md)。 クライアントは完全なメッセージ アイテム  *(HDRSYNC の pmsgFull として*  ) **[をダウンロードします](hdrsync.md)** 。 これが成功した場合、クライアントは **HDRSYNC** の *ulFlags* も **HSF_OK。** **IOSTX::SyncHdrEnd** の場合、Outlook は **HDRSYNC** で結果をチェックし *、pprog* と **HDRSYNC** の情報を使用してローカル メッセージ ヘッダーを更新します。 
  
ローカル ストアは、前の **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** より前の状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

