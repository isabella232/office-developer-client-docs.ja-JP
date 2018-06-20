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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800650"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**適用されます**: Outlook 
  
前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in]以前のメソッドの呼び出しで生成されたエラー コードへのハンドル。
    
 _ulFlags_
  
> [in]_LppMAPIError_が指す**MAPIERROR**の構造体で返されるテキストの書式を示すフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 文字列は、Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列を引き起こすことがあります。
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。 返されるエラー情報がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> エラー情報が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>備考

**IMAPIProp::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。 クライアントは、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
すべての MAPI によって提供されている**GetLastError**の実装は、 [IAddrBook](iaddrbookimapiprop.md)の実装を除いて、ANSI の実装です。 **IAddrBook**に含まれている**GetLastError**メソッドは、Unicode をサポートしています。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

HRESULT 値のさまざまな原因となる特定のエラー条件が異なるさまざまなトランスポートのため、リモートの詳細トランスポート プロバイダーのこのメソッドを実装し、トランスポート プロバイダーでは、このメソッドが返すメッセージとはプロバイダーです。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIERROR**構造体を_lppMAPIError_パラメーターで戻り値が S_OK の場合にのみ、1 つ**発生しました**提供する場合を使用することができます。 どのような最後のエラーまたはエラーを報告するのにはそれ以上には、 **GetLastError**は判断できません。 このような場合は、NULL へのポインターが返されます_lppMAPIError_の代わりにします。 
  
**MAPIERROR**構造体のメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MAPI の拡張エラー](mapi-extended-errors.md)

