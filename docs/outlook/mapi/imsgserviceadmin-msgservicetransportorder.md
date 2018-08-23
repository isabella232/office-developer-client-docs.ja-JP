---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570794"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
どのトランスポートにメッセージを配信するプロバイダーの呼び出し順序を設定します。
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>パラメーター

 _cUID_
  
> [in]_LpUIDList_パラメーターに一意の識別子の数。 
    
 _lpUIDList_
  
> [in]トランスポート プロバイダーを表す一意の識別子の配列へのポインター。 配列には、現在のプロファイルで構成されているトランスポート プロバイダーごとに 1 つの識別子が含まれています。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 輸送注文が正常に設定されました。
    
MAPI_E_BUSY 
  
> _CUID_パラメーターの値は、プロファイルの中に、トランスポート プロバイダーの数によって異なります。 
    
MAPI_E_NOT_FOUND 
  
> _LpUIDList_パラメーターで渡された[MAPIUID](mapiuid.md)の構造体の 1 つ以上は、プロファイルの現在のトランスポート プロバイダーを参照しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::MsgServiceTransportOrder**メソッドは、プロファイルに、トランスポート プロバイダーの配信順序を設定します。 _LpUIDList_パラメーターには、 [IMsgServiceAdmin から返されるテーブルの**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) のプロパティから取得したトランスポート プロバイダーのエントリの識別子の一覧が含まれている必要があります。GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドです。 クライアント アプリケーションは、 _lpUIDList_の完全なリストを渡す必要があります。
  
 **SetTransportOrder**のオーバーライドは、STATUS_XP_PREFER_LAST フラグを**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティの設定などのプロバイダーの設定を転送します。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

