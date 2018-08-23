---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578627"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスにサービス プロバイダーを追加します。 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>パラメーター

 _lpszProvider_
  
> [in]追加するプロバイダーの名前へのポインター。
    
 _あう_
  
> [in]_LpProps_パラメーターで指定されたプロパティ値の数。 
    
 _lpProps_
  
> [in]追加するプロバイダーのプロパティを記述するプロパティ値の配列へのポインター。
    
 _ulUIParam_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。 _UlFlags_パラメーターで、MAPI_DIALOG フラグが設定されている場合、 _ulUIParam_パラメーターが使用されます。 
    
 _ulFlags_
  
> [in]プロバイダーの追加を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
  - MAPI_DIALOG:、構成情報の入力を求めるダイアログ ボックスが表示されます。
      
  - MAPI_UNICODE: Unicode 形式では、プロバイダーの名前と文字列のプロパティです。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。
    
 _lpUID_
  
> [out]追加するプロバイダーを表す一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロバイダーはメッセージ サービスに正常に追加されました。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

**IProviderAdmin::CreateProvider**メソッドでは、メッセージ サービスにサービス プロバイダーを追加します。 _LpszProvider_パラメーターは、メッセージ サービスに属しているプロバイダーの名前をポイントする必要があります。 **CreateProvider**は名前がサービスのプロバイダーの名前と一致するかどうかを確認していません。渡された名前がサービス名に一致しない場合、呼び出しが成功したが、結果は予測できません。 ほとんどのメッセージ サービスでは、プロバイダーを追加または削除、プロファイルを使用している間は許可されません。 
  
結局のところ、サービスに関する情報のプロバイダーはプロファイルに追加されて、Mapisvc.inf ファイルの**CreateProvider**は、 _ulContext_パラメーターを MSG_SERVICE_ を設定したメッセージ サービスのエントリ ポイント関数を呼び出しますPROVIDER_CREATE。 MAPI_DIALOG は、 **CreateProvider**メソッドの_ulFlags_パラメーターで設定されている場合、 _ulUIParam_と_ulFlags_パラメーターの値も、エントリ ポイント関数に渡されます。 これらの追加パラメーターは、構成設定を入力できるように、プロパティ シートを表示するサービス プロバイダーを有効にします。 
  
## <a name="see-also"></a>関連項目

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

