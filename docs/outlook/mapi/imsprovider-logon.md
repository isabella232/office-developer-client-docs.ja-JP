---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1cc5d841e28275ad4ccdcaa6f7a41ff1f7bd4b4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620661"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーの 1 つのインスタンスに MAPI をログオンします。
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>パラメーター

 _lpMAPISup_
  
> [in]メッセージ ストアの現在の MAPI サポート オブジェクトへのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 
    
 _lpszProfileName_
  
> [in]ストア プロバイダーのログオンに使用されるプロファイルの名前を含む文字列へのポインター。 この文字列は、ダイアログ ボックスに表示したり、ログ ファイルに書き出したり、単に無視することができます。 _ulFlags_ パラメーターでフラグを設定MAPI_UNICODE Unicode 形式である必要があります。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _lpEntryID_
  
> [in]メッセージ ストアのエントリ識別子へのポインター。 _lpEntryID_ で null を渡す場合は、メッセージ ストアがまだ選択されていないと、ユーザーがメッセージ ストアを選択できるダイアログ ボックスを表示できます。  
    
 _ulFlags_
  
> [in]ログオンの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のオブジェクトが呼び出し元の実装で使用できない場合でも、呼び出しは成功できます。 オブジェクトが使用できない場合は、そのオブジェクトに対する後続の呼び出しでエラーが発生する可能性があります。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このMAPI_UNICODE設定されていない場合、文字列は ANSI 形式です。
    
MDB_NO_DIALOG 
  
> ログオン ダイアログ ボックスの表示を防止します。 このフラグを設定すると、ログオンが失敗MAPI_E_LOGON_FAILEDエラー値が返されます。 このフラグが設定されていない場合、メッセージ ストア プロバイダーは、名前またはパスワードの修正、ディスクの挿入、またはストアへの接続を確立するために必要なその他のアクションを実行するようユーザーに求めできます。
    
MDB_NO_MAIL 
  
> メッセージ ストアは、メールの送受信には使用できません。 このフラグは、このメッセージ ストアが開いている MAPI スプーラーに通知しない MAPI を通知します。 このフラグが設定され、メッセージ ストアがトランスポート プロバイダーと緊密に結合されている場合、プロバイダーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを呼び出す必要があります。 
    
MDB_TEMPORARY 
  
> ダイアログ ボックスを使用せずに、プロファイル セクションからプログラムで情報を取得できるよう、ストアにログを記録します。 このフラグは、MAPI に対して、ストアをメッセージ ストア テーブルに追加し、ストアを永続的にできないことを指示します。 このフラグが設定されている場合、メッセージ ストア プロバイダーは [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) メソッドを呼び出す必要があります。 
    
MDB_WRITE 
  
> 読み取り/書き込みアクセス許可を要求します。
    
 _lpInterface_
  
> [in]ログオンするメッセージ ストアのインターフェイス識別子 (IID) へのポインター。 null **を渡** す場合は、メッセージ ストア [(IMsgStore)](imsgstoreimapiprop.md)の MAPI インターフェイスが返されます。 _lpInterface パラメーター_ は、メッセージ ストアの適切なインターフェイスの識別子 (たとえば、IID_IUnknown または IID_IMAPIProp) に設定することもできます。 
    
 _lpcbSpoolSecurity_
  
> [out]  _lppbSpoolSecurity_ パラメーター内の検証データのサイズ (バイト単位) をストア プロバイダーが返す変数へのポインター。 
    
 _lppbSpoolSecurity_
  
> [out]返される検証データへのポインターを指すポインター。 この検証データは [、IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) メソッドが MAPI スプーラーをメッセージ ストア プロバイダーと同じストアに記録するために提供されます。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される [MAPIERROR](mapierror.md) 構造体へのポインター (該当する場合) へのポインター。 _lppMAPIError パラメーター_ は、戻す **MAPIERROR** 構造がない場合は null に設定できます。 
    
 _lppMSLogon_
  
