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
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801062"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**適用されます**: Outlook 
  
メッセージをログでは、プロバイダーを格納します。 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーを強制的にシャット ダウンするのには**IMSLogon::Logoff**メソッドを実装します。 **IMSLogon::Logoff**は、次の状況で呼び出されます。 
  
- MAPI は、クライアント、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出した後ログオフ中にします。 
    
- MAPI メッセージ ストア プロバイダーは、ログ中にします。 MAPI のサポート オブジェクト、 [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)または**IUnknown を処理している間、メッセージ ストア プロバイダーを作成するの[](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドの処理の一部として**IMSLogon::Logoff**がここと呼ばれます。リリース**メッセージ ストアのオブジェクトに対するメソッド呼び出しです。 
    
## <a name="see-also"></a>関連項目



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)
