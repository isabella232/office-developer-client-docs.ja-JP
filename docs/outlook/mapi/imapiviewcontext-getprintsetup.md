---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 58eccafa4faec96de0acacd4338798dba9f110d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556463"
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
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lppFormPrintSetup_
  
> [out]印刷情報を保持する構造体へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 印刷情報が正常に取得されました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **、IMAPIViewContext::GetPrintSetup** メソッドを呼び出して、現在のメッセージを印刷する前にプリンターのセットアップに関する情報を取得します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

Win32 関数 GlobalAlloc を使用して [、FORMPRINTSETUP](formprintsetup.md)構造体の **hDevMode** メンバーと **hDevName** メンバー **を割り当てる**。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppFormPrintSetup_ パラメーターが指す **FORMPRINTSETUP** 構造体の **hDevMode** メンバーと **hDevName** メンバーが Unicode 文字列である場合は _、ulFlags_ を MAPI_UNICODE に設定します。 それ以外の場合 **、GetPrintSetup** は ANSI 形式でこれらの文字列を返します。 
  
Win32 関数 GlobalFree を呼び出して **、FORMPRINTSETUP** 構造体の **hDevMode** メンバーと **hDevName** メンバーを **解放します**。 MAPIFreeBuffer **を呼び出して FORMPRINTSETUP** 構造 [全体を解放します](mapifreebuffer.md)。 
  
## <a name="see-also"></a>関連項目



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

