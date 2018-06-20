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
ms.openlocfilehash: cf5060ba2113032fe1e13e5417590006808a53e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801137"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**適用されます**: Outlook 
  
設定またはクライアントの既定のプロファイルを削除します。
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

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
    
## <a name="remarks"></a>備考

**IProfAdmin::SetDefaultProfile**メソッドは、クライアントの既定のプロファイルとして特定のプロファイルを確立するか、または現在の既定のプロファイルを削除します。 既定のプロファイルは、クライアントは、MAPI セッションを開始するたびに自動的に使用されるプロファイルです。 **SetDefaultProfile**は、新しい既定のプロファイルの**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) のプロパティを TRUE に設定します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

既定のプロファイル セッションを開始するには、 [MAPILogonEx](mapilogonex.md)関数に MAPI_USE_DEFAULT フラグを渡します。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[PidTagDefaultProfile の標準的なプロパティ](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)

