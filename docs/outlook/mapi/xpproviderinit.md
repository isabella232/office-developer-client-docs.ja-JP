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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428537"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作のためにトランスポートプロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|実装元:  <br/> |トランスポートプロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
   
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

## <a name="parameters"></a>パラメーター

 _hInstance_
  
> 順番dll を読み込んだときに MAPI が使用するトランスポートプロバイダーのダイナミックリンクライブラリ (dll) のインスタンス。
    
 _lpmalloc_
  
> 順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 **IStream**などの特定のインターフェイスを使用する場合、トランスポートプロバイダーはこの allocation メソッドを使用する必要がある場合があります。 
    
 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> 順番フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、ユーザーインターフェイスにアクセスできない特別な種類のプロセスである Windows サービスのコンテキストに読み込まれています。 
    
 _ulMAPIVer_
  
> 順番Mapi .dll が使用するサービスプロバイダインターフェイス (SPI) のバージョン番号。 現在のバージョン番号については、Mapispi ヘッダーファイルを参照してください。 
    
 _lアウト providerver_
  
> 読み上げこのトランスポートプロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppxps プロバイダ_
  
> 読み上げ初期化されたトランスポートプロバイダオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。
    
## <a name="remarks"></a>注釈

MAPI は、クライアントログオンの後にトランスポートプロバイダーを初期化するために、エントリポイント関数の**xps providerinit**を呼び出します。 クライアントのプロファイルに指定されている各トランスポートプロバイダーに対して、 **xps providerinit**が1回呼び出されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

トランスポートプロバイダーは、プロバイダーの DLL で、エントリポイント関数として、 **xps providerinit**を実装する必要があります。 この実装は、Mapispi でも指定されている、 **xps の init**関数プロトタイプに基づいている必要があります。 mapi では、STDMAPIINITCALLTYPE という標準の MAPI 初期化呼び出しの種類であるを使用するように、 **xps の init**が定義されています。これにより、 **xps の init**は CDECL の呼び出し規則に従います。 CDECL の利点は、呼び出し元のパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できることです。 
  
プロバイダーは、複数のプロファイルに同時に表示された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。 プロバイダーオブジェクトにはコンテキストが含まれているため、同じプロセス内で複数の初期化があっても、各初期化に対して、 **xps providerinit**は別のプロバイダーオブジェクトを_lppxps プロバイダー_で返す必要があります。 
  
トランスポートプロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。 特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。 プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。 
  
**xp の init**の記述の詳細については、「[トランスポートプロバイダーの初期化](initializing-the-transport-provider.md)」を参照してください。 エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

