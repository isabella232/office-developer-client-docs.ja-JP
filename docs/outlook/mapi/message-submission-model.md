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
  
メッセージの送信は、MAPI スプーラーからトランスポートプロバイダーへの一連の呼び出しによって行われます。 呼び出しは次のように順序付けられます。
  
1. MAPI スプーラーは[IXPLogon:: submitmessage](ixplogon-submitmessage.md)を呼び出して、 [IMessage: imapiprop](imessageimapiprop.md)インスタンスを渡し、プロセスを開始します。 
    
2. その後、トランスポートプロバイダーは、" **submitmessage**" で参照されている場所で、参照値 (このメッセージへの今後の参照で使用されるトランスポート定義識別子) を配置します。
    
3. トランスポートプロバイダーは、渡された**IMessage**インスタンスを使用して、メッセージデータにアクセスします。 渡される**IMessage**の各受信者について、トランスポートプロバイダーは**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、を返します。
    
4. トランスポートプロバイダーは、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、配信できない受信者を認識するか、または標準的な配信レポートを作成するかを指定できます。 **StatusRecips**は、一部の受信者が配信できないこと、またはユーザーまたはクライアントアプリケーションが基盤としているメッセージングシステムからの配信情報を受信したことが確認されたトランスポートプロバイダーの便宜的な方法です。役に立つでしょう。 
    
5. mapi スプーラーの[IXPLogon:: endmessage](ixplogon-endmessage.md)への呼び出しは、mapi スプーラーからトランスポートプロバイダーへのメッセージの最終責任です。 
    
6. MAPI スプーラーは、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)を使用して、 **submitmessage**または**endmessage**呼び出し中のメッセージ処理をキャンセルできます。 
    

