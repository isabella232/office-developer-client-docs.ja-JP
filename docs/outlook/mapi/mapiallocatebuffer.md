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
  
メモリバッファーを割り当てます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>パラメーター

 _cbSize_
  
> 順番割り当てるバッファーのサイズ (バイト単位)。 
    
 _lppbuffer_
  
> 読み上げ返された割り当て済みバッファーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、要求されたメモリバッファーが返されました。
    
## <a name="remarks"></a>注釈

**MAPIAllocateBuffer**呼び出し処理の間、呼び出し側の実装はオペレーティングシステムからメモリブロックを取得します。 メモリバッファーは、偶数番号のバイトアドレスに割り当てられます。 長い整数アクセスがより効率的になるプラットフォームでは、オペレーティングシステムは、バイト数が4の倍数であるアドレスにバッファーを割り当てます。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すと、メモリが不要になったときに、 [MAPIAllocateMore](mapiallocatemore.md)関数とそれにリンクされているすべてのバッファーを呼び出すことによって、 **MAPIAllocateBuffer**によって割り当てられたメモリバッファーを解放します。 
  
## <a name="see-also"></a>関連項目



[MAPIReallocateBuffer](mapireallocatebuffer.md)

