---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: '[アカウント の追加] ダイアログ 設定 [新しいアカウントの追加] ダイアログ ボックスが表示されます。'
ms.openlocfilehash: 22a9165fa5cd29e0f9da9de64c243806e6fb1712
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561923"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

[アカウント の追加 **] ダイアログ 設定**[新しいアカウントの **追加] ダイアログ ボックスを** 表示します。 
  
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
  
> [in]表示されるダイアログ ボックスがモーダルであるウィンドウへのハンドル。 ゼロの場合があります。
    
_dwFlags_
  
> [in]表示の動作を変更するフラグ。 
    
   - **ACCTUI_NO_WARNING**—再起動するまで変更が有効になOutlook表示しません。 アプリケーションがプロセス内で実行中の場合にのみ適用Outlook.exe。
    
   - **ACCTUI_SHOW_DATA_TAB**— [データ] タブ **を選択設定[** アカウント のアカウント]**ダイアログ ボックス** を表示します。 この値は **、ACCTUI_SHOW_ACCTWIZARD** 設定されていない場合にのみ有効です。 
    
   - **ACCTUI_SHOW_ACCTWIZARD**—[新しいアカウントの **追加] ダイアログ ボックスを** 表示します。 
    
_wszTitle_
  
> [in]このパラメーターは使用されないので、NULL である必要があります。
    
_cCategories_
  
> [in]このパラメーターは使用されないので、NULL である必要があります。 
    
_rgclsidCategories_
  
> [in]このパラメーターは使用されないので、NULL である必要があります。
    
_pclsidType_
  
> [in]このパラメーターは使用されないので、NULL である必要があります。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_ACCT_UI_BUSY  <br/> |ダイアログ ボックスを作成できません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |[ **新しいアカウントの追加]** ダイアログ ボックスにエラーが返されました。  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |_cCategories_ _、rgclsidCategories、__または pclsidType_ パラメーターは NULL 以外です。  <br/> |
|MAPI_E_USER_CANCEL  <br/> |[**アカウントの設定]** ダイアログ ボックスにエラーが返されました。  <br/> |
   
## <a name="remarks"></a>注釈

_cCategories、rgclsidCategories、_ および _pclsidType_ パラメーターは現時点では使用されません。NULL である必要があります。   _wszTitle_ は使用されません。また、NULL である必要があります。 
  

