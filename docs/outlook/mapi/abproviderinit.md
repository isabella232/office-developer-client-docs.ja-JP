---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799613"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**適用されます**: Outlook 
  
操作のためのアドレス帳プロバイダーを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装されます。  <br/> |アドレス帳プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in]それにリンクされている場合に使用される MAPI アドレス帳プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンスです。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 アドレス帳プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。 
    
 _lpAllocateBuffer_
  
> [in]使用して MAPI によって必要なメモリを割り当て、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]使用して MAPI によって必要に応じて追加のメモリを割り当て、 [MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]MAPI によってメモリを解放するために必要な場合に使用する[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> [in]フラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、Windows サービス、特別な種類のすべてのユーザー インターフェイスにアクセスすることがなくプロセスのコンテキストで行われます。 
    
 _ulMAPIVer_
  
> [in]サービス プロバイダー インターフェイス (SPI)、MAPI のバージョン番号です。DLL を使用します。 現在のバージョン番号は、MAPISPI を参照してください。H ヘッダー ファイルです。 
    
 _lpulProviderVer_
  
> [out]このアドレス帳プロバイダーを使用する SPI のバージョン番号へのポインター。 
    
 _lppABProvider_
  
> [out]初期化済みのアドレス帳プロバイダー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。
    
## <a name="remarks"></a>備考

MAPI は、クライアント ログオンの後、アドレス帳プロバイダーを初期化するために**ABProviderInit**エントリ ポイント関数が呼び出されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

アドレス帳プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**ABProviderInit**を実装する必要があります。 実装は、 **ABPROVIDERINIT**関数のプロトタイプで指定されている MAPISPI もに基づいている必要があります。H. MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**ABProviderInit**を STDMAPIINITCALLTYPE、 **ABPROVIDERINIT**を定義します。 
  
プロバイダーは、同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示されるため、複数回初期化できます。 プロバイダー オブジェクトには、コンテキストが含まれている、ため**ABProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppABProvider_で、別のプロバイダー オブジェクトを返す必要があります。 
  
アドレス帳プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。 具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。 プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
  
**ABProviderInit**の作成方法の詳細については、[アドレス帳プロバイダーのエントリ ポイント関数を実装する](implementing-an-address-book-provider-entry-point-function.md)を参照してください。 エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [IABProvider: IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

