---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339299"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ログオフプロセスを開始します。
  
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
  
> ログオフプロセスが正常に開始されました。
    
## <a name="remarks"></a>解説

ログオフプロセスは、通常、クライアントが[imapisession:: logoff](imapisession-logoff.md)メソッドを呼び出してセッションを終了するときに開始されます。 次に、MAPI は各アドレス帳プロバイダーの**IABLogon:: logoff**メソッドを呼び出して、ログオフプロセスを開始します。 
  
**IABLogon:: Logoff**メソッドは、次の処理を行います。 
  
- すべてのオブジェクトを解放します (任意のオブジェクト、または status オブジェクトなど)。
    
- プロバイダーのサポートオブジェクトを解放します。
    
アドレス帳プロバイダーのログオフプロセスの詳細については、「[サービスプロバイダーをシャットダウンする](shutting-down-a-service-provider.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

