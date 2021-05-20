---
title: OSC と Outlook およびソーシャル ネットワークとの関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook ソーシャル コネクタ (OSC) は、同僚、友人、または関連付けられているユーザーの Office 連絡先カードと Outlook ユーザー ウィンドウのアクティビティ、状態、または写真の更新プログラムに表示できます。
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428012"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>OSC と Outlook およびソーシャル ネットワークとの関連付け

Outlook ソーシャル コネクタ (OSC) は、同僚、友人、または関連付けられているユーザーの Office 連絡先カードと Outlook ユーザー ウィンドウのアクティビティ、状態、または写真の更新プログラムに表示できます。 既定では、OSC には、選択Outlook受信したメール、添付ファイル、および会議出席依頼のリストが表示されます。 選択したユーザーとユーザー Officeが SharePoint サイトで共同作業を行う場合、OSC は、そのサイトからのドキュメント更新プログラムや他のサイト アクティビティSharePointします。 Office ユーザーが関心を持つ関連付けのコンテキストに応じて、Office ユーザーは、業務アプリケーション、社内 Web サイト、または LinkedIn、Facebook、および Windows Live などのさまざまなプロフェッショナルおよびソーシャル ネットワーク サイト用の OSC プロバイダーをインストールできます。
  
Office クライアント アプリケーション間での機能の共有をサポートするために、OSC コア エンジンは Office 共有コンポーネントの一部として実装され、People Pane は Outlook アドインとして実装されます。 OSC を使用するには、Office ユーザーがクライアント コンピューターに Outlook をインストールし、プロファイルを使用して Outlook を構成し、OSC が連絡先フォルダーに連絡先をキャッシュできる必要があります。 
  
OSC プロバイダーはコンポーネント オブジェクト モデル (COM) DLL で、各ソーシャル ネットワークの API とは独立した方法で OSC がソーシャル ネットワーク データにアクセスできます。 OSC プロバイダー DLL をクライアント コンピューターにローカルにインストールする必要があります。 ソーシャル ネットワークの OSC プロバイダーは、インターネット上のソーシャル ネットワークOutlookの一部である OSC を接続します。
  
OSC プロバイダーは、OSC プロバイダーの機能拡張の一部として定義された一連のインターフェイスを実装して、OSC と通信する必要があります。 OSC プロバイダーの機能拡張は、オープン プラットフォームとして利用できます。
  
OSC のプロバイダー アーキテクチャを使用すると、複数のプロバイダーが OSC コア エンジンを操作し、友人やアクティビティなどのソーシャル情報を集約できます。 図 1 は、OSC プロバイダーのアーキテクチャを示しています。
  
**図 1.Outlookソーシャル コネクタ プロバイダーのアーキテクチャ**

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>用語

このページOutlook、ソーシャル ネットワークを使用して、次の種類のサイトを参照します。 
  
- コラボレーション サイト (SharePoint)。
    
- Facebook や Live などのソーシャル ネットワーク Windowsサイト。
    
- Professional LinkedIn などのネットワーク サイトを管理します。
    
- ネットワークに使用されるその他の業務用アプリケーションまたは企業の内部 Web サイト。
    
フレンドという用語は、通常、友人、家族、同僚、接続、および Office ユーザーが SharePoint などの共同作業コンテキストに関連付けられている、またはユーザーのソーシャル ネットワーク アカウントに追加された他のユーザーを含めるのに使用されます。 フレンド以外のユーザーは、フレンドのアクティビティ更新プログラムで参照されますが、ユーザーのソーシャル ネットワーク アカウントに追加されたOfficeではありません。 連絡先は、連絡先フォルダー内Outlookユーザーです。 
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

