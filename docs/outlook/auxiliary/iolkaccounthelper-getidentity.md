---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: アカウントのプロファイル名を取得します。
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799468"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

アカウントのプロファイル名を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>パラメーター

_pwszIdentity_
  
> [in][out]プロファイルの名前。
    
_pcch_
  
> [in][out]このメソッドを呼び出した時に (文字数) のサイズが割り当てられている_pwszIdentity_が含まれています。 関数が戻るとき、返されるプロファイル名の 0 終端文字を含めて、実際の長さが含まれています。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OUTOFMEMORY  <br/> |返されるプロファイル名は、 _pwszIdentity_のサイズを超えています。  <br/> |
|E_INVALIDARG  <br/> | _pcch_は、NULL です。  <br/> |
   
## <a name="remarks"></a>注釈

_PwszIdentity_プロファイルの名前を保持するには小さすぎる場合は、返された場合は、設定できませんし、 _pcch_ _pwszIdentity_に必要なサイズをポイントします。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

