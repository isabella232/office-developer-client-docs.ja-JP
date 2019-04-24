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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329002"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番前のメソッド呼び出しで生成されたエラーを含む HRESULT。
    
 _ulFlags_
  
> 順番返される文字列の型を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。 _lppMAPIError_パラメーターは、適切な情報を持つ**MAPIERROR**構造体を提供できない場合は NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode がサポートされているかどうか。
    
## <a name="remarks"></a>解説

**IMAPITable:: GetLastError**メソッドは、エラーが発生した前のメソッド呼び出しに関する詳細情報を返します (使用可能な場合)。 この情報は、メッセージまたはダイアログボックスに表示できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

エラーに関する情報をユーザーに表示する必要がある場合は、必ず**GetLastError**を呼び出します。 
  
table オブジェクトが S_OK を返す場合にのみ、 _lppMAPIError_パラメーターでポイントする[MAPIERROR](mapierror.md)構造を使用できます。 **** 場合によっては、テーブルの実装によって、最後のエラーが発生したかどうか、またはエラーについてのレポートを作成できないことがあります。 この状況では、 _lppMAPIError_にあるポインターが NULL に設定されています。 
  
**MAPIERROR**構造体に割り当てられているすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

