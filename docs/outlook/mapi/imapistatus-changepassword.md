---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c98f3c2d3f14893fc37ab9c876d41ed65de409fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596170"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー インターフェイスを表示せずにサービス プロバイダーのパスワードを変更します。 このメソッドは、サービス プロバイダーが実装する状態オブジェクトで必要に応じてサポートされます。
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpOldPass_
  
> [in]古いパスワードへのポインター。
    
 _lpNewPass_
  
> [in]新しいパスワードへのポインター。
    
 _ulFlags_
  
> [in]パスワードの形式を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> パスワードは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、パスワードは ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> パスワードの変更が成功しました。
    
MAPI_E_NO_ACCESS 
  
> _lpOldPass_ が指す古いパスワードが無効です。 
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトは、status オブジェクトの PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_CHANGE_PASSWORD フラグがない場合 **に** 示されるこの操作をサポートします。
    
## <a name="remarks"></a>注釈

すべての状態オブジェクトが **IMAPIStatus::ChangePassword メソッドをサポートしている** 場合ではありません。 これは、クライアントにパスワードの入力を要求するサービス プロバイダーでのみサポートされます。 MAPI が実装する状態オブジェクトのいずれも、パスワード変更操作をサポートしません。 
  
 **ChangePassword は** 、ユーザーの操作なしで、プログラムによってパスワードを変更します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート トランスポート プロバイダーは、ここで指定 **した ChangePassword** を実装します。 特別な考慮事項はありません。 
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

