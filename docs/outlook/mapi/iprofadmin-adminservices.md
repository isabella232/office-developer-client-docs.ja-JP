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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801134"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**適用されます**: Outlook 
  
プロファイル内のメッセージ サービスを変更する場合、メッセージ サービスの管理オブジェクトへのアクセスを提供します。
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in]変更するプロファイルの名前へのポインター。 _LpszProfileName_パラメーターを NULL にする必要がありますはできません。 
    
 _lpszPassword_
  
> [in]常に NULL を返します。 
    
 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウのハンドルです。
    
 _ulFlags_
  
> [in]メッセージ サービスの管理オブジェクトの検索を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> ユーザー インターフェイスの表示を有効にします。 
    
MAPI_UNICODE 
  
> プロファイル名は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の名前です。
    
 _lppServiceAdmin_
  
> [out]メッセージ サービス管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービスの管理オブジェクトが正常に返されました。
    
MAPI_E_LOGON_FAILED 
  
> 指定されたプロファイルが存在しないまたはパスワードが間違っていたし、 _ulFlags_で MAPI_DIALOG が設定されていないために、正しいパスワードを要求するユーザーに、ダイアログ ボックスを表示できませんでした。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

**IProfAdmin::AdminServices**メソッドは、プロファイル内のメッセージ サービスの構成を変更のメッセージ サービスの管理オブジェクトへのアクセスを提供します。 
  
 _LpszPassword_パラメーターは、NULL または長さ 0 の文字列へのポインターである必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを取得するには、このメソッドまたは[IMAPISession::AdminServices](imapisession-adminservices.md)のいずれか、ですが、厳密に構成のクライアントがあり、メッセージング機能を提供していない場合**IProfAdmin::AdminServices**を呼び出します。 **IProfAdmin::AdminServices**では、セッション オブジェクトを作成できませんし、読み込まれないすべてのサービス プロバイダーでは、パフォーマンスが向上します。 
  
**IProfAdmin::AdminServices**を使用して、プロファイルを作成することはできません。 したがって、 _lpszProfileName_では、既存の有効なプロファイルを指定してください。 指定されたプロファイルが存在しない場合、 **IProfAdmin::AdminServices**は MAPI_E_LOGON_FAILED を返します。 
  
プロファイルの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。
  
- すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。 
    
- 埋め込みスペースがいない先頭または末尾のスペース。
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI では、 **IProfAdmin::AdminServices**メソッドを使用して、サービスを追加するのには選択したプロファイルのメッセージ サービスの管理オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

