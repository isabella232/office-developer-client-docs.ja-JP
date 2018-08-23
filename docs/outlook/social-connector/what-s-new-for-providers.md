---
title: プロバイダーの新機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: このトピックでは、Outlook ソーシャル コネクタ 2013 (OSC) での主な変更点を示します。 Outlook ソーシャル コネクタ 2013 と Outlook ソーシャル コネクタ 1.1 の間で利用できる機能の比較を表示します。
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804478"
---
# <a name="whats-new-for-providers"></a>プロバイダーの新機能

このトピックでは、Outlook ソーシャル コネクタ 2013 (OSC) での主な変更点を示します。 Outlook ソーシャル コネクタ 2013 と Outlook ソーシャル コネクタ 1.1 の間で利用できる機能の比較を表示します。 インターフェイスのメンバーと追加、変更、または廃止されている XML 要素についても説明します。 
  
Office 2013 のでは、OSC は、プレゼンス情報と連絡先カードをサポートするクライアント アプリケーションとだけでなく、Outlook も SharePoint サーバー、SharePoint ワークスペース、Lync クライアントでは、他のすべての Office で動作します。 OSC プロバイダー**新**] タブで、Outlook 人物情報ウィンドウ、および連絡先カードのソーシャル情報の更新を公開できます。 
  
Outlook ソーシャル コネクタ 2013 で、いくつかの主な変更点を以下に示します。 
  
- 場合、プロバイダーのアクティビティの表示をサポートしているプロバイダー オン ・ デマンドでの処理を常に同期し、キャッシュ済みのアクティビティでは、不要になった。 プロバイダー メモリに格納友人の活動と友人ではない最新の活動を表示することを意味します。
    
- セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、(ハイパー テキスト転送プロトコル (HTTP) をセキュリティで保護されたソケット レイヤー (SSL)) を HTTPS プロトコルを使用する必要があります。 それ以外の場合、メール ・ アドレス、ソーシャル ネットワーク活動、およびその他のユーザーのデータの傍受または送信中に公開されるというリスクがあります。
    
- Outlook の以前のバージョンで動作しているプロバイダーがあれば、Office 2013 をサポートする必要がありますを更新するセットアップ パッケージです。 詳細については、[インストールのチェックリスト](installation-checklist.md)を参照してください。 
    
次の表は、Outlook ソーシャル コネクタ 1.1 と比較した場合、Outlook ソーシャル コネクタ 2013 でさまざまな機能の可用性を示します。
  
|**機能**|**Outlook Social Connector 2013**|**Outlook ソーシャル コネクタ 1.1**|
|:-----|:-----|:-----|
|エンド ・ ユーザー ・ インタ フェース  <br/> |SharePoint Server、SharePoint ワークスペースでは、Lync クライアント、すべての Office クライアント アプリケーションで連絡先カードおよび outlook 人物情報ウィンドウ  <br/> |Outlook 人物情報ウィンドウ  <br/> |
|基本認証  <br/> |はい  <br/> |はい  <br/> |
|フォームベース認証  <br/> |はい  <br/> |はい  <br/> |
|キャッシュ認証  <br/> |はい  <br/> |はい  <br/> |
|友人を既定の連絡先フォルダーのキャッシュの同期の保存します。  <br/> |はい  <br/> |はい  <br/> |
|**ニュースフィード**の隠しフォルダーを友人のキャッシュされたアクティビティの同期  <br/> |いいえ  <br/> |はい  <br/> |
|オンデマンド同期 (画像、名前、タイトルなど) やネットワーク上の非友人の友人たちは  <br/> |はい  <br/> |はい  <br/> |
|友人やネットワーク上の友人以外のオンデマンド アクティビティ同期  <br/> |はい  <br/> |はい  <br/> |
|ネットワーク上、次  <br/> |はい  <br/> |はい  <br/> |
|ネットワーク上に従っていません  <br/> |はい  <br/> |はい  <br/> |
|ユーザー プロファイル ページを参照してください。  <br/> |リンク経由で  <br/> |ネットワークのバッジを使用して  <br/> |
|(プロファイルとなどを表示できるようにする以外の友人の活動項目の表示など)、ソーシャル ネットワーク上のプライバシーの設定を確認します。  <br/> |はい  <br/> |はい  <br/> |
|ハッシュ化された e メール アドレスがプロバイダーに渡されます  <br/> |はい  <br/> |はい  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>OSC プロバイダーの拡張機能の以前のバージョンからの変更点

追加されたり、対応するインターフェイスでは推奨されませんが、メンバーを次の表に示します。
  
|**インターフェイスとメンバー**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Outlook ソーシャル コネクタ 2013 で廃止されました。 Outlook ソーシャル コネクタ 1.1 以降も**ISocialSession::GetActivities**を推奨されていませんを注意してください。  <br/> アクティビティ フィードの同期を実行するには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装する必要があります。 **True を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示には、 **dynamicActivitiesLookupEx**を設定します。  <br/> |
   
次の表は、変更が加えられたスキーマ要素を示しています。
  
|**スキーマ要素**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Outlook ソーシャル コネクタ 2013 の追加: **allowChangesToAutoConfigure**要素です。  <br/> Outlook ソーシャル コネクタ 2013 では非推奨: **cacheActivities**要素です。  <br/> |
|**人物** <br/> |Outlook ソーシャル コネクタ 2013 の追加: **askmeabout**、 **businessAddress**、 **businessCity**、 **businessCountryOrRegion**、 **businessState**、 **businessZip**、**業界**、**興味のあること**、 **場所**、**かまいません**、 **otherCity**、 **otherCountryOrRegion**、 **otherState**、 **otherZip**、**スキル**、**学校**、および**web サイト**の要素です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)
- [友人の XML](xml-for-friends.md)
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

