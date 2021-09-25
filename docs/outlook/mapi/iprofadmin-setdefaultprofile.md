---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c59eb9a4972c72ae1afea4e21118df24eae756a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556316"
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

 _lpszProfileName_
  
> [in]既定のプロファイルまたは NULL になるプロファイルの名前へのポインター。 _lpszProfileName_ を NULL に設定すると **、SetDefaultProfile** は既存の既定のプロファイルを削除し、クライアントは既定のままにする必要があります。 
    
 _ulFlags_
  
> [in]  _lpszProfileName_ が指す文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> プロファイル名は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、プロファイル名は ANSI 形式です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のプロファイルが正常に確立または削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定したプロファイルが存在しません。
    
## <a name="remarks"></a>注釈

**IProfAdmin::SetDefaultProfile** メソッドは、クライアントの既定のプロファイルとして特定のプロファイルを確立するか、現在の既定のプロファイルをクリアします。 既定のプロファイルは、クライアントが MAPI セッションを開始するたびに自動的に使用されるプロファイルです。 **SetDefaultProfile は** **PR_DEFAULT_PROFILE、** 新しい既定のプロファイルのプロパティ [(PidTagDefaultProfile) プロパティ (PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md)を TRUE に設定します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

既定のプロファイルでセッションを開始するには [、MAPILogonEx](mapilogonex.md) MAPI_USE_DEFAULTフラグを渡します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile 標準プロパティ](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

