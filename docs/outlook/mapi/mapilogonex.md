---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a37ad43414efc82cd2418fcaa848a354d116a62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556071"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションをメッセージング システムとのセッションにログに記録します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]ログオン ダイアログ ボックスがモーダルであるウィンドウを処理します。 呼び出し中にダイアログ ボックスが表示されない場合  _、ulUIParam_ パラメーターは無視されます。 このパラメーターには 0 を指定できます。 
    
 _lpszProfileName_
  
> [in]ユーザーがログオンするときに使用するプロファイルの名前を含む文字列へのポインター。 この文字列は、64 文字に制限されています。
    
 _lpszPassword_
  
> [in]プロファイルのパスワードを含む文字列へのポインター。 _lpszPassword パラメーター_ は NULL である必要があります。 
    
 _flFlags_
  
> [in]ログオンの実行方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_ALLOW_OTHERS 
  
> 共有セッションを返す必要があります。これにより、後のクライアントはユーザー資格情報を提供せずにセッションを取得できます。 
    
MAPI_BG_SESSION
  
> セッションにログオンし、バックグラウンドで任意の操作を実行します。 一般に、クライアントがフォアグラウンド スレッドに対して控えめな方法でバックグラウンド スレッドまたは別のプロセスで処理を行う場合は、MAPI_BG_SESSION フラグを使用して呼び出す必要があります。 インデックス エンジンや、バックグラウンドタイプアクセス用の個人用フォルダー ファイル (PST) を開くなどのクライアント アプリケーションは、ユーザーが使用する場所の例MAPI_BG_SESSION。MAPILogonEx。
    
MAPI_EXPLICIT_PROFILE 
  
> 既定のプロファイルを使用し、ユーザーがプロファイルを指定する必要があります。 
    
MAPI_EXTENDED 
  
> 拡張機能を使用してログオンします。 このフラグは常に設定する必要があります。
    
MAPI_FORCE_DOWNLOAD 
  
> 戻る前に、すべてのユーザーのメッセージをダウンロードする必要があります。 このフラグMAPI_FORCE_DOWNLOAD設定されていない場合、MAPILogonEx の呼び出しが返された後、メッセージをバックグラウンドでダウンロードできます。 
    
MAPI_LOGON_UI 
  
> 必要に応じて、ログオン情報の入力を求めるダイアログ ボックスが表示されます。 MAPI_LOGON_UIフラグが設定されていない場合、呼び出し元のクライアントはログオン ダイアログ ボックスを表示し、ユーザーがログオンしていない場合はエラー値を返します。
    
MAPI_NEW_SESSION 
  
> 共有セッションを取得する代わりに、新しい MAPI セッションを作成する必要があります。 このフラグMAPI_NEW_SESSION設定されていない場合  _、lpszprofileName_ パラメーターが NULL でなくても、MAPILogonEx は既存の共有セッションを使用します。 
    
MAPI_NO_MAIL 
  
> MAPI は、セッションの存在を MAPI スプーラーに通知する必要があります。 その結果、緊密に結合されたストアとトランスポートのペアを除き、セッションでメッセージを送信または受信できません。 呼び出し元のクライアントは、エージェントとして機能している場合、構成作業を行う必要がある場合、またはクライアントが使用可能なメッセージ ストアを参照している場合に、このフラグを設定します。 
    
MAPI_NT_SERVICE 
  
> 呼び出し元は、Windowsサービスとして実行されています。 サービスとして実行されていない呼び出し元Windowsこのフラグを設定する必要があります。サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx は、プロファイル内の各メッセージ サービスの構成ダイアログ ボックスを表示する必要があります。 このダイアログ ボックスは、プロファイルが選択された後、メッセージ サービスがログオンする前に表示されます。 ログオンの MAPI 共通ダイアログ ボックスには、同じ操作を要求するチェック ボックスも含まれる。 
    
MAPI_TIMEOUT_SHORT 
  
> 数秒間以上ブロックされた場合、ログオンは失敗する必要があります。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
MAPI_USE_DEFAULT 
  
> メッセージング サブシステムは、lpszProfileName パラメーターの既定のプロファイルのプロファイル名  _を置き換える必要_ があります。 _lpszProfileName_ が NULL または空の場合を指定しない限り、MAPI_EXPLICIT_PROFILEフラグは無視されます。 
    
 _lppSession_
  
> [out]MAPI セッション インターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオンが成功しました。
    
MAPI_E_LOGON_FAILED 
  
> MAPILogonEx に対する 1 つ以上のパラメーターが無効であるか、既に開いているセッションが多すぎたため、ログオンが失敗しました。
    
MAPI_E_TIMEOUT 
  
> MAPI は、ミューテックスを介してすべてのログオンをシリアル化します。 この値は、MAPI_TIMEOUT_SHORTフラグが設定され、別のスレッドがミューテックスを保持している場合に返されます。 
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

MAPI クライアント アプリケーションは MAPILogonEx 関数を呼び出して、メッセージング システムとのセッションにログオンします。 MAPI 呼び出しで渡され、MAPI 呼び出しとの間で返される文字列はすべて null で終了し、呼び出し元のクライアントまたはプロバイダーのオペレーティング システムの現在の文字セットまたはコード ページで指定する必要があります。
  
_lpszProfileName_ パラメーターは、MAPI_ALLOW_OTHERS フラグが設定された MapiLogonEx と呼ばれる既存の以前のセッションがある場合、およびフラグ MAPI_NEW_SESSION が設定されていない場合は無視されます。 _lpszProfileName_ パラメーターが NULL または空の文字列をポイントし _、flFlags_ パラメーターに MAPI_LOGON_UI フラグが含まれる場合、MAPILogonEx 関数は、プロファイル名の空のフィールドを持つログオン ダイアログ ボックスを生成します。 
  
特定のプロファイルにログオンする場合、クライアントはプロファイル名に加MAPI_NEW_SESSION MAPILogonEx にメッセージ フラグを渡す必要があります。 それ以外の場合、別のクライアントが MAPI_ALLOW_OTHERS でログオンして共有セッションを確立した場合、クライアントは要求されたプロファイルではなく共有セッションにログオンします。 
  
この MAPI_EXPLICIT_PROFILEフラグを指定しても  _、lpszProfileName_ が NULL または空の場合、既定のプロファイル名は使用されません(MAPI_USE_DEFAULT フラグも存在しない限り)。 
  
このMAPI_NO_MAILには、MAPI スプーラーを使用しない場合に次のような効果があります。
  
- このセッション中に MAPI スプーラーによってメッセージを送信または配信できません。 緊密に結合されたストアプロバイダーとトランスポート プロバイダーだけがメッセージを送受信できます。 
    
- サーバー ベースのストアは、メッセージを送信または配信する場合があります。 
    
- サーバー ベースのストアによって送信または配信されたメッセージは、フック プロバイダーによって処理されません。 
    
- トランスポートのメッセージごとのオプションと受信者ごとのオプションは使用できません。 
    
- 状態テーブルにはトランスポート プロバイダーのエントリは含めず、状態オブジェクトに依存するトランスポート機能 (構成など) は使用できません。 
    
- 状態テーブルのメッセージ スプーラー行には、次の値STATUS_FAILUREされます。 
    
- ピギーバックされたログオンは許可されますが、これらのログオンでは、前回のログオンで状態オブジェクトの更新プログラムが受信されません。 
    
サービスは常に、このフラグを使用MAPI_NO_MAILする必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI は MAPILogonEx メソッドを使用して MAPI にログオンします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

