---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424120"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションをメッセージングシステムとのセッションに記録します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
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

 _uluiparam_
  
> 順番ログオンダイアログボックスがモーダルであるウィンドウを処理します。 呼び出し中にダイアログボックスが表示されない場合、 _uluiparam_パラメーターは無視されます。 このパラメーターには0を指定できます。 
    
 _lpszprofilename_
  
> 順番ユーザーがログオンするときに使用するプロファイルの名前を含む文字列へのポインター。 この文字列は、64 文字に制限されています。
    
 _lpszpassword_
  
> 順番プロファイルのパスワードを含む文字列へのポインター。 _lpszpassword_パラメーターは NULL である必要があります。 
    
 _flflags_
  
> 順番ログオンの実行方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_ALLOW_OTHERS 
  
> 共有セッションが返されます。これにより、後のクライアントがユーザーの資格情報を指定せずにセッションを取得できるようになります。 
    
MAPI_BG_SESSION
  
> セッションにログオンし、バックグラウンドで任意の操作を実行します。 一般に、クライアントがバックグラウンドスレッドで処理を行う場合や、フォアグラウンドスレッドに対して安全でない方法で処理を行う場合は、MAPI_BG_SESSION フラグを指定して呼び出します。 MAPI_BG_SESSION を使用する場所の例として、インデックスエンジンなどのクライアントアプリケーションや、バックグラウンドの種類のアクセスのための個人用フォルダーファイル (PST) を開くことがあります。MAPILogonEx。
    
MAPI_EXPLICIT_PROFILE 
  
> 既定のプロファイルを使用しないで、ユーザーがプロファイルを提供する必要があります。 
    
MAPI_EXTENDED 
  
> 拡張機能を使用してログオンします。 このフラグは常に設定する必要があります。
    
MAPI_FORCE_DOWNLOAD 
  
> 戻る前に、すべてのユーザーのメッセージをダウンロードするように試行する必要があります。 MAPI_FORCE_DOWNLOAD フラグが設定されていない場合、MAPILogonEx の呼び出し後に、メッセージをバックグラウンドでダウンロードできます。 
    
MAPI_LOGON_UI 
  
> 必要に応じて、ユーザーにログオン情報の入力を求めるダイアログボックスが表示されます。 MAPI_LOGON_UI フラグが設定されていない場合、呼び出し元クライアントはログオンダイアログボックスを表示せず、ユーザーがログオンしていない場合はエラー値を返します。
    
MAPI_NEW_SESSION 
  
> 共有セッションを取得するのではなく、新しい MAPI セッションを作成しようとしています。 MAPI_NEW_SESSION フラグが設定されていない場合、MAPILogonEx は、 _lpszprofilename_パラメーターが NULL でない場合でも、既存の共有セッションを使用します。 
    
MAPI_NO_MAIL 
  
> mapi では、セッションの存在が mapi スプーラーに通知されません。 その結果、密結合ストアとトランスポートペアを使用した場合を除き、セッションでメッセージを送受信できなくなります。 呼び出し元クライアントがエージェントとして機能している場合、構成作業を実行する必要がある場合、または使用可能なメッセージストアをクライアントが参照している場合は、このフラグが設定されます。 
    
MAPI_NT_SERVICE 
  
> 発信者が Windows サービスとして実行されている。 Windows サービスとして実行されていない発信者は、このフラグを設定してはなりません。サービスとして実行されている発信者は、このフラグを設定する必要があります。 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx は、プロファイル内の各メッセージサービスについて、構成ダイアログボックスを表示する必要があります。 このダイアログボックスは、プロファイルが選択された後、メッセージサービスがログオンする前に表示されます。 ログオン用の MAPI コモンダイアログボックスにも、同じ操作を要求するチェックボックスがあります。 
    
MAPI_TIMEOUT_SHORT 
  
> 数秒以上ブロックされた場合、ログオンは失敗します。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
MAPI_USE_DEFAULT 
  
> メッセージングサブシステムは、 _lpszprofilename_パラメーターの既定のプロファイルのプロファイル名を置き換える必要があります。 _lpszprofilename_が NULL または空の場合を除き、MAPI_EXPLICIT_PROFILE フラグは無視されます。 
    
 _lppsession_
  
> 読み上げMAPI セッションインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオンに成功しました。
    
MAPI_E_LOGON_FAILED 
  
> MAPILogonEx への1つ以上のパラメーターが無効であったか、既に開いているセッションが多すぎるため、ログオンに失敗しました。
    
MAPI_E_TIMEOUT 
  
> MAPI は、ミューテックスを介してすべてのログオンをシリアル化します。 これは、MAPI_TIMEOUT_SHORT フラグが設定されていて、別のスレッドがミューテックスを保持した場合に返されます。 
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

MAPI クライアントアプリケーションは、MAPILogonEx 関数を呼び出して、メッセージングシステムとのセッションにログオンします。 MAPI 呼び出しとの間で送受信されるすべての文字列は、null で終了し、呼び出し元クライアントまたはプロバイダーのオペレーティングシステムの現在の文字セットまたはコードページで指定する必要があります。
  
MAPI_ALLOW_OTHERS フラグを設定して MapiLogonEx を呼び出し、フラグ MAPI_NEW_SESSION が設定されていない場合は、既に前のセッションが存在する場合、 _lpszprofilename_パラメーターは無視されます。 _lpszprofilename_パラメーターが NULL の場合、または空の文字列をポイントしていて、 _flflags_パラメーターに MAPI_LOGON_UI フラグが含まれている場合、MAPILogonEx 関数はプロファイル名に空のフィールドを持つログオンダイアログボックスを生成します。 
  
特定のプロファイルにログオンする場合、クライアントはプロファイル名に加えて MAPI_NEW_SESSION フラグを MAPILogonEx に渡す必要があります。 または、別のクライアントが MAPI_ALLOW_OTHERS を使用してログオンして共有セッションを確立した場合、クライアントは要求されたプロファイルではなく、共有セッションにログオンします。 
  
MAPI_EXPLICIT_PROFILE フラグは、MAPI_USE_DEFAULT フラグも存在しない限り、 _lpszprofilename_が NULL または空の場合は、既定のプロファイル名を使用しません。 
  
MAPI_NO_MAIL フラグには、MAPI スプーラーを使用しない場合に、次のようないくつかの影響があります。
  
- このセッション中に MAPI スプーラーでメッセージを送信または配信することはできません。 密結合ストアとトランスポートプロバイダーのみが、メッセージの送受信を行うことができます。 
    
- サーバーベースのストアは依然としてメッセージを送信または配信する場合があります。 
    
- サーバーベースのストアによって送信または配信されたメッセージは、フックプロバイダーによって処理されません。 
    
- トランスポートのメッセージ単位および受信者ごとのオプションは使用できません。 
    
- 状態テーブルには、トランスポートプロバイダーのエントリは含まれていません。状態オブジェクトに依存するトランスポート機能 (構成など) は使用できません。 
    
- 状態テーブルのメッセージスプーラー行には、STATUS_FAILURE の値が含まれています。 
    
- 上乗せログオンは許可されますが、これらのログオンによって、以前のログオンがステータスオブジェクトの更新を受信することはありません。 
    
サービスは常に MAPI_NO_MAIL フラグを使用してログオンする必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects  <br/> |cmapiobjects:: MAPILogonEx  <br/> |mfcmapi は、MAPILogonEx メソッドを使用して MAPI にログオンします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

