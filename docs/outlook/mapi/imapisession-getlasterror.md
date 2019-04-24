---
title: imapisessiongetlasterror
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338683"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のセッションエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
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
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 MAPI が**MAPIERROR**構造体について適切な情報を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、セッションは UNICODE をサポートしていません。
    
## <a name="remarks"></a>解説

**imapisession:: GetLastError**メソッドは、 **imapisession**メソッド呼び出しによって返された最後のエラーに関する情報を取得します。 クライアントは、この情報をダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIERROR**構造体は、 _lppMAPIError_パラメーターで指定された MAPI が S_OK を返す場合にのみ**** 使用できます。 MAPI では、最後のエラーが発生したかどうかを判断できない場合や、エラーについてのレポートを持っている場合もあります。 このような場合、 _lppMAPIError_では、 **GetLastError**は NULL へのポインターを代わりに返します。 
  
**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

