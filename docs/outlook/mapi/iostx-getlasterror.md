---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 73a5559a22ceece27e692e95d2ab1bc01c654336
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604776"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後のエラーに関する拡張情報を取得します。
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
>  [in]エラー コード。 
    
 _ulFlags_
  
>  [in]動作を変更するフラグです。 これは 0 である必要があります。 
    
 _lppMAPIError_
  
>  [out]エラーの **拡張情報を** 含む MAPIERROR 構造体へのポインター。 LPMAPIERROR の型定義については **、mapidefs.h を参照してください**。 
    
## <a name="see-also"></a>関連項目



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

