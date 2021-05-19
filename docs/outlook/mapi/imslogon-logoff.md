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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348875"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーをログオフします。 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in]予約済み。はゼロへのポインターである必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーを強制的にシャットダウンする **IMSLogon::Logoff** メソッドを実装します。 **IMSLogon::Logoff は** 、次の状況で呼び出されます。 
  
- [IMAPISession::Logoff](imapisession-logoff.md)メソッドの呼び出し後に MAPI がクライアントからログオフしている間。 
    
- MAPI がメッセージ ストア プロバイダーからログオフしている間。 この場合 **、IMSLogon::Logoff** は、メッセージ ストア オブジェクトの [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)または **IUnknown::Release** メソッド呼び出しの処理中にメッセージ ストア プロバイダーが作成するサポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを処理する MAPI の一部として呼び出されます。 
    
## <a name="see-also"></a>関連項目



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

