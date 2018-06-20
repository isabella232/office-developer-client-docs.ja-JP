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
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800982"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**適用されます**: Outlook 
  
現在は廃止されています。 メッセージ サービスに新しい名前が割り当てられます。 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in]名前を変更するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpszDisplayName_
  
> [in]メッセージ サービスの新しい名前へのポインター。
    
## <a name="return-value"></a>�߂�l

MAPI_E_NO_SUPPORT 
  
> MAPI では、このメッセージ サービスの名前を変更することはできません。 **RenameMsgService**は、常にこの値を返します。 
    
## <a name="remarks"></a>備考

メッセージ サービスに新しい名前を割り当てるには、クライアントは、メッセージ サービスの**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティを使用してください。 メッセージ サービスのサービス プロバイダーの名前は、それらのプロパティの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に格納されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

