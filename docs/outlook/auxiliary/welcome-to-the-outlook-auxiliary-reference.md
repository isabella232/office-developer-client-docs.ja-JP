---
title: Outlook の補助リファレンスへようこそ
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Outlook の補助リファレンスには、概念的なコンテンツ、Api、コード サンプル、および開発者を拡張し、Outlook との統合に使用できる再配布可能インストーラーの 4 つのセットのリファレンス ドキュメントが含まれています。 このリファレンスの Api は、機能拡張には、Outlook オブジェクト モデルの外部では、Outlook によって公開されます。
ms.openlocfilehash: 5f289a1be8fe5d10ddac37394c940f2627415136
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799591"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Outlook の補助リファレンスへようこそ

Outlook の補助リファレンスには、概念的なコンテンツ、Api、コード サンプル、および開発者を拡張し、Outlook との統合に使用できる再配布可能インストーラーの 4 つのセットのリファレンス ドキュメントが含まれています。 このリファレンスの Api は、機能拡張には、Outlook オブジェクト モデルの外部では、Outlook によって公開されます。 
  
Outlook ソリューションの開発に慣れていない場合は、Api とお客様のニーズに最も適したテクノロジを識別する[、API または Outlook のソリューションを開発するためのテクノロジを選択する](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)を参照してください。 

Outlook オブジェクト モデルの詳細については、 [Outlook の VBA リファレンス](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx)を参照してください。 

固有の情報について Messaging API (MAPI) Outlook でサポートされている[Outlook MAPI のリファレンス](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)を参照してください。

## <a name="conceptual"></a>概念 

概念の説明には、次の項目が含まれています。
  
- [スパム対策の設定について](about-anti-spam-settings.md)
    
- [管理メッセージは、POP3 アカウントのダウンロードします。](managing-message-downloads-for-pop3-accounts.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [カスタムの項目の種類の競合の解決について](about-conflict-resolution-for-custom-item-types.md)
    
- [オフライン アドレス帳の最終更新時刻について](about-the-last-update-time-of-an-offline-address-book.md)
    
- [自動構成の新しいドメインの登録について](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [情報更新および完全な更新としての会議出席依頼について](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [夏時間のプログラムを使用して予定表を再配置について](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)(インストーラーが用意されても、再配布可能なサード ・ パーティの予定表の再配置ツールの以前のバージョンの Outlook にも、Outlook 2010 以降です。 インストーラーをダウンロードするを参照してください[Outlook 2010: 補助型の参照の再頒布可能なインストーラーと再配置の予定表のヘッダー ファイル](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)。)。
    
- [バイナリ プロパティをストリームに永続化の TZDEFINITION について](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>リファレンス

参照コンテンツには次のものが含まれています。
  
- [Api は、Outlook にエクスポート](about-apis-exported-by-outlook.md)するには、関数とデータ構造を内部で使用して実装されていたと一般的な使用は、今すぐが含まれます。 
    
- [アカウント管理 API](about-the-account-management-api.md)は、ユーザー アカウント情報およびアカウントの変更の通知へのアクセスを提供します。 
    
- [データ劣化のレイヤーの API](about-the-data-degradation-layer-api.md)は、オブジェクトのネイティブな文字の書式設定よりも優先される文字書式内の Outlook アイテムにアクセスするクライアントをサポートします。 
    
- [空き/予約済みの API](about-the-free-busy-api.md)は、特定の時間範囲内の特定のユーザー アカウントの空き時間情報のステータス情報を提供します。 

## <a name="sample-tasks"></a>サンプル タスク (英語)

Outlook 補助リファレンスに関する「方法」タスクの例を以下に示します。
    
- [Outlook アイテムが変更されたが、(Outlook の補助参照) が保存されていないかどうかを決定します。](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [TZREG 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [(Outlook の補助参照) を Outlook で連絡先の画像を表示するかどうかを指定します。](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
    
- [空き時間情報データにアクセスする相対時間を使用します。](how-to-use-relative-time-to-access-free-busy-data.md)
    
各 API への参照には、定数、型定義、およびその他の機能を使用する開発者が実装する必要があるインターフェイスが一覧表示されます。
  
> [!NOTE]
> 開発者は、このリファレンスに記載されている場合にのみ、これらの Api を実装する必要があります。 特定のインターフェイスのメンバーとメソッドのパラメーターは、事前の通知なく変更される場合は Outlook の内部使用のために予約されているために、プレース ホルダーとして呼ばれます。 
  
