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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317158"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージヘッダーの同期を開始します。
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>パラメーター

 _cbeid_
  
> 順番メッセージのエントリ ID のバイト数。
    
 _lpeid_
  
> 順番メッセージのエントリ ID。
    
 _ppv_
  
>  [in]/[out] メッセージヘッダーの**[HDRSYNC](hdrsync.md)** 構造体へのポインター。 
    
## <a name="remarks"></a>解説

**iostx:: SyncHdrBeg**では、ローカルストアは、[メッセージヘッダーのダウンロード状態](download-message-header-state.md)に移行します。 Outlook は、ストア内の現在のメッセージヘッダーと親フォルダーを使用して、クライアントの**HDRSYNC**構造を初期化します。 クライアントは、完全なメッセージアイテム ( **HDRSYNC**では*pmsgfull*として) をダウンロードする必要があります。 これが成功した場合、クライアントは**HSF_OK**として**HDRSYNC**の*ulflags*も設定します。 **[iostx:: SyncHdrEnd](iostx-synchdrend.md)** では、Outlook が**HDRSYNC**で結果をチェックし、 **HDRSYNC**の情報を使用してローカルメッセージヘッダーを更新します。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

