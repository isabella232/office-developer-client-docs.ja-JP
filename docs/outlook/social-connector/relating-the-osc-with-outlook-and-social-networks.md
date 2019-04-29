---
title: OSC と Outlook およびソーシャル ネットワークとの関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: outlook Social Connector (.osc) は、同僚、友人、または関連付けられている個人の Office 連絡先カードと outlook のユーザーウィンドウの活動、状態、または写真の更新を表示することができます。
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428012"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>OSC と Outlook およびソーシャル ネットワークとの関連付け

outlook Social Connector (.osc) は、同僚、友人、または関連付けられている個人の Office 連絡先カードと outlook のユーザーウィンドウの活動、状態、または写真の更新を表示することができます。 既定では、このメッセージには、選択したユーザーから受信した Outlook メール、添付ファイル、会議出席依頼が表示されます。 選択したユーザーと Office ユーザーが sharepoint サイトで共同作業を行うと、その sharepoint サイトからのドキュメント更新やその他のサイトアクティビティも表示されます。 office ユーザーは、office ユーザーが関心を持っている関連付けのコンテキストに応じて、基幹業務アプリケーション、社内の web サイト、または LinkedIn などのさまざまな professional およびソーシャルネットワークサイトに対して、.osc プロバイダーをインストールすることができます。Facebook、Windows Live。
  
office クライアントアプリケーション間での機能の共有をサポートするために、.osc コアエンジンは office 共有コンポーネントの一部として実装され、People ウィンドウは Outlook アドインとして実装されます。 .osc を使用するには、Office ユーザーがそのクライアントコンピューターに outlook をインストールし、outlook をプロファイルを使用して構成している必要があります。このため、.osc は連絡先フォルダー内の連絡先をキャッシュできます。 
  
.osc プロバイダーは、コンポーネントオブジェクトモデル (COM) DLL で、各ソーシャルネットワークの api とは無関係に、.osc がソーシャルネットワークデータにアクセスできるようにします。 .osc プロバイダ DLL は、クライアントコンピューターにローカルにインストールする必要があります。 ソーシャルネットワークの .osc プロバイダーは、Outlook の一部である .osc をインターネット上のソーシャルネットワークに接続します。
  
.osc プロバイダーは、.osc と通信するために、.osc プロバイダー拡張機能の一部として定義された一連のインターフェイスを実装する必要があります。 .osc プロバイダ拡張機能は、オープンプラットフォームとして使用できます。
  
.osc のプロバイダアーキテクチャを使用すると、複数のプロバイダーが .osc コアエンジンと、フレンドやアクティビティなどのソーシャル情報を集約して動作するようになります。 図1は、.osc プロバイダアーキテクチャを示しています。
  
**図1。Outlook Social Connector プロバイダーのアーキテクチャ**

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>用語

この Outlook social Connector プロバイダーリファレンスでは、ソーシャルネットワークを使用して、次の種類のサイトを参照します。 
  
- SharePoint などのコラボレーションサイト。
    
- Facebook や Windows Live などのソーシャルネットワークサイト。
    
- LinkedIn などのプロフェッショナルネットワークサイト。
    
- ネットワークに使用されるその他の基幹業務アプリケーションまたは企業内部 web サイト。
    
friend という用語は、一般に、友人、家族、同僚、接続、および Office ユーザーが SharePoint などのコラボレーションコンテキストで関連付けられている場合や、ユーザーのソーシャルネットワークアカウントに追加されている場合に使用されます。 友人以外のユーザーは、友人のアクティビティの更新で参照されていますが、Office ユーザーのソーシャルネットワークアカウントに追加されている友人ではありません。 連絡先は、Outlook の連絡先フォルダー内のユーザーです。 
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

