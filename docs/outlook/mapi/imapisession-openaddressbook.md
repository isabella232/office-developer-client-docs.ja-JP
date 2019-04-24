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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329422"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 統合アドレス帳を開き、さらにアクセスするために[IAddrBook](iaddrbookimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番[共通アドレス] ダイアログボックスとその他の関連する表示の親ウィンドウへのハンドル。
    
 _lpinterface_
  
> 順番アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 **null**を渡すと、アドレス帳の標準インターフェイス[IAddrBook: imapiprop](iaddrbookimapiprop.md)へのポインターが返されます。 
    
 _ulFlags_
  
> 順番アドレス帳を開くかどうかを制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> ダイアログボックスの表示を抑制します。 AB_NO_DIALOG フラグが設定されていない場合、統合アドレス帳に投稿されるアドレス帳プロバイダーは、必要な情報の入力をユーザーに求めることができます。 
    
 _lppadrbook_
  
> 読み上げアドレス帳へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳が正常に開かれました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、1つ以上のアドレス帳プロバイダーのコンテナーを開くことができませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapisession:: OpenAddressBook**メソッドを実行すると、MAPI 統合アドレス帳 (プロファイル内のすべてのアドレス帳プロバイダーのトップレベルコンテナーのコレクション) が開きます。 _lppadrbook_パラメーターで返されるポインターは、アドレス帳の内容へのアクセスをさらに提供します。 これにより、発信者は、個々のコンテナーを開いたり、メッセージングユーザーを検索したり、共通のアドレスダイアログボックスを表示したりするなどのタスクを実行できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook**は、プロファイルにアドレス帳プロバイダーを1つ以上読み込むことができない場合、MAPI_W_ERRORS_RETURNED を返します。 この値は、エラー値ではなく警告です。これを S_OK として処理します。 **OpenAddressBook**は、いくつかのアドレス帳プロバイダーの読み込みに失敗したとしても、 _lppadrbook_パラメーターには常に有効なポインターを返します。 そのため、ログオフする前に、いつでもアドレス帳の[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。 
  
**OpenAddressBook**が MAPI_W_ERRORS_RETURNED を返す場合は、 [imapisession:: GetLastError](imapisession-getlasterror.md)を呼び出して、エラーが発生しているプロバイダーに関する情報を含む[MAPIERROR](mapierror.md)構造を取得します。 すべてのプロバイダーによって提供される情報を含む単一の**MAPIERROR**構造体が返されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects  <br/> |cmapiobjects:: GetAddrBook  <br/> |mfcmapi は、 **imapisession:: OpenAddressBook**メソッドを使用して、統合されたアドレス帳を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

