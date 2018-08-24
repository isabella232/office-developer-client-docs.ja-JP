---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a6eba20fb346f53052808abf8fcae8993d423d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589561"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在は廃止されています。 メッセージ サービスに新しい名前が割り当てられます。 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]名前を変更するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpszDisplayName_
  
> [in]メッセージ サービスの新しい名前へのポインター。
    
## <a name="return-value"></a>戻り値

MAPI_E_NO_SUPPORT 
  
> MAPI では、このメッセージ サービスの名前を変更することはできません。 **RenameMsgService**は、常にこの値を返します。 
    
## <a name="remarks"></a>注釈

メッセージ サービスに新しい名前を割り当てるには、クライアントは、メッセージ サービスの**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティを使用してください。 メッセージ サービスのサービス プロバイダーの名前は、それらのプロパティの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に格納されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

