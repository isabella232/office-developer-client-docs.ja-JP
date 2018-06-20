---
title: IMAPISupportDetails
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800728"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [out]返されたダイアログ ボックスの親ウィンドウへのハンドルへのポインター。
    
 _lpfnDismiss_
  
> [in][DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じると、 **IMAPISupport::Details**ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。 
    
 _lpvDismissContext_
  
> [in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。 このパラメーターは、 _ulFlags_パラメーターに DIALOG_SDI フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]詳細情報が表示されているエントリの識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in][LPFNBUTTON](lpfnbutton.md)関数のプロトタイプでは関数へのポインター。 **LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用するデータへのポインター。 
    
 _lpszButtonText_
  
> [in]そのボタンは拡張可能な場合は、[追加] ボタンに適用するテキストを含む文字列へのポインター。 _LpszButtonText_パラメーターは、拡張ボタンは、必要でない場合、NULL にすることがあります。 
    
 _ulFlags_
  
> [in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
DIALOG_MODAL
  
> 共通のアドレス] ダイアログ ボックスのモーダル バージョンを表示します。 このフラグは、DIALOG_SDI と相互に排他的です。
    
DIALOG_SDI
  
>  モードレスのバージョンの共通のアドレス] ダイアログ ボックスを表示します。 このフラグは、DIALOG_MODAL と相互に排他的です。 
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 詳細] ダイアログ ボックスは、アドレス帳のエントリを正常に表示されました。
    
## <a name="remarks"></a>備考

アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::Details**メソッドを実装します。 アドレス帳プロバイダーは、アドレス帳の特定のエントリについて説明するダイアログ ボックスを表示する**詳細情報**を呼び出します。 ボタンを追加する、クライアントの定義] ダイアログ ボックスには、 _lpfButtonCallback_、 _lpvButtonContext_、および_lpszButtonText_パラメーターを使用できます。 ボタンがクリックされると、MAPI は、 _lpvButtonContext_のボタンとデータの両方のエントリ id を渡すこと_lpfButtonCallback_で指定されたコールバック関数を呼び出します。 拡張ボタンが必要でない場合_lpszButtonText_は NULL である必要があります。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

