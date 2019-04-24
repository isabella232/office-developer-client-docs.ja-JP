---
title: プロバイダーの新機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: このトピックでは、Outlook Social Connector 2013 (.osc) の主な変更点を示します。 outlook social connector 2013 と outlook social connector 1.1 の間で利用できる機能の比較を示します。
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329114"
---
# <a name="whats-new-for-providers"></a>プロバイダーの新機能

このトピックでは、Outlook Social Connector 2013 (.osc) の主な変更点を示します。 outlook social connector 2013 と outlook social connector 1.1 の間で利用できる機能の比較を示します。 また、追加、変更、または廃止されたインターフェイスメンバーと XML 要素についても説明します。 
  
Office 2013 では、.osc は Outlook だけでなく、sharepoint Server、sharepoint Workspace、Lync クライアント、およびプレゼンス情報および連絡先カードをサポートする他のすべての Office クライアントアプリケーションでも機能します。 .osc プロバイダーは、連絡先カードだけでなく、Outlook People ウィンドウの [**新機能**] タブでソーシャル情報の更新を表示できます。 
  
Outlook Social Connector 2013 には、次のようないくつかの大きな変更が加えられています。 
  
- プロバイダーがアクティビティの表示をサポートしている場合、プロバイダーは常に、必要に応じてアクティビティを同期し、以前にキャッシュされたアクティビティに依存しなくなります。 そのため、プロバイダーは、より多くの現在のアクティビティを表示するために、フレンドと非友人のアクティビティをメモリに格納します。
    
- セキュリティ上の理由から、インターネットを介してサーバーと通信するプロバイダーは HTTPS (ハイパーテキスト転送プロトコル (HTTP) with Secure Socket Layer (SSL) プロトコル) を使用する必要があります。 そうしないと、送信中に電子メールアドレス、ソーシャルネットワークアクティビティ、およびその他のユーザーデータが傍受または公開されるリスクがあります。
    
- 以前のバージョンの Outlook で動作するプロバイダーが Office 2013 をサポートするには、セットアップパッケージを更新する必要があります。 詳細については、「[インストールチェックリスト](installation-checklist.md)」を参照してください。 
    
次の表は、outlook social connector 1.1 と比較した場合の outlook social connector 2013 のさまざまな機能の利用可能性を示しています。
  
|**機能**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|エンドユーザーインターフェイス  <br/> |sharepoint Server、sharepoint Workspace、Lync クライアント、すべての Office クライアントアプリケーションの連絡先カード、Outlook の [ユーザー] ウィンドウ  <br/> |Outlook の [ユーザー] ウィンドウ  <br/> |
|基本認証  <br/> |はい  <br/> |はい  <br/> |
|フォームベース認証  <br/> |はい  <br/> |はい  <br/> |
|キャッシュされた認証  <br/> |はい  <br/> |はい  <br/> |
|既定のストアにある friends の連絡先フォルダーへのキャッシュ同期  <br/> |はい  <br/> |はい  <br/> |
|友人が非表示の**ニュースフィード**フォルダーに対して同期するキャッシュされたアクティビティ  <br/> |いいえ  <br/> |はい  <br/> |
|ネットワーク上の友人および友人以外のオンデマンド同期 (画像、名前、タイトル)  <br/> |はい  <br/> |はい  <br/> |
|ネットワーク上の友人および友人以外のオンデマンドアクティビティの同期  <br/> |はい  <br/> |はい  <br/> |
|ネットワークでフォローする  <br/> |はい  <br/> |はい  <br/> |
|ネットワークでフォローしない  <br/> |はい  <br/> |はい  <br/> |
|ユーザープロファイルページにアクセスする  <br/> |リンク経由  <br/> |ネットワークバッジ経由  <br/> |
|ソーシャルネットワークのプライバシー設定を監視する (たとえば、プロファイルの表示と、そのような表示を許可する友人以外のアクティビティを表示する)  <br/> |はい  <br/> |はい  <br/> |
|プロバイダーに渡されるハッシュ化された電子メールアドレス  <br/> |はい  <br/> |はい  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>.osc プロバイダー拡張機能の前のバージョンからの変更点

次の表に、対応するインターフェイスで追加または廃止されたメンバーを示します。
  
|**インターフェイスとメンバー**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Outlook Social Connector 2013 では廃止されました。 isocial **alsession:: getactivities**は、Outlook Social Connector 1.1 以降も使用されていないことに注意してください。  <br/> アクティビティフィードを同期するには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装する必要があります。 **dynamicActivitiesLookupEx**を**true**に設定して、 **ISocialSession2:: GetActivitiesEx**を呼び出すよう、.osc に指示します。  <br/> |
   
次の表に、変更されたスキーマ要素を示します。
  
|**Schema 要素**|**Comment**|
|:-----|:-----|
|**能力** <br/> |Outlook Social Connector 2013: **allowChangesToAutoConfigure**要素に追加されました。  <br/> Outlook Social Connector 2013: **cacheactivities**要素で廃止されました。  <br/> |
|**人物** <br/> |Outlook Social Connector 2013 に追加されました。 **: askmeabout**、 **businessaddress**、 **businessaddress**、 **businessCountryOrRegion**、 **businessaddress**、 **businessaddress**、**産業**、**興味**、 **location**、 **otheraddress**、 **otheraddress**、 **otherCountryOrRegion**、 **otheraddress**、 **otheraddress**、**スキル**、**学校**、 **web サイト**の各要素。  <br/> |
   
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [Friends の XML](xml-for-friends.md)
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

