---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: de399f12e95c94560ad5bd65cdd0a111871f0766
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592257"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスからサービス プロバイダーを削除します。
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in, out]削除するプロバイダーを表す一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーがメッセージ サービスから正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> **lpUID パラメーター** が指す _MAPIUID_ が認識されませんでした。 
    
## <a name="remarks"></a>注釈

**IProviderAdmin::D eleteProvider** メソッドは、メッセージ サービスからサービス プロバイダーを削除します。 **DeleteProvider は**_、lpUID_ が指す **MAPIUID** 構造と、アクティブなサービス プロバイダーによって登録された一連の識別子を照合して、サービス プロバイダーが削除を決定します。 
  
ほとんどのメッセージ サービスでは、プロファイルの実行中にプロバイダーを削除することはできません。 削除するプロバイダーが使用されている場合 **、DeleteProvider** は削除のマークを付け、すぐに削除する代わりに削除S_OK。 プロバイダーが使用されなくなった場合は、削除されます。 
  
 **DeleteProvider は** 、プロバイダーがサービスから削除される前に、メッセージ サービスのエントリ ポイント関数を呼び出します。 _ulContext パラメーター_ は、次の値にMSG_SERVICE_PROVIDER_DELETE。 メッセージ サービス エントリ ポイント関数は、次のタスクを実行します。 
  
- サービス プロバイダーを削除します。
    
- サービス プロバイダーのプロファイル セクションを削除します。
    
プロバイダーが削除された後、メッセージ サービスエントリ ポイント関数は再度呼び出されません。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

