---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425275"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーが 1 つ以上の受信メッセージを受信したかどうかを示します。
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>パラメーター

 _lpulIncoming_
  
> [out]受信メッセージの存在を示す値。 0 以外の値は、受信メッセージが含まれます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI スプーラーは定期的に **IXPLogon::P oll** メソッドを呼び出します。トランスポート プロバイダーが新しいメッセージについてポーリングする必要がある場合、プロバイダーは LOGON_SP_POLL フラグをセッションの開始時に [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) メソッドの呼び出しに渡します。 トランスポート プロバイダーがポーリング呼び出しに応答して、処理できる受信メッセージが 1 つ以上あると示す場合、MAPI スプーラーは[IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドを呼び出して、プロバイダーが最初の受信メッセージを処理できます。 トランスポート プロバイダーは  _、lpulIncoming_ パラメーターの値を 0 以外の値に設定して、受信メッセージを示します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

