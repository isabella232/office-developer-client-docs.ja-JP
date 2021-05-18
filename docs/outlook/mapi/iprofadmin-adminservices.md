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
  
プロファイル内のメッセージ サービスに変更を加えるメッセージ サービス管理オブジェクトへのアクセスを提供します。
  
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

 _lpszProfileName_
  
> [in]変更するプロファイルの名前へのポインター。 _lpszProfileName パラメーター_ は NULL にすることはできません。 
    
 _lpszPassword_
  
> [in]常に NULL。 
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウのハンドル。
    
 _ulFlags_
  
> [in]メッセージ サービス管理オブジェクトの取得を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ユーザー インターフェイスの表示を有効にします。 
    
MAPI_UNICODE 
  
> プロファイル名は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、名前は ANSI 形式になります。
    
 _lppServiceAdmin_
  
> [out]メッセージ サービス管理オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービス管理オブジェクトが正常に返されました。
    
MAPI_E_LOGON_FAILED 
  
> 指定されたプロファイルが存在しないか、パスワードが間違っていたため、MAPI_DIALOG が  _ulFlags_ で設定されていないので、正しいパスワードを要求するダイアログ ボックスをユーザーに表示できません。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IProfAdmin::AdminServices** メソッドは、プロファイル内のメッセージ サービスに構成変更を加えるメッセージ サービス管理オブジェクトへのアクセスを提供します。 
  
 _lpszPassword パラメーター_ は NULL または長さ 0 の文字列へのポインターである必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

このメソッドまたは [IMAPISession::AdminServices](imapisession-adminservices.md)を呼び出すことによって [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを取得することができますが、厳密に構成クライアントを持ち、メッセージング機能を提供しない場合は **、IProfAdmin::AdminServices** を呼び出します。 **IProfAdmin::AdminServices** はセッション オブジェクトを作成し、サービス プロバイダーを読み込み、パフォーマンスを向上させます。 
  
**IProfAdmin::AdminServices を使用してプロファイル** を作成することはできません。 したがって、lpszProfileName で既存の有効な  _プロファイルを指定する必要があります_。 指定したプロファイルが存在しない場合 **、IProfAdmin::AdminServices** は、このMAPI_E_LOGON_FAILED。 
  
プロファイルの名前の長さは最大 64 文字で、次の文字を含めることができます。
  
- アクセント文字とアンダースコア文字を含むすべての英数字。 
    
- 埋め込みスペースですが、先頭または末尾のスペースは使用できません。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI は **、IProfAdmin::AdminServices** メソッドを使用して、選択したプロファイルのメッセージ サービス管理オブジェクトを開き、サービスを追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

