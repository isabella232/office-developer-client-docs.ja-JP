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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 06341f897a7865c09a565db67bb409fc9f49f8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800744"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**適用対象**: Outlook 
  
構成のプロパティ シートを表示します。
  
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
  
> [in]プロパティ シート上のコントロールを表示するを記述する表示のテーブルへのポインター。
    
 _lpConfigData_
  
> [in]プロパティ シートに表示される設定のプロパティにアクセスするために使用する[IMAPIProp](imapipropiunknown.md)実装へのポインター。 
    
 _ulTopPage_
  
> [in]プロパティ ・ シートの一番上の既定ページの 0 から始まるインデックス。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 構成のプロパティ シートが表示されます。
    
## <a name="remarks"></a>注釈

サポートのすべてのオブジェクトの**IMAPISupport::DoConfigPropsheet**メソッドを実装します。 **DoConfigPropSheet**は、サービス プロバイダーとサービスのメッセージのプロパティを表示するための標準のユーザー インターフェイスを提供します。 ユーザーは、一貫性のある Windows のインターフェイスから利用できるように、すべての構成プロパティが表示されますのこの標準のダイアログ ボックスを使用してください。 
  
サービス プロバイダーは、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドまたはプロパティの詳細を表示するボタンですから、それぞれの実装の一部として**DoConfigPropSheet**を呼び出します。 メッセージ サービスは、メッセージ サービスのエントリ ポイント関数から**DoConfigPropSheet**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[BuildDisplayTable](builddisplaytable.md)関数を呼び出すことによって、またはカスタム コードと、 _lpDisplayTable_パラメーターが指す、表示された表を作成できます。 
  
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

