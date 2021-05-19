---
title: メッセージ送信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421124"
---
# <a name="message-submission-model"></a>メッセージ送信モデル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信は、MAPI スプーラーからトランスポート プロバイダーへの一連の呼び出しによって実行されます。 呼び出しは次のように順序付けされます。
  
1. MAPI スプーラーは [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を呼び出し [、IMessage : IMAPIProp](imessageimapiprop.md) インスタンスを渡してプロセスを開始します。 
    
2. 次に、トランスポート プロバイダーは、SubmitMessage で参照される場所に、このメッセージへの将来の参照で使用されるトランスポート定義の識別子である参照値 **を設定します**。
    
3. トランスポート プロバイダーは、渡された IMessage インスタンスを使用してメッセージ **データにアクセス** します。 渡された **IMessage** の受信者が責任を受け入れるごとに、トランスポート プロバイダーは **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、次に返します。
    
4. トランスポート プロバイダーは [、IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを使用して、配信できない受信者を認識するか、標準の配信レポートを作成することができます。 **StatusRecips** は、受信者の一部を配信できないと判断したトランスポート プロバイダーや、ユーザーまたはクライアント アプリケーションが役に立つ可能性がある基になるメッセージング システムから配信情報を受け取ったトランスポート プロバイダーにとって便利です。 
    
5. [IXPLogon::EndMessage](ixplogon-endmessage.md)への MAPI スプーラーの呼び出しは、MAPI スプーラーからトランスポート プロバイダーへのメッセージの最終的な責任ハンドオフです。 
    
6. MAPI スプーラーは [、IXPLogon::TransportNotify](ixplogon-transportnotify.md) を使用して **、SubmitMessage** 呼び出しまたは **EndMessage** 呼び出し中にメッセージ処理をキャンセルできます。 
    

