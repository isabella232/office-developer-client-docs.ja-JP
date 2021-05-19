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
  
ログオフ プロセスを開始します。 
  
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
  
> 呼び出しは成功し、予期される値または値を返しました。 ユーザー以外のS_OK返された場合、プロバイダーはログオフされます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPLogon::TransportLogoff** メソッドを呼び出して、特定のユーザーのトランスポート プロバイダー セッションを終了します。 **TransportLogoff** を呼び出す前に、MAPI スプーラーは [、IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドで渡されたこのセッションでサポートされているメッセージング アドレスの種類に関するデータを破棄します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

トランスポート プロバイダーは、いつでも **TransportLogoff** への呼び出しを受け入れる準備をする必要があります。 メッセージが処理されている場合、プロバイダーは送信プロセスを停止する必要があります。 
  
トランスポート プロバイダーは、現在のセッションに割り当てられているすべてのリソースを解放する必要があります。 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数でこのセッションにメモリが割り当てられている場合は[、MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放する必要があります。 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドの呼び出しを満たすためにトランスポート プロバイダーによって割り当てられたメモリは、この時点で安全に解放できます。 
  
通常 **、TransportLogoff** 呼び出しを完了すると、 [プロバイダーはまず IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) メソッドを呼び出してログオン オブジェクトを無効にしてから、そのサポート オブジェクトを解放する必要があります。 サポート オブジェクトが解放されると、MAPI スプーラーはプロバイダー オブジェクト自体を解放できるので、プロバイダーの **TransportLogoff** の実装は、サポート オブジェクトを最後に解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

