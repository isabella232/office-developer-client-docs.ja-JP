---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425695"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリ バッファーを割り当てる。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>パラメーター

 _cbSize_
  
> [in]割り当てるバッファーのサイズ (バイト単位)。 
    
 _lppBuffer_
  
> [out]返された割り当てられたバッファーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、要求されたメモリ バッファーが返されました。
    
## <a name="remarks"></a>注釈

**MAPIAllocateBuffer 呼び出し処理** 中に、呼び出し元の実装はオペレーティング システムからメモリ ブロックを取得します。 メモリ バッファーは、番号が付くバイト アドレスに割り当てされます。 長整数アクセスの方が効率的なプラットフォームでは、オペレーティング システムは、バイト単位のサイズが 4 の倍数であるアドレスにバッファーを割り当てる。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **、MAPIAllocateBuffer** によって割り当てられたメモリ バッファーが解放されます [。MAPIAllocateMore](mapiallocatemore.md)関数と、その関数にリンクされているバッファーは、メモリが不要になったときに呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIReallocateBuffer](mapireallocatebuffer.md)

