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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317123"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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

 _lpszprofilename_
  
> 順番変更するパスワードに関連付けられているプロファイルの名前へのポインター。
    
 _lpszoldpassword_
  
> 順番現在のパスワードへのポインター。
    
 _lpszNewPassword_
  
> 順番新しいパスワードへのポインター。
    
 _ulFlags_
  
> 順番渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> プロファイル名とパスワードは、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> このメソッドが呼び出されると、S_OK が返されます。 ただし、アクションは何も実行されません。
    
## <a name="remarks"></a>解説

このメソッドは使用しないでください。 MAPI では、プロファイルのパスワードがサポートされていません。
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

