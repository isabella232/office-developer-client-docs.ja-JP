---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c436f4c33fdb88674eb090e0174fe728c6152562
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567530"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
前のセッション エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
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
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 MAPI が MAPIERROR 構造に適切な情報を提供できない場合は  _、lppMAPIError_ パラメーターを **NULL に設定** できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このMAPI_UNICODEが設定され、セッションは Unicode をサポートしていない。
    
## <a name="remarks"></a>注釈

**IMAPISession::GetLastError** メソッドは **、IMAPISession** メソッド呼び出しによって返された最後のエラーに関する情報を取得します。 クライアントは、この情報をダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が 1 つを提供する場合 **、MAPIERROR** 構造体を使用できます  _。lppMAPIError_ パラメーターが指すのは **、GetLastError** が値を返す場合S_OK。 MAPI では、最後のエラーが何だったのか判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では **、GetLastError は** 代わりに  _lppMAPIError_ で NULL へのポインターを返します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MAPI 拡張エラー](mapi-extended-errors.md)

