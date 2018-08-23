---
title: MAPI プロファイル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c6701f5b7f63fdc7d21b219a5588feb0580db48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579859"
---
# <a name="mapi-profiles"></a>MAPI プロファイル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイルは、サービス ・ プロバイダーおよびコンピューターにインストールされているメッセージのサービスに関する情報を格納します。 すべてのセッションは、ログオン時にクライアントは、使用するプロバイダーとのサービスを説明する 1 つのプロファイルを選択します。 できるプロファイルのコレクションから選択して、クライアントが必要な場合は、既定値として 1 つを確立します。 既定のプロファイルは、クライアントがセッションを開始して、プロファイルを明示的に指定することがないときに自動的に選択されているプロファイルです。
  
これらのトピックでは、バイナリ ストリームに格納されているニックネームのキャッシュの詳細を検索は。
  
- [ニックネーム キャッシュ](nickname-cache.md)
    
- [オートコンプリート ストリーム](autocomplete-stream.md)
    
- [バイナリ ファイルの解析](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>プロファイル セクション

プロファイルは、クライアント セクションに分かれていますが、ユーザーにプロファイル プロパティを表示する、または構成を変更するのにはサービス ・ プロバイダーがアクセスします。 プロファイル セクションは、 **IProfSect**インターフェイスを実装する MAPI オブジェクト、 **IMAPIProp**から派生し、追加のメソッドを持たないインタ フェースです。 詳細についてを参照してください[IProfSect: IMAPIProp](iprofsectimapiprop.md)。 その唯一の目的は、プロファイル セクションのプロパティを操作するためです。 クライアントとサービス ・ プロバイダーは、特定のプロファイル セクションに、 **IProfSect**のポインターを取得するためにメソッドを呼び出します。 
  
|||
|:-----|:-----|
|クライアントが呼び出すことができます。  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|サービス プロバイダーを呼び出すことができます。  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|クライアントまたはプロバイダーのいずれかを呼び出すことができます。  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
プロファイルは階層構造により、MAPISVC のように。INF ファイルです。 階層の上部には、プロファイルに関連する情報が含まれているプロファイル セクションがあります。 中間レベルには、特定のメッセージのサービスに関する情報が含まれているセクションが含まれています、下位レベルには、メッセージ サービスのサービス プロバイダーのいずれかに関する情報が含まれているセクションが含まれています。 
  
すべてのプロファイルには、1 つまたは複数のプロファイルのセクションに格納されているいくつかの必要なプロパティがあります。 たとえば、すべてのプロファイルは、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティを持ちます。 プロファイルの検索キーは、MAPIGUID で定義されている値に設定されます。MUID_PROFILE_INSTANCE と H し、常にすべてのプロファイルが既に存在します。 2 つのプロファイルには、同じ名前を持つことができます、検索キーを同時に持つことはできません。 検索キーは、特定の種類のデータではなくバイナリ データとして扱います。
  
メッセージ ストア プロバイダーは、プロファイルのプロファイルのセクションで、メッセージ ・ ストアの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを含めるし、メッセージのプロバイダーを格納して、これらのエントリの同期を維持するには必要です。 メッセージ ストアが作成されると、プロバイダーはこれらのプロファイル セクションに格納されている値に基づいて**PR_DISPLAY_NAME**を設定します。 
  
プロファイル セクションと**IMAPIProp**を継承する他のオブジェクトとの間の 2 つの主な違いがあります。 
  
- プロファイル セクションでは、トランザクションをサポートしていません。
    
- プロファイル セクションでは、 **IMAPIProp::GetIDsFromNames**と**IMAPIProp::GetNamesFromIDs**の導入から MAPI_E_NO_SUPPORT を取得する、名前付きプロパティをサポートしていません。 詳細については、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)および[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)を参照してください。
    
プロファイル セクションでは、トランザクション、 **IMAPIProp::CopyProps**への呼び出しに加えられた変更をサポートしていないため**CopyTo**、または**SetProps**即時に反映します。 詳細については、 [IMAPIProp::CopyProps](imapiprop-copyprops.md)を参照してください。 クライアントとサービス ・ プロバイダーはプロファイル セクションの**IMAPIProp::SaveChanges**メソッドを呼び出すことができ、成功しますが、プロファイル セクションのデータには影響しません。 詳細については、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を参照してください。 すぐに変更することは、サービス プロバイダーがユーザーにプロファイル プロパティを表示するクライアントを使用するプロパティ シートを実装する方法に影響します。 ユーザーが延期または変更を元に戻すことができるようにするサービス プロバイダーでは、実際のセクションではなく、プロファイルの各セクションのコピーでは、そのプロパティ シートを実装しなければなりません。 コピーを使用すると、ユーザーが変更を加えるし、後でそれらの変更をキャンセル、元のプロファイル セクションを変更を加えずにそのままです。 
  
プロファイルの情報が表示される順序は、MAPI のリソースを構成して、セッション内の割り当てに影響します。 プロファイルの順序では、以下の割り当てが影響を受けます。
  
- 既定のメッセージ ストア
    
- 個人用アドレス帳
    
- 既定のメッセージ ストアの検索パス
    
- 既定のアドレス帳の検索パス
    
- トランスポート プロバイダーの順序
    
MAPI では、STATUS_DEFAULT_STORE フラグの既定のストアができることを示す、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに設定するプロファイルの最初のメッセージ ストアを使用する既定のメッセージ ストアを設定します。 クライアントは、 **IMAPISession::SetDefaultStore**を呼び出すことによってこの設定を上書きすることができます。 詳細については、 [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md)を参照してください。
  
MAPI は、送信および受信メッセージを処理するためのトランスポートの順番を作成します。 特定の種類のメッセージの 2 つ以上のトランスポート プロバイダーが登録されると、MAPI はこの順序を使用して、どのプロバイダーがメッセージを処理する必要がありますを決定します。 MAPI でトランスポート プロバイダーは、1 つの例外 - 輸送船の**PR_RESOURCE_FLAGS**プロパティに STATUS_XP_PREFER_LAST フラグを設定するプロファイルに追加されたが、順序で配置最後の順序を使用するトランスポートの順番を設定します。 クライアントは、 **IMsgServiceAdmin::MsgServiceTransportOrder**を呼び出すことによって、トランスポートの順番を設定できます。 詳細については、 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)を参照してください。
  
サービス プロバイダーおよびメッセージ サービスを注文するためのガイドラインも競合しています。 競合がある場合、コードは競合を解決する必要があります。 メール コントロール パネルのプログラムを使用すると、期待どおりに、プロバイダーが構成されているかどうかを判断するのには作成したプロファイルを検査します。
  

