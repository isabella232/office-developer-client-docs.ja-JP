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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435391"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数で以前に割り当てられた別のバッファーにリンクされているメモリ バッファーを割り当てる。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>パラメーター

 _cbSize_
  
> [in]割り当てる新しいバッファーのサイズ (バイト単位)。 
    
 _lpObject_
  
> [in] **MAPIAllocateBuffer** を使用して割り当てられた既存の MAPI バッファーへのポインター。
    
 _lppBuffer_
  
> [out]返された、新しく割り当てられたバッファーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、要求されたメモリへのポインターを返しました。
    
## <a name="remarks"></a>注釈

**MAPIAllocateMore** 呼び出し処理中に、呼び出し元の実装はオペレーティング システムからメモリ ブロックを取得します。 メモリ バッファーは、番号が付くバイト アドレスに割り当てされます。 長整数アクセスの方が効率的なプラットフォームでは、オペレーティング システムは、バイト単位のサイズが 4 の倍数であるアドレスにバッファーを割り当てる。 
  
**MAPIAllocateMore** で割り当てられたバッファーを解放する唯一の方法は _、lpObject_ パラメーターで指定されたバッファー ポインターを [MAPIFreeBuffer](mapifreebuffer.md)関数に渡す方法です。 [MAPIAllocateBuffer](mapiallocatebuffer.md)と **MAPIAllocateMore** で割り当てられたメモリ バッファー間のリンクにより **、MAPIFreeBuffer** は 1 回の呼び出しで両方のバッファーを解放できます。 
  

