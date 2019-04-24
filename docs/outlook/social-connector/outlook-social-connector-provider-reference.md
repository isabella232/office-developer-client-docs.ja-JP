---
title: Outlook Social Connector プロバイダーのリファレンス
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 は、個人およびプロフェッショナルコミュニケーションのための通信ハブを提供します。
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359837"
---
# <a name="outlook-social-connector-provider-reference"></a>Outlook Social Connector プロバイダーのリファレンス

Outlook Social Connector 2013 は、個人およびプロフェッショナルコミュニケーションのための通信ハブを提供します。 Outlook Social Connector (.osc) は、sharepoint Server、sharepoint Workspace、Lync クライアント、およびプレゼンス情報をサポートするすべての Office クライアントアプリケーションと連絡先カードが、.osc をサポートしています。 

特に outlook の場合、電子メールや会議出席依頼などの outlook アイテムを選択し、そのアイテムの送信者または受信者をクリックして、outlook を終了せずに、ユーザーは自分の [ユーザー] ウィンドウでこのユーザーのアクティビティ、写真、進捗の更新を閲覧できます。お気に入りのソーシャルネットワーク。 ユーザーは、このユーザーから受信したすべての Outlook メール、添付ファイル、会議を表示することができます。 組織環境では、sharepoint サイト上のユーザーは、sharepoint サイトでこの人物の [ユーザー] ウィンドウのドキュメントの更新やその他のサイトアクティビティにも表示できます。
  
ソーシャルネットワークは、アプリケーションをサポートするためにソーシャルネットワークの更新を同期および表面化するための、.osc のプロバイダーを開発できます。 LinkedIn、Facebook、Windows Live などの一般的なソーシャルネットワークは、.osc のプロバイダーを提供しています。 
  
「Outlook Social Connector 2013 プロバイダリファレンス」では、.osc プロバイダ拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。 
  
Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。 
  
## <a name="in-this-section"></a>このセクションの内容

- 「 [Outlook Social Connector プロバイダーの開発の](getting-started-with-developing-an-outlook-social-connector-provider.md)概要」では、次のような .osc の概要を説明します。 .osc プロバイダーが役に立つ方法、プロバイダーを開発するための簡単な手順、技術要件、ベストプラクティスについて説明します。プロバイダーの開発とこのリリースの新機能
    
- [.osc サンプルテンプレート](osc-sample-templates.md): プロバイダーを開発するためのいくつかの Visual Studio テンプレートについて説明します。
    
- [.osc 一般的な呼び出しシーケンス](osc-typical-calling-sequences.md): .osc プロバイダー機能拡張インターフェイスのメンバーの .osc による、いくつかの一般的な呼び出しシーケンスについて説明します。 これにより、これらのインターフェイスを実装する方法をより深く理解できるようになります。
    
- [.osc xml スキーマを使用してプロバイダーを開発](developing-a-provider-with-the-osc-xml-schema.md)する: .osc プロバイダ拡張インターフェイスと、.osc xml スキーマが、.osc プロバイダーをサポートするように設計されていることを説明します。
    
- [プロバイダーのデバッグ](debugging-a-provider.md): .osc プロバイダーのデバッグに役立ついくつかの方法が提案されています。
    
- [プロバイダーの展開](deploying-a-provider.md): .osc プロバイダーの登録要件について説明し、プロバイダーをインストールするためのチェックリストを示します。
    
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md): .osc プロバイダーを解放する前に実行できるテストを示します。
    
- [Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md): .osc プロバイダ拡張インターフェイスと .osc XML スキーマに関するリファレンス情報を提供し、エラーコードを一覧表示します。
    
## <a name="see-also"></a>関連項目

- [Outlook Social Connector 2013 プロバイダリファレンスの著作権情報](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [ドキュメントの表記規則](https://msdn.microsoft.com/office/aa905365.aspx)   
- [マイクロソフト製品のアクセシビリティ機能](https://www.microsoft.com/enable/products/default.aspx)  
- [Microsoft �v���C�o�V�[�Ɋւ��鐺��](https://privacy.microsoft.com/en-us/privacystatement)
    

