---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d5200a901cc692d4929edfba5a547a45ffe23c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551150"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリ バッファーを再割り当てします。 [MAPIAllocateBuffer 関数と共に使用](mapiallocatebuffer.md)されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |omapix.h  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> 割り当て可能なメモリへのポインター。
    
 _ulSize_
  
> 割り当てるバッファーのサイズ (バイト単位)。
    
 _lppv_
  
> 返される割り当てられたバッファーへのポインター。
    
## <a name="remarks"></a>注釈

 **MAPIReallocateBuffer** は、要求されたサイズの新しいメモリ ブロックを割り当て、この新しいメモリ ブロックに渡されるバッファーの内容をコピーします。 渡されるメモリ ブロックに内部ポインターが含まれている場合、ポインターは新しい場所に合わせて変更されません。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)

