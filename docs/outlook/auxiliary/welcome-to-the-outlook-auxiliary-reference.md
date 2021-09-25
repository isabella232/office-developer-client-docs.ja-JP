---
title: 外部補助Outlookへようこそ
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Outlook補助リファレンスには、4 組の API、コード サンプル、および再頒布可能なインストーラーの概念的なコンテンツとリファレンス ドキュメントが含まれています。開発者は Outlook と拡張して統合できます。 この参照の API は、Outlookモデルの外部で、機能拡張Outlook公開されます。
ms.openlocfilehash: 478dbf3057972b01a453d2dda105135c25517607
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564491"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>外部補助Outlookへようこそ

Outlook補助リファレンスには、4 組の API、コード サンプル、および再頒布可能なインストーラーの概念的なコンテンツとリファレンス ドキュメントが含まれています。開発者は Outlook と拡張して統合できます。 この参照の API は、Outlookモデルの外部で、機能拡張Outlook公開されます。 
  
Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。 

オブジェクト モデルの詳細についてはOutlook VBA リファレンスOutlook[参照してください](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx)。 

ユーザーがサポートするメッセージング API (MAPI) の詳細についてはOutlook MAPI リファレンスOutlook[参照してください](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)。

## <a name="conceptual"></a>概念 

概念的な議論には、次のテーマが含まれます。
  
- [スパム対策の設定について](about-anti-spam-settings.md)
    
- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [ユーザー設定アイテム タイプの競合解決について](about-conflict-resolution-for-custom-item-types.md)
    
- [オフライン アドレス帳の最終更新時刻について](about-the-last-update-time-of-an-offline-address-book.md)
    
- [自動構成のための新しいドメインの登録について](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [情報更新および完全な更新としての会議出席依頼について](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [夏時間](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)に合わせてカレンダーをプログラムで再調整する方法について (Outlook 2010 以降、以前のバージョンの Outlook でも動作するサードパーティの予定表の再分散ツール用の再配布可能なインストーラーもあります。 インストーラーをダウンロードするには[、「Outlook 2010:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)補助参照再頒布可能インストーラーと予定表の再分散用ヘッダー ファイル」を参照してください。
    
- [バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>参照

参照コンテンツには、次の内容が含まれます。
  
- この[API は、Outlook](about-apis-exported-by-outlook.md)に実装され、パブリックに使用するために公開されている関数とデータ構造を含む必要があります。 
    
- アカウント [管理 API は、](about-the-account-management-api.md) ユーザー アカウント情報へのアクセスとアカウント変更の通知を提供します。 
    
- データ[低下層 API](about-the-data-degradation-layer-api.md)は、オブジェクトのネイティブ文字形式Outlook優先文字形式でアイテムにアクセスするクライアントをサポートします。 
    
- 空 [き時間情報 API は](about-the-free-busy-api.md) 、特定の時間範囲内の特定のユーザー アカウントに関する空き時間情報を提供します。 

## <a name="sample-tasks"></a>サンプル タスク

「補助リファレンス」のサンプルのOutlookを次に示します。
    
- [Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)
    
各 API の参照には、追加の機能を使用するために開発者が実装する必要がある定数、型定義、およびインターフェイスが一覧表示されます。
  
> [!NOTE]
> 開発者は、この参照に記載されている API のみを実装する必要があります。 特定のインターフェイス メンバーとメソッド パラメーターは、Outlook の内部使用のために予約され、予告なしに変更される可能性があるため、プレースホルダーとして名前が付けされます。 
  

