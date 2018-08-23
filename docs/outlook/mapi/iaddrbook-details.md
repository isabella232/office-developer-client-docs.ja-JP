---
title: IAddrBookDetails
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592347"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。
  
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
  
> [in][DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じるとき**の詳細**] ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。 
    
 _lpvDismissContext_
  
> [in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。 このパラメーターは、 _ulFlags_パラメーターに DIALOG_SDI フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]詳細情報が表示されているエントリのエントリの識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in][LPFNBUTTON](lpfnbutton.md)関数のプロトタイプでは関数へのポインター。 **LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用されていたデータへのポインター。 
    
 _lpszButtonText_
  
> [in]そのボタンは拡張可能な場合、[追加] ボタンに適用するテキストを含む文字列へのポインター。 拡張ボタンを必要としない場合、 _lpszButtonText_パラメーターは NULL にする必要があります。 
    
 _ulFlags_
  
> [in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
AB_TELL_DETAILS_CHANGE
  
> **詳細**が S_OK を返すことを示しますアドレスに実際に変更を加えた場合。それ以外の場合、**詳細**は、S_FALSE を返します。 
    
DIALOG_MODAL
  
> Outlook 以外のクライアントでは常に表示は、一般的なアドレス] ダイアログ ボックスのモーダル バージョンを表示します。 このフラグは、DIALOG_SDI と相互に排他的です。
    
DIALOG_SDI
  
>  モードレスのバージョンの共通のアドレス] ダイアログ ボックスを表示します。 Outlook 以外のクライアントでは、このフラグは無視されます。 
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 詳細] ダイアログ ボックスは、アドレス帳のエントリを正常に表示されました。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションでは、アドレス帳の特定のエントリに関する詳細情報を提供するダイアログ ボックスを表示する**詳細**のメソッドを呼び出します。 ボタンを追加する、クライアントの定義] ダイアログ ボックスに、 _lpfButtonCallback_、 _lpvButtonContext_、および_lpszButtonText_パラメーターを使用できます。 ボタンがクリックされると、MAPI は、 _lpvButtonContext_のボタンとデータの両方のエントリ id を渡すこと_lpfButtonCallback_で指定されたコールバック関数を呼び出します。 場合は、[拡張] ボタンを使用する必要はありません、 _lpszButtonText_は NULL である必要があります。 
  
 **詳細**は、Unicode 文字の文字列をサポートしています。Unicode 文字列は、[詳細] タブに表示される前に、マルチバイト文字 (MBCS) の文字列形式に変換されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI では、**詳細**メソッドを使用して、アドレス帳エントリの詳細情報を示すダイアログ ボックスを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

