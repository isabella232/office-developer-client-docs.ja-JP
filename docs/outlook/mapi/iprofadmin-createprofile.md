---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 92d5dcdf3e5e3fbdb7490d777a24976c9ae4af1a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582792"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロファイルを作成する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFAULT_SERVICES 
  
> MAPI には、Mapisvc.inf ファイルの [サービスの既定値] セクションに含まれるメッセージ サービスを使用して新しいプロファイルを作成する必要があります。
    
MAPI_DIALOG 
  
> メッセージ サービスに追加するプロバイダーのそれぞれの構成のプロパティ シートを表示できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいプロファイルが作成されました。
    
MAPI_E_NO_ACCESS 
  
> 指定された新しいプロファイルが既に存在します。
    
## <a name="remarks"></a>注釈

**IProfAdmin::CreateProfile**メソッドは、新しいプロファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateProfile**は、インストール時にアプリケーションまたはセッション中にいつでも呼び出すことができます。 インストール時にこのメソッドが呼び出されると、Mapisvc.inf の構成ファイルから構成設定の多くのもの。 アクティブなセッション中にこのメソッドを呼び出すと、設定した一連のプロパティ シートが表示されますユーザーに起因します。 
  
_UlFlags_パラメーターに MAPI_DEFAULT_SERVICES フラグを設定すると、 **CreateProfile**は、Mapisvc.inf ファイルの [サービスの既定値] セクションでは、各メッセージ サービスのメッセージ サービスのエントリ ポイント関数を呼び出します。 メッセージの各サービスのエントリ ポイント関数は、MSG_SERVICE_CREATE に_ulContext_パラメーターを使用して呼び出されます。 
  
MAPI_DIALOG と MAPI_DEFAULT_SERVICES の両方のフラグが設定されている場合、 _ulUIParam_と_ulFlags_パラメーターの値もメッセージ サービスのエントリ ポイント関数に渡されます。 メッセージ サービスのエントリ ポイント関数は、Mapisvc.inf ファイルからのすべての利用可能な情報がプロファイルに追加された後にのみ呼び出されます。 
  
新しいプロファイルとパスワードの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。
  
- すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。
    
- 埋め込みスペースがいない先頭または末尾のスペース。
    
_LpszPassword_パラメーターは、NULL または長さ 0 の文字列へのポインターである必要があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

