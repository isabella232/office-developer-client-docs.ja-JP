---
title: SMTP ゲートウェイおよびトランスポートでの TNEF 関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578536"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>SMTP ゲートウェイおよびトランスポートでの TNEF 関連付け

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ゲートウェイとインターネットに接続するためのトランスポートは、システムでは、SMTP を使用して、TNEF の相関関係を実装するために SMTP のメッセージ Id ヘッダーと、 **PR_TNEF_CORRELATION_KEY**プロパティの値を使用しているものに基づいています。 
  
送信メッセージのメッセージ Id ヘッダーの値は、 **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) のプロパティにコピーし、TNEF ストリームの[attMAPIProps](attmapiprops.md)属性内にエンコードする必要があります。 **PR_TNEF_CORRELATION_KEY**は、バイナリのプロパティにあるときにメッセージ Id 文字列。null 終端文字は、コピーでは比較に含まれているはずです。 
  
この手法は、MAPI ベースのメッセージング システムを Microsoft Exchange Server などのインターネットに接続するすべての Microsoft ソフトウェアによって使用されます。 この方法は、任意の SMTP ゲートウェイとの相互運用性を最大化するために MAPI クライアントをサポートしているシステムに接続するためのトランスポートで使用する必要があります。
  

