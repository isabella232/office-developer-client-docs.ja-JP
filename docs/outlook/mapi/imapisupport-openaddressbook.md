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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800774"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**適用されます**: Outlook 
  
アドレス帳へのアクセスを提供します。
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in]アドレス帳にアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 有効な値は、NULL の場合、標準のアドレス帳のインターフェイス[IAddrBook](iaddrbookimapiprop.md)を示す、IID_IAddrBook です。
    
 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _lppAdrBook_
  
> [out]アドレス帳へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> アドレス帳へのアクセスが提供されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しが成功したが、1 つまたは複数のアドレス帳プロバイダーをロードできませんでした。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::OpenAddressBook**メソッドを実装します。 サービス プロバイダーでは、通常は、密結合のメッセージは、ストア、トランスポート プロバイダー、およびアドレス帳へのアクセスを取得する**OpenAddressBook**を呼び出します。 さまざまなメッセージング ユーザーは、表示するアドレス] ダイアログ ボックスの検索、アドレス帳コンテナーを開くことを含め、アドレス帳のタスクでは、 **IAddrBook**の戻り値のポインターを使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenAddressBook**は、1 つまたは複数の現在のプロファイルで、アドレス帳プロバイダーを読み込めない場合、MAPI_W_ERRORS_RETURNED を返すことができます。 この値は警告であり、呼び出しは成功として扱う必要があります。 場合でも、すべてのアドレス帳プロバイダーは、読み込みに失敗しました、 **OpenAddressBook**が成功すると、 _lppAdrBook_パラメーターで MAPI_W_ERRORS_RETURNED と、 **IAddrBook**ポインターを返します。 **OpenAddressBook**は、常に**IAddrBook**の有効なポインターを返す、ために使用することが終了したら解放する必要があります。 
  
1 つまたは複数のアドレス帳プロバイダーは、読み込みに失敗しました、する場合は、読み込まれなかったプロバイダーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を取得するのには[IMAPISupport::GetLastError](imapisupport-getlasterror.md)を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

