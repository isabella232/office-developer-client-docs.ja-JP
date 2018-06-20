---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800716"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**適用されます**: Outlook 
  
ユーザー インターフェイスを表示せずには、サービス プロバイダーのパスワードを変更します。 サービス プロバイダーを実装する状態オブジェクトには、このメソッドはサポートされて必要に応じてします。
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpOldPass_
  
> [in]古いパスワードへのポインター。
    
 _lpNewPass_
  
> [in]新しいパスワードへのポインター。
    
 _ulFlags_
  
> [in]パスワードの形式を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> パスワードは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のパスワードです。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> パスワードの変更が正常に完了しました。
    
MAPI_E_NO_ACCESS 
  
> _LpOldPass_で指定された古いパスワードが正しくありません。 
    
MAPI_E_NO_SUPPORT 
  
> 状態オブジェクトは、この操作をサポートしていません状態オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_CHANGE_PASSWORD フラグがない場合で示される。
    
## <a name="remarks"></a>備考

ステータスのすべてのオブジェクトは、 **IMAPIStatus::ChangePassword**メソッドをサポートします。 クライアントがパスワードの入力を必要とするサービス ・ プロバイダーでのみサポートされています。 MAPI が実装している状態のオブジェクトの [なし] は、パスワードの変更操作をサポートします。 
  
 **パスワードの変更**は、ユーザーの介入なしプログラムで、パスワードを変更します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

リモート トランスポート プロバイダーは、ここで指定されている**パスワードの変更**を実装します。 特別な考慮事項はありません。 
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods の標準的なプロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)

