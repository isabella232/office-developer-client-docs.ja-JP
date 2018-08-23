---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572999"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在は廃止されています。 プロファイルのパスワードを変更します。
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszProfileName_
  
> [in]変更するパスワードに関連付けられているプロファイルの名前へのポインター。
    
 _lpszOldPassword_
  
> [in]現在のパスワードへのポインター。
    
 _lpszNewPassword_
  
> [in]新しいパスワードへのポインター。
    
 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> プロファイル名とパスワード、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> このメソッドが呼び出されると、S_OK を返します。 ただし、動作も起こりません。
    
## <a name="remarks"></a>注釈

このメソッドを使用することはしません。 MAPI は、プロファイルのパスワードをサポートしていません。
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

