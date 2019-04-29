---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410785"
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

 _lpinterface_
  
> 順番status オブジェクトへのアクセスに使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイス、 [imapistatus: imapistatus](imapistatusimapiprop.md)が返されます。
    
 _ulFlags_
  
> 順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセスで開かれ、呼び出し元は読み取り/書き込みアクセス許可が与えられていると想定することはできません。
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppentry_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、状態オブジェクトが開かれています。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは、状態オブジェクトへのアクセスを許可するために**openstatusentry**メソッドを実装します。 少なくとも[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドをサポートする状態オブジェクトを実装するには、すべてのアドレス帳プロバイダーが必要です。 詳細については、「 [Status オブジェクトの実装](status-object-implementation.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

