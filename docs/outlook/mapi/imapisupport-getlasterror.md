---
title: IMAPISupportGetLastError
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577507"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
以前のサポート オブジェクトのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]サポート オブジェクトの以前のメソッドの呼び出しで生成されたエラー値へのハンドル。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。 適切なエラー情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された MAPI が Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、MAPI は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>注釈

サポートのすべてのオブジェクトの**IMAPISupport::GetLastError**メソッドを実装します。 呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が指定、 _lppMAPIError_パラメーターで**発生しました**が S_OK を返す場合にのみ場合は、 **MAPIERROR**構造体へのポインターを使用できます。 場合によっては MAPI が最後にエラーがあったものを判定することはできませんまたはエラーのレポートには関係ありません。 このような場合は、 _lppMAPIError_のポインターを返します NULL に代わりにします。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
MAPI によって割り当てられたすべてのメモリを解放するには、返された**MAPIERROR**構造体の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI �g���G���[](mapi-extended-errors.md)

