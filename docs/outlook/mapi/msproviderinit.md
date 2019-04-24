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
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342792"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作用のメッセージストアプロバイダーを初期化します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
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
  
> 順番MAPI がリンクしたときに使用したメッセージストアプロバイダーのダイナミックリンクライブラリ (DLL) のインスタンス。 
    
 _lpmalloc_
  
> 順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 メッセージストアプロバイダーは、 **IStream**など特定のインターフェイスを使用するときに、この割り当て方法を使用する必要がある場合があります。 
    
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
  
> 順番MAPI が使用するサービスプロバイダインターフェイス (SPI) のバージョン番号。 現在のバージョン番号については、Mapispi ヘッダーファイルを参照してください。 
    
 _lアウト providerver_
  
> 読み上げこのメッセージストアプロバイダーが使用する SPI のバージョン番号へのポインター。 
    
 _lppmsprovider_
  
> 読み上げ初期化されたメッセージストアプロバイダオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_VERSION 
  
> MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。
    
## <a name="remarks"></a>解説

MAPI はエントリポイント関数**msproviderinit**を呼び出して、クライアントログオンの後にメッセージストアプロバイダーを初期化します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージストアプロバイダーは、プロバイダーの DLL で**msproviderinit**をエントリポイント関数として実装する必要があります。 この実装は、MAPISPI でも指定されている**msproviderinit**関数プロトタイプに基づいている必要があります。H. mapi は、 **msproviderinit**を定義して、標準の mapi 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用します。これにより、 **msproviderinit**は CDECL の呼び出し規則に従います。 CDECL の利点は、呼び出し元のパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できることです。 
  
プロバイダーは、複数のプロファイルに同時に使用された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。 プロバイダーオブジェクトにはコンテキストが含まれているため、 **msproviderinit**は、同じプロセス内で複数の初期化があっても、各初期化に対して_lppmsprovider_の異なるプロバイダーオブジェクトを返す必要があります。 
  
プロバイダー DLL は、mapix にリンクしてはなりません。 代わりに、これらのポインターを使用してメモリの割り当てまたは割り当てを解除する必要があります。 
  
メッセージストアプロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。 特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。 プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。 
  
**msproviderinit**の記述の詳細については、「[メッセージストアプロバイダーの読み込み](loading-message-store-providers.md)」を参照してください。 エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

