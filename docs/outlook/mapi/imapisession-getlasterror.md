---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800681"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**適用されます**: Outlook 
  
前のセッションのエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in]以前のメソッドの呼び出しで生成されたエラーの値へのハンドル。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。 MAPI は、 **MAPIERROR**構造体の適切な情報を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定され、セッションが Unicode をサポートしていません。
    
## <a name="remarks"></a>備考

**IMAPISession::GetLastError**メソッドは、 **IMAPISession**メソッドの呼び出しによって返された最後のエラーに関する情報を取得します。 クライアントは、ダイアログ ボックスでこの情報を含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が提供を 1 つ**返します**は S_OK を返し、 _lppMAPIError_パラメーター場合にのみが指す場合は、 **MAPIERROR**構造体を使用できます。 場合があります、MAPI ではその最後のエラーを判断できないか、エラーの報告には関係ありません。 このような場合は、 **GetLastError**のポインターを返します NULL に_lppMAPIError_の代わりにします。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MAPI の拡張エラー](mapi-extended-errors.md)

