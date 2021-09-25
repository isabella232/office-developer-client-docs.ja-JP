---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c7344829c9d4478d098a79b15a0a8cff4824a404
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567516"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 統合アドレス帳を開き [、IAddrBook](iaddrbookimapiprop.md) ポインターを返してさらにアクセスします。 
  
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
  
> [in]共通のアドレス ダイアログ ボックスの親ウィンドウへのハンドルと、その他の関連する表示。
    
 _lpInterface_
  
> [in]アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 **null を渡** すと、アドレス帳の標準インターフェイス [IAddrBook : IMAPIProp へのポインターが返されます](iaddrbookimapiprop.md)。 
    
 _ulFlags_
  
> [in]アドレス帳の開きを制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> ダイアログ ボックスの表示を抑制します。 AB_NO_DIALOGフラグが設定されていない場合、統合アドレス帳に貢献するアドレス帳プロバイダーは、必要な情報をユーザーに求めるメッセージを表示できます。 
    
 _lppAdrBook_
  
> [out]アドレス帳へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳が正常に開かされました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、1 つ以上のアドレス帳プロバイダーのコンテナーを開く必要がありました。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISession::OpenAddressBook** メソッドは、プロファイル内のすべてのアドレス帳プロバイダーのトップ レベル コンテナーのコレクションである MAPI 統合アドレス帳を開きます。 _lppAdrBook_ パラメーターで返されるポインターは、アドレス帳の内容にさらにアクセスできます。 これにより、呼び出し元は、個々のコンテナーの開き方、メッセージング ユーザーの検索、共通のアドレス ダイアログ ボックスの表示などのタスクを実行できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook** はMAPI_W_ERRORS_RETURNED 1 つ以上のアドレス帳プロバイダーを読み込めない場合に、この値を返します。 この値は警告で、エラー値ではありません。使用する場合と同S_OK。 **OpenAddressBook** は、アドレス帳プロバイダーの読み込みに失敗した数に関係なく  _、lppAdrBook_ パラメーター内の有効なポインターを常に返します。 したがって、ログオフする前に、必ずアドレス帳の [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを呼び出す必要があります。 
  
**OpenAddressBook** が MAPI_W_ERRORS_RETURNED を返す場合は [、IMAPISession::GetLastError](imapisession-getlasterror.md)を呼び出して、障害が発生したプロバイダーに関する情報を含む [MAPIERROR](mapierror.md)構造体を取得します。 すべてのプロバイダー **によって提供される** 情報を含む 1 つの MAPIERROR 構造体が返されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI は **IMAPISession::OpenAddressBook** メソッドを使用して統合アドレス帳を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

