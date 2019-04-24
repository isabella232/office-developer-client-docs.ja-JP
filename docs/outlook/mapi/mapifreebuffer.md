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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346663"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリバッファーを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lpbuffer_
  
> 順番以前に割り当てられたメモリバッファーへのポインター。 _lpbuffer_パラメーターで NULL が渡された場合、 **MAPIFreeBuffer**は何も実行しません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、要求されたメモリが解放されました。 **MAPIFreeBuffer**は、既に解放されている場所にある S_OK を返すことも、 **MAPIAllocateBuffer**および**MAPIAllocateMore**を使用してメモリブロックが割り当てられていない場合もあります。
    
## <a name="remarks"></a>解説

通常、クライアントアプリケーションまたはサービスプロバイダーが[MAPIAllocateBuffer](mapiallocatebuffer.md)または[MAPIAllocateMore](mapiallocatemore.md)を呼び出す場合、オペレーティングシステムは、複数のポインターレベルを持つ1つまたは複数の複雑な構造体に1つ以上の連続したメモリバッファーを構築します。 mapi 関数またはメソッドがこのような内容のバッファーを作成すると、クライアントは後でバッファーに格納されているすべての構造を解放して、バッファーを作成した mapi 関数によって返されるバッファーへのポインターを**MAPIFreeBuffer**に渡します。 **MAPIFreeBuffer**を使用してメモリバッファーを解放するサービスプロバイダーの場合は、プロバイダーのサポートオブジェクトで返されるバッファーにポインターを渡す必要があります。 
  
**MAPIFreeBuffer**の呼び出しは、クライアントまたはプロバイダーがこのバッファーを使用して終了した直後に、特定のバッファーを解放する必要があります。 MAPI セッションの終了時に[imapisession:: Logoff](imapisession-logoff.md)メソッドを呼び出すだけでは、メモリバッファーは自動的には解放されません。 
  
クライアントまたはサービスプロバイダーは、 **MAPIFreeBuffer**から正常に復帰した後、 _lpbuffer_で渡されたポインターが無効であることを前提として動作する必要があります。 **MAPIAllocateBuffer**または**MAPIAllocateMore**を介して、メッセージングシステムによって割り当てられていないメモリブロックまたは空きメモリブロックのいずれかがポインターに示されている場合、 **MAPIFreeBuffer**の動作は未定義です。 
  
> [!NOTE]
> **MAPIFreeBuffer**に null ポインターを渡すと、 **MAPIFreeBuffer**はポインターを null に初期化し、それを最初にテストしなくても、ポインターを null に初期化し、クリーンアップコード内でそれらを解放できるため、アプリケーションのクリーンアップコードがより簡単になります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

