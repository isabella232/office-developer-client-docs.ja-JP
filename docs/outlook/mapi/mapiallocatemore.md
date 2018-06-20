---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801497"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**適用されます**: Outlook 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で割り当てられている別のバッファーにリンクされているメモリ バッファーを割り当てます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameters

 _cbSize_
  
> [in]割り当てられる新しいバッファーのバイト単位のサイズです。 
    
 _lpObject_
  
> [in]**MAPIAllocateBuffer**を使用して割り当てられている既存の MAPI バッファーへのポインター。
    
 _lppBuffer_
  
> [out]返されるへのポインターでは、バッファーが新しく割り当てられます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、要求されたメモリへのポインターが返されます。
    
## <a name="remarks"></a>備考

**MAPIAllocateMore**の中に処理を呼び出す、呼び出し元の実装は、オペレーティング システムからメモリ ブロックを取得します。 メモリ バッファーは、偶数のバイト アドレスに割り当てられます。 長整数型のアクセスがより効率的なプラットフォームでは、オペレーティング システムは、バイト単位でサイズが 4 の倍数のアドレスにバッファーを割り当てます。 
  
**MAPIAllocateMore**で割り当てられたバッファーを解放する唯一の方法では、 [MAPIFreeBuffer](mapifreebuffer.md)関数に_lpObject_パラメーターで指定されたバッファーのポインターを渡します。 [MAPIAllocateBuffer](mapiallocatebuffer.md)と**MAPIAllocateMore**で割り当てられたメモリ バッファーの間のリンクは、1 回の呼び出しの両方のバッファーを解放する**MAPIFreeBuffer**を有効にします。 
  

