---
title: IPSTXGetLastError
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801199"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**適用されます**: Outlook 
  
最後のエラーに関する情報を拡張します。
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
>  [in]エラー コードです。 
    
 _ulFlags_
  
>  [in]動作を変更するフラグです。 0 でなければなりません。 
    
 _lppMAPIError_
  
>  [out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。 **LPMAPIERROR**の型の定義の mapidefs.h を参照してください。 
    
## <a name="see-also"></a>関連項目



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

