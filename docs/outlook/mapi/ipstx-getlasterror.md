---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 855d50699a7ada58bd144831709cc72dc65ef322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620486"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
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



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

