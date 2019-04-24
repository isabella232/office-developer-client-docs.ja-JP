---
title: imapisupportdoconfigpropsheet
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322373"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成プロパティシートを表示します。
  
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

 _uluiparam_
  
> 順番プロパティシートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpsztitle_
  
> 順番プロパティシートのタイトルへのポインター。
    
 _lpdisplaytable_
  
> 順番プロパティシートに表示されるコントロールを説明する表示テーブルへのポインター。
    
 _lpconfigdata_
  
> 順番プロパティシートに表示される構成プロパティにアクセスするために使用される[imapiprop](imapipropiunknown.md)実装へのポインター。 
    
 _ultoppage_
  
> 順番プロパティシートの既定のトップページの0から始まるインデックス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 構成プロパティシートが表示されました。
    
## <a name="remarks"></a>解説

**imapisupport::D oconfigpropsheet**メソッドは、すべてのサポートオブジェクトに実装されています。 **doconfigpropsheet**は、サービスプロバイダーとメッセージサービスのプロパティを表示するための標準的なユーザーインターフェイスを提供します。 ユーザーが一貫した Windows インターフェイスを利用できるようにするには、すべての構成プロパティでこの標準ダイアログボックスを使用する必要があります。 
  
サービスプロバイダーは、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドの実装の一部として、またはプロパティの詳細を表示するために使用されるボタンから、 **doconfigpropsheet**を呼び出します。 メッセージサービスは、メッセージサービスエントリポイント関数から**doconfigpropsheet**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpdisplaytable_パラメーターによって示される表示テーブルは、 [builddisplaytable](builddisplaytable.md)関数またはカスタムコードを呼び出すことによって作成できます。 
  
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

