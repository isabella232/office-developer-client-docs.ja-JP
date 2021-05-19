---
title: TNEF を使用したメッセージの送信
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
# <a name="sending-messages-with-tnef"></a>TNEF を使用したメッセージの送信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのトランスポート プロバイダーは、トランスポート ニュートラル カプセル化形式 (TNEF) を使用してすべての送信メッセージを自動的に送信します。 TNEF は、多くのクライアントとメッセージ ストア プロバイダーがメッセージでサポートする書式設定されたテキスト、さまざまな種類の添付ファイル、カスタム メッセージ クラスのカスタム プロパティを送信するために使用されます。 ほとんどのトランスポート プロバイダーの既定のモードでは、TNEF を使用して送信メッセージを送信しますが、一部のトランスポート プロバイダーではサポートされていません。 TNEF のサポートが不足している場合は、IPM メッセージを送受信する標準的なメッセージング クライアントでは問題ではありません。 ただし、カスタム プロパティを必要とするフォーム ベースのクライアントまたはクライアントでは、TNEF の使用が不可欠です。 フォームまたはカスタム プロパティに依存するクライアントのデザイナーは、使用するトランスポート プロバイダーの機能を認識する必要があります。
  
メッセージ受信者は、トランスポート プロバイダーが TNEF でメッセージを送信するかどうかを制御するには、PR_SEND_RICH_INFOプロパティ **を設定** します。 詳細については、「PR_SEND_RICH_INFO **(** [PidTagSendRichInfo )」を参照してください](pidtagsendrichinfo-canonical-property.md)。 受信者のプロパティPR_SEND_RICH_INFO  TRUE に設定すると、TNEF をサポートするトランスポート プロバイダーがメッセージと一緒に送信します。 プロパティが FALSE に設定されている場合、書式設定は破棄されます。 この **PR_SEND_RICH_INFO** 存在しない場合は、既定のアクション コースを選択する必要があります。 
  
クライアントとサービス プロバイダーがカスタム受信者を作成すると _、ulFlags_ パラメーターの MAPI_SEND_NO_RICH_INFO フラグを **IAddrBook::CreateOneOff** または **IMAPISupport::CreateOneOff** 呼び出しに渡して、PR_SEND_RICH_INFO プロパティの値に影響を与える可能性があります。  詳細については [、「IAddrBook::CreateOneOff」](iaddrbook-createoneoff.md) および [「IMAPISupport::CreateOneOff」を参照してください](imapisupport-createoneoff.md)。 このMAPI_SEND_NO_RICH_INFOすると、MAPI はカスタム受信者のユーザー設定プロパティ **PR_SEND_RICH_INFO** FALSE に設定します。ほとんどの場合、フラグを渡していない場合、MAPI はプロパティを TRUE に設定します。 1 つの例外は、カスタム受信者のアドレスがインターネット アドレスと解釈される場合です。 この 1 つの状況では、MAPI は、エラー **PR_SEND_RICH_INFO** FALSE に設定します。 
  

