---
title: imapistatuschangepassword
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410358"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーインターフェイスを表示せずに、サービスプロバイダーのパスワードを変更します。 このメソッドは、サービスプロバイダーが実装する status オブジェクトで必要に応じてサポートされます。
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpOldPass_
  
> 順番古いパスワードへのポインター。
    
 _lpnewpass_
  
> 順番新しいパスワードへのポインター。
    
 _ulFlags_
  
> 順番パスワードの形式を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> パスワードは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、パスワードは ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> パスワードの変更に成功しました。
    
MAPI_E_NO_ACCESS 
  
> _lpOldPass_が指す古いパスワードが無効です。 
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_CHANGE_PASSWORD フラグが設定されていない場合、status オブジェクトはこの操作をサポートしていません。
    
## <a name="remarks"></a>注釈

すべてのステータスオブジェクトが**imapistatus:: ChangePassword**メソッドをサポートするわけではありません。 クライアントがパスワードを入力する必要があるサービスプロバイダーのみがサポートしています。 MAPI で実装されているステータスオブジェクトは、パスワードの変更操作をサポートしていません。 
  
 **ChangePassword**ユーザーによる操作なしで、プログラムによってパスワードを変更します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモートトランスポートプロバイダーは、ここで指定したように**ChangePassword**を実装します。 特別な考慮事項はありません。 
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

