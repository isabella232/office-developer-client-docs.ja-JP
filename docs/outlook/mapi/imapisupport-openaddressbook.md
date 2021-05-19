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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416882"
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

 _lpInterface_
  
> [in]アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 有効な値は NULL で、標準のアドレス帳インターフェイス [IAddrBook](iaddrbookimapiprop.md)を示し、IID_IAddrBook。
    
 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _lppAdrBook_
  
> [out]アドレス帳へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳へのアクセスが提供された。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、1 つ以上のアドレス帳プロバイダーを読み込む必要がありました。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISupport::OpenAddressBook** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダー (通常は緊密に結合されたメッセージ ストアとトランスポート プロバイダー) は、アドレス帳へのアクセスを取得するために **OpenAddressBook** を呼び出します。 返される **IAddrBook** ポインターは、アドレス帳コンテナーの開き方、メッセージング ユーザーの検索、アドレスダイアログ ボックスの表示など、さまざまなアドレス帳タスクに使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook** は、現在MAPI_W_ERRORS_RETURNED 1 つ以上のアドレス帳プロバイダーを読み込めない場合に、そのアドレス帳を返します。 この値は警告であり、呼び出しは成功として扱う必要があります。 すべてのアドレス帳プロバイダーが読み込めなくても **、OpenAddressBook** は引き続き成功し _、lppAdrBook_ パラメーターに MAPI_W_ERRORS_RETURNED と **IAddrBook** ポインターを返します。 **OpenAddressBook は** 常に有効な **IAddrBook** ポインターを返すので、使用が終了したら解放する必要があります。 
  
1 つ以上のアドレス帳プロバイダーの読み込みに失敗した場合は [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) を呼び出して、読み込みなかったプロバイダーに関する情報を含む [MAPIERROR](mapierror.md) 構造を取得します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

