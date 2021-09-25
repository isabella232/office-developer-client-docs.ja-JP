---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea53639308f96c0b13641119e0e59dcc0a0359c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592726"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作用にアドレス帳プロバイダーを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
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
  
> [in]MAPI がリンク時に使用したアドレス帳プロバイダーの動的リンク ライブラリ (DLL) のインスタンス。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 アドレス帳プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。 
    
 _lpAllocateBuffer_
  
> [in]MAPI がメモリを割り当てる必要がある場合に使用する [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in] [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。MAPI が追加のメモリを割り当てる必要がある場合に使用します。 
    
 _lpFreeBuffer_
  
> [in] [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。MAPI がメモリを解放するために必要な場合に使用します。 
    
 _ulFlags_
  
> [in]フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、ユーザー インターフェイスにアクセスすることなく、Windowsサービスのコンテキストで読み込まれています。 
    
 _ulMAPIVer_
  
> [in]ユーザーが使用するサービス プロバイダー インターフェイス (SPI) MAPI.DLL番号。 現在のバージョン番号については、MAPISPI を参照してください。H ヘッダー ファイル。 
    
 _lpulProviderVer_
  
> [out]このアドレス帳プロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppABProvider_
  
> [out]初期化されたアドレス帳プロバイダー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。
    
## <a name="remarks"></a>注釈

MAPI は、エントリ ポイント関数 **ABProviderInit** を呼び出して、クライアント ログオン後にアドレス帳プロバイダーを初期化します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アドレス帳プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **ABProviderInit** を実装する必要があります。 実装は、MAPISPI.H でも指定 **されている ABPROVIDERINIT** 関数プロトタイプに基づく必要があります。 MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **ABPROVIDERINIT** が定義されています。この場合 **、ABProviderInit** は CDECL 呼び出し規約に従います。 
  
同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。 プロバイダー オブジェクトにはコンテキストが含まれているため **、ABProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppABProvider_ 内の異なるプロバイダー オブジェクトを返す必要があります。 
  
アドレス帳プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。 特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。 プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。 
  
**ABProviderInit の記述の詳細については、「** アドレス帳プロバイダーエントリ ポイント関数の実装 [」を参照してください](implementing-an-address-book-provider-entry-point-function.md)。 エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の実装 [」を参照してください](implementing-a-service-provider-entry-point-function.md)。 
  
## <a name="see-also"></a>関連項目

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

