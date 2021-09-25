---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0830efe7ef5b76f2f25aca86a7d737bdc0810a03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567432"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトを使用不可としてマークします。
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _lpObject_
  
> [in]無効になるオブジェクトへのポインター。 オブジェクトのインターフェイスは **、IUnknown から派生する必要があります**。
    
 _ulRefCount_
  
> [in]オブジェクトの現在の参照カウント。
    
 _cMethods_
  
> [in]オブジェクトの vtable 内のメソッドの数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが使用不能として正常にマークされました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::MakeInvalid メソッド** は、すべてのサポート オブジェクトに実装されます。 無効になるオブジェクトは **、IUnknown インターフェイスまたは IUnknown** から派生したインターフェイスから派生 **している必要があります**。
  
 **MakeInvalid** は、オブジェクトの vtable を **、IUnknown::AddRef** メソッドと **IUnknown::Release** メソッドが期待通り実行する類似のサイズのスタブ vtable に置き換え、オブジェクトを使用不能としてマークします。 ただし、他のメソッドは失敗し、値が返MAPI_E_INVALID_OBJECT。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーとメッセージ サービスは、通常、シャットダウン時に **MakeInvalid** を呼び出します。 ただし **、MakeInvalid** は、いつでも呼び出されます。 たとえば、クライアントが一部のサブオブジェクトを解放せずにオブジェクトを解放する場合は **、MakeInvalid** をすぐに呼び出して、それらのサブオブジェクトを解放できます。 
  
無効にしようとするオブジェクトを所有する必要があります。 長さ 16 バイト以上で、vtable には少なくとも 3 つのメソッドが必要です。 
  
**MakeInvalid** を呼び出して、関連付けられたデータ構造の破棄など、通常はオブジェクトのリリース中に実行されるシャットダウン作業を実行できます。 MAPI は [MAPIFreeBuffer](mapifreebuffer.md) を呼び出してオブジェクトを解放することでメモリを解放しますので、オブジェクトをサポートするコードをメモリに保持する必要はありません。 リソースを解放し **、MakeInvalid を呼び出** し、無効化されたオブジェクトを無視できます。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

