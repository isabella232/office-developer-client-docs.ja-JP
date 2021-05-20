---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435832"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のエラー [に関する](mapierror.md) 情報を含む MAPIERROR 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]前のメソッド呼び出しで生成されたエラー コードのハンドル。
    
 _ulFlags_
  
> [in]_lppMAPIError_ によって指される **MAPIERROR** 構造で返されるテキストの形式を示すフラグのビットマスクです。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列は Unicode 形式である必要があります。 このフラグMAPI_UNICODE設定しない場合、文字列は ANSI 形式である必要があります。
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 _lppMAPIError パラメーター_ は、返すエラー情報がない場合は NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エラー情報が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetLastError** メソッドは、失敗した以前のメソッド呼び出しに関する情報を提供します。 クライアントは、ダイアログ ボックスに **MAPIERROR** 構造のデータを含め、エラーに関する詳細情報をユーザーに提供できます。 
  
MAPI によって提供される **GetLastError** の実装はすべて [、IAddrBook](iaddrbookimapiprop.md) 実装を除く ANSI 実装です。 **IAddrBook に含まれる GetLastError** メソッド **は Unicode** をサポートしています。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート トランスポート プロバイダーによるこのメソッドの実装の詳細と、このメソッドが返すメッセージの詳細は、さまざまな HRESULT 値につながる特定のエラー条件がトランスポート プロバイダーによって異なってきます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

戻り値が指定されている場合にのみ **、GetLastError** が 1 を提供する場合は _、lppMAPIError_ パラメーターが指す **MAPIERROR** 構造をS_OK。 **GetLastError では、** 最後のエラーが何だったのか、またはエラーについて報告する必要がなにもない場合があります。 この状況では、代わりに  _lppMAPIError_ で NULL へのポインターが返されます。 
  
**MAPIERROR** 構造体のメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

