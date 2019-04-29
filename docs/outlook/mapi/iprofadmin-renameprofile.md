---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419521"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルに新しい名前を割り当てます。
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszoldprofilename_
  
> 順番名前を変更するプロファイルの現在の名前へのポインター。
    
 _lpszoldpassword_
  
> 順番常に NULL。
    
 _lpsznewprofilename_
  
> 順番名前を変更するプロファイルの新しい名前へのポインター。
    
 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> 順番常に NULL。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルの名前が正常に変更されました。
    
MAPI_E_LOGON_FAILED 
  
> プロファイルのパスワードが正しくありません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

**IProfAdmin:: renameprofile**メソッドは、プロファイルに新しい名前を割り当てます (プロファイルがある場合)。 **renameprofile**を呼び出したときに、名前を変更するプロファイルがクライアントによって使用されている場合、 **renameprofile**はプロファイルをマークし、S_OK を返します。プロファイルが使用されている間に名前を変更する操作を試行するのではなく、S_OK を返します。 プロファイルが使用されなくなると、 **renameprofile**は新しい名前を割り当てます。 
  
プロファイルの新旧の名前は最大64文字の長さにすることができ、次の文字を含めることができます。
  
- アクセント記号とアンダースコア文字を含むすべての英数字。
    
- スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。
    
_lpszpassword_は常に NULL にするか、長さ0の文字列へのポインターにする必要があります。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

