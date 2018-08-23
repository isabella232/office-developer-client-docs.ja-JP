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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800347"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**適用対象**: Outlook 
  
プロバイダーの状態のオブジェクトを開きます。
  
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
  
> [in]状態オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 オブジェクトの標準のインターフェイスを返します NULL を渡す[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)。
    
 _ulFlags_
  
> [in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、呼び出し元の読み取り/書き込み権限が付与されていると仮定する必要があります。
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppEntry_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、状態オブジェクトが開かれています。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは、その状態のオブジェクトへのアクセスを許可する**OpenStatusEntry**メソッドを実装します。 すべてのアドレス帳プロバイダーは、最低限、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートする状態オブジェクトを実装する必要があります。 詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

