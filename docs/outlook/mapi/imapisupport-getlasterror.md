---
title: imapisupportgetlasterror
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316598"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
以前のサポートオブジェクトエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番サポートオブジェクトの前のメソッド呼び出しで生成されたエラー値へのハンドル。
    
 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 適切なエラー情報を持つ**MAPIERROR**構造を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、mapi が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、mapi が unicode のみをサポートしています。
    
## <a name="remarks"></a>解説

**imapisupport:: GetLastError**メソッドは、すべてのサポートオブジェクトに実装されています。 呼び出し元は、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIERROR**構造体へのポインターは、 _lppMAPIError_パラメーターでは、 **GetLastError**が S_OK を返す場合にのみ使用できます。 MAPI では、最後のエラーが発生したかどうかを判断できない場合や、エラーについてのレポートを持っていない場合もあります。 このような状況では、 _lppMAPIError_は代わりに NULL へのポインターを返します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
MAPI によって割り当てられたすべてのメモリを解放するには、返された**MAPIERROR**構造体の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

