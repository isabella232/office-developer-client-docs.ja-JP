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
  
メッセージを配信するためにトランスポートプロバイダーが呼び出される順序を設定します。
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>パラメーター

 _cuid_
  
> 順番_lpuidlist_パラメーターの一意の識別子の数。 
    
 _lpuidlist_
  
> 順番トランスポートプロバイダーを表す一意の識別子の配列へのポインター。 配列には、現在のプロファイルで構成されている各トランスポートプロバイダーの識別子が1つ含まれています。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポートオーダーが正常に設定されました。
    
MAPI_E_BUSY 
  
> _cuid_パラメーターの値は、プロファイルに実際に含まれるトランスポートプロバイダーの数とは異なります。 
    
MAPI_E_NOT_FOUND 
  
> _lpuidlist_パラメーターに渡された1つ以上の[MAPIUID](mapiuid.md)構造体が、プロファイルに現在含まれているトランスポートプロバイダーを参照していません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin:: msgservicetransportorder**メソッドは、プロファイル内のトランスポートプロバイダーの配信順序を設定します。 _lpuidlist_パラメーターには、IMsgServiceAdmin から返されるテーブルの**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) プロパティから取得した、トランスポートプロバイダーのエントリ識別子の並べ替えられたリストを含める必要があります[。getprovidertable](imsgserviceadmin-getprovidertable.md)メソッド。 クライアントアプリケーションは、完全なリストを_lpuidlist_に渡す必要があります。
  
 **settransportorder**は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定された STATUS_XP_PREFER_LAST フラグなど、トランスポートプロバイダーの設定より優先されます。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

