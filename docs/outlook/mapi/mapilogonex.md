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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801493"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**適用されます**: Outlook 
  
メッセージング システムとのセッションに、クライアント アプリケーションを記録します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in][ログオン] ダイアログ ボックスはモーダル ウィンドウへのハンドルします。 呼び出し時にダイアログ ボックスが表示されない場合は、 _ulUIParam_パラメーターは無視されます。 このパラメーターは、0 にすることができます。 
    
 _lpszProfileName_
  
> [in]ユーザーがログオンしたときに使用するプロファイルの名前を含む文字列へのポインター。 この文字列は、64 文字に制限されています。
    
 _lpszPassword_
  
> [in]プロファイルのパスワードを含む文字列へのポインター。 _LpszPassword_パラメーターは、NULL である必要があります。 
    
 _flFlags_
  
> [in]ログオンを実行する方法を制御するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_ALLOW_OTHERS 
  
> 以降のクライアントのユーザーの資格情報を提供することがなくセッションを取得することができますが、共有セッションが返されます。 
    
MAPI_BG_SESSION
  
> セッションにログオンし、バック グラウンドですべての操作を実行します。 一般に、クライアントがバック グラウンド スレッドかフォア グラウンド スレッドに目障りではない方法で別のプロセスでの処理を実行しようとすると場合は、MAPI_BG_SESSION フラグを指定して呼び出す必要があります。 インデックス エンジンまたはバック グラウンドのアクセス権の種類の個人用フォルダー ファイル (PST) を開くなどのクライアント アプリケーションは、MAPI_BG_SESSION を使用する場所の例を示します。MAPILogonEx。
    
MAPI_EXPLICIT_PROFILE 
  
> 既定のプロファイルを使用しない必要があり、ユーザーはプロファイルを指定する要求する必要があります。 
    
MAPI_EXTENDED 
  
> 拡張機能を使用してログオンします。 このフラグを設定することが常にする必要があります。
    
MAPI_FORCE_DOWNLOAD 
  
> 返す前にすべてのユーザーのメッセージをダウンロードするのには試行する必要があります。 MAPI_FORCE_DOWNLOAD フラグが設定されていない場合、MAPILogonEx への呼び出しが返された後のメッセージはバック グラウンドでダウンロードできます。 
    
MAPI_LOGON_UI 
  
> ダイアログ ボックスは、ログオン情報を求めるメッセージが必要な場合に表示する必要があります。 MAPI_LOGON_UI フラグが設定されていないと呼び出し元のクライアント ログオンのダイアログ ボックスは表示されません、ユーザーがログオンしていない場合、エラー値を返します。
    
MAPI_NEW_SESSION 
  
> 共有セッションを取得するのではなく新しい MAPI セッションを作成する試行する必要があります。 MAPI_NEW_SESSION フラグが設定されていない場合、MAPILogonEx は、 _lpszprofileName_パラメーターが NULL でない場合でも、既存の共有セッションを使用します。 
    
MAPI_NO_MAIL 
  
> MAPI は MAPI スプーラー セッションの存在を通知する必要があります。 メッセージの送信も密結合を保存 [トランスポートのペア以外のセッションで受信したことになります。 呼び出し側のクライアントは、構成作業を行う必要がある場合、エージェントとして動作しています。 クライアントが使用可能なメッセージ ストアを参照する場合、またはこのフラグを設定します。 
    
MAPI_NT_SERVICE 
  
> 呼び出し元は、Windows サービスとして実行しています。 Windows サービスではこのフラグが設定されていない必要がありますように実行されていない呼び出し元サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx は、プロファイル内の各メッセージ サービスの構成] ダイアログ ボックスが表示されます。 プロファイルが選択されていますが、任意のメッセージの前にサービスがログオンした後、ダイアログ ボックスが表示されます。 ログオンの MAPI のコモン ダイアログ ボックスには、同じ操作を要求する] チェック ボックスも含まれています。 
    
MAPI_TIMEOUT_SHORT 
  
> 数秒以上ブロックされている場合、ログオンが失敗する必要があります。 
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
MAPI_USE_DEFAULT 
  
> メッセージング サブシステムでは、 _lpszProfileName_パラメーターの既定のプロファイルのプロファイル名を置き換える必要があります。 _LpszProfileName_が NULL または空でない場合、MAPI_EXPLICIT_PROFILE フラグは無視されます。 
    
 _lppSession_
  
> [out]MAPI セッションのインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ログオンに成功しました。
    
MAPI_E_LOGON_FAILED 
  
> MAPILogonEx パラメーターの 1 つ以上無効であったためか、または存在しているセッションが多すぎます既にために、ログオンは成功すると、でした。
    
MAPI_E_TIMEOUT 
  
> MAPI では、すべてのログオン ミュー テックスをシリアル化します。 MAPI_TIMEOUT_SHORT フラグが設定された別のスレッドには、相互排他ロックが保持されている場合、この関数が返されます。 
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

MAPI クライアント アプリケーションでは、メッセージング システムとのセッションにログオンする MAPILogonEx 関数を呼び出します。 渡されして、MAPI の呼び出しから返されるすべての文字列は null で終わるが現在の文字セットで指定する必要がありますや、コードの呼び出し元のクライアントやプロバイダーのオペレーティング システムのページ。
  
フラグ MAPI_NEW_SESSION が設定されていない場合、MAPI_ALLOW_OTHERS フラグを設定して [MapiLogonEx と呼ばれる既存の以前のセッションがある場合、 _lpszProfileName_パラメーターは無視されます。 _LpszProfileName_パラメーターが NULL または空の文字列、および_flFlags_パラメーターへのポインターには、MAPI_LOGON_UI フラグが含まれています、MAPILogonEx 関数は、プロファイル名を空のフィールドを持つログオン] ダイアログ ボックスを生成します。 
  
特定のプロファイルにログオンしていると、クライアントする必要がありますフラグを渡す MAPI_NEW_SESSION MAPILogonEx にプロファイル名だけでなく。 それ以外の場合場合、別のクライアントは、MAPI_ALLOW_OTHERS にログオンし、共有セッションを確立しましたが、クライアントがログオンするプロファイルを要求するのではなく共有セッションに。 
  
MAPI_EXPLICIT_PROFILE フラグ_lpszProfileName_が NULL の場合に使用する既定のプロファイル名が発生したりしない空の場合を除き、MAPI_USE_DEFAULT のフラグもあります。 
  
MAPI_NO_MAIL フラグには、MAPI スプーラーを使用するいないと、次が発生するいくつかの効果があります。
  
- メッセージの送信もこのセッション中に、MAPI スプーラーによって配信されることができます。 唯一の密結合ストアおよびトランスポート プロバイダーは、送信し、メッセージを配信できます。 
    
- サーバー ベース ストアの送信またはメッセージの配信可能性がありますもします。 
    
- フック プロバイダーによって送信またはサーバー ベースのストアに配信されるメッセージは処理されません。 
    
- メッセージと受信者ごとのトランスポート オプションはご利用いただけません。 
    
- ステータス テーブルに、トランスポート プロバイダーのエントリが含まれていないと、(構成) などのオブジェクトの状態に依存する任意のトランスポート機能を利用できません。 
    
- メッセージ スプーラー テーブル内の行ステータスにはには、STATUS_FAILURE の値が含まれています。 
    
- 上乗せのログオンが許可されるが、これらのログオン状態のオブジェクトの更新を受信する前のログオンは発生しません。 
    
サービスは、MAPI_NO_MAIL フラグを使用してをログオンする必要があります常にします。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI では、MAPILogonEx メソッドを使用して、MAPI にログオンします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

