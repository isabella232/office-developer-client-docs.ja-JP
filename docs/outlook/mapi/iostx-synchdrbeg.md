---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8059830b65045890ceb4b3e75bd059c420e58761
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592278"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ヘッダーの同期を開始します。
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>パラメーター

 _cbeid_
  
> [in]メッセージのエントリ ID のバイト数。
    
 _lpeid_
  
> [in]メッセージのエントリ ID。
    
 _ppv_
  
>  [in]/[out] メッセージ ヘッダーの **[HDRSYNC](hdrsync.md)** 構造へのポインター。 
    
## <a name="remarks"></a>注釈

**IOSTX::SyncHdrBeg** の場合、ローカル ストアはダウンロード メッセージ ヘッダーの状態 [に移行します](download-message-header-state.md)。 Outlook、ストア内のメッセージ ヘッダーと親フォルダーの現在の表現を使用して **、クライアントの HDRSYNC** 構造を初期化します。 その後、クライアントは完全なメッセージ アイテム  *(HDRSYNC の pmsgFull として)*  を **ダウンロードする必要があります** 。 これが成功した場合、クライアントは **HDRSYNC** の *ulFlags* も **HSF_OK。** **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** のOutlook **HDRSYNC** で結果をチェックし **、HDRSYNC** の情報を使用してローカル メッセージ ヘッダーを更新します。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

