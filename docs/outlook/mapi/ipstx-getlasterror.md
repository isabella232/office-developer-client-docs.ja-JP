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
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592592"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最後のエラーに関する情報を拡張します。
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
>  [in]エラー コードです。 
    
 _ulFlags_
  
>  [in]動作を変更するフラグです。 0 でなければなりません。 
    
 _lppMAPIError_
  
>  [out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。 **LPMAPIERROR**の型の定義の mapidefs.h を参照してください。 
    
## <a name="see-also"></a>関連項目



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

