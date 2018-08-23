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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801484"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**適用対象**: Outlook 
  
メモリ バッファーを割り当てます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>パラメーター

 _cbSize_
  
> [in]割り当てられるバッファーのバイト単位のサイズです。 
    
 _lppBuffer_
  
> [out]返されるバッファーへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、要求されたメモリ バッファーが返されます。
    
## <a name="remarks"></a>注釈

**MAPIAllocateBuffer**の中に処理を呼び出す、呼び出し元の実装は、オペレーティング システムからメモリ ブロックを取得します。 メモリ バッファーは、偶数のバイト アドレスに割り当てられます。 長整数型のアクセスがより効率的なプラットフォームでは、オペレーティング システムは、バイト単位でサイズが 4 の倍数のアドレスにバッファーを割り当てます。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数のリリースを呼び出す、 [MAPIAllocateMore](mapiallocatemore.md)関数とすべてのバッファーを呼び出すことによって、 **MAPIAllocateBuffer**、によって割り当てられたメモリ バッファーにリンクして、メモリが不要になったとき。 
  
## <a name="see-also"></a>関連項目



[MAPIReallocateBuffer](mapireallocatebuffer.md)

