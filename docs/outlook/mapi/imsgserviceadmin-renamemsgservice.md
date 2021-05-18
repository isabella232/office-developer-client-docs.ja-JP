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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422104"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非推奨。 メッセージ サービスに新しい名前を割り当てる。 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]名前を変更するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpszDisplayName_
  
> [in]メッセージ サービスの新しい名前へのポインター。
    
## <a name="return-value"></a>戻り値

MAPI_E_NO_SUPPORT 
  
> MAPI では、このメッセージ サービスの名前の変更はサポートされていません。 **RenameMsgService は常** にこの値を返します。 
    
## <a name="remarks"></a>注釈

新しい名前をメッセージ サービスに割り当てるには、クライアントがメッセージ サービスの PR_SERVICE_NAME **(** [PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティを使用する必要があります。 メッセージ サービス内のサービス プロバイダーの名前は、メッセージ サービス **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) PR_DISPLAY_NAMEプロパティに格納されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

