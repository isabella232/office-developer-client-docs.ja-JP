---
title: IMAPISupportMakeInvalid
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570738"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オブジェクトを使用不可としてマークを付けます。
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _lpObject_
  
> [in]無効化するオブジェクトへのポインター。 オブジェクトのインターフェイスは、 **IUnknown**から派生する必要があります。
    
 _ulRefCount_
  
> [in]オブジェクトの現在の参照カウント。
    
 _cMethods_
  
> [in]オブジェクトの vtable 内のメソッドの数。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> オブジェクトは、使用不可が正しく設定されました。
    
## <a name="remarks"></a>注釈

サポートのすべてのオブジェクトの**IMAPISupport::MakeInvalid**メソッドを実装します。 オブジェクトが無効になりますは、 **IUnknown**インターフェイスから、または**IUnknown**から派生したインターフェイスから派生する必要があります。
  
 **MakeInvalid**は、スタブのようなサイズが、 **IUnknown::AddRef**と**リ ス**のメソッドが期待どおりの vtable が同じオブジェクトの vtable に置き換えることによって使用不可としてオブジェクトをマークします。 ただし、他のすべてのメソッドが失敗する、MAPI_E_INVALID_OBJECT の値を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーとサービスのメッセージは通常のシャット ダウン時に**MakeInvalid**を呼び出します。 ただし、 **MakeInvalid**は、いつでも呼び出すことができます。 などのクライアントは、その下位オブジェクトのいくつかのボタンを押したままオブジェクトを解放する場合、は、これらの下位オブジェクトを解放するには、すぐに**MakeInvalid**を呼び出すことができます。 
  
無効にしようとするオブジェクトを所有する必要があります。 16 バイト長と、その vtable の少なくとも 3 つの方法があること必要があります。 
  
**MakeInvalid**を呼び出すし、シャット ダウンなどの作業、関連するデータ構造を破棄するオブジェクトのリリース中に通常行われるを実行できます。 MAPI が[MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによってメモリを解放して、オブジェクトを解放するため、オブジェクトをサポートするためにコードをメモリに保存されない必要があります。 リソースを解放し、 **MakeInvalid**を呼び出すし、無効化されたオブジェクトを無視できます。 
  
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

