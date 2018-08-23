---
title: IMAPIViewContextGetPrintSetup
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800880"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**適用対象**: Outlook 
  
現在、印刷情報を取得します。
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]関数が返す文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lppFormPrintSetup_
  
> [out]印刷の情報を保持する構造体へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 印刷の情報が正常に取得しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、現在のメッセージを印刷する前に、プリンターのセットアップに関する情報を取得するために**IMAPIViewContext::GetPrintSetup**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**GlobalAlloc**の Win32 関数を使用する[FORMPRINTSETUP](formprintsetup.md)構造体の**hDevMode**および**hDevName**のメンバーを割り当てます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

予定の場合、 **hDevMode** 、 **hDevName** 、 **FORMPRINTSETUP**構造体のメンバーが Unicode 文字列を指定する_lppFormPrintSetup_パラメーターが指す、 _ulFlags_を MAPI_UNICODE に設定します。 それ以外の場合、 **GetPrintSetup**では、ANSI 形式でこれらの文字列が返されます。 
  
**GlobalFree**の Win32 関数を呼び出すことによって、 **hDevMode**および**hDevName** 、 **FORMPRINTSETUP**構造体のメンバーを解放します。 [MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによって、全体の**FORMPRINTSETUP**構造体を解放します。 
  
## <a name="see-also"></a>関連項目



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

