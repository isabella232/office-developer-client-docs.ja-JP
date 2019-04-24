---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: アカウントのプロファイル名を取得します。
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322107"
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
  
> 順番読み上げプロファイル名。
    
_pcch_
  
> 順番読み上げこのメソッドを呼び出すと、割り当てられている_pwszIdentity_のサイズ (文字数) が格納されます。 戻り時には、返されるプロファイル名の実際の長さ (0 終端文字を含む) が格納されます。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OUTOFMEMORY  <br/> |返されたプロファイル名が_pwszIdentity_のサイズを超えています。  <br/> |
|E_INVALIDARG  <br/> | _pcch_が NULL です。  <br/> |
   
## <a name="remarks"></a>解説

_pwszIdentity_が小さすぎてプロファイル名を保持できない場合は、戻り値に設定されず、 _pcch_は_pwszIdentity_に必要なサイズをポイントします。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

