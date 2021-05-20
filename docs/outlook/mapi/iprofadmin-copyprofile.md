---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437239"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルをコピーします。
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszOldProfileName_
  
> [in]コピーするプロファイルの名前へのポインター。
    
 _lpszOldPassword_
  
> [in]コピーするプロファイルのパスワードへのポインター。
    
 _lpszNewProfileName_
  
> [in]コピーされたプロファイルの新しい名前へのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロファイルのコピー方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> コピーするプロファイルの正しいパスワードをユーザーに求めるダイアログ ボックスを表示します。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルが正常にコピーされました。
    
MAPI_E_ACCESS_DENIED 
  
> 新しいプロファイル名は、既存のプロファイルと同じです。
    
MAPI_E_LOGON_FAILED 
  
> プロファイルをコピーするパスワードが正しくないので、MAPI_DIALOG が  _ulFlags_ パラメーターで設定されていないので、正しいパスワードを要求するダイアログ ボックスをユーザーに表示できません。 
    
MAPI_E_NOT_FOUND 
  
> 指定したプロファイルが存在しません。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IProfAdmin::CopyProfile** メソッドは _、lpszOldProfileName_ が指すプロファイルのコピーを作成し _、lpszNewProfileName_ によって指される名前を与える。 プロファイルをコピーすると、コピーには元のパスワードと同じパスワードが残ります。
  
元のプロファイルの名前、パスワード、およびコピーの長さは最大 64 文字で、次の文字を含めることができます。
  
- アクセント文字とアンダースコア文字を含むすべての英数字。
    
- 埋め込みスペースですが、先頭または末尾のスペースは使用できません。
    
プロファイル パスワードは、すべてのオペレーティング システムではサポートされていません。 プロファイル パスワードをサポートしないオペレーティング システムでは  _、lpszOldPassword_ には NULL または長さ 0 の文字列へのポインターを指定できます。 
  
_lpszOldPassword_ が NULL に設定されている場合、コピーするプロファイルにはパスワードが必要であり、MAPI_DIALOGフラグが設定されます。パスワードの入力を求めるダイアログ ボックスが表示されます。 パスワードが必要ですが  _、lpszOldPassword_ が NULL に設定され、MAPI_DIALOG フラグが設定されていない場合 **、CopyProfile** はパスワードをMAPI_E_LOGON_FAILED。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

