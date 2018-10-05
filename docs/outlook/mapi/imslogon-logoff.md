---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399236"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージをログでは、プロバイダーを格納します。 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーを強制的にシャット ダウンするのには**IMSLogon::Logoff**メソッドを実装します。 **IMSLogon::Logoff**は、次の状況で呼び出されます。 
  
- MAPI は、クライアント、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出した後ログオフ中にします。 
    
- MAPI メッセージ ストア プロバイダーは、ログ中にします。 MAPI のサポート オブジェクト、 [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)または**IUnknown を処理している間、メッセージ ストア プロバイダーを作成するの[](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドの処理の一部として**IMSLogon::Logoff**がここと呼ばれます。リリース**メッセージ ストアのオブジェクトに対するメソッド呼び出しです。 
    
## <a name="see-also"></a>関連項目



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

