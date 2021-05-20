---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429017"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成プロパティ シートを表示します。
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]プロパティ シートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpszTitle_
  
> [in]プロパティ シートのタイトルへのポインター。
    
 _lpDisplayTable_
  
> [in]プロパティ シートに表示するコントロールを説明する表示テーブルへのポインター。
    
 _lpConfigData_
  
> [in]プロパティ シートに表示する構成プロパティにアクセスするために使用する [IMAPIProp](imapipropiunknown.md) 実装へのポインター。 
    
 _ulTopPage_
  
> [in]プロパティ シートの既定のトップ ページへの 0 から始るインデックス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 構成プロパティ シートが表示された。
    
## <a name="remarks"></a>注釈

**IMAPISupport::D oConfigPropsheet** メソッドは、すべてのサポート オブジェクトに実装されます。 **DoConfigPropSheet は** 、サービス プロバイダーとメッセージ サービスのプロパティを表示するための標準的なユーザー インターフェイスを提供します。 すべての構成プロパティの表示には、この標準のダイアログ ボックスを使用して、ユーザーが一貫性のあるインターフェイスを利用Windows必要があります。 
  
サービス プロバイダーは [、IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドの実装の一環として、またはプロパティの詳細を表示するために使用されるボタンから **DoConfigPropSheet** を呼び出します。 メッセージ サービスは、メッセージ サービスエントリ ポイント関数から **DoConfigPropSheet** を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[BuildDisplayTable](builddisplaytable.md)関数を呼び出すことによって、またはカスタム コードを使用して _、lpDisplayTable_ パラメーターが指す表示テーブルを作成できます。 
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

