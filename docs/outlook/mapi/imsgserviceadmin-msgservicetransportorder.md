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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420095"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを配信するためにトランスポート プロバイダーが呼び出される順序を設定します。
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>パラメーター

 _cUID_
  
> [in]lpUIDList パラメーター内の一  _意の識別子の_ 数。 
    
 _lpUIDList_
  
> [in]トランスポート プロバイダーを表す一意の識別子の配列へのポインター。 配列には、現在のプロファイルで構成されているトランスポート プロバイダーごとに 1 つの識別子が含まれています。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポートの順序が正常に設定されました。
    
MAPI_E_BUSY 
  
> _cUID パラメーターの値_ は、プロファイル内の実際のトランスポート プロバイダーの数と異なります。 
    
MAPI_E_NOT_FOUND 
  
> _lpUIDList_ パラメーターで渡される 1 つ以上の [MAPIUID](mapiuid.md)構造体は、プロファイル内の現在のトランスポート プロバイダーを参照していない。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::MsgServiceTransportOrder** メソッドは、プロファイル内のトランスポート プロバイダーの配信順序を設定します。 _lpUIDList_ パラメーターには [、IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドから返されるテーブルの **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) プロパティから取得したトランスポート プロバイダーエントリ識別子の並べ替えリストが含まれている必要があります。 クライアント アプリケーションは、lpUIDList の完全なリスト  _を渡す必要があります_。
  
 **SetTransportOrder** は、STATUS_XP_PREFER_LAST **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定された PR_RESOURCE_FLAGS フラグなどのトランスポート プロバイダーの基本設定を上書きします。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

