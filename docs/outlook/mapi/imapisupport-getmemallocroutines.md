---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577815"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI メモリの割り当てと割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lppAllocateBuffer_
  
> [out]**MAPIAllocateBuffer**関数へのポインターへのポインター。 **MAPIAllocateBuffer**は、メモリを割り当てます。 
    
 _lppAllocateMore_
  
> [out]**MAPIAllocateMore**関数へのポインターへのポインター。 **MAPIAllocateMore**は、 **MAPIAllocateBuffer**を使用して割り当てられているメモリの追加のメモリを割り当てます。
    
 _lppFreeBuffer_
  
> [out]**MAPIFreeBuffer**関数へのポインターへのポインター。 **MAPIFreeBuffer**は、メモリを解放します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 関数のアドレスが正常に返されました。
    
## <a name="remarks"></a>注釈

サポートのすべてのオブジェクトの**IMAPISupport::GetMemAllocRoutines**メソッドを実装します。 サービス プロバイダーは、 [ABProviderInit](abproviderinit.md)、 [MSProviderInit](msproviderinit.md)、( [XPProviderInit](xpproviderinit.md)) は、その初期化関数に渡される 3 つのメモリ割り当て関数のアドレスを取得するのには**GetMemAllocRoutines**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

