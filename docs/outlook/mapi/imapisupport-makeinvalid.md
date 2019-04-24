---
title: imapisupportmakeinvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316661"
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
  
> 予約語0である必要があります。
    
 _lpObject_
  
> 順番無効化されるオブジェクトへのポインター。 オブジェクトのインターフェイスは、 **IUnknown**から派生している必要があります。
    
 _ulrefcount_
  
> 順番オブジェクトの現在の参照カウント。
    
 _cmethods_
  
> 順番オブジェクトの vtable 内のメソッドの数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に使用できないとマークされました。
    
## <a name="remarks"></a>解説

**imapisupport:: makeinvalid**メソッドは、すべてのサポートオブジェクトに実装されています。 無効化するオブジェクトは、 **iunknown**インターフェイスまたは**iunknown**から派生したインターフェイスから派生している必要があります。
  
 **makeinvalid**は、オブジェクトの vtable を、 **iunknown:: AddRef**メソッドと**iunknown:: Release**メソッドが期待どおりに実行するのと同じようなサイズのスタブ vtable で置き換えることにより、オブジェクトを使用不能としてマークします。 ただし、その他のメソッドは失敗し、値 MAPI_E_INVALID_OBJECT が返されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービスプロバイダーとメッセージサービスは、通常、シャットダウン時に**makeinvalid**を呼び出します。 ただし、 **makeinvalid**はいつでも呼び出すことができます。 たとえば、クライアントがオブジェクトを解放せずにそのサブオブジェクトの一部を解放しない場合は、直ちに**makeinvalid**を呼び出すことで、それらのサブオブジェクトを解放できます。 
  
無効にしようとしているオブジェクトを所有している必要があります。 少なくとも16バイトの長さで、vtable に少なくとも3つのメソッドが含まれている必要があります。 
  
**makeinvalid**を呼び出してから、関連付けられたデータ構造を破棄するなど、通常はオブジェクトのリリース時に実行されるすべてのシャットダウン作業を実行できます。 MAPI は[MAPIFreeBuffer](mapifreebuffer.md)を呼び出してメモリを解放し、その後オブジェクトを解放するため、オブジェクトをサポートするコードをメモリに保持する必要はありません。 リソースを解放し、 **makeinvalid**を呼び出し、無効化されたオブジェクトを無視することができます。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

