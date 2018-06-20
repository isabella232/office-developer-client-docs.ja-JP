---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b8ee83ad550106ae82f3308b9ef5692f66f5f5b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800837"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**適用されます**: Outlook 
  
テーブルの前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in]HRESULT がメソッドの以前の呼び出しで生成されたエラーが含まれています。
    
 _ulFlags_
  
> [in]関数が返す文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報が含まれている返された**MAPIERROR**構造体へのポインターへのポインター。 適切な情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装には、Unicode のみサポートしています。
    
## <a name="remarks"></a>備考

**IMAPITable::GetLastError**メソッドは、可能な場合、失敗したメソッド呼び出しに関する詳細についてを返します。 メッセージまたはダイアログ ボックスでは、この情報を表示できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

エラーに関する情報をユーザーに表示する必要があるときに、 **GetLastError**を呼び出します。 
  
[MAPIERROR](mapierror.md)の使用を行うことができます構造が、 _lppMAPIError_パラメーターが指す場合は、table オブジェクトでは 1 つが提供される**GetLastError**が S_OK を返す場合にのみです。 テーブルの実装では、どのような最後のエラーまたはエラーの報告には関係ありませんを決定できません。 このような場合は、 _lppMAPIError_でポインターは NULL に設定します。 
  
**MAPIERROR**構造体に割り当てられたすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

