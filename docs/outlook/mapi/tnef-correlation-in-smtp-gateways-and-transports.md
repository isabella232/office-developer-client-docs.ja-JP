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
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804113"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>SMTP ゲートウェイおよびトランスポートでの TNEF 関連付け

  
  
**適用対象**: Outlook 
  
ゲートウェイとインターネットに接続するためのトランスポートは、システムでは、SMTP を使用して、TNEF の相関関係を実装するために SMTP のメッセージ Id ヘッダーと、 **PR_TNEF_CORRELATION_KEY**プロパティの値を使用しているものに基づいています。 
  
送信メッセージのメッセージ Id ヘッダーの値は、 **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) のプロパティにコピーし、TNEF ストリームの[attMAPIProps](attmapiprops.md)属性内にエンコードする必要があります。 **PR_TNEF_CORRELATION_KEY**は、バイナリのプロパティにあるときにメッセージ Id 文字列。null 終端文字は、コピーでは比較に含まれているはずです。 
  
この手法は、MAPI ベースのメッセージング システムを Microsoft Exchange Server などのインターネットに接続するすべての Microsoft ソフトウェアによって使用されます。 この方法は、任意の SMTP ゲートウェイとの相互運用性を最大化するために MAPI クライアントをサポートしているシステムに接続するためのトランスポートで使用する必要があります。
  

