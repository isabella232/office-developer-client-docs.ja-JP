---
title: プロバイダーの新機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: このトピックでは、ソーシャル コネクタ 2013 (OSC) Outlookの主な変更点を示します。 ソーシャル コネクタ 2013 とソーシャル コネクタ 1.1 のOutlook機能Outlook比較します。
ms.openlocfilehash: a9f8836313ee49e0e3d7fa18ffcf1ee7e2babb75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598963"
---
# <a name="whats-new-for-providers"></a>プロバイダーの新機能

このトピックでは、ソーシャル コネクタ 2013 (OSC) Outlookの主な変更点を示します。 ソーシャル コネクタ 2013 とソーシャル コネクタ 1.1 のOutlook機能Outlook比較します。 また、追加、変更、または廃止されたインターフェイス メンバーと XML 要素について説明します。 
  
Office 2013 では、OSC は Outlook だけでなく、SharePoint Server、SharePoint Workspace、Lync クライアント、およびプレゼンス情報と連絡先カードをサポートする他のすべての Office クライアント アプリケーションでも動作します。 OSC プロバイダーは、ユーザー ウィンドウの **[WHAT'S NEW]** タブと連絡先カードOutlookソーシャル情報の更新を表示できます。 
  
ソーシャル コネクタ 2013 Outlookの主な変更点は次のとおりです。 
  
- プロバイダーがアクティビティの表示をサポートしている場合、プロバイダーは常にオンデマンドでアクティビティを同期し、以前にキャッシュされたアクティビティに依存しなくなりました。 つまり、プロバイダーは、現在のアクティビティを表示するために、友人や友人以外のアクティビティをメモリに格納します。
    
- セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) プロトコルを使用する必要があります。 それ以外の場合、転送中に電子メール アドレス、ソーシャル ネットワークアクティビティ、その他のユーザー データが傍受または公開されるリスクがあります。
    
- 以前のバージョンの Outlook 2013 をサポートするプロバイダーがあるOfficeセットアップ パッケージを更新する必要があります。 詳細については [、「インストール チェックリスト](installation-checklist.md) 」を参照してください。 
    
次の表は、ソーシャル コネクタ 1.1 と比較Outlookソーシャル コネクタ 2013 のさまざまな機能Outlook示しています。
  
|**機能**|**Outlook Social Connector 2013**|**Outlookソーシャル コネクタ 1.1**|
|:-----|:-----|:-----|
|エンド ユーザー インターフェイス  <br/> |SharePointサーバー、SharePoint ワークスペース、Lync クライアント、すべてのクライアント アプリケーションの連絡先カード、Office ユーザー ウィンドウOutlook  <br/> |[ユーザー] ウィンドウ (Outlook  <br/> |
|基本認証  <br/> |はい  <br/> |必要  <br/> |
|フォームベース認証  <br/> |はい  <br/> |必要  <br/> |
|キャッシュ認証  <br/> |はい  <br/> |必要  <br/> |
|既定のストアの連絡先フォルダーへの友人のキャッシュ同期  <br/> |はい  <br/> |必要  <br/> |
|友人のキャッシュされたアクティビティが非表示の **ニュースフィード フォルダーに同期** される  <br/> |いいえ  <br/> |はい  <br/> |
|ネットワーク上の友人や友人以外のオンデマンド同期 (画像、名前、タイトル)  <br/> |はい  <br/> |必要  <br/> |
|ネットワーク上の友人や友人以外のオンデマンド アクティビティの同期  <br/> |はい  <br/> |必要  <br/> |
|ネットワークでフォローする  <br/> |はい  <br/> |必要  <br/> |
|ネットワーク上でフォローしない  <br/> |はい  <br/> |必要  <br/> |
|[ユーザー プロファイル] ページにアクセスする  <br/> |リンク経由  <br/> |ネットワーク バッジ経由  <br/> |
|ソーシャル ネットワークでのプライバシー設定の監視 (たとえば、そのようなユーザーの表示を許可する友人以外のプロファイルとアクティビティの表示)  <br/> |はい  <br/> |必要  <br/> |
|プロバイダーに渡されるハッシュされた電子メール アドレス  <br/> |はい  <br/> |必要  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>OSC プロバイダーの機能拡張の以前のバージョンからの変更

次の表に、対応するインターフェイスから追加または廃止されたメンバーを示します。
  
|**インターフェイスとメンバー**|**コメント**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |ソーシャル コネクタ 2013 Outlookで廃止されました。 **ISocialSession::GetActivities** は、ソーシャル コネクタ 1.1 以降Outlook廃止されています。  <br/> アクティビティ フィードを同期するには [、ISocialSession2::GetActivitiesEx メソッドを実装する必要](isocialsession2-getactivitiesex.md) があります。 **dynamicActivitiesLookupEx** を **true** に設定すると、代わりに **ISocialSession2::GetActivitiesEx** を呼び出すメッセージが OSC に表示されます。  <br/> |
   
次の表に、変更されたスキーマ要素を示します。
  
|**Schema 要素**|**コメント**|
|:-----|:-----|
|**capabilities** <br/> |ソーシャル コネクタ 2013 Outlookで追加: **allowChangesToAutoConfigure** 要素。  <br/> Social Connector 2013 Outlook **cacheActivities 要素では非推奨** です。  <br/> |
|**人** <br/> |Outlook Social Connector 2013 で追加:  **askmeabout**、 **businessAddress**、 **businessCity**、 **businessCountryOrRegion**、 businessState 、 **businessZip**、 industries , interests , **location**, **otherAddress**, otherCity ,  **otherCountryOrRegion**, otherState ,  **otherZip**,**スキル**,**学校,** および **Web** サイト要素。   <br/> |
   
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [友人のための XML](xml-for-friends.md)
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

