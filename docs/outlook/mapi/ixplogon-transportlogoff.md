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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586313"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ログオフ処理を開始します。 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。 以外 S_OK が返された場合、プロバイダーがログオフされます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、特定のユーザー用のトランスポート プロバイダー セッションを終了する**IXPLogon::TransportLogoff**メソッドを呼び出します。 **TransportLogoff**を呼び出す前に、MAPI スプーラーは、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドに渡されたこのセッションでサポートされているメッセージング アドレスの種類に関するデータを破棄します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

トランスポート プロバイダーは、いつでも**TransportLogoff**への呼び出しを受け入れるように準備する必要があります。 メッセージは、プロセスでは、プロバイダーは送信プロセスを停止する必要があります。 
  
トランスポート プロバイダーが現在のセッションに割り当てられているすべてのリソースを解放する必要があります。 場合は[MAPIAllocateBuffer](mapiallocatebuffer.md)関数では、このセッションで、すべてのメモリを割り当てられて、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放してする必要があります。 この時点で、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドの呼び出しを満たすためにトランスポート プロバイダーによって割り当てられたメモリを安全に解放できます。 
  
通常、 **TransportLogoff**の呼び出しを完了するには、プロバイダー [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、最初のログオン オブジェクトを無効にしてくださいのサポート オブジェクトを解放します。 サポート オブジェクトが解放されると、MAPI スプーラー プロバイダー オブジェクト自体にもリリースできますので、 **TransportLogoff**のプロバイダーの実装はサポート オブジェクトを最後に、開放しなければなりません。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

