---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317165"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
form オブジェクトの前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 フォームが**MAPIERROR**構造に適切な情報を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、アドレス帳プロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、アドレス帳プロバイダーが unicode のみをサポートしています。
    
## <a name="remarks"></a>解説

Form オブジェクトは、失敗した前のメソッド呼び出しに関する情報を提供する**IPersistMessage:: GetLastError**メソッドを実装します。 フォームビューアーでは、 [MAPIERROR](mapierror.md)構造体のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。 
  
**GetLastError**を呼び出しても、フォームの状態には影響しません。 **GetLastError**が戻ると、フォームは呼び出しが行われる前の状態のままになります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームが S_OK を返す場合にのみ、 _lppMAPIError_パラメーターによってポイントされている場合は、 **MAPIERROR**構造体を使用できます。 **** 場合によっては、フォームで、エラーについてのレポートに最後のエラーがあったかどうかを判断できないこともあります。 このような状況では、フォームは代わりに_lppMAPIError_で NULL へのポインターを返します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

