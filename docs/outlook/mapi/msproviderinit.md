---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5d9a31a768ca588971fa0e22c1ab8c4d659753d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595652"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作用にメッセージ ストア プロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
   
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
  
> [in]MAPI がリンク時に使用したメッセージ ストア プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンス。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 メッセージ ストア プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。 
    
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
  
> [in]MAPI が使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号。 現在のバージョン番号については、Mapispi.h ヘッダー ファイルを参照してください。 
    
 _lpulProviderVer_
  
> [out]このメッセージ ストア プロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppMSProvider_
  
> [out]初期化されたメッセージ ストア プロバイダー オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。
    
## <a name="remarks"></a>注釈

MAPI は、エントリ ポイント関数 **MSProviderInit** を呼び出して、クライアント ログオン後にメッセージ ストア プロバイダーを初期化します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージ ストア プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **MSProviderInit** を実装する必要があります。 実装は **、MAPISPI.H でも指定されている MSPROVIDERINIT** 関数プロトタイプに基づく必要があります。 MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **MSPROVIDERINIT** が定義されています。この場合 **、MSProviderInit** は CDECL 呼び出し規約に従います。 CDECL の利点は、呼び出しパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できる点です。 
  
同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。 プロバイダー オブジェクトにはコンテキストが含まれているため **、MSProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppMSProvider_ 内の別のプロバイダー オブジェクトを返す必要があります。 
  
プロバイダー DLL は、プロバイダー DLL とリンクMapix.dll。 代わりに、メモリ割り当てまたは割り当て解除にこれらのポインターを使用する必要があります。 
  
メッセージ ストア プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。 特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。 プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。 
  
**MSProviderInit の記述の詳細については、「メッセージ** ストア プロバイダーの読み込 [み」を参照してください](loading-message-store-providers.md)。 エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の [実装」を参照してください](implementing-a-service-provider-entry-point-function.md)。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

