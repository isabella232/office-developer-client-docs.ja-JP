---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435286"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリバッファーを再割り当てします。 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数で使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |omapix  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
    
 _ulsize_
  
> 割り当てるバッファーのサイズ (バイト単位)。
    
 _lppv_
  
> 返された割り当て済みバッファーへのポインター。
    
## <a name="remarks"></a>注釈

 **MAPIReallocateBuffer**は、要求されたサイズの新しいメモリブロックを割り当て、この新しいメモリブロックに渡されるバッファーの内容をコピーします。 渡されるメモリブロックに内部ポインターが含まれている場合、新しい位置に合わせてポインターが変更されることはありません。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)

