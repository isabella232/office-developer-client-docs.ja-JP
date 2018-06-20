---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: アカウントの設定または新しいアカウントの追加] ダイアログ ボックスが表示されます。
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799475"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

**アカウントの設定**または**新しいアカウントの追加**] ダイアログ ボックスが表示されます。 
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>パラメーター

_hwnd_
  
> [in]表示されたダイアログ ボックスはモーダル ウィンドウへのハンドルです。 0 にすることがあります。
    
_dwFlags_
  
> [in]表示の動作を変更するフラグを設定します。 
    
   - **ACCTUI_NO_WARNING**-こと変更は有効になりませんが、Outlook を再起動するまで、警告は表示されません。 アプリケーションが Outlook.exe でインプロセスで実行中である場合にのみ適用されます。
    
   - **ACCTUI_SHOW_DATA_TAB**: [**データ**] タブで、[**アカウント設定**] ダイアログ ボックスを表示します。 **ACCTUI_SHOW_ACCTWIZARD**が設定されていない場合にのみ有効にします。 
    
   - **ACCTUI_SHOW_ACCTWIZARD**:**新しいアカウントの追加**] ダイアログ ボックスを表示します。 
    
_wszTitle_
  
> [in]このパラメーターは、実行されていないと、NULL にする必要があります。
    
_cCategories_
  
> [in]このパラメーターは、実行されていないと、NULL にする必要があります。 
    
_rgclsidCategories_
  
> [in]このパラメーターは、実行されていないと、NULL にする必要があります。
    
_pclsidType_
  
> [in]このパラメーターは、実行されていないと、NULL にする必要があります。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_ACCT_UI_BUSY  <br/> |ダイアログ ボックスを作成できませんでした。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |**新しいアカウントの追加**] ダイアログ ボックスには、エラーが返されます。  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |_CCategories_、 _rgclsidCategories_、または_pclsidType_パラメーターは、NULL 以外です。  <br/> |
|MAPI_E_USER_CANCEL  <br/> |**アカウント設定**] ダイアログ ボックスには、エラーが返されます。  <br/> |
   
## <a name="remarks"></a>備考

_CCategories_、 _rgclsidCategories_、および_pclsidType_パラメーターは、この時点では使用されず、NULL にする必要があります。  _wszTitle_は、使用しないと、NULL 必要があります。 
  

