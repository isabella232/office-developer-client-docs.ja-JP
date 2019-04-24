---
title: Outlook 補助リファレンスへようこそ
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: outlook の補助リファレンスには、4つの api セットの概念に関するコンテンツと参照ドキュメント、コードサンプル、および開発者が Outlook を拡張して統合できるようにする再頒布可能なインストーラーが含まれています。 このリファレンスの api は、outlook オブジェクトモデルの外部にある拡張機能のために outlook によって公開されます。
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328984"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Outlook 補助リファレンスへようこそ

outlook の補助リファレンスには、4つの api セットの概念に関するコンテンツと参照ドキュメント、コードサンプル、および開発者が Outlook を拡張して統合できるようにする再頒布可能なインストーラーが含まれています。 このリファレンスの api は、outlook オブジェクトモデルの外部にある拡張機能のために outlook によって公開されます。 
  
Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。 

outlook オブジェクトモデルの詳細については、「 [outlook VBA リファレンス](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx)」を参照してください。 

outlook でサポートされているメッセージング API (MAPI) の詳細については、「 [outlook mapi リファレンス](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)」を参照してください。

## <a name="conceptual"></a>概要 

概念に関する説明には、次の情報が含まれます。
  
- [スパム対策の設定について](about-anti-spam-settings.md)
    
- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)
    
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [ユーザー設定アイテム タイプの競合解決について](about-conflict-resolution-for-custom-item-types.md)
    
- [オフラインアドレス帳の最終更新時刻について](about-the-last-update-time-of-an-offline-address-book.md)
    
- [自動構成のための新しいドメインの登録について](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [情報更新および完全な更新としての会議出席依頼について](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [夏時間でプログラムによって予定表を再配置することについて](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)(outlook 2010 以降では、以前のバージョンの outlook にも対応していますが、サードパーティの予定表の再配置ツール用の再頒布可能なインストーラーもあります。 インストーラーをダウンロードするには、「 [Outlook 2010: 補助的な参照の再配置可能インストーラーと、予定表を再配置するためのヘッダーファイル](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)」を参照してください。
    
- [バイナリ プロパティをストリームに永続化の TZDEFINITION について](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>リファレンス

参照コンテンツには、以下が含まれます。
  
- [Outlook によってエクスポート](about-apis-exported-by-outlook.md)される api には、内部使用のために最初に実装された関数とデータ構造が含まれるようになり、一般に公開されるようになりました。 
    
- [アカウント管理 API](about-the-account-management-api.md)は、アカウントの変更に関するユーザーアカウント情報と通知へのアクセスを提供します。 
    
- [データ低下層 API](about-the-data-degradation-layer-api.md)は、Outlook アイテムに対して、オブジェクトのネイティブ文字形式ではなく、優先する文字形式でアクセスするクライアントをサポートします。 
    
- 空き時間情報[API](about-the-free-busy-api.md)は、特定の時間範囲内の特定のユーザーアカウントに関する空き時間情報の状態情報を提供します。 

## <a name="sample-tasks"></a>サンプル タスク

Outlook の補助リファレンスのサンプルの操作方法は次のとおりです。
    
- [Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)
    
各 API のリファレンスには、追加機能を使用するために開発者が実装する必要がある定数、型定義、およびインターフェイスが記載されています。
  
> [!NOTE]
> 開発者は、このリファレンスで説明されているとおりに、これらの api を実装する必要があります。 特定のインターフェイスメンバーおよびメソッドパラメーターは、Outlook の内部使用のために予約されており、予告なしに変更される可能性があるため、プレースホルダーとして名前が付けられます。 
  

