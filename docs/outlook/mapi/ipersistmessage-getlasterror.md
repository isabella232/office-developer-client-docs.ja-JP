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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a39deb57a24b3a89ee10020a6442bcb1bca612a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575309"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム オブジェクトでは、前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。 フォームは、 **MAPIERROR**構造体の適切な情報を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトでは、失敗したメソッド呼び出しに関する情報を提供する**IPersistMessage::GetLastError**メソッドを実装します。 フォーム ビューアーは、ダイアログ ボックスに[MAPIERROR](mapierror.md)構造体のデータを含めることによって、ユーザーにエラーに関する詳細な情報を提供できます。 
  
**GetLastError**の呼び出しは、フォームの状態には影響しません。 **GetLastError**から制御が戻るとき、フォームは、呼び出しが行われた前の状態には。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームが用意されて、1 つが**発生しました**が S_OK を返す場合にのみ、 _lppMAPIError_パラメーターで示される場合は、 **MAPIERROR**構造体を使用できます。 どのような最後のエラーまたはエラーを報告するのにはそれ以上には、フォームは判断できません。 このような場合は、フォームにポインターを返します NULL _lppMAPIError_の代わりにします。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

