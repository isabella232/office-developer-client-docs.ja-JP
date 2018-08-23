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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801122"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**適用対象**: Outlook 
  
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
  
> [in]コピー先のプロファイルの新しい名前へのポインター。
    
 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロファイルをコピーする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> プロファイルの正しいパスワードをコピーするのにはユーザーの入力を求めるダイアログ ボックスが表示されます。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイルは正常にコピーされました。
    
MAPI_E_ACCESS_DENIED 
  
> 新しいプロファイル名は、既存のプロファイルと同じです。
    
MAPI_E_LOGON_FAILED 
  
> コピーするプロファイルのパスワードが正しくないと、MAPI_DIALOG が_ulFlags_パラメーターで設定されていませんでしたので、正しいパスワードを要求するユーザーに、ダイアログ ボックスを表示できませんでした。 
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

**IProfAdmin::CopyProfile**メソッドは、 _lpszNewProfileName_で指定された名前を付けることが_lpszOldProfileName_を指すプロファイルのコピーを使用します。 プロファイルのコピー元と同じパスワードを使用してコピーを残します。
  
元のプロファイル、そのパスワード、およびコピーの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。
  
- すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。
    
- 埋め込みスペースがいない先頭または末尾のスペース。
    
プロファイルのパスワードは、すべてのオペレーティング システムではサポートされていません。 プロファイルのパスワードをサポートしていないオペレーティング システムで_lpszOldPassword_できます NULL または長さ 0 の文字列へのポインター。 
  
コピーするプロファイルがパスワードを必要とし、MAPI_DIALOG フラグが設定されている_lpszOldPassword_は、NULL に設定されている場合ユーザーにパスワードの入力を求めるダイアログ ボックスが表示されます。 パスワードが必要ですが、 _lpszOldPassword_は NULL に設定されて、MAPI_DIALOG フラグが設定されていない場合、 **CopyProfile**は MAPI_E_LOGON_FAILED を返します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

