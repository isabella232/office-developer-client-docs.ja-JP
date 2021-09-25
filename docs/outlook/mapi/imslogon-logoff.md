---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: edc80ce468325d820c00e4822cb207836c58e436
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561482"
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

