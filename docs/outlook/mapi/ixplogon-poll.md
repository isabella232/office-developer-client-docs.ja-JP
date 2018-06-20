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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801255"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーが 1 つまたは複数の受信メッセージを受信したかどうかを示します。
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parameters

 _lpulIncoming_
  
> [out]受信メッセージの存在を示す値。 0 以外の値は、受信メッセージがあることを示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

MAPI スプーラーは、トランスポート プロバイダーは、新しいメッセージは、プロバイダーの LOGON_SP_POLL を渡すことによってフラグが[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の呼び出しにポーリングする必要がありますを示す場合は、定期的に**IXPLogon::Poll**メソッドを呼び出しますセッションの開始時の方法です。 トランスポート プロバイダーは、1 つを使用する必要がある**ポーリング**呼び出しへの応答としてまたはより受信メッセージの処理では、MAPI スプーラーを入手することは、プロバイダーの最初のプロセスからを許可する[IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドを呼び出す場合は、受信します。メッセージ。 トランスポート プロバイダーは、0 以外の値を_lpulIncoming_パラメーターに値を設定することにより受信メッセージを示します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

