---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: アカウントのプロファイル名を取得します。
ms.openlocfilehash: d24f108aa4227ce8fe38e46b48a8f56a0eb29cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625687"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

アカウントのプロファイル名を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountHelper」を参照してください](iolkaccounthelper.md)。
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>パラメーター

_pwszIdentity_
  
> [in][out]プロファイル名。
    
_pcch_
  
> [in][out]このメソッドを呼び出す際に、割り当てられた  _pwszIdentity_ のサイズ (文字数) が含まれています。 返された場合、返されるプロファイル名の実際の長さ (0 終端文字を含む) が含まれる。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OUTOFMEMORY  <br/> |返されるプロファイル名は  _、pwszIdentity_ のサイズよりも長くなります。  <br/> |
|E_INVALIDARG  <br/> | _pcch は_ NULL です。  <br/> |
   
## <a name="remarks"></a>注釈

_pwszIdentity が_ 小さすぎてプロファイル名を保持できない場合、戻り値に設定され _、pcch_ は _pwszIdentity_ に必要なサイズを指します。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