> [out]MAPI がログオンするメッセージ ストア ログオン オブジェクトへのポインターを指すポインター。
    
 _lppMDB_
  
> [out]MAPI スプーラーおよびクライアント アプリケーションがログオンするメッセージ ストア オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_FAILONEPROVIDER 
  
> このプロバイダーはログオンできませんが、このエラーはサービスを無効にすることはできません。 
    
MAPI_E_LOGON_FAILED 
  
> ログオン セッションを確立できません。
    
MAPI_E_UNCONFIGURED 
  
> プロファイルには、ログオンが完了するのに十分な情報が含まれている必要があります。 この値が返された場合、MAPI はメッセージ ストア プロバイダーのメッセージ サービス エントリ ポイント関数を呼び出します。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
MAPI_E_UNKNOWN_CPID 
  
> サーバーは、クライアントのコード ページをサポートするように構成されていません。
    
MAPI_E_UNKNOWN_LCID 
  
> サーバーは、クライアントのロケール情報をサポートするように構成されていません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは成功しましたが、メッセージ ストア プロバイダーにエラー情報が表示されます。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。 プロバイダーからエラー情報を取得するには [、IMAPISession::GetLastError メソッドを呼び出](imapisession-getlasterror.md) します。 
    
## <a name="remarks"></a>注釈

MAPI は **、IMSProvider::Logon** メソッドを呼び出して、メッセージ ストアへのアクセスを取得するために必要な大部分の処理を実行します。 メッセージ ストア プロバイダーは、特定のストアにアクセスするために必要なユーザー資格情報を検証し、MAPI スプーラーとクライアント アプリケーションがログオンできる  _lppMDB_ パラメーターのメッセージ ストア オブジェクトを返します。 
  
クライアントと MAPI スプーラーを使用するための返されるメッセージ ストア オブジェクトに加えて、プロバイダーは、開いているストアの制御に使用する MAPI 用のメッセージ ストア ログオン オブジェクトも返します。 メッセージ ストア のログオン オブジェクトとメッセージ ストア オブジェクトは、メッセージ ストア プロバイダー内で緊密にリンクし、それぞれがもう一方に影響を与える可能性があります。 ストア オブジェクトとログオン オブジェクトの使用は同じである必要があります。オブジェクトが 2 つのインターフェイスを公開する 1 つのオブジェクトである場合と同様に、ログオン オブジェクトとストア オブジェクトの間には 1 対 1 の対応が必要です。 2 つのオブジェクトも一緒に作成し、一緒に解放する必要があります。 
  
