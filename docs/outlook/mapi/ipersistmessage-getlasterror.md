---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b82c42eb969c808810a571bd408e7c17b4f25cfe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604769"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム オブジェクトの前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される [MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 フォームが MAPIERROR 構造に適切な情報を提供できない場合は  _、lppMAPIError_ パラメーターを **NULL に設定** できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> アドレス帳MAPI_UNICODEフラグが設定され、アドレス帳プロバイダーが Unicode をサポートしていないか、MAPI_UNICODE が設定されていないと、アドレス帳プロバイダーは Unicode のみをサポートします。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **、IPersistMessage::GetLastError** メソッドを実装して、失敗した以前のメソッド呼び出しに関する情報を提供します。 フォーム ビューアーは、ダイアログ ボックスに [MAPIERROR](mapierror.md) 構造のデータを含め、エラーに関する詳細情報をユーザーに提供できます。 
  
**GetLastError の呼び出しは**、フォームの状態には影響を与えかねない。 **GetLastError が** 返された場合、フォームは呼び出しが行われた前の状態のままです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームが 1 つを提供する場合は **、GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターによって指される **MAPIERROR** 構造をS_OK。 フォームで、最後のエラーが何だったのかを判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では、フォームは代わりに  _lppMAPIError_ で NULL へのポインターを返します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

