---
title: imapisupportdetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426780"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
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
  
> 読み上げ返されたダイアログボックスの親ウィンドウへのハンドルへのポインター。
    
 _lpfnDismiss_
  
> 順番[DISMISSMODELESS](dismissmodeless.md)プロトタイプに基づく関数へのポインター、または NULL。 このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。 MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに**DISMISSMODELESS**関数を呼び出し、imapisupport を呼び出していることをクライアントに通知し**ます。 etails**は、このダイアログボックスがアクティブでなくなったことを示します。 
    
 _lpvDismissContext_
  
> 順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。 このパラメーターは、DIALOG_SDI フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番詳細が表示されるエントリ識別子へのポインター。
    
 _lpfbuttoncallback_
  
> 順番[LPFNBUTTON](lpfnbutton.md)関数プロトタイプに基づく関数へのポインター。 **LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。 
    
 _lpvbuttoncontext_
  
> 順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されるデータへのポインター。 
    
 _lpszbuttontext_
  
> 順番追加されたボタンが拡張可能な場合に、そのボタンに適用されるテキストを含む文字列へのポインター。 拡張ボタンを必要としない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。 
    
 _ulFlags_
  
> 順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログボックスのモーダルバージョンを表示します。 このフラグは、DIALOG_SDI とは相互に排他的です。
    
DIALOG_SDI
  
>  [共通アドレス] ダイアログボックスのモードレスバージョンを表示します。 このフラグは、DIALOG_MODAL とは相互に排他的です。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳エントリに対して [詳細] ダイアログボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

**imapisupport::D etails**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対して実装されています。 アドレス帳プロバイダーは、アドレス帳の特定のエントリに関する詳細情報を表示するダイアログボックスを表示するために呼び出す**詳細情報**を提供します。 _lpfbuttoncallback_、 _lpfbuttoncallback_、および_lpszbuttontext_パラメーターを使用して、クライアント定義ボタンをダイアログボックスに追加できます。 ボタンがクリックされると、MAPI は_lpfbuttoncallback_が指すコールバック関数を呼び出し、ボタンのエントリ識別子と_lpfbuttoncallback_のデータの両方を渡します。 拡張ボタンが必要ない場合は、 _lpszbuttontext_を NULL にする必要があります。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

