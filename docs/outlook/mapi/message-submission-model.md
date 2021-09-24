---
title: メッセージ送信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4862fca03df1f152c757becc7f6c9e56b3e92363
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551059"
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
    

