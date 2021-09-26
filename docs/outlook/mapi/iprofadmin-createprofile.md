---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 06fe432cbf1c1a577d612b1212123f9db206ad29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620570"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいプロファイルを作成します。
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszProfileName_
  
> [in]新しいプロファイルの名前へのポインター。
    
 _lpszPassword_
  
> [in]新しいプロファイルのパスワードへのポインター。 
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロファイルの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFAULT_SERVICES 
  
> MAPI は、Mapisvc.inf ファイルの [既定のサービス] セクションに含まれるメッセージ サービスを新しいプロファイルに設定する必要があります。
    
MAPI_DIALOG 
  
> 追加するメッセージ サービス内の各プロバイダーの構成プロパティ シートを表示できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいプロファイルが作成されました。
    
MAPI_E_NO_ACCESS 
  
> 指定した新しいプロファイルが既に存在します。
    
## <a name="remarks"></a>注釈

**IProfAdmin::CreateProfile** メソッドは、新しいプロファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateProfile は、アプリケーション** のインストール時またはセッション中にいつでも呼び出します。 インストール時にこのメソッドが呼び出される場合、構成設定の多くは Mapisvc.inf 構成ファイルから取得されます。 アクティブ なセッション中にこのメソッドが呼び出された場合、設定は、一連のプロパティ シートを介してプロンプトが表示されるユーザーから行います。 
  
_ulFlags_ パラメーターで MAPI_DEFAULT_SERVICES フラグが設定されている場合 **、CreateProfile** は Mapisvc.inf ファイルの [既定のサービス] セクションの各メッセージ サービスのメッセージ サービス エントリ ポイント関数を呼び出します。 各メッセージ サービス エントリ ポイント関数は  _、ulContext_ パラメーターを指定して呼び出MSG_SERVICE_CREATE。 
  
MAPI_DIALOG フラグと MAPI_DEFAULT_SERVICES フラグの両方が設定されている場合は  _、ulUIParam_ パラメーターと  _ulFlags_ パラメーターの値もメッセージ サービスエントリ ポイント関数に渡されます。 メッセージ サービスエントリ ポイント関数は、Mapisvc.inf ファイルから利用可能なすべての情報がプロファイルに追加された後にのみ呼び出されます。 
  
新しいプロファイルの名前とそのパスワードの長さは最大 64 文字で、次の文字を含めることができます。
  
- アクセント文字とアンダースコア文字を含むすべての英数字。
    
- 埋め込みスペースですが、先頭または末尾のスペースは使用できません。
    
_lpszPassword パラメーター_ は NULL または長さ 0 の文字列へのポインターである必要があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

