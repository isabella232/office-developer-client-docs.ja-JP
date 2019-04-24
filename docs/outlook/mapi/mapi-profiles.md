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
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340083"
---
# <a name="mapi-profiles"></a>MAPI プロファイル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルは、コンピューターにインストールされているサービスプロバイダーとメッセージサービスに関する情報を格納します。 セッションごとに、ログオン時のクライアントは、使用するプロバイダーとサービスを記述する1つのプロファイルを選択します。 クライアントはプロファイルのコレクションから選択でき、必要に応じて既定値として1つを設定します。 既定のプロファイルは、クライアントがセッションを開始し、プロファイルを明示的に指定していないときに自動的に選択されるプロファイルです。
  
また、これらのトピックでは、バイナリストリームに格納されているニックネームキャッシュについての説明も記載されています。
  
- [ニックネーム キャッシュ](nickname-cache.md)
    
- [オートコンプリートストリーム](autocomplete-stream.md)
    
- [バイナリファイルの解析](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>プロファイルセクション

プロファイルは、クライアントとサービスプロバイダーがプロファイルプロパティをユーザーに表示したり、構成を変更したりするためにアクセスするセクションに分かれています。 プロファイルセクションは、 **IProfSect**インターフェイスを実装する MAPI オブジェクトです。このインターフェイスは、 **imapiprop**から派生し、追加のメソッドを持っていません。 詳細については、「 [IProfSect: imapiprop](iprofsectimapiprop.md)」を参照してください。 この唯一の目的は、プロファイルセクションのプロパティを操作することです。 特定のプロファイルセクションへの**IProfSect**ポインターを取得するには、クライアントとサービスプロバイダーは次のメソッドを呼び出します。 
  
|||
|:-----|:-----|
|クライアントは、以下を呼び出すことができます。  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|サービスプロバイダーは、次のものを呼び出すことができます。  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|クライアントまたはプロバイダーは、次のいずれかを呼び出すことができます。  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
プロファイルは、mapisvc.inf のように階層的に編成されます。INF ファイル 階層の最上位には、プロファイルに関連する情報を含むプロファイルセクションがあります。 中間レベルには、特定のメッセージサービスに関する情報を含むセクションが含まれており、下位レベルには、メッセージサービスのサービスプロバイダーの1つに関する情報を含むセクションが含まれています。 
  
すべてのプロファイルには、プロファイルの1つ以上のセクションに格納されている必要なプロパティがいくつかあります。 たとえば、すべてのプロファイルには、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) および**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティがあります。 プロファイルの検索キーは、mapiguid で定義された値に設定されます。H as MUID_PROFILE_INSTANCE として、常にすべてのプロファイルで一意であることが保証されます。 2つのプロファイルは同じ名前を持つことができますが、同じ検索キーを持つことはできません。 検索キーは、特定の種類のデータではなく、バイナリデータとして扱う必要があります。
  
メッセージストアプロバイダーでは、メッセージストアの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティをプロファイルのプロファイルセクションに含める必要があり、メッセージストアプロバイダーには、これらのエントリを同期された状態に保つ必要があります。 メッセージストアが作成されると、プロバイダーはこれらのプロファイルセクションに格納されている値に基づいて**PR_DISPLAY_NAME**を設定します。 
  
プロファイルセクションと、 **imapiprop**から継承するその他のオブジェクトには、次の2つの大きな違いがあります。 
  
- プロファイルセクションは、トランザクションをサポートしていません。
    
- プロファイルセクションは、名前付きプロパティをサポートしておらず、 **imapiprop:: getidsfromnames**および**imapiprop:: GetNamesFromIDs**の実装から MAPI_E_NO_SUPPORT を返します。 詳細については、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)および[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)を参照してください。
    
プロファイルセクションはトランザクションをサポートしていないため、 **imapiprop:: copyprops**、 **CopyTo**、または**setprops**への呼び出しによって加えられた変更は、直ちに有効になります。 詳細については、「 [imapiprop:: copyprops](imapiprop-copyprops.md)」を参照してください。 クライアントおよびサービスプロバイダーは、プロファイルセクションの**imapiprop:: SaveChanges**メソッドを呼び出すことができますが、これは成功しますが、プロファイルセクションのデータには影響しません。 詳細については、「 [imapiprop:: SaveChanges](imapiprop-savechanges.md)」を参照してください。 変更がすぐに発生する場合は、サービスプロバイダーがプロファイルプロパティをユーザーに表示するために使用するプロパティシートを実装する方法に影響を与える可能性があります。 ユーザーが変更を延期または元に戻すことができるようにするサービスプロバイダーは、実際のセクションではなく、プロファイルセクションのコピーを使用して、プロパティシートを実装する必要があります。 コピーを使用すると、ユーザーは変更を加えてから、元のプロファイルセクションを変更しないで、変更を取り消すことができます。 
  
プロファイルに情報が表示される順序によって、MAPI がリソースを構成し、セッションで割り当てが行われる方法が変わります。 プロファイルの順序によって、次の割り当てが影響を受けます。
  
- 既定のメッセージストア
    
- 個人用アドレス帳
    
- 既定のメッセージストア検索パス
    
- 既定のアドレス帳検索パス
    
- トランスポートプロバイダーの順序
    
MAPI では、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに STATUS_DEFAULT_STORE フラグが設定されているプロファイルの最初のメッセージストアとして既定のメッセージストアが設定されます。これは、既定のストアであることを示します。 クライアントは**imapisession:: setdefaultstore**を呼び出すことによって、この設定を上書きすることができます。 詳細については、「 [imapisession:: setdefaultstore](imapisession-setdefaultstore.md)」を参照してください。
  
MAPI は、送信メッセージと受信メッセージを処理するためのトランスポート順序を作成します。 特定の種類のメッセージに対して複数のトランスポートプロバイダーが登録されている場合、MAPI はこの順序を使用して、メッセージを処理する必要があるプロバイダーを決定します。 MAPI は、トランスポートプロバイダーがプロファイルに追加された順序を、1つの例外として設定します。これは、 **PR_RESOURCE_FLAGS**プロパティに STATUS_XP_PREFER_LAST フラグを設定したトランスポートが順に最後に配置されます。 クライアントは、 **IMsgServiceAdmin:: msgservicetransportorder**を呼び出すことで、トランスポート順序を設定できます。 詳細については、「 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)」を参照してください。
  
サービスプロバイダーとメッセージサービスの注文に関するガイドラインは、競合する場合があります。 競合がある場合は、コードで競合を解決する必要があります。 メールコントロールパネルプログラムを使用して、作成したプロファイルを調べ、プロバイダーが期待どおりに構成されているかどうかを判断できます。
  

