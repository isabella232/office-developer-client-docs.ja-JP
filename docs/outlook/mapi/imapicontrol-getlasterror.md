---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421152"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のボタンコントロールのエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番前のメソッド呼び出しで生成されたエラー値へのハンドル。
    
 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 プロバイダーが適切な情報を使用して**MAPIERROR**構造を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>注釈

サービスプロバイダーは、失敗した前のメソッド呼び出しに関する情報を提供する**IMAPIControl:: GetLastError**メソッドを実装します。 MAPI では、メッセージまたはダイアログボックスに**MAPIERROR**構造のデータを表示することにより、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

すべてのエラーについて、 **MAPIERROR**構造体に情報を含める必要はありません。 以前のエラーの原因を特定できない場合があります。 情報がある場合は、 **MAPIERROR**構造体の S_OK および適切なデータを返します。 情報を使用できない場合は、 _lppMAPIError_パラメーターの S_OK および NULL へのポインターを返します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