MAPI によって作成され  _、lpMAPISup_ パラメーターでプロバイダーに渡される MAPI サポート オブジェクトは、プロバイダーが必要とする MAPI の関数へのアクセスを提供します。 これには、プロファイル情報の保存と取得、アドレス帳へのアクセスなどの機能が含まれます。 _lpMAPISup ポインター_ は、開いているストアごとに異なる場合があります。 ログオン後にメッセージ ストアの呼び出しを処理する場合、ストア プロバイダーは、そのストアに固有の  _lpMAPISup_ 変数を使用する必要があります。 メッセージストアを開き、メッセージ ストア ログオン オブジェクトの作成に成功するログオン呼び出しの場合、プロバイダーはストア ログオン オブジェクトの MAPI サポート オブジェクトへのポインターを保存し、サポート オブジェクトの参照を追加するには[、IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。 
  
_ログオン呼び出し中_ にプロバイダーがダイアログ ボックスを表示する場合は、ulUIParam パラメーターを **使用する必要** があります。 ただし  _、ulFlags_ に新しいフラグが含まれている場合は、ダイアログ ボックスMDB_NO_DIALOGできません。 ユーザー インターフェイスを呼び出す必要があるが  _、ulFlags_ がそれを許可しない場合、または何らかの理由でユーザー インターフェイスを表示できない場合、プロバイダーは MAPI_E_LOGON_FAILED を返す必要があります。 [**ログオン]** でダイアログ ボックスが表示され、ユーザーがログオンを取り消す場合は、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックすると、プロバイダーはダイアログ ボックスをMAPI_E_USER_CANCEL。 
  
_lpEntryID_ パラメーターには nullを指定するか、このメッセージ ストアが以前に作成したラップされていないストア エントリ識別子をポイントできます。 _lpEntryID が_ ラップされていないエントリ識別子をポイントする場合、そのエントリ識別子は次のいずれかの場所から取得できます。 
  
- これは、ストア プロバイダーが以前にラップし、プロファイル セクションに PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティとして書 **き込んだ** エントリ識別子です。
    
- プロバイダーが以前にラップし、呼び出し元のクライアントに戻されたエントリ識別子を、PR_STORE_ENTRYID **(** [PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティとして指定できます。 
    
- プロバイダーが以前にラップし、メッセージ ストア オブジェクトの PR_ENTRYID プロパティとして呼び出し元 **のクライアントに返された** エントリ識別子を指定できます。 
    
このような場合は、現在使用されているコンピューターとは異なるコンピューターでエントリ識別子が作成されている可能性があります。
  
_lpEntryID が_ **null** ではない場合は、メッセージ ストアの識別と検索に必要なすべての情報が含まれている必要があります。 この情報には、ネットワーク ボリューム名、電話番号、ユーザー アカウント名などがあります。 エントリ識別子のデータを使用してストアへの接続を行えない場合、ストア プロバイダーは、ユーザーが開くストアを選択できるダイアログ ボックスを表示する必要があります。 たとえば、サーバーの名前が変更された場合、アカウント名が変更された場合、またはネットワークの一部が使用できない場合など、ダイアログ ボックスが必要になる場合があります。
  
_lpEntryID が_ **null の場合**、使用するメッセージ ストアがまだ選択されていません。 プロバイダーは、さらにストアを指定するメソッドをサポートしている場合、ダイアログ ボックスを表示せずにストアにアクセスできます。 たとえば、プロバイダーは初期化ファイルを確認したり、構成時にメッセージ サービスのプロファイル セクションに配置された追加のプロパティを探したりできます。
  
プロバイダーが、必要なすべての情報がプロファイルに含されていないと見つけた場合は、プロファイルを返MAPI_E_UNCONFIGURED。 MAPI はプロバイダーのメッセージ サービス エントリ ポイント関数を呼び出して、ユーザーがストアを選択したり、ストアを作成したり、必要に応じてアカウント名とパスワードを入力したりできます。 MAPI は、新しいストアの新しいプロファイル セクションを自動的に作成します。この新しいプロファイル セクションは、追加された方法に応じて、一時的または永続的な場合があります。 ストア プロバイダーが **IMAPISupport::ModifyProfile** メソッドを呼び出した場合、新しいプロファイル セクションが永続的になり [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドによって返されるメッセージ ストアの一覧にストアが追加されます。 
  
_lpInterface パラメーター_ は、新しく開いたストア オブジェクトに必要なインターフェイスの IID を指定します。 _lpInterface で null を渡_ す場合は、MAPI メッセージ ストア インターフェイス **である IMsgStore** が必要です。  メッセージ ストア オブジェクトを渡 **IID_IMsgStore、IMsgStore が必要な場合も** 指定します。 _lpInterface_ IID_IUnknown渡された場合、プロバイダーは、プロバイダーに最適な [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から派生したインターフェイスを使用してストアを開く必要があります (これは通常 **、IMsgStore** です)。 このIID_IUnknown、呼び出し元の実装では [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) メソッドを使用して、ストアを開く操作が成功した後でインターフェイスを選択します。 
  
**IMSProvider::Logon** 呼び出しでは、ストアへのパスや、ストアにアクセスするための資格情報などの十分な情報が返され、MAPI スプーラーがダイアログ ボックスを表示せずにストア プロバイダーと同じストアにログオンできます。 _この情報を取得するには、lpcbSpoolSecurity_ パラメーターと _lppbSpoolSecurity_ パラメーターを使用します。 プロバイダーは [、MSProviderInit](msproviderinit.md) 関数の  _lpfAllocateBuffer_ パラメーター内のバッファーにポインターを渡して、このデータのメモリを割り当てる。プロバイダーは、このバッファーのサイズを  _lpcbSpoolSecurity に入ります_。 
  
MAPI は、必要に応じてこのバッファーを解放します。 MAPI スプーラーのストアへのログオンをプロファイル セクションの情報だけで実行できる場合、プロバイダーは _、lppbSpoolSecurity で null、lpcbSpoolSecurity_ の情報のサイズに 0 を返します。  MAPI スプーラー ログオンは、ストア ログオンとは異なるプロセスの一部として実行されます。渡された情報を含むバッファーはプロセス間でコピーされますので、MAPI スプーラー プロセスとストア プロバイダー プロセスの同じ場所にメモリが含まれている可能性があります。 したがって、プロバイダーは、このバッファーにアドレスを入れる必要があります。 MAPI スプーラー ログオンの詳細については [、「IMSProvider::SpoolerLogon メソッド」を参照](imsprovider-spoolerlogon.md) してください。 
  
ほとんどのストア プロバイダーは _、lpMAPISup_ パラメーターで渡されたサポート オブジェクトの [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)メソッドを使用して、ユーザーの資格情報とオプションを保存および取得します。 **OpenProfileSection** を使用すると、ストア プロバイダーはプロファイル セクションに追加の任意の情報を保存し、それを特定のリソースに関連付けできます。 たとえば、ストア プロバイダーは、リソースに関連付けられたユーザー アカウント名とパスワード、そのリソースへのアクセスに必要なパスや他の情報を保存できます。 
  
プロパティ識別子が0x6600 0x67FFプロパティは、プロファイル セクションにプライベート データを格納するためにプロバイダーが使用できるセキュリティで保護されたプロパティです。 プロファイル セクション オブジェクトでのプロパティの使用の詳細については [、「IProfSect : IMAPIProp メソッド」を参照](iprofsectimapiprop.md) してください。 
  
0x6600 ~ 0x67FF の識別子を持つプロパティのプライベート データに加えて、ストア プロバイダーはプロファイル セクションで **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの情報を提供する必要があります。 **この** メッセージ ストアをアクセス権のある他のユーザーと区別するために、ユーザーに表示される識別文字列 ("Microsoft 個人情報ストア" など) であるプロバイダー自体の表示名を PR_DISPLAY_NAME に入れる必要があります。 **PR_DISPLAY_NAME** 一般的には、サーバー名、ユーザー アカウント名、またはパスが含まれる場合があります。 
  
一部のプロファイル セクションのプロパティは、メッセージ ストア テーブルに表示されます。MAPI サブシステムのセットアップ、インストール、および構成中に他のユーザーが表示されます。 プロバイダーは、通常、保存された資格情報や個人情報を含む新しいプロファイル セクションと、プロパティ情報が変更されたと見つけた場合の両方について、これらの表示プロパティに関する情報を提供します。 プロファイル セクションの詳細については [、「IMAPISupport::OpenProfileSection」を参照してください](imapisupport-openprofilesection.md)。
  
ユーザーに正常にログオンした後、MAPI に戻る前に、ストア プロバイダーはリソースの状態行のプロパティの配列を作成し [、IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出す必要があります。 
  
 **現在** の MAPI セッションで既に開いているメッセージ ストアを開くログオン呼び出しは、前に説明した処理の多くをスキップします。 これらの呼び出しは、状態行を作成したり、メッセージ ストア ログオン オブジェクトを返したり、MAPI サポート オブジェクト **の AddRef** を呼び出したり、MAPI スプーラー ログオンのデータを返したりしません。 これらの呼び出しは、S_OKを返し、要求されたインターフェイスを持つメッセージ ストア オブジェクトを返します。 
  
このような呼び出しを検出するには、プロバイダーは、このプロバイダー オブジェクト用に既に開いているストアのメッセージ ストア プロバイダー オブジェクト内のリストを維持する必要があります。 Logon 呼び **出しを** 処理する場合、プロバイダーは開いているストアのこの一覧をスキャンし、ログオンするストアが既に開いているかどうかを判断する必要があります。 その場合は、ユーザー資格情報をチェックする必要が生じず、可能な場合はダイアログ ボックスの表示を避ける必要があります。 ダイアログ ボックスを表示する必要がある場合、プロバイダーは返された情報をチェックして、ストアが 2 度目に開いているかどうかを確認する必要があります。 さらに、プロバイダーは、ログオン呼び出し処理の開始時に  _lpEntryID_ を使用して重複する開始 **を確認する** 必要があります。 
  
開いているストアに **アクセスする Logon** 呼び出しの標準処理は次のとおりです。 
  
1. 要求される新しいインターフェイスが既存のストアのインターフェイスと同じ場合、ストア プロバイダーは既存のストア オブジェクトの **AddRef** を呼び出します。 それ以外の場合は **、QueryInterface を呼び出** して新しいインターフェイスを取得します。 ストアが新しいインターフェイスをサポートしていない場合、プロバイダーはエラー値を返す必要MAPI_E_INTERFACE_NOT_SUPPORTED。 
    
2. プロバイダーは  _、lppMDB_ の既存のストア オブジェクトの必要なインターフェイスへのポインターを返します。
    
3. プロバイダーは _、lppMSLogon で null を返します_。 
    
4. プロバイダーは、呼び出しで渡されたサポート オブジェクトのプロファイルを開く必要があります。 さらに、プロバイダーの一意の識別子を登録したり、状態行を登録したり、MAPI スプーラー ログオン データを返したりする必要があります。
    
5. プロバイダーは、オブジェクトへのポインターを必要としないので、サポート オブジェクトの **AddRef** を呼び出す必要があります。 
    
可能な限り、プロバイダーは、 **ログオン** 呼び出しに対して適切なエラー文字列と警告文字列を返す必要があります。そのため、何かが機能しなかった理由を判断する際のユーザーの負担が大幅に軽減されます。 これらの文字列を取得するために、プロバイダーは MAPIERROR 構造体の **メンバーを設定** します。 MAPI は、プロバイダーから返された **MAPIERROR** 構造体を見て、使用し、解放します。 
  
この **MAPIERROR** 構造体のメモリは **、MSProviderInit** 呼び出しで _lpfAllocateBuffer_ で渡されるバッファーを使用して割り当てる必要があります。 返される構造体に含まれるエラー文字列は、Logon _ulFlags_ で MAPI_UNICODE が設定されている場合は **Unicode** 形式である必要があります。それ以外の場合は、ANSI 文字セットに含まれている必要があります。 
  
Logon から返されるほとんどのエラー値 **では**、MAPI は、障害が発生したプロバイダーが属するメッセージ サービスを無効にします。 MAPI は、MAPI セッションの一生の間、これらのサービスに属するプロバイダーを呼び出す必要があります。 これに対し **、Logon** がログオンからエラー MAPI_E_FAILONEPROVIDERを返しても、MAPI はプロバイダーが属するメッセージ サービスを無効にしない。 **セッション** の一MAPI_E_FAILONEPROVIDERサービス全体を無効にしないエラーが発生した場合、ログオンはエラーを返す必要があります。 たとえば、プロバイダーがユーザー インターフェイスの表示を許可しない場合に、必要なパスワードが使用できない場合に、このエラーが返される場合があります。 
  
プロバイダーがログオンからMAPI_E_UNCONFIGURED場合、MAPI はプロバイダーのメッセージ サービス エントリ関数を呼び出し、ログオンを再試行します。 MAPI はMSG_SERVICE_CONFIGUREをコンテキストとして渡して、サービスに自身を構成する機会を与えます。 クライアントがログオン時にユーザー インターフェイスを許可する場合、サービスは構成プロパティ シートを提示して、ユーザーが構成情報を入力できます。
  
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

