---
title: MAPI 機能の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4f1e4e09b6e1b200a8930ae7df7781a8e449539b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567222"
---
# <a name="mapi-feature-overview"></a>MAPI 機能の概要
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI にはいくつかの重要な機能があり、開発者がシームレスに異なるメッセージング システムを使用して作業し、使用するための一貫性のある方法を提供できます。 これらの機能には、包括的でオープンなプログラミング インターフェイス、業界標準のサポートが含まれます。 
  
MAPI はオープン プログラミング インターフェイスなので、一般的な方法でサービスを提供し、ユーザーは現在および将来必要なカスタマイズを追加できます。 MAPI プログラミング インターフェイスは、ドキュメントのみを送信する機能が必要なワードプロセス アプリケーションや、さまざまな種類のデータを共有して保存する機能が必要なワークグループ アプリケーションなど、多様なメッセージングニーズを持つクライアント アプリケーションの要件を満たします。 実際、特定の形式で情報を交換または保存する必要があるアプリケーションは、MAPI プログラミング インターフェイスの利点を利用できます。 どのサービス プロバイダーも、インターフェイスを使用してメッセージング システムの固有の機能を公開し、アプリケーション ユーザーに最もメリットを提供する機能を選択できます。
  
MAPI は、フロントエンド メッセージング クライアント アプリケーションで使用されるプログラミング インターフェイスと、バック エンド サービス プロバイダーが使用するプログラミング インターフェイスを分離します。 クライアント インターフェイスをサービス プロバイダーから分離すると、1 つのアプリケーションで複数のメッセージング システムと複数のアプリケーションを使用して、1 つのサービス プロバイダーを使用できます。 すべてのコンポーネントは、一般的な Microsoft Windowsベースのユーザー インターフェイスで動作します。 これはユーザーにとって大きな利点です。 ユーザーは、一度にニーズに応じてさまざまなシステムから選択でき、選択した各システムと一貫して動作し、特定のメッセージング システムから真の独立性を提供できます。 
  
たとえば、1 つのメッセージング クライアント アプリケーションが FAX、ボイス メール、RSS フィードからメッセージを受信できます。 これらのすべてのシステムからのメッセージは、到着時に 1 つの場所 (ユニバーサル受信トレイ) に配置できます。 これらのシステムを 1 つのアプリケーションで処理すると、開発、ユーザー トレーニング、およびシステム管理のコストが削減されます。 
  
クライアント インターフェイスをプロバイダー インターフェイスから分離すると、メッセージング システムによってアプリケーションに配置されるプログラミングの依存関係が削除され、その逆も削除されます。 クライアント アプリケーションとサービス プロバイダーの開発者は、アプリケーション固有の機能やメッセージング システム固有の機能の多様なセットではなく、MAPI 機能の標準セットにコードを書き込みます。 開発者は、コンポーネントがクライアントプロバイダーかサービス プロバイダーかに焦点を当て、MAPI が残りの部分を処理し、開発時間とコストを削減します。
  
MAPI プログラミング インターフェイスは、一連の包括的な機能を提供します。 MAPI は、FAX、DEC All-In-1、ボイス メール、および AT&T Easylink Services、CompuServe、MCI MAIL などのパブリック コミュニケーション サービスなど、さまざまなメッセージング システムと通信するワークグループ アプリケーションの強力な新しい市場を目指しています。 MAPI インターフェイスを使用すると、サービス プロバイダーをこれらのすべてのシステムで使用できます。 
  
MAPI に準拠したオブジェクトは、コンポーネント オブジェクト モデル (COM) オブジェクトに似ています。 COM オブジェクトは、1 つ以上のインターフェイスに属する一連のメソッド、または COM でのオブジェクトの動作と動作を定義する関連関数のコレクションを実装します。 ユーザーは、これらのインターフェイスへのポインターを介して COM オブジェクトにのみアクセスします。
  
MAPI は、SMTP や X.400 などの業界標準を介してクロスプラットフォーム サポートを提供します。 MAPI アプリケーションは、Windows 7、Windows Vista、Windows Server 2008、Windows Server 2003、および Windows XP で実行できます。 
  
## <a name="see-also"></a>関連項目

- [MAPI の機能とアーキテクチャ](mapi-features-and-architecture.md)

