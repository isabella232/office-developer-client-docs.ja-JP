---
title: iostxgetlasterror
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332166"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最新のエラーに関する拡張情報を取得します。
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
>  順番エラーコード。 
    
 _ulFlags_
  
>  [in]動作を変更するフラグです。 これは0である必要があります。 
    
 _lppMAPIError_
  
>  読み上げエラーの拡張情報を含む**MAPIERROR**構造体へのポインター。 **LPMAPIERROR**の型定義については、「mapidefs.h」を参照してください。 
    
## <a name="see-also"></a>関連項目



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

