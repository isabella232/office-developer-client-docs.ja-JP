---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801655"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**適用対象**: Outlook 
  
操作のメッセージ ストア プロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>パラメーター

 _hInstance_
  
> [in]メッセージのインスタンスは、それにリンクされている場合、MAPI が使用されるプロバイダーのダイナミック リンク ライブラリ (DLL) を格納します。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 メッセージ ストア プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> [in]フラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、Windows サービス、特別な種類のすべてのユーザー インターフェイスにアクセスすることがなくプロセスのコンテキストで行われます。 
    
 _ulMAPIVer_
  
> [in]MAPI を使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号です。 現在のバージョン番号は、Mapispi.h ヘッダー ファイルを参照してください。 
    
 _lpulProviderVer_
  
> [out]このメッセージ ストア プロバイダーを使用する SPI のバージョン番号へのポインター。 
    
 _lppMSProvider_
  
> [out]初期化メッセージ ストア プロバイダー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。
    
## <a name="remarks"></a>注釈

MAPI は、クライアント ログオンの後、メッセージ ストア プロバイダーを初期化するために**MSProviderInit**エントリ ポイント関数が呼び出されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

メッセージ ストア プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**MSProviderInit**を実装する必要があります。 実装は、 **MSPROVIDERINIT**関数のプロトタイプで指定されている MAPISPI もに基づいている必要があります。H. MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**MSProviderInit**を STDMAPIINITCALLTYPE、 **MSPROVIDERINIT**を定義します。 CDECL の利点は、呼び出しのパラメーターの数が定義されているパラメーターの数と一致しない場合でも呼び出しを試行することができます。 
  
プロバイダーは、同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示されるため、複数回初期化できます。 プロバイダー オブジェクトには、コンテキストが含まれている、ため**MSProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppMSProvider_で、別のプロバイダー オブジェクトを返す必要があります。 
  
Mapix.dll で、プロバイダーの DLL をリンクしないようにします。 代わりに、メモリの割り当てまたは割り当て解除用には、これらのポインターを使用してください。 
  
メッセージ ストア プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。 具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。 プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
  
**MSProviderInit**の作成方法の詳細については、[メッセージ ストア プロバイダーの読み込み](loading-message-store-providers.md)を参照してください。 エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

