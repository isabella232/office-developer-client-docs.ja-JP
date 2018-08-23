---
title: IMAPIFormGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetLastError
api_type:
- COM
ms.assetid: 81af8a0b-4ec2-459c-8ab2-29d28a8b680f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8b29298ab97518c2e346c2cdc5dee6baec28f8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800503"
---
# <a name="imapiformgetlasterror"></a>IMAPIForm::GetLastError

  
  
**適用対象**: Outlook 
  
前のフォーム オブジェクトによって生成されたエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
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
  
> セット、 _lppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列が Unicode 形式内にある場合。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。 取得する**MAPIERROR**構造体が存在しない場合、このパラメーターを NULL に設定することができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**発生しました**が、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていませんでしたし、 **GetLastError**は、Unicode だけをサポートしています。 
    
## <a name="remarks"></a>注釈

**IMAPIForm::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。 呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIERROR**指す構造体、 _lppMAPIError_パラメーターで 1 つは、MAPI が提供している場合**発生しました**が S_OK を返す場合にのみを使用することができます。 場合があります、MAPI ではその最後のエラーを判断できないか、エラーの報告には関係ありません。 このような場合は、NULL へのポインターが返されます_lppMAPIError_の代わりにします。 
  
**GetLastError**メソッドの詳細については、[拡張エラーの使用](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

