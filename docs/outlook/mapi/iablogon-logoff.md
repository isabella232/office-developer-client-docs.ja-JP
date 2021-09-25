---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2f51e657fb3ab2c05a28af24a91c38d990b5d132
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616937"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ログオフ プロセスを開始します。
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフ プロセスが正常に開始されました。
    
## <a name="remarks"></a>注釈

通常、ログオフ プロセスは、クライアントが [IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出してセッションを終了するときに開始されます。 MAPI は、各アドレス帳プロバイダーの **IABLogon::Logoff** メソッドを呼び出して、ログオフ プロセスを開始します。 
  
**IABLogon::Logoff メソッドは** 次の処理を行います。 
  
- サブオブジェクトや status オブジェクトなど、開いているすべてのオブジェクトを解放します。
    
- プロバイダーのサポート オブジェクトを解放します。
    
アドレス帳プロバイダーのログオフ プロセスの詳細については、「サービス プロバイダーのシャットダウン [」を参照してください](shutting-down-a-service-provider.md)。
  
## <a name="see-also"></a>関連項目



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

