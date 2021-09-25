---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 21905af0f4215dc5d25c4d768a5ecff9d0447b60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616860"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。
  
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

 _lpulUIParam_
  
> [in]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。
    
 _lpfnDismiss_
  
> [in] [DISMISSMODELESS](dismissmodeless.md) プロトタイプまたは NULL に基づく関数へのポインター。 このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。 MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった詳細を呼び出しているクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。 
    
 _lpvDismissContext_
  
> [in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。 このパラメーターは  _、ulFlags_ パラメーターに DIALOG_SDIフラグを含めて、ダイアログ ボックスのモードレス バージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]詳細が表示されるエントリのエントリ識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in] [LPFNBUTTON 関数プロトタイプに基づく関数への](lpfnbutton.md) ポインター。 **LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。 
    
 _lpszButtonText_
  
> [in]追加されたボタンに適用するテキストを含む文字列へのポインター (そのボタンが拡張可能な場合)。 _拡張可能ボタンが必要ない場合、lpszButtonText_ パラメーターは NULL である必要があります。 
    
 _ulFlags_
  
> [in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> Details が **アドレスに** 実際にS_OK変更された場合に、そのアドレスを返します。それ以外の場合 **、Details** はS_FALSE。 
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。これは、常にクライアント以外のクライアントOutlookされます。 このフラグは、このフラグと相互にDIALOG_SDI。
    
DIALOG_SDI
  
>  [共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。 このフラグは、クライアント以外のクライアントOutlookされます。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳エントリの詳細ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは Details メソッド **を呼び** 出して、アドレス帳内の特定のエントリに関する詳細を示すダイアログ ボックスを表示します。 _lpfButtonCallback_ パラメーター _、lpvButtonContext_ パラメーター、_および lpszButtonText_ パラメーターを使用して、クライアント定義ボタンをダイアログ ボックスに追加できます。 ボタンをクリックすると、MAPI は  _lpfButtonCallback_ が指すコールバック関数を呼び出し、ボタンのエントリ識別子と  _lpvButtonContext_ のデータの両方を渡します。 拡張可能ボタンが必要ない場合  _、lpszButtonText_ は NULL である必要があります。 
  
 **詳細は** Unicode 文字文字列をサポートします。Unicode 文字列は、詳細ダイアログ ボックスに表示される前に、マルチバイト文字文字列 (MBCS) 形式に変換されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI は Details メソッド **を** 使用して、アドレス帳エントリの詳細を示すダイアログ ボックスを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

