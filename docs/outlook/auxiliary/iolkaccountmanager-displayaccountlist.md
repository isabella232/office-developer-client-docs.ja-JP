---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: '[アカウント設定] または [新しいアカウントの追加] ダイアログボックスを表示します。'
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415034"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

[**アカウント設定**] または [**新しいアカウントの追加**] ダイアログボックスを表示します。 
  
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
  
> 順番表示されるダイアログボックスがモーダルであるウィンドウへのハンドル。 0の場合があります。
    
_dwFlags_
  
> 順番表示の動作を変更するフラグです。 
    
   - **ACCTUI_NO_WARNING**-Outlook が再起動されるまで変更が有効にならないという警告は表示されません。 アプリケーションが Outlook .exe でインプロセスで実行されている場合にのみ適用されます。
    
   - **ACCTUI_SHOW_DATA_TAB**— [**データ**] タブが選択された状態で [**アカウント設定**] ダイアログボックスを表示します。 **ACCTUI_SHOW_ACCTWIZARD**が設定されていない場合にのみ有効です。 
    
   - **ACCTUI_SHOW_ACCTWIZARD**-[**新しいアカウントの追加**] ダイアログボックスを表示します。 
    
_wszTitle_
  
> 順番このパラメーターは使用されておらず、NULL である必要があります。
    
_ccategories_
  
> 順番このパラメーターは使用されておらず、NULL である必要があります。 
    
_rgclsidCategories_
  
> 順番このパラメーターは使用されておらず、NULL である必要があります。
    
_pclsidtype_
  
> 順番このパラメーターは使用されておらず、NULL である必要があります。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_ACCT_UI_BUSY  <br/> |ダイアログボックスを作成できませんでした。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |[**新しいアカウントの追加**] ダイアログボックスでエラーが返されました。  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |_ccategories_、 _rgclsidCategories_、または_pclsidtype_パラメーターが NULL ではない。  <br/> |
|MAPI_E_USER_CANCEL  <br/> |[**アカウント設定**] ダイアログボックスでエラーが返されました。  <br/> |
   
## <a name="remarks"></a>注釈

_ccategories_、 _rgclsidCategories_、 _pclsidtype_パラメーターは、現時点では使用されておらず、NULL である必要があります。  _wszTitle_は使用されず、NULL でもある必要があります。 
  

