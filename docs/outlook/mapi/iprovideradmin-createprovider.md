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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279557"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスにサービスプロバイダーを追加します。 
  
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

 _lpszprovider_
  
> 順番追加するプロバイダーの名前へのポインター。
    
 _cvalues_
  
> 順番_lpprops_パラメーターによって示されるプロパティ値の数。 
    
 _lpprops_
  
> 順番追加するプロバイダーのプロパティを記述するプロパティ値配列へのポインター。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、MAPI_DIALOG フラグが_ulflags_パラメーターで設定されている場合に使用されます。 
    
 _ulFlags_
  
> 順番プロバイダーの追加を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - MAPI_DIALOG: 構成情報を求めるダイアログボックスを表示します。
      
  - MAPI_UNICODE: プロバイダー名と文字列プロパティは、UNICODE 形式です。 MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。
    
 _lpuid_
  
> 読み上げ追加するプロバイダーを表す一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーがメッセージサービスに正常に追加されました。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

**IProviderAdmin:: createprovider**メソッドによって、サービスプロバイダーがメッセージサービスに追加されます。 _lpszprovider_パラメーターは、メッセージサービスに属するプロバイダーの名前を指している必要があります。 **createprovider**は、名前がサービスのプロバイダーの名前と一致しているかどうかを確認しません。渡された名前がサービス名と一致しない場合、呼び出しは成功しますが、結果は予測できません。 ほとんどのメッセージサービスでは、プロファイルが使用されている間、プロバイダーを追加または削除することはできません。 
  
サービスプロバイダーに関するすべての利用可能な情報が mapisvc.inf ファイルからプロファイルに追加された後、 **createprovider**は_ulcontext_パラメーターを MSG_SERVICE_ に設定したメッセージサービスのエントリポイント関数を呼び出します。PROVIDER_CREATE。 MAPI_DIALOG が**createprovider**メソッドの_ulflags_パラメーターで設定されている場合、 _uluiparam_パラメーターと_ulflags_パラメーターの値もエントリポイント関数に渡されます。 これらの追加パラメーターにより、サービスプロバイダーはプロパティシートを表示して、ユーザーが構成設定を入力できるようにします。 
  
## <a name="see-also"></a>関連項目

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

