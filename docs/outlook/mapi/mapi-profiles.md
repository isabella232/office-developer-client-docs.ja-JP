---
title: MAPI プロファイル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ef17c0f1cfb3a4cf90e687616b299484be90f44b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610217"
---
# <a name="mapi-profiles"></a>MAPI プロファイル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルには、コンピューターにインストールされているサービス プロバイダーとメッセージ サービスに関する情報が格納されます。 セッションごとに、ログオン時のクライアントが、使用するプロバイダーとサービスを記述するプロファイルを 1 つ選択します。 クライアントはプロファイルのコレクションから選択し、必要に応じて既定のプロファイルとして設定できます。 既定のプロファイルは、クライアントがセッションを開始するときに自動的に選択され、プロファイルを明示的に指定していないプロファイルです。
  
また、これらのトピックでは、バイナリ ストリームに格納されているニックネーム キャッシュについて説明します。
  
- [ニックネーム キャッシュ](nickname-cache.md)
    
- [オートコンプリート ストリーム](autocomplete-stream.md)
    
- [バイナリ ファイルの解析](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>プロファイル セクション

プロファイルは、クライアントとサービス プロバイダーがユーザーにプロファイル プロパティを表示したり、構成を変更したりするためにアクセスするセクションに分かれています。 プロファイル セクションは **、IProfSect** インターフェイス **、IMAPIProp** から派生し、追加のメソッドを持つインターフェイスを実装する MAPI オブジェクトです。 詳細については [、「IProfSect : IMAPIProp 」を参照してください](iprofsectimapiprop.md)。 その唯一の目的は、プロファイル セクションのプロパティを操作する方法です。 特定のプロファイル **セクションへの IProfSect** ポインターを取得するには、クライアントとサービス プロバイダーは次のメソッドを呼び出します。 
  
|||
|:-----|:-----|
|クライアントは次の呼び出しを行えます。  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|サービス プロバイダーは、次の呼び出しを行います。  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|クライアントまたはプロバイダーは、次のいずれかの呼び出しを行えます。  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
プロファイルは、MAPISVC と同様に階層的に整理されます。INF ファイル。 階層の上部には、プロファイルに関連する情報を含むプロファイル セクションがあります。 中間レベルには、特定のメッセージ サービスに関する情報を含むセクションが含まれます。下位レベルには、メッセージ サービスのサービス プロバイダーの 1 つに関する情報を含むセクションが含まれます。 
  
すべてのプロファイルには、プロファイルの 1 つ以上のセクションに格納されるいくつかの必須プロパティがあります。 たとえば、すべてのプロファイルには、PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティと PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティがあります。 プロファイルの検索キーは、MAPIGUID で定義された値に設定されます。H はMUID_PROFILE_INSTANCEプロファイル間で一意である必要があります。 2 つのプロファイルに同じ名前を指定することができますが、同じ検索キーを持つ必要があります。 検索キーは、特定の種類のデータではなくバイナリ データとして扱う必要があります。
  
メッセージ ストア プロバイダーは、プロファイルとメッセージ ストア プロバイダーのプロファイル セクションにメッセージ ストアの **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを含め、これらのエントリを同期する必要があります。 メッセージ ストアを作成すると、プロバイダーはPR_DISPLAY_NAMEに格納されている値に基づいてデータを設定します。 
  
IMAPIProp から継承するプロファイル セクションと他のオブジェクトには、次の 2 つの大きな **違いがあります**。 
  
- プロファイル セクションでは、トランザクションはサポートされていません。
    
- プロファイル セクションでは **、IMAPIProp:::GetIDsFromNames** および **IMAPIProp::GetNamesFromIDs** 実装から MAPI_E_NO_SUPPORT を返す名前付きプロパティはサポートされていません。 詳細については [、「IMAPIProp::GetIDsFromNames」](imapiprop-getidsfromnames.md) および [「IMAPIProp::GetNamesFromIDs」を参照してください](imapiprop-getnamesfromids.md)。
    
プロファイル セクションはトランザクションをサポートしないので **、IMAPIProp::CopyProps、CopyTo、****または SetProps** の呼び出しで行われた変更は直ちに有効になります。  詳細については [、「IMAPIProp::CopyProps」を参照してください](imapiprop-copyprops.md)。 クライアントとサービス プロバイダーは、プロファイル セクションの **IMAPIProp::SaveChanges** メソッドを呼び出し、成功しますが、プロファイル セクション のデータには影響しません。 詳細については [、「IMAPIProp::SaveChanges」を参照してください](imapiprop-savechanges.md)。 変更が直ちに行われると、サービス プロバイダーがユーザーにプロファイル プロパティを表示するためにクライアントが使用するプロパティ シートの実装方法に影響を与える可能性があります。 変更を延期または元に戻せとすサービス プロバイダーは、実際のセクションではなくプロファイル セクションのコピーを使用してプロパティ シートを実装する必要があります。 コピーを使用すると、ユーザーは変更を加え、後でそれらの変更を取り消し、元のプロファイル セクションはそのまま残します。 
  
プロファイルに情報が表示される順序は、MAPI がリソースを構成し、セッションで割り当てを行う方法に影響します。 次の割り当ては、プロファイルの順序の影響を受ける。
  
- 既定のメッセージ ストア
    
- 個人用アドレス帳
    
- 既定のメッセージ ストアの検索パス
    
- 既定のアドレス帳検索パス
    
- トランスポート プロバイダーの注文
    
MAPI は、既定のメッセージ ストアを **、PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに設定された STATUS_DEFAULT_STORE フラグを持つプロファイルの最初のメッセージ ストアに設定します。これは、既定のストアであることを示します。 クライアントは **、IMAPISession::SetDefaultStore を呼び出すことによって、この設定を上書きできます**。 詳細については [、「IMAPISession::SetDefaultStore」を参照してください](imapisession-setdefaultstore.md)。
  
MAPI は、送信メッセージと受信メッセージを処理するトランスポート注文を作成します。 特定の種類のメッセージに対して複数のトランスポート プロバイダーが登録されている場合、MAPI はこの順序を使用して、メッセージを処理するプロバイダーを決定します。 MAPI は、トランスポート プロバイダーがプロファイルに追加された順序を 1 つの例外として設定します **。PR_RESOURCE_FLAGS** プロパティに STATUS_XP_PREFER_LAST フラグを設定するトランスポートは、順序の最後に配置されます。 クライアントは **、IMsgServiceAdmin::MsgServiceTransportOrder を** 呼び出すことによってトランスポート順序を設定できます。 詳細については [、「IMsgServiceAdmin::MsgServiceTransportOrder」を参照してください](imsgserviceadmin-msgservicetransportorder.md)。
  
サービス プロバイダーとメッセージ サービスの注文に関するこれらのガイドラインは、競合する場合があります。 競合がある場合、コードは競合を解決する必要があります。 メール コントロール パネル プログラムを使用して、作成したプロファイルを検査して、プロバイダーが期待通り構成されているかどうかを判断できます。
  

