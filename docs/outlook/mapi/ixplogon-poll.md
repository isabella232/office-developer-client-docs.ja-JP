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
  
トランスポートプロバイダーが1つ以上の受信メッセージを受信したかどうかを示します。
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>パラメーター

 _lアウト受信_
  
> 読み上げ受信メッセージの存在を示す値。 0以外の値は、受信メッセージがあることを示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

次に示すように、MAPI スプーラーは**IXPLogon::P oll**メソッドを定期的に呼び出します。これは、トランスポートプロバイダーが新しいメッセージをポーリングする必要があることを示している場合、プロバイダーは、LOGON_SP_POLL フラグを[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)への呼び出しに渡すことによって行われます。メソッドは、セッションの開始時に行います。 トランスポートプロバイダーが**ポーリング**呼び出しに応答して、1つまたは複数の受信メッセージを処理できることを示している場合、MAPI スプーラーは[IXPLogon:: startmessage](ixplogon-startmessage.md)メソッドを呼び出して、プロバイダーが最初の受信を処理できるようにします。メッセージ。 トランスポートプロバイダーは、 _lな着信_パラメーターの値を0以外の値に設定することにより、受信メッセージを示します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

