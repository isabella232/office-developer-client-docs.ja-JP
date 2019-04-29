---
title: ipstxgetlasterror
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414978"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
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



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

