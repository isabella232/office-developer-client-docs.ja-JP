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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430806"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーをメッセージ サービスに追加します。 
  
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
    
 _cValues_
  
> [in]  _lpProps_ パラメーターが指すプロパティ値の数。 
    
 _lpProps_
  
> [in]追加するプロバイダーのプロパティを表すプロパティ値配列へのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されている場合に使用されます。 
    
 _ulFlags_
  
> [in]プロバイダーの追加を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - MAPI_DIALOG: 構成情報の入力を求めるダイアログ ボックスを表示します。
      
  - MAPI_UNICODE: プロバイダー名と文字列プロパティは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。
    
 _lpUID_
  
> [out]追加するプロバイダーを表す一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーがメッセージ サービスに正常に追加されました。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IProviderAdmin::CreateProvider** メソッドは、サービス プロバイダーをメッセージ サービスに追加します。 _lpszProvider_ パラメーターは、メッセージ サービスに属するプロバイダーの名前を指している必要があります。 **CreateProvider** は、名前がサービス内のプロバイダーの名前と一致するかどうかを確認します。渡された名前がサービス名と一致しない場合、呼び出しは成功しますが、結果は予測できません。 ほとんどのメッセージ サービスでは、プロファイルの実行中にプロバイダーを追加または削除することはできません。 
  
Mapisvc.inf ファイルからサービス プロバイダーに関する利用可能なすべての情報がプロファイルに追加された後 **、CreateProvider** は  _ulContext_ パラメーターを MSG_SERVICE_PROVIDER_CREATE に設定してメッセージ サービスのエントリ ポイント関数を呼び出します。 **CreateProvider** MAPI_DIALOGの _ulFlags_ パラメーターで設定されている場合 _、ulUIParam_ パラメーターと _ulFlags_ パラメーターの値もエントリ ポイント関数に渡されます。 これらの追加のパラメーターを使用すると、サービス プロバイダーはプロパティ シートを表示して、ユーザーが構成設定を入力できます。 
  
## <a name="see-also"></a>関連項目

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

