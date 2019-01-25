---
title: Outlook MAPI リファレンス概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '最終更新日: 2013 年 2 月 1 日'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723020"
---
# <a name="outlook-mapi-reference-overview"></a>Outlook MAPI リファレンス概要

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、Outlook 2013 MAPI リファレンス ドキュメントに関する概要情報を示します。
  
## <a name="about-this-documentation"></a>このドキュメントについて

このドキュメントは、Microsoft Outlook 2013 のメッセージ API (MAPI) の実装に適用されます。 
  
Microsoft Office Outlook 2007 より前の MAPI プログラマーズ リファレンスは、Microsoft Exchange ドキュメントの一部でした。
  
> [!NOTE]
> Microsoft Exchange Server 2007 以降の Exchange では MAPI の使用が重視されていないため、Exchange 実装のサポートは制限されています。 
  
MAPI の Outlook 実装は、Microsoft Exchange の実装とは異なります。 Outlook の実装は、クライアント コンピューターでの実行に最適化されていて、待機時間の短さが重視されています。 Exchange の実装は、高可用性とマルチスレッド処理の優秀さが重要になるサーバーを対象としています。
  
このドキュメントは、エンド ユーザーのシステムで実行するアプリケーションに使用してください。 サーバー アプリケーションについては、MAPI の Exchange 実装を使用してください (適切な場合)。または、現行の Exchange API (Exchange Web サービスなど) を使用してください。 Exchange Web サービスの詳細については、「[Exchange Web サービスのリファレンス](https://msdn.microsoft.com/library/bb204119.aspx)」を参照してください。
  
MAPI の Outlook 実装または Exchange 実装のどちらでも動作するアプリケーションを作成することは可能です。 たとえば、MFCMAPI はどちらのプラットフォームでも適切に動作します。 実装には多数の共通機能がありますが、明確な相違点と微妙な相違点の両方が存在します。 すべての環境でアプリケーションが動作するようにするには、両方のプラットフォームで十分にテストする必要があります。 このテストには 2 つのシステムが必要になります。これは、同じオペレーティング システムのインストール環境で両方の実装を実行することはサポートされていないためです。
  
MAPI は、MAPI ストア内のデータへのローレベル アクセスや、トランスポート、メッセージストア、アドレス帳プロバイダーの作成に適しています。 MAPI は Outlook のビジネス ロジックをバイパスするため、ソリューションの作成の際に API を評価するときには、Outlook オブジェクト モデルの使用についても検討する必要があります。 Outlook オブジェクト モデルは Outlook ビジネス ロジックをカプセル化しますが、マルチスレッド コード、同期プロバイダー、または Windows サービス アプリケーションには適していません。
  
このエディションの新機能の詳細については、次のトピックを参照してください。
  
- [このエディションの新機能](what-s-new-in-this-edition.md)
    
- [このエディションで非推奨の API 要素](api-elements-deprecated-in-this-edition.md)
    
Outlook 用の MAPI アプリケーションを初めて開発する場合は、次のトピックを参照してください。
  
- [Outlook 2013 用のソリューションを開発するための API またはテクノロジの選択](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [よく使用されるヘッダー ファイル](commonly-used-header-files.md)
    
- [よく使用されるプロパティ](commonly-used-properties.md)
    
- [よく使用されるオブジェクト](commonly-used-objects.md)
    
このリファレンスの残りの部分は、次の 3 種類の情報に分類されています。
  
- [MAPI のサンプル](mapi-samples.md): さまざまな API 要素の使用法と、基本的な MAPI プロバイダーの実装方法および Outlook アイテムの作成方法を示す多数のコード サンプルに誘導します。 
    
- [MAPI の概念](mapi-concepts.md): MAPI の概念とアーキテクチャについて説明します。 
    
- [MAPI リファレンス](mapi-reference.md): MAPI の関数、インターフェイス、構造体、プロパティに関する詳細な情報を示します。 
    
## <a name="see-also"></a>関連項目

- [Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)
- [MAPI のサンプル](mapi-samples.md)
- [MAPI の概念](mapi-concepts.md)

