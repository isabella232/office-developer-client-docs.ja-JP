---
title: imapisupportnewuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330199"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造を作成します。 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>パラメーター

 _lpmuid_
  
> 新しい**MAPIUID**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しい**MAPIUID**構造が作成されました。 
    
## <a name="remarks"></a>解説

**imapisupport:: newuid**メソッドは、すべてのサポートオブジェクトに実装されています。 サービスプロバイダーとメッセージサービスは、長期の一意の識別子を生成する必要があるときに、 **newuid**を呼び出します。 たとえば、メッセージストアプロバイダーは**newuid**を呼び出して、新しく作成されたメッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティに入れる**MAPIUID**を取得することができます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

ログオン時に登録した**MAPIUID**構造を、 **newuid**メソッドが作成する**MAPIUID**構造体と混同しないでください。 [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出すときに登録する**MAPIUID**構造は、アドレス帳またはメッセージストアプロバイダーを MAPI に対して表し、さまざまなプロバイダーが作成するエントリ識別子を区別するために使用されます。 この**MAPIUID**構造体は、ハードコーディングされている必要があり、 **newuid**への呼び出しによって取得されることはありません。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

