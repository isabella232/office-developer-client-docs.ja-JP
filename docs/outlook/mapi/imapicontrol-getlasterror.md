---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ab4aab0fe555445b56e2c42fbe7bc00505e44b36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596345"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のボタン コントロール エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
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
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

サービス プロバイダーは **、IMAPIControl::GetLastError** メソッドを実装して、失敗した以前のメソッド呼び出しに関する情報を提供します。 MAPI は、メッセージまたはダイアログ ボックスに **MAPIERROR** 構造のデータを表示することで、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

エラーごとに **MAPIERROR** 構造に含める情報を持つ必要はない。 以前のエラーが何だったかを判断できない場合があります。 情報がある場合は **、MAPIERROR** S_OK適切なデータを返します。 情報が使用できない場合は  _、lppMAPIError_ パラメーター S_OK NULL へのポインターを返します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

