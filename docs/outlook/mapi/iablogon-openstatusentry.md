---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1082e3680ed9a53894c5fd810be91b42eac22cee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596457"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーの状態オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]status オブジェクトへのアクセスに使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイス [IMAPIStatus : IMAPIProp が返されます](imapistatusimapiprop.md)。
    
 _ulFlags_
  
> [in]status オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセス権で開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されたと見なす必要があります。
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppEntry_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、status オブジェクトが開かされました。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは、 **状態オブジェクトへのアクセスを許可する OpenStatusEntry** メソッドを実装します。 すべてのアドレス帳プロバイダーは、少なくとも [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドをサポートする状態オブジェクトを実装する必要があります。 詳細については [、「Status Object Implementation」を参照してください](status-object-implementation.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

