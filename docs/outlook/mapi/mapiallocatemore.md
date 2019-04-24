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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357317"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で以前に割り当てられた別のバッファーにリンクされているメモリバッファーを割り当てます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>パラメーター

 _cbSize_
  
> 順番割り当てる新しいバッファーのサイズをバイト単位で指定します。 
    
 _lpObject_
  
> 順番**MAPIAllocateBuffer**を使用して割り当てられた既存の MAPI バッファーへのポインター。
    
 _lppbuffer_
  
> 読み上げ新しく割り当てられたバッファーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、要求されたメモリへのポインターが返されました。
    
## <a name="remarks"></a>解説

**MAPIAllocateMore**呼び出し処理の間、呼び出し側の実装はオペレーティングシステムからメモリブロックを取得します。 メモリバッファーは、偶数番号のバイトアドレスに割り当てられます。 長い整数アクセスがより効率的になるプラットフォームでは、オペレーティングシステムは、バイト数が4の倍数であるアドレスにバッファーを割り当てます。 
  
**MAPIAllocateMore**で割り当てられたバッファーを解放する唯一の方法は、 _lpObject_パラメーターで指定したバッファーポインターを[MAPIFreeBuffer](mapifreebuffer.md)関数に渡すことです。 [MAPIAllocateBuffer](mapiallocatebuffer.md)および**MAPIAllocateMore**で割り当てられたメモリバッファー間のリンクによって、 **MAPIFreeBuffer**は両方のバッファーを1回の呼び出しで解放できます。 
  

