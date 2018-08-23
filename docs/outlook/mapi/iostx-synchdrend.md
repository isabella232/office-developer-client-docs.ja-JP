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
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801090"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**適用対象**: Outlook 
  
メッセージ ヘッダーの同期を終了します。
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>パラメーター

 _pprog_
  
> [in]同期のための**[IMAPIProgress](imapiprogressiunknown.md)** インタ フェースは、移動またはメッセージをコピーします。 **LPMAPIPROGRESS**の型の定義の mapidefs.h を参照してください。 
    
## <a name="remarks"></a>注釈

**[IOSTX::SyncBeg](iostx-syncbeg.md)**、時に、ローカル ストアは、[メッセージ ヘッダーの状態をダウンロード](download-message-header-state.md)するを入力します。 クライアントは、( *pmsgFull*の**[HDRSYNC](hdrsync.md)** で) として、完全なメッセージ項目をダウンロードします。 これが成功した場合は、クライアントも*ulFlags*の設定**HDRSYNC** **HSF_OK**とします。 **IOSTX::SyncHdrEnd**、時に、Outlook は**HDRSYNC**の結果をチェックし、ローカル メッセージのヘッダーを更新するのには、 **HDRSYNC**で*pprog*との情報を使用します。 
  
ローカル ストアは、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** の前の前に、の状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

