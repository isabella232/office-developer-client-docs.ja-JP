---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6fba63f5939eb6fb6e789fa2b083c9a7716c528c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592397"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メモリ割り当ておよび割り当て解除関数[(MAPIAllocateBuffer、MAPIAllocateMore、および](mapiallocatemore.md) [MAPIFreeBuffer)](mapifreebuffer.md)のアドレスを取得します。[](mapiallocatebuffer.md)
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lppAllocateBuffer_
  
> [out] **MAPIAllocateBuffer** 関数へのポインターへのポインター。 **MAPIAllocateBuffer はメモリ** を割り当てる。 
    
 _lppAllocateMore_
  
> [out] **MAPIAllocateMore 関数へのポインターへの** ポインター。 **MAPIAllocateMore は****、MAPIAllocateBuffer** を使用して最初に割り当てられたメモリに追加のメモリを割り当てします。
    
 _lppFreeBuffer_
  
> [out] **MAPIFreeBuffer** 関数へのポインターへのポインター。 **MAPIFreeBuffer はメモリ** を解放します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数のアドレスが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::GetMemAllocRoutines** メソッドは、すべてのサポート オブジェクトに実装されます。 サービス プロバイダーは **GetMemAllocRoutines** を呼び出して、初期化関数 [(ABProviderInit、MSProviderInit、](abproviderinit.md)[または XPProviderInit)](xpproviderinit.md)に渡される 3 つのメモリ割り当て関数のアドレスを取得します。 [](msproviderinit.md) 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

