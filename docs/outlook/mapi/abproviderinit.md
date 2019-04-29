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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428285"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作のアドレス帳プロバイダーを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
   
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

## <a name="parameters"></a>パラメーター

 _hInstance_
  
> 順番MAPI がリンクしたときに使用したアドレス帳プロバイダーのダイナミックリンクライブラリ (DLL) のインスタンスです。 
    
 _lpmalloc_
  
> 順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 **IStream**など特定のインターフェイスを使用している場合、アドレス帳プロバイダーはこの割り当て方法を使用する必要がある場合があります。 
    
 _lpAllocateBuffer_
  
> 順番MAPI がメモリを割り当てる際に必要となる、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番MAPI が追加のメモリを割り当てる際に必要な、 [MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番MAPI がメモリを解放するために必要な場合に使用される、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> 順番フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、ユーザーインターフェイスにアクセスできない特別な種類のプロセスである Windows サービスのコンテキストに読み込まれています。 
    
 _ulMAPIVer_
  
> 順番MAPI が提供するサービスプロバイダインターフェイス (SPI) のバージョン番号。DLL はを使用します。 現在のバージョン番号については、MAPISPI を参照してください。H ヘッダーファイル。 
    
 _lアウト providerver_
  
> 読み上げこのアドレス帳プロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppabprovider_
  
> 読み上げ初期化されたアドレス帳プロバイダオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。
    
## <a name="remarks"></a>注釈

MAPI はエントリポイント関数**abproviderinit**を呼び出して、クライアントログオンの後にアドレス帳プロバイダーを初期化します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アドレス帳プロバイダーは、 **abproviderinit**をプロバイダーの DLL のエントリポイント関数として実装する必要があります。 この実装は、MAPISPI でも指定されている**abproviderinit**関数プロトタイプに基づいている必要があります。H. mapi では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用するように**abproviderinit**が定義されており、これにより、 **abproviderinit**が CDECL 呼び出し規則に従います。 
  
プロバイダーは、複数のプロファイルに同時に使用された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。 プロバイダーオブジェクトにはコンテキストが含まれているため、同じプロセス内で複数の初期化があっても、 **abproviderinit**がそれぞれの異なるプロバイダーオブジェクトを_lppabprovider_で返す必要があります。 
  
アドレス帳プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。 特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。 プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。 
  
**abproviderinit**の記述の詳細については、「[アドレス帳プロバイダーエントリポイント関数の実装](implementing-an-address-book-provider-entry-point-function.md)」を参照してください。 エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

