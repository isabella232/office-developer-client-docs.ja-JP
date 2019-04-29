---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417862"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ログオフプロセスを開始します。 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。 S_OK 以外のものが返された場合、プロバイダーはログオフされます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは**IXPLogon:: transportlogoff**メソッドを呼び出して、特定のユーザーのトランスポートプロバイダセッションを終了します。 **transportlogoff**を呼び出す前に、MAPI スプーラーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドで渡されたこのセッションについて、サポートされているメッセージアドレスの種類に関するデータをすべて破棄します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

トランスポートプロバイダーは、いつでも**transportlogoff**への通話を承諾するように準備する必要があります。 メッセージが処理中の場合、プロバイダーは送信プロセスを停止する必要があります。 
  
トランスポートプロバイダーは、現在のセッションに割り当てられているすべてのリソースを解放する必要があります。 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用してこのセッションのメモリを割り当てている場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放する必要があります。 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドへの呼び出しを満たすためにトランスポートプロバイダーによって割り当てられたメモリは、この時点では安全にリリースできます。 
  
通常、 **transportlogoff**呼び出しの完了時に、プロバイダーは、 [imapisupport:: makeinvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、そのサポートオブジェクトを解放することによって、最初にログオンオブジェクトを無効にする必要があります。 サポートオブジェクトが解放されると、MAPI スプーラーはプロバイダーオブジェクト自体を解放することができるため、プロバイダーの**transportlogoff**の実装では、support オブジェクトを最後に解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

