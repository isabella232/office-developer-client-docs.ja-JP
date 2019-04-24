---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332187"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージヘッダーの同期を終了します。
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>パラメーター

 _pprog_
  
> 順番移動またはコピーされたメッセージを同期するための**[imapiprogress](imapiprogressiunknown.md)** インターフェイス。 **LPMAPIPROGRESS**の型定義については、「mapidefs.h」を参照してください。 
    
## <a name="remarks"></a>解説

**[iostx:: SyncBeg](iostx-syncbeg.md)** の場合、ローカルストアは[ダウンロードメッセージヘッダーの状態](download-message-header-state.md)を入力します。 クライアントは、完全なメッセージアイテム ( **[HDRSYNC](hdrsync.md)** では*pmsgfull* ) をダウンロードします。 この処理が成功した場合、クライアントは**HSF_OK**として**HDRSYNC**の*ulflags*も設定します。 **iostx:: SyncHdrEnd**の場合、Outlook は**HDRSYNC**の結果をチェックし、 *pprog*と**HDRSYNC**内の情報を使用して、ローカルメッセージヘッダーを更新します。 
  
ローカルストアは、前の**[iostx:: SyncHdrBeg](iostx-synchdrbeg.md)** の前の状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

