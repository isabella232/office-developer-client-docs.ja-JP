---
title: Outlook とソーシャル ネットワークの OSC の関連
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook ソーシャル コネクタ (OSC) は、同僚、友人、またはすべてのユーザーに関連付けられている場合の Office の連絡先カードおよび Outlook 人物情報ウィンドウのアクティビティ、状態、または写真の更新プログラムで表示できます。
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804462"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Outlook とソーシャル ネットワークの OSC の関連

Outlook ソーシャル コネクタ (OSC) は、同僚、友人、またはすべてのユーザーに関連付けられている場合の Office の連絡先カードおよび Outlook 人物情報ウィンドウのアクティビティ、状態、または写真の更新プログラムで表示できます。 既定では、OSC が Outlook の電子メールの添付ファイルを表示し、選択したユーザーから受信した会議出席依頼します。 選択したユーザーと Office ユーザーは、SharePoint サイトの共同作業する場合、OSC も、ドキュメントの更新とその SharePoint サイトから他のサイトのアクティビティが表示されます。 Office ユーザーが基幹業務アプリケーション、企業の内部の web サイトまたは LinkedIn などの本格的なソーシャル ネットワーク サイトのさまざまな OSC プロバイダーのインストール時に、Office ユーザーに興味を示している関連のコンテキストに応じてFacebook、および Windows Live をします。
  
Office クライアント アプリケーション間での機能の共有をサポートする OSC の中核となるエンジンは、Office の共有コンポーネントの一部として実装し、人物情報ウィンドウは、Outlook のアドインとして実装されます。 OSC を使用するには、Office ユーザーは、クライアント コンピューターに Outlook がインストールされているし、OSC は、連絡先フォルダーに連絡先をキャッシュできるように、プロファイルを使用して Outlook を構成します。 
  
OSC プロバイダーでは、コンポーネント オブジェクト モデル (COM) DLL の各ソーシャル ネットワークの Api に依存しない方法でデータをソーシャル ネットワークにアクセスする OSC を可能にします。 OSC プロバイダー DLL は、クライアント コンピューターにローカルにインストールする必要があります。 ソーシャル ネットワークの OSC プロバイダーは、インターネット上のソーシャル ネットワークでの OSC は、Outlook の一部を接続します。
  
OSC プロバイダーは、OSC と通信するのには、OSC のプロバイダーの機能拡張の一部として定義されているインターフェイスのセットを実装しなければなりません。 OSC プロバイダーの拡張機能は、オープン ・ プラットフォームとして使用できます。
  
OSC のプロバイダーのアーキテクチャは、OSC の中核となるエンジンと友人や活動などの集計のソーシャル情報を処理する複数のプロバイダーを有効にします。 OSC プロバイダーのアーキテクチャを図 1 に示します。
  
**図 1 です。Outlook ソーシャル コネクタ プロバイダー アーキテクチャ**

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>用語

この Outlook ソーシャル コネクタ プロバイダー リファレンスで、ソーシャル ネットワークを使用して、次の種類のサイトを参照してください。 
  
- SharePoint などのコラボレーション サイトです。
    
- Facebook や Windows Live などのソーシャル ネットワーク サイトです。
    
- LinkedIn などのプロのネットワーク サイトです。
    
- 他の基幹業務アプリケーションや企業の内部 web サイトがネットワークで利用できます。
    
用語の友人は、友人、家族、仕事仲間、接続、および他のユーザーが、Office ユーザーは、SharePoint のような共同作業のコンテキストに関連付けられてまたは、ユーザーのソーシャル ネットワークのアカウントに追加するのには一般的に使用されます。 非友人は、友人のアクティビティの更新プログラムで参照されているユーザーが Office ユーザーのソーシャル ネットワークのアカウントに追加されている友人。 連絡先は、Outlook の連絡先フォルダー内のユーザーです。 
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

