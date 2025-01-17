---
title: クライアント アプリケーションの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4e3aaf8de7726ca75816105fbe81b2019fcaa107
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578453"
---
# <a name="types-of-client-applications"></a>クライアント アプリケーションの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング クライアントには、主に、対人間メッセージ (IPM) を処理するメッセージング クライアントと、プロセス間通信 (IPC) メッセージを処理するメッセージング クライアントの 2 種類があります。 これらの種類の中で、メッセージング クライアント アプリケーションは次のように分類できます。
  
- ユーザー間
    
- ユーザーからコンピューターへのアクセス
    
- コンピューター間
    
- 機械間
    
- 人と機械の組み合わせ
    
ユーザー間アプリケーションには、メッセージの交換を開始するユーザーと、応答する別のユーザーが含まれます。 このカテゴリのアプリケーションには、従来の電子メール アプリケーションと、ドキュメントルーティングや経費承認などのより構造化された交換が含まれます。
  
ユーザー間アプリケーションには、メッセージの交換を開始するユーザーと、応答するコンピューターが含まれます。 このカテゴリには、電子メールを使用してデータベース クエリを送信したり、メーリングリストにサブスクライブするアプリケーションが含まれます。
  
コンピューター間アプリケーションには、メッセージの交換を開始するコンピューターと、応答するユーザーが含まれます。 このカテゴリには、ニュース フィードや意見調査などのドキュメントを配布するアプリケーションが含まれます。
  
コンピューター間アプリケーションには、メッセージの交換を開始するコンピューターと応答するコンピューターが含まれます。 このカテゴリには、リンク ハートビート監視、ディレクトリレプリケーション、データベース レプリケーションなどのアプリケーションが含まれます。
  
最終的なカテゴリは、人とコンピューターの組み合わせで、より複雑なシナリオを伴います。 このカテゴリには、必ずしも送信者と受信者の間でメッセージを送信しないアプリケーションが含まれます。 代わりに、パブリック フォルダーに直接投稿したり、メッセージ ストアでサポートされている Web サイト フォーラムに投稿したりすることもできます。 その後、メッセージは、他の閲覧者、管理者、またはソフトウェア エージェントによってオンデマンドで使用できます。
  
ユーザー間アプリケーション、コンピューター間アプリケーション、またはパブリック フォーラムにメッセージを投稿するアプリケーションを作成する場合は、IPM メッセージを送受信するアプリケーションを設計します。 ユーザー間またはコンピューター間アプリケーションを作成する場合は、IPC メッセージを送受信するように設計できます。 人間のユーザーの操作を必要とするアプリケーションは、IPM メッセージをサポートする必要があります。 さまざまなシナリオでユーザーとコンピューターの両方を含むアプリケーションは、多くの場合、IPM メッセージと IPC メッセージの両方をサポートする必要があります。 2 つのクラスの唯一の本当の違いは、メッセージ ストア内の IPM メッセージがメッセージング クライアントのユーザーに表示されるのに対し、IPC メッセージは通常、クライアント アプリケーション ユーザーには表示されない点です。 
  
MAPI スーパークラス、IPM、IPC によって提供される機能にメッセージを制限するのではなく、新しい IPM または IPC サブクラスを作成することで、これらのクラスをカスタマイズおよび強化できます。 メッセージ サブクラスを作成するには、スーパークラスから継承する新しいメッセージ クラスを作成する必要があります。 たとえば、ユーザー間アプリケーションが顧客関係管理に特化している場合は、IPM を定義して IPM スーパークラスをサブクラス化できます。Contact.Customer クラスと、顧客を記述するプロパティを作成します。 これらのカスタム プロパティのサポートに加えて、IPM を使用します。Contact.Customer メッセージは、すべての IPM メッセージでサポートされているプロパティを継承します。
  

