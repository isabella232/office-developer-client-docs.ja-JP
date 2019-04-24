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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309570"
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

 _lpszoldprofilename_
  
> 順番コピーするプロファイルの名前へのポインター。
    
 _lpszoldpassword_
  
> 順番コピーするプロファイルのパスワードへのポインター。
    
 _lpsznewprofilename_
  
> 順番コピーされたプロファイルの新しい名前へのポインター。
    
 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番プロファイルのコピー方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> コピーするプロファイルの正しいパスワードをユーザーに確認するダイアログボックスが表示されます。 このフラグが設定されていない場合は、ダイアログボックスは表示されません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルが正常にコピーされました。
    
MAPI_E_ACCESS_DENIED 
  
> 新しいプロファイル名は、既存のプロファイルの名前と同じです。
    
MAPI_E_LOGON_FAILED 
  
> コピーするプロファイルのパスワードが正しくありません。 MAPI_DIALOG が_ulflags_パラメーターで設定されていないため、ユーザーに正しいパスワードを要求するためのダイアログボックスを表示できませんでした。 
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

**IProfAdmin:: copyprofile**メソッドは、 _lpszoldprofilename_によって参照されているプロファイルのコピーを作成し、 _lpszoldprofilename_で指定された名前を付与します。 プロファイルをコピーすると、元のパスワードと同じパスワードでコピーが残ります。
  
元のプロファイルの名前、パスワード、およびコピーの長さは最大64文字で、次の文字を含めることができます。
  
- アクセント記号とアンダースコア文字を含むすべての英数字。
    
- スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。
    
プロファイルパスワードは、すべてのオペレーティングシステムでサポートされていません。 プロファイルパスワードをサポートしていないオペレーティングシステムでは、 _lpszoldpassword_は NULL または長さ0の文字列へのポインターにすることができます。 
  
_lpszoldpassword_が NULL に設定されている場合、コピーされるプロファイルにはパスワードが必要です。また、MAPI_DIALOG フラグが設定されています。ユーザーにパスワードの入力を求めるダイアログボックスが表示されます。 パスワードが必要で、 _lpszoldpassword_が NULL に設定されていて、MAPI_DIALOG フラグが設定されていない場合、 **copyprofile**は MAPI_E_LOGON_FAILED を返します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

