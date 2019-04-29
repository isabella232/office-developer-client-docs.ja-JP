---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422083"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のメッセージサービスに変更を加えるためのメッセージサービス管理オブジェクトへのアクセスを提供します。
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>パラメーター

 _lpszprofilename_
  
> 順番変更するプロファイルの名前へのポインターを指定します。 _lpszprofilename_パラメーターを NULL にすることはできません。 
    
 _lpszpassword_
  
> 順番常に NULL。 
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウのハンドル。
    
 _ulFlags_
  
> 順番メッセージサービス管理オブジェクトの取得を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ユーザーインターフェイスの表示を有効にします。 
    
MAPI_UNICODE 
  
> プロファイル名が Unicode 形式である。 MAPI_UNICODE フラグが設定されていない場合、名前は ANSI 形式になります。
    
 _lppserviceadmin_
  
> 読み上げメッセージサービス管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービス管理オブジェクトが正常に返されました。
    
MAPI_E_LOGON_FAILED 
  
> 指定されたプロファイルが存在しないか、またはパスワードが正しくないため、ユーザーに正しいパスワードを要求するためにダイアログボックスを表示できませんでした。 MAPI_DIALOG が_ulflags_で設定されていませんでした。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

**IProfAdmin:: adminservices**メソッドは、プロファイル内のメッセージサービスに対する構成変更を行うためのメッセージサービス管理オブジェクトへのアクセスを提供します。 
  
 _lpszpassword_パラメーターは、NULL または長さ0の文字列へのポインターである必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターは、このメソッドまたは[imapisession:: adminservices](imapisession-adminservices.md)のいずれかを呼び出すことによって取得できますが、厳密に構成クライアントがあり、メッセージング機能を提供していない場合は、 **IProfAdmin:: adminservices**を呼び出すことができます。 **IProfAdmin:: adminservices**では、セッションオブジェクトは作成されず、サービスプロバイダーは読み込まれません。これにより、パフォーマンスが向上します。 
  
**IProfAdmin:: adminservices**を使用してプロファイルを作成することはできません。 そのため、 _lpszprofilename_に既存の有効なプロファイルを指定する必要があります。 指定したプロファイルが存在しない場合、 **IProfAdmin:: adminservices**は MAPI_E_LOGON_FAILED を返します。 
  
プロファイルの名前は最大64文字の長さにすることができ、次の文字を含めることができます。
  
- アクセント記号とアンダースコア文字を含むすべての英数字。 
    
- スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> | hraddservicetoprofile  <br/> |mfcmapi は、 **IProfAdmin:: adminservices**メソッドを使用して、選択されたプロファイルのメッセージサービス管理オブジェクトを開き、サービスを追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

