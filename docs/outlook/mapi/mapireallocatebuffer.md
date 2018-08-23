---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801522"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**適用対象**: Outlook 
  
メモリ バッファーを再割り当ています。 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数で使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |omapix.h  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>パラメーター

 _lpv_
  
> 再割り当てするメモリへのポインター。
    
 _ulSize_
  
> 割り当てられるバッファーのバイト単位のサイズです。
    
 _lppv_
  
> 返されるバッファーへのポインター。
    
## <a name="remarks"></a>注釈

 **MAPIReallocateBuffer**は、新しい要求されたサイズのメモリ ブロックを割り当て、この新しいメモリのブロックに渡されるバッファーの内容をコピーします。 渡されたメモリのブロックには、内部ポインターが含まれている場合、ポインターが新しい位置に合わせて変更されません。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)

