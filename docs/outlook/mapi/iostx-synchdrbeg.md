---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405094"
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

