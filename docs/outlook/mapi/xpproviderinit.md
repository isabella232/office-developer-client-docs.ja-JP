---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804245"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**適用されます**: Outlook 
  
操作のためのトランスポート プロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装されます。  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in]DLL が読み込まれるときに使用されるトランスポート プロバイダーのダイナミック リンク ライブラリ (DLL)、MAPI のインスタンスです。
    
 _lpMalloc_
  
> [in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 トランスポート プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。 
    
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
  
> [in]Mapi.dll を使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号です。 現在のバージョン番号は、Mapispi.h ヘッダー ファイルを参照してください。 
    
 _lpulProviderVer_
  
> [out]このトランスポート プロバイダーを使用する SPI のバージョン番号へのポインター。 
    
 _lppXPProvider_
  
> [out]初期化されたトランスポート プロバイダー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。
    
## <a name="remarks"></a>備考

MAPI は、クライアント ログオンを次のトランスポート プロバイダーを初期化するために**XPProviderInit**エントリ ポイント関数が呼び出されます。 **XPProviderInit**は、クライアントのプロファイルで指定されたトランスポート プロバイダーごとに 1 回呼び出されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

トランスポート プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**XPProviderInit**を実装する必要があります。 実装は、 **XPPROVIDERINIT**関数のプロトタイプで指定されている Mapispi.h もに基づいている必要があります。 MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**XPProviderInit**を STDMAPIINITCALLTYPE、 **XPPROVIDERINIT**を定義します。 CDECL の利点は、呼び出しのパラメーターの数が定義されているパラメーターの数と一致しない場合でも呼び出しを試行することができます。 
  
同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示される結果として、プロバイダーを複数回初期化できます。 プロバイダー オブジェクトには、コンテキストが含まれている、ため**XPProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppXPProvider_で、別のプロバイダー オブジェクトを返す必要があります。 
  
トランスポート プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。 具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。 プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
  
**XPProviderInit**の作成方法の詳細については、[トランスポート プロバイダーの初期化](initializing-the-transport-provider.md)を参照してください。 エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IXPProvider: IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

