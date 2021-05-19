---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410554"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリ バッファーを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lpBuffer_
  
> [in]以前に割り当てられたメモリ バッファーへのポインター。 lpBuffer パラメーターで  _NULL が渡_ された場合 **、MAPIFreeBuffer は何** もしません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、要求されたメモリを解放しました。 **MAPIFreeBuffer** は、既に解放されたS_OKまたは **MAPIAllocateBuffer** と **MAPIAllocateMore** でメモリ ブロックが割り当てられていない場合に、この値を返す場合もあります。
    
## <a name="remarks"></a>注釈

通常、クライアント アプリケーションまたはサービス プロバイダーが [MAPIAllocateBuffer](mapiallocatebuffer.md) または [MAPIAllocateMore](mapiallocatemore.md)を呼び出す場合、オペレーティング システムは、複数のレベルのポインターを持つ 1 つ以上の複雑な構造を 1 つの連続したメモリ バッファーに構築します。 MAPI 関数またはメソッドがこのような内容のバッファーを作成すると、クライアントは、バッファーを作成した MAPI 関数によって返されるバッファーへのポインターを **MAPIFreeBuffer** に渡して、バッファーに含まれるすべての構造体を後で解放できます。 サービス プロバイダーが **MAPIFreeBuffer** を使用してメモリ バッファーを解放するには、プロバイダーのサポート オブジェクトで返されるバッファーへのポインターを渡す必要があります。 
  
特定のバッファーを **解放する MAPIFreeBuffer** の呼び出しは、クライアントまたはプロバイダーがこのバッファーの使用を終了するとすぐに行う必要があります。 MAPI セッションの [最後に IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出すだけで、メモリ バッファーは自動的に解放されません。 
  
クライアントまたはサービス プロバイダーは  _、MAPIFreeBuffer_ から正常に戻った後、lpBuffer で渡されたポインターが無効であるという前提で **動作する必要があります**。 **MAPIAllocateBuffer** または **MAPIAllocateMore** または空きメモリ ブロックを介してメッセージング システムによって割り当てられていないメモリ ブロックがポインターによって示されている場合 **、MAPIFreeBuffer** の動作は未定義です。 
  
> [!NOTE]
> **MAPIFreeBuffer** に null ポインターを渡すと **、MAPIFreeBuffer** は NULL へのポインターを初期化し、最初にテストすることなくクリーンアップ コードで解放できるので、アプリケーションのクリーンアップ コードを簡単かつ小さくできます。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

