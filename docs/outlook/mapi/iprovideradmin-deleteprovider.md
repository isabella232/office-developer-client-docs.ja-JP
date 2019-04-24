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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279550"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスからサービスプロバイダーを削除します。
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> [入力]削除するプロバイダーを表す一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーがメッセージサービスから正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> _lpuid_パラメーターが指す**MAPIUID**が認識されませんでした。 
    
## <a name="remarks"></a>解説

**IProviderAdmin::D eleteprovider**メソッドは、メッセージサービスからサービスプロバイダーを削除します。 **deleteprovider**は、アクティブなサービスプロバイダによって登録された一連の識別子を使用して、 _lpuid_が指す**MAPIUID**構造を照合することによって、削除するサービスプロバイダーを決定します。 
  
ほとんどのメッセージサービスでは、プロファイルが使用されている間、プロバイダーを削除することはできません。 削除するプロバイダーが使用されている場合、 **deleteprovider**はすぐに削除するのではなく、削除対象としてマークし、S_OK を返します。 プロバイダーが使用されなくなると、そのプロバイダーは削除されます。 
  
 **deleteprovider**は、プロバイダーがサービスから削除される前に、メッセージサービスのエントリポイント関数を呼び出します。 _ulcontext_パラメーターは MSG_SERVICE_PROVIDER_DELETE に設定されています。 メッセージサービスエントリポイント関数は、次のタスクを実行します。 
  
- サービスプロバイダーを削除します。
    
- サービスプロバイダーのプロファイルセクションを削除します。
    
プロバイダーが削除された後、メッセージサービスエントリポイント関数が再度呼び出されることはありません。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

