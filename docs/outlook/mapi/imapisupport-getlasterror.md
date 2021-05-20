---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438548"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
以前のサポート オブジェクト エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]サポート オブジェクトの前のメソッド呼び出しで生成されたエラー値のハンドル。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 適切なエラー情報を持つ MAPIERROR 構造体を指定できない場合は  _、lppMAPIError_ パラメーターを **NULL** に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、MAPI が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE MAPI は Unicode のみをサポートします。
    
## <a name="remarks"></a>注釈

**IMAPISupport::GetLastError** メソッドは、すべてのサポート オブジェクトに実装されます。 発信者は **、MAPIERROR** 構造のデータをダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が 1 つを提供する場合 **、MAPIERROR** 構造体へのポインターを  _lppMAPIError_ パラメーターで使用できるのは **、GetLastError** が関数を返す場合S_OK。 MAPI では、最後のエラーが何だったのか判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では  _、lppMAPIError は_ NULL へのポインターを代わりに返します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
MAPI によって割り当てられたすべてのメモリを解放するには、返される MAPIERROR 構造体の [MAPIFreeBuffer](mapifreebuffer.md) 関数 **を呼び出** します。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

