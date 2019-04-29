---
title: TNEF を使用してメッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7ff7f79b5e74412e9bbb4b4882c6a7d45e50fe6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420851"
---
# <a name="sending-messages-with-tnef"></a>TNEF を使用してメッセージを送信する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのトランスポートプロバイダーは、トランスポートニュートラルカプセル化形式 (TNEF) を使用して、すべての送信メッセージを自動的に送信します。 TNEF は、多くのクライアントやメッセージストアプロバイダーがメッセージでサポートしている書式付きテキスト、さまざまな種類の添付ファイル、およびカスタムメッセージクラスのカスタムプロパティを送信するために使用されます。 ほとんどのトランスポートプロバイダーの既定のモードは TNEF を使用して送信メッセージを送信するものですが、一部のトランスポートプロバイダーではサポートされていません。 TNEF がサポートされていない場合でも、IPM メッセージを送受信する標準のメッセージングクライアントには問題はありません。 ただし、カスタムプロパティを必要とするフォームベースのクライアントまたはクライアントの場合は、TNEF の使用が重要です。 フォームまたはカスタムプロパティに依存するクライアントの設計者は、使用するトランスポートプロバイダーの機能を認識する必要があります。
  
メッセージ受信者は、 **PR_SEND_RICH_INFO**プロパティを設定することで、トランスポートプロバイダーが TNEF でメッセージを送信するかどうかを制御できます。 詳細については、「 **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))」を参照してください。 受信者の**PR_SEND_RICH_INFO**プロパティが TRUE に設定されている場合、TNEF をサポートするトランスポートプロバイダーがメッセージと共にそれを送信します。 このプロパティを FALSE に設定すると、書式設定は破棄されます。 **PR_SEND_RICH_INFO**が存在しない場合は、トランスポートプロバイダーが既定のアクションを選択する必要があります。 
  
クライアントとサービスプロバイダーはカスタム受信者を作成するときに、 _ulflags_パラメーターの**** MAPI_SEND_NO_RICH_INFO フラグを**IAddrBook:: createoneoff** **に渡すことによって、PR_SEND_RICH_INFO プロパティの値に影響を与える可能性があります。imapisupport:: createoneoff**呼び出し。 詳細については、「 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md) 」および「 [imapisupport:: createoneoff](imapisupport-createoneoff.md)」を参照してください。 MAPI_SEND_NO_RICH_INFO を渡すと、MAPI はカスタム受信者の**PR_SEND_RICH_INFO**プロパティを FALSE に設定します。ほとんどの場合、フラグを渡さないと、MAPI によってプロパティが TRUE に設定されます。 1つの例外は、カスタム受信者のアドレスがインターネットアドレスとして解釈される場合です。 この1つの状況では、MAPI は**PR_SEND_RICH_INFO**を FALSE に設定します。 
  

