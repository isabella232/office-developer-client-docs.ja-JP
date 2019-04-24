---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329030"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳へのアクセスを提供します。
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 有効な値は NULL で、標準のアドレス帳インターフェイス[IAddrBook](iaddrbookimapiprop.md)および IID_IAddrBook を示します。
    
 _ulFlags_
  
> 予約語0である必要があります。
    
 _lppadrbook_
  
> 読み上げアドレス帳へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳へのアクセスが提供されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、1つ以上のアドレス帳プロバイダーを読み込めませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapisupport:: OpenAddressBook**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダは通常、メッセージストアとトランスポートプロバイダーを密結合し、 **OpenAddressBook**を呼び出してアドレス帳へのアクセス権を取得します。 返される**IAddrBook**ポインターは、アドレス帳コンテナーを開く、メッセージングユーザーを検索する、アドレスダイアログボックスを表示するなど、さまざまなアドレス帳タスクに使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook**は、現在のプロファイルにアドレス帳プロバイダーの1つ以上を読み込むことができない場合、MAPI_W_ERRORS_RETURNED を返すことができます。 この値は警告で、呼び出しを成功として扱う必要があります。 すべてのアドレス帳プロバイダーが読み込まれなかった場合でも、 **OpenAddressBook**は成功し、 _lppadrbook_パラメーターで MAPI_W_ERRORS_RETURNED と**IAddrBook**ポインターを返します。 **OpenAddressBook**は常に有効な**IAddrBook**ポインターを返すため、これを使用し終えたら解放する必要があります。 
  
1つ以上のアドレス帳プロバイダーが読み込みに失敗した場合は、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)を呼び出して、読み込まれていないプロバイダーに関する情報を含む[MAPIERROR](mapierror.md)構造を取得します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

