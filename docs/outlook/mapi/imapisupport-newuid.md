---
title: IMAPISupportNewUID
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406998"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一意の [識別子として使用する新しい MAPIUID](mapiuid.md) 構造を作成します。 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>パラメーター

 _lpMuid_
  
> 新しい **MAPIUID 構造へのポインター** 。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しい **MAPIUID** 構造が作成されました。 
    
## <a name="remarks"></a>注釈

**IMAPISupport::NewUID** メソッドは、すべてのサポート オブジェクトに実装されます。 サービス プロバイダーとメッセージ サービスは、長期的な一意識別子を生成する必要がある場合は常に **NewUID** を呼び出します。 たとえば、メッセージ ストア プロバイダーは NewUID を呼び出して、新しく作成されたメッセージの **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティに入れる **MAPIUID** を取得できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

ログオン時に登録する **MAPIUID** 構造と **、NewUID** メソッドが作成する **MAPIUID** 構造体を混同し、混同しなさらね。 [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出す際に登録する **MAPIUID** 構造は、MAPI へのアドレス帳またはメッセージ ストア プロバイダーを表し、異なるプロバイダーが作成するエントリ識別子を区別するために使用されます。 この **MAPIUID** 構造体はハードコードされ **、NewUID** の呼び出しでは取得されません。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

