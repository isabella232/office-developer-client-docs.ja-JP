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
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801138"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**適用されます**: Outlook 
  
現在は廃止されています。 プロファイルのパスワードを変更します。
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

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
    
## <a name="remarks"></a>備考

このメソッドを使用することはしません。 MAPI は、プロファイルのパスワードをサポートしていません。
  
## <a name="see-also"></a>関連項目



[IProfAdmin: IUnknown](iprofadminiunknown.md)

