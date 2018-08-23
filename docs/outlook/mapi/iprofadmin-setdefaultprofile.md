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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587706"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
設定またはクライアントの既定のプロファイルを削除します。
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszProfileName_
  
> [in]プロファイルを既定値になりますが、または NULL の名前へのポインター。 _LpszProfileName_を NULL に設定すると、デフォルトがないクライアントをそのままで既存の既定のプロファイルを**SetDefaultProfile**が削除する必要があることを示します。 
    
 _ulFlags_
  
> [in]_LpszProfileName_が指す文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> プロファイル名は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のプロファイル名です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 既定のプロファイルを設定または削除に成功しました。
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
## <a name="remarks"></a>注釈

**IProfAdmin::SetDefaultProfile**メソッドは、クライアントの既定のプロファイルとして特定のプロファイルを確立するか、または現在の既定のプロファイルを削除します。 既定のプロファイルは、クライアントは、MAPI セッションを開始するたびに自動的に使用されるプロファイルです。 **SetDefaultProfile**は、新しい既定のプロファイルの**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) のプロパティを TRUE に設定します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

既定のプロファイル セッションを開始するには、 [MAPILogonEx](mapilogonex.md)関数に MAPI_USE_DEFAULT フラグを渡します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile 標準プロパティ](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

