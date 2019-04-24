---
title: imapipropgetlasterror
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342050"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番前のメソッド呼び出しで生成されたエラーコードへのハンドル。
    
 _ulFlags_
  
> 順番_lppMAPIError_でポイントされている**MAPIERROR**構造体で返されるテキストの形式を示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列は、Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式である必要があります。
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 エラー情報を返さない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エラー情報が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>解説

**imapiprop:: GetLastError**メソッドは、失敗した前のメソッド呼び出しに関する情報を提供します。 クライアントは、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。 
  
MAPI で提供される**GetLastError**のすべての実装は、 [IAddrBook](iaddrbookimapiprop.md)の実装を除く ANSI 実装です。 **IAddrBook**に含まれている**GetLastError**メソッドは、Unicode をサポートしています。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

このメソッドのリモートトランスポートプロバイダーによる実装の詳細と、このメソッドが返すメッセージは、トランスポートプロバイダーによって異なります。これは、さまざまな HRESULT 値につながる特定のエラー条件が異なるトランスポートに対して異なるためです。会社.
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppMAPIError_パラメーターで示されている**MAPIERROR**構造体は、戻り値**** が S_OK の場合にのみ使用できます。 **GetLastError**では、最後のエラーが発生したかどうか、またはエラーについてのレポートを何にも持っていない場合があります。 このような場合、代わりに_lppMAPIError_で NULL へのポインターが返されます。 
  
**MAPIERROR**構造体のメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

