---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396975"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
さらにアクセスするための[IAddrBook](iaddrbookimapiprop.md)ポインターを返す MAPI 統合アドレス帳を開きます。 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]表示に関連して、共通のアドレス] ダイアログ ボックスおよびその他の親ウィンドウへのハンドル。
    
 _lpInterface_
  
> [in]アドレス帳にアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 アドレス帳の標準的なインターフェイスへのポインターを返します**null**を渡す[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)。 
    
 _ulFlags_
  
> [in]アドレス帳の開始を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
AB_NO_DIALOG 
  
> ダイアログ ボックスの表示を抑制します。 AB_NO_DIALOG フラグが設定されていない場合内蔵のアドレス帳に寄与するアドレス帳プロバイダーで必要な情報がないユーザーに確認することができます。 
    
 _lppAdrBook_
  
> [out]アドレス帳へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳が正常に開かれました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しが成功したが、1 つまたは複数のアドレス帳プロバイダーのコンテナーを開くことができませんでした。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPISession::OpenAddressBook**メソッドでは、MAPI の統合のアドレス帳をプロファイル内のアドレス帳プロバイダーのすべての最上位のコンテナーのコレクションを開きます。 _LppAdrBook_パラメーターで返されるポインターをアドレス帳の内容へのアクセスをさらに提供します。 これにより、個々 のコンテナーを開き、メッセージング ユーザーの検索、および共通のアドレス] ダイアログ ボックスを表示するなどのタスクを実行する呼び出し元です。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook**は、1 つまたは複数のプロファイルで、アドレス帳プロバイダーをロードすることがある場合に MAPI_W_ERRORS_RETURNED を返します。 この値は、警告が表示されないエラーの値です。S_OK の場合と同様に処理します。 **OpenAddressBook**は、常に読み込みに失敗をアドレス帳プロバイダーの数に関係なく、 _lppAdrBook_パラメーターに有効なポインターを返します。 そのため、常にメソッドを呼び出してください、アドレス帳[が](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)ある時点でログオフする前にします。 
  
**OpenAddressBook**に MAPI_W_ERRORS_RETURNED が返されるときは、障害のあるプロバイダーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を取得するのには[IMAPISession::GetLastError](imapisession-getlasterror.md)を呼び出します。 すべてのプロバイダーから提供された情報が含まれる 1 つの**MAPIERROR**構造体が返されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI では、 **IMAPISession::OpenAddressBook**メソッドを使用して、内蔵のアドレス帳を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

