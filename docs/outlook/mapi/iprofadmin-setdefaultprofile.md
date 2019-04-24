---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270169"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントの既定のプロファイルを設定またはクリアします。
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszprofilename_
  
> 順番既定値になるプロファイルの名前、または NULL のポインター。 _lpszprofilename_を NULL に設定すると、 **setdefaultprofile**が既存の既定のプロファイルを削除して、クライアントを既定にしないようにする必要があることを示します。 
    
 _ulFlags_
  
> 順番_lpszprofilename_が指す文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> プロファイル名が Unicode 形式である。 MAPI_UNICODE フラグが設定されていない場合、プロファイル名は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のプロファイルが正常に確立または削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
## <a name="remarks"></a>解説

**IProfAdmin:: setdefaultprofile**メソッドは、特定のプロファイルをクライアントの既定のプロファイルとして確立するか、現在の既定のプロファイルをクリアします。 既定のプロファイルは、クライアントが MAPI セッションを開始するときに自動的に使用されるプロファイルです。 **setdefaultprofile**は、新しい既定のプロファイルの**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティも TRUE に設定します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

既定のプロファイルを使用してセッションを開始するには、MAPI_USE_DEFAULT フラグを[MAPILogonEx](mapilogonex.md)関数に渡します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile 標準プロパティ](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

