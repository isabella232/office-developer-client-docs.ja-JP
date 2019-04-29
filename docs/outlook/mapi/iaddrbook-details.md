---
title: iaddrbookdetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424680"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のアドレス帳エントリの詳細を表示するダイアログボックスを表示します。
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _l出 uiparam_
  
> 順番ダイアログボックスの親ウィンドウのハンドルへのポインター。
    
 _lpfnDismiss_
  
> 順番[DISMISSMODELESS](dismissmodeless.md)プロトタイプに基づく関数へのポインター、または NULL。 このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。 MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに、そのダイアログボックスがアクティブでなくなったことを示す**詳細**を呼び出していることをクライアントに通知する**DISMISSMODELESS**関数を呼び出します。 
    
 _lpvDismissContext_
  
> 順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。 このパラメーターは、DIALOG_SDI フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番詳細が表示されるエントリのエントリ識別子へのポインター。
    
 _lpfbuttoncallback_
  
> 順番[LPFNBUTTON](lpfnbutton.md)関数プロトタイプに基づく関数へのポインター。 **LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。 
    
 _lpvbuttoncontext_
  
> 順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。 
    
 _lpszbuttontext_
  
> 順番追加されたボタンに適用されるテキストを含む文字列へのポインター。ボタンが拡張可能な場合です。 拡張ボタンが必要ない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。 
    
 _ulFlags_
  
> 順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> アドレスに変更が実際に加えられた場合に、**詳細**が S_OK を返すことを示します。それ以外の場合、**詳細**は S_FALSE を返します。 
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログボックスのモーダルバージョンを表示します。これは、常に非 Outlook クライアントに表示されます。 このフラグは、DIALOG_SDI とは相互に排他的です。
    
DIALOG_SDI
  
>  [共通アドレス] ダイアログボックスのモードレスバージョンを表示します。 このフラグは、Outlook 以外のクライアントでは無視されます。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳エントリに対して [詳細] ダイアログボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは**Details**メソッドを呼び出して、アドレス帳の特定のエントリに関する詳細情報を提供するダイアログボックスを表示します。 _lpfbuttoncallback_、 _lpfbuttoncallback_、および_lpszbuttontext_パラメーターを使用して、クライアント定義ボタンをダイアログボックスに追加できます。 ボタンがクリックされると、MAPI は_lpfbuttoncallback_が指すコールバック関数を呼び出し、ボタンのエントリ識別子と_lpfbuttoncallback_のデータの両方を渡します。 拡張ボタンが必要ない場合は、 _lpszbuttontext_を NULL にする必要があります。 
  
 **詳細**は、Unicode 文字列をサポートしています。Unicode 文字列は、マルチバイト文字文字列 (MBCS) 形式に変換されてから、[詳細] ダイアログボックスに表示されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|basedialog  <br/> |cbasedialog:: onopenentryid  <br/> |mfcmapi は、 **details**メソッドを使用して、アドレス帳エントリの詳細を表示するダイアログボックスを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

