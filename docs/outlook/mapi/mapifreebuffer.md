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
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569142"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数または[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しで割り当てられたメモリ バッファーを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>パラメーター

 _lpBuffer_
  
> [in]以前に割り当てられたメモリ バッファーへのポインター。 _LpBuffer_パラメーターに NULL を渡した場合は、 **MAPIFreeBuffer**は何もしません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、要求されたメモリを解放します。 **MAPIFreeBuffer**では、既に解放された場所または**MAPIAllocateBuffer**と**MAPIAllocateMore**を持つメモリ ブロックが割り当てられていないかどうかに S_OK を返すこともします。
    
## <a name="remarks"></a>注釈

通常、クライアント アプリケーションまたはサービス プロバイダーを呼び出すと[MAPIAllocateBuffer](mapiallocatebuffer.md)または[MAPIAllocateMore](mapiallocatemore.md)、1 つの連続するメモリ バッファーにオペレーティング システムの構成要素のポインターの複数のレベルの 1 つまたは複数の複雑な構造です。 MAPI の関数またはメソッドは、このような内容でバッファーを作成するとき、クライアントは後で**MAPIFreeBuffer**にバッファーを作成した MAPI 関数から返されるバッファーへのポインターを渡すことによって、バッファーに含まれるすべての構造体を解放できます。 サービス プロバイダーが**MAPIFreeBuffer**を使用してメモリ バッファーを解放するには、プロバイダーのサポート オブジェクトが返されるバッファーへのポインターを渡す必要があること。 
  
特定のバッファーを解放するのには、 **MAPIFreeBuffer**への呼び出しは、クライアントとすぐに行う必要があります。 またはプロバイダーは、このバッファーの使用を終了します。 MAPI セッションの最後に[IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すだけでも、メモリ バッファーは自動的に解放されません。 
  
クライアントまたはサービス プロバイダーは、 _lpBuffer_で、渡されたポインターが無効である**MAPIFreeBuffer**から正常に戻った後を前提として動作する必要があります。 ポインターには、 **MAPIAllocateBuffer**または**MAPIAllocateMore**またはメモリの空きブロックを使用してメッセージング システムによって割り当てられなかったメモリ ブロックが示されている場合の**MAPIFreeBuffer**の動作は定義されていません。 
  
> [!NOTE]
> **MAPIFreeBuffer**に null ポインターを渡すことにより、アプリケーションのクリーンアップ コードより単純で小さな**MAPIFreeBuffer**が NULL へのポインターを初期化し、それらを最初にテストすることがなくクリーンアップ コードで解放するためです。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

