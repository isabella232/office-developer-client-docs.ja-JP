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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317116"
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

 _lpszprofilename_
  
> 順番新しいプロファイルの名前へのポインター。
    
 _lpszpassword_
  
> 順番新しいプロファイルのパスワードへのポインター。 
    
 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番プロファイルの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFAULT_SERVICES 
  
> MAPI は、mapisvc.inf ファイルの [Default services] セクションに含まれているメッセージサービスで新しいプロファイルを作成する必要があります。
    
MAPI_DIALOG 
  
> 追加するメッセージサービスの各プロバイダーの構成プロパティシートを表示できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいプロファイルが作成されました。
    
MAPI_E_NO_ACCESS 
  
> 指定した新しいプロファイルが既に存在します。
    
## <a name="remarks"></a>解説

**IProfAdmin:: createprofile**メソッドは、新しいプロファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**createprofile**は、アプリケーションのインストール時またはセッション中にいつでも呼び出すことができます。 このメソッドがインストール時に呼び出された場合、構成設定の多くは mapisvc.inf 構成ファイルから取得されます。 アクティブなセッション中にこのメソッドが呼び出された場合、設定は一連のプロパティシートを使用してメッセージを表示するユーザーから取得されます。 
  
MAPI_DEFAULT_SERVICES フラグが_ulflags_パラメーターで設定されている場合、 **createprofile**は mapisvc.inf ファイルの [DEFAULT SERVICES] セクションにある各メッセージサービスに対してメッセージサービスエントリポイント関数を呼び出します。 各メッセージサービスエントリポイント関数は、 _ulcontext_パラメーターを MSG_SERVICE_CREATE に設定して呼び出します。 
  
MAPI_DIALOG と MAPI_DEFAULT_SERVICES の両方のフラグが設定されている場合、 _uluiparam_パラメーターと_ulflags_パラメーターの値もメッセージサービスエントリポイント関数に渡されます。 メッセージサービスのエントリポイント関数は、mapisvc.inf ファイルのすべての利用可能な情報がプロファイルに追加された後にのみ呼び出されます。 
  
新しいプロファイルの名前とパスワードは、最大64文字の長さにすることができ、次の文字を含めることができます。
  
- アクセント記号とアンダースコア文字を含むすべての英数字。
    
- スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。
    
_lpszpassword_パラメーターは、NULL または長さ0の文字列へのポインターである必要があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

