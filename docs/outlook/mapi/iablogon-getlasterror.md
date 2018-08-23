---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1cd432540a4336b46a589e953b5ce4dde7553597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573664"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
以前のアドレス帳プロバイダーのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]以前のメソッドの呼び出しで生成されたエラーの値へのハンドル。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。 プロバイダーは、適切な情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは、失敗したメソッド呼び出しに関する情報を提供する**GetLastError**メソッドを実装します。 呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetLastError**が S_OK を返す場合にのみ、アドレス帳プロバイダーは、構造体を提供する場合、 _lppMAPIError_パラメーターが指す**MAPIERROR**構造体を使用することができます。 場合によってどのような最後のエラーまたはエラーを報告するのにはそれ以上には、アドレス帳プロバイダーは判断できません。 このような場合は、アドレス帳プロバイダーのポインター NULL に_lppMAPIError_の代わりに返します。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

