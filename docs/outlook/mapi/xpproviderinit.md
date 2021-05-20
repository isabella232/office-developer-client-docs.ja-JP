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
  
操作用にトランスポート プロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|実装元:  <br/> |トランスポート プロバイダー  <br/> |
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
  
> [in]MAPI が DLL の読み込み時に使用したトランスポート プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンス。
    
 _lpMalloc_
  
> [in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 トランスポート プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _ulFlags_
  
> [in]フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NT_SERVICE 
  
> プロバイダーは、ユーザー インターフェイスにアクセスすることなく、Windowsサービスのコンテキストで読み込まれています。 
    
 _ulMAPIVer_
  
> [in]ユーザーが使用するサービス プロバイダー インターフェイス (SPI) Mapi.dll番号。 現在のバージョン番号については、Mapispi.h ヘッダー ファイルを参照してください。 
    
 _lpulProviderVer_
  
> [out]このトランスポート プロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppXPProvider_
  
> [out]初期化されたトランスポート プロバイダー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。
    
## <a name="remarks"></a>注釈

MAPI は、エントリ ポイント関数 **XPProviderInit** を呼び出して、クライアント ログオン後にトランスポート プロバイダーを初期化します。 **XPProviderInit は** 、クライアントのプロファイルで指定されたトランスポート プロバイダーごとに 1 回呼び出されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

トランスポート プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **XPProviderInit** を実装する必要があります。 実装は **、Mapispi.h でも指定された XPPROVIDERINIT** 関数プロトタイプに基づく必要があります。 MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **XPPROVIDERINIT** が定義されています。この場合 **、XPProviderInit** は CDECL 呼び出し規約に従います。 CDECL の利点は、呼び出しパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できる点です。 
  
同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。 プロバイダー オブジェクトにはコンテキストが含まれているため **、XPProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppXPProvider_ 内の別のプロバイダー オブジェクトを返す必要があります。 
  
トランスポート プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。 特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。 プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。 
  
**XPProviderInit の記述の詳細については、「トランスポート** プロバイダーの [初期化」を参照してください](initializing-the-transport-provider.md)。 エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の [実装」を参照してください](implementing-a-service-provider-entry-point-function.md)。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

