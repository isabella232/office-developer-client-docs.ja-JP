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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420242"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非推奨。 プロファイルのパスワードを変更します。
  
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
  
> [in]渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> プロファイル名とパスワードは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> このメソッドが呼び出された場合、このメソッドはS_OK。 ただし、アクションは実行されます。
    
## <a name="remarks"></a>注釈

このメソッドは使用しない。 MAPI では、プロファイルのパスワードはサポートされていません。
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

