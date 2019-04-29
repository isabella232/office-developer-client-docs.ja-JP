---
title: imapiviewcontextgetprintsetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425128"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在の印刷情報を取得します。
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される文字列の型を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lppformprintsetup_
  
> 読み上げ印刷情報を保持する構造体へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 印刷情報が正常に取得されました。
    
## <a name="remarks"></a>注釈

Form オブジェクトは、現在のメッセージを印刷する前に、プリンターの設定に関する情報を取得するために**imapiviewcontext:: getprintsetup**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

Win32 関数**GlobalAlloc**を使用して、 [formprintsetup](formprintsetup.md)構造の**hdevmode**および**hDevName**メンバーを割り当てます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppformprintsetup_パラメーターで指定された**formprintsetup**構造の**hdevmode**および**hDevName**メンバーが Unicode 文字列であると想定される場合は、 _ulflags_を MAPI_UNICODE に設定します。 それ以外の場合、 **getprintsetup**は ANSI 形式の文字列を返します。 
  
Win32 関数**GlobalFree**を呼び出すことにより、 **formprintsetup**構造の**hdevmode**および**hDevName**メンバーを解放します。 [MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことで、 **formprintsetup**構造全体を解放します。 
  
## <a name="see-also"></a>関連項目



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

