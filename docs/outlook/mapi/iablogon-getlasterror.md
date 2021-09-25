---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1a72a65a1d53329a13eac38364b8af8de73a2c0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571928"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
以前のアドレス [帳プロバイダー エラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]前のメソッド呼び出しで生成されたエラー値のハンドル。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 プロバイダーが適切な情報を MAPIERROR 構造体に指定できない場合は  _、lppMAPIError_ パラメーターを **NULL** に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> アドレス帳MAPI_UNICODEフラグが設定され、アドレス帳プロバイダーが Unicode をサポートしていないか、MAPI_UNICODE が設定されていないと、アドレス帳プロバイダーは Unicode のみをサポートします。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは **、GetLastError メソッドを実装して** 、失敗した以前のメソッド呼び出しに関する情報を提供します。 発信者は **、MAPIERROR** 構造のデータをダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

アドレス帳プロバイダーが構造体を提供する場合、および **GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターが示す **MAPIERROR** 構造をS_OK。 アドレス帳プロバイダーは、最後のエラーが何だったのか、エラーについて報告する必要がなにもない場合があります。 この状況では、アドレス帳プロバイダーは、代わりに  _lppMAPIError_ で NULL へのポインターを返します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

