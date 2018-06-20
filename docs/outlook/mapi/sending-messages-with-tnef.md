---
title: TNEF メッセージを送信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fb26d854b47894d8f37763b17e5ba0b26fd25ff6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803883"
---
# <a name="sending-messages-with-tnef"></a>TNEF メッセージを送信します。

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーの多くは、すべての送信メッセージと、トランスポート ニュートラル カプセル化形式 (TNEF) を自動的に送信します。 TNEF を使用して、そのメッセージは、さまざまな種類、およびカスタム メッセージ クラス用のカスタム プロパティの添付ファイルで多くのクライアントとメッセージ ストア プロバイダーをサポートしている書式設定されたテキストを送信します。 ほとんどのトランスポート プロバイダーの既定のモードは、TNEF で送信するメッセージを送信するが、トランスポート プロバイダーによってサポートしません。 TNEF のサポートの欠如は、IPM メッセージを送受信するメッセージング クライアントが標準的な問題ではありません。 ただし、フォーム ベースのクライアントまたはユーザー設定のプロパティを必要とするクライアントでは、TNEF の使用が不可欠です。 フォームまたはユーザー設定のプロパティに依存するクライアントの設計者は、それらを使用するトランスポート プロバイダーの機能に注意してくださいする必要があります。
  
メッセージの受信者は、 **PR_SEND_RICH_INFO**プロパティを設定することによって、トランスポート プロバイダーが TNEF メッセージを送信するかどうかを制御できます。 詳細については、 **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) を参照してください。 受信者の**PR_SEND_RICH_INFO**プロパティを TRUE に設定すると、TNEF をサポートするトランスポート プロバイダーは、メッセージに送信します。 プロパティを FALSE に設定するとと、には、書式設定は破棄されます。 **PR_SEND_RICH_INFO**が存在しない場合は、トランスポート プロバイダーは、既定の一連のアクションを選択する責任です。 
  
_UlFlags_パラメーターで**IAddrBook::CreateOneOff**または**に MAPI_SEND_NO_RICH_INFO フラグを渡すことによって、 **PR_SEND_RICH_INFO**プロパティの値を持ちますクライアントおよびサービス ・ プロバイダーは、カスタム受信者を作成するときIMAPISupport::CreateOneOff**を呼び出します。 詳細については、 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)および[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を参照してください。 渡される MAPI_SEND_NO_RICH_INFO と、MAPI は、カスタム受信者の**PR_SEND_RICH_INFO**プロパティを FALSE に設定します。ほとんどの場合は、フラグが渡されていないと、MAPI プロパティを TRUE に設定します。 1 つの例外は、インターネット アドレスを使用するかどうか、カスタム受信者のアドレスが解釈されます。 この 1 つの状況では、MAPI は、false を指定する**PR_SEND_RICH_INFO**を設定します。 
  

