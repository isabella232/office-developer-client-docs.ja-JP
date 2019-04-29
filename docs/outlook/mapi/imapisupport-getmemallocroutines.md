---
title: imapisupportgetmemallocroutines
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415538"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メモリ割り当て関数および割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lppallocatebuffer_
  
> 読み上げ**MAPIAllocateBuffer**関数へのポインターへのポインター。 **MAPIAllocateBuffer**はメモリを割り当てます。 
    
 _lppAllocateMore_
  
> 読み上げ**MAPIAllocateMore**関数へのポインターへのポインター。 **MAPIAllocateMore**は、 **MAPIAllocateBuffer**を使用して最初に割り当てられたメモリの追加メモリを割り当てます。
    
 _lppfreebuffer_
  
> 読み上げ**MAPIFreeBuffer**関数へのポインターへのポインター。 **MAPIFreeBuffer**はメモリを解放します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数のアドレスが正常に返されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: getmemallocroutines**メソッドは、すべてのサポートオブジェクトに実装されています。 サービスプロバイダーは、 **getmemallocroutines**を呼び出して、初期化関数 ( [abproviderinit](abproviderinit.md)、 [msproviderinit](msproviderinit.md)、または[xps プロバイダー init](xpproviderinit.md)) に渡される3つのメモリ割り当て関数のアドレスを取得します。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

