---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: db09b44bd8eeeb3ab56513b1b9c2cab69f776002
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590086"
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
  
> [で [チェック アウト]削除するプロバイダーを表す一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロバイダーは、メッセージ サービスから正しく削除されました。
    
MAPI_E_NOT_FOUND 
  
> _LpUID_パラメーターで指定された**MAPIUID**が認識されませんでした。 
    
## <a name="remarks"></a>注釈

**IProviderAdmin::DeleteProvider**メソッドは、メッセージ サービスのサービス プロバイダーを削除します。 **DeleteProvider**は、アクティブなサービスのプロバイダーが登録されている識別子のセットを_lpUID_で指定された**MAPIUID**構造を照合することによって削除するのにはサービス ・ プロバイダーを決定します。 
  
メッセージ サービスのほとんどは、プロバイダー プロファイルを使用している間に削除するには許可されません。 削除するプロバイダーを使用している場合**DeleteProvider**はすぐに削除する代わりに削除のマークが付けし、S_OK を返します。 プロバイダーが使用されていないがときに、削除されます。 
  
 **DeleteProvider**は、プロバイダーがサービスから削除される前に、メッセージ サービスのエントリ ポイント関数を呼び出します。 _UlContext_パラメーターは、MSG_SERVICE_PROVIDER_DELETE に設定されます。 メッセージ サービスのエントリ ポイント関数は、次のタスクを実行します。 
  
- サービス プロバイダーを削除します。
    
- サービス プロバイダーのプロファイル セクションを削除します。
    
プロバイダーが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

