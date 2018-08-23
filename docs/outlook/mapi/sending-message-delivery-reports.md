---
title: メッセージ配信レポートの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803868"
---
# <a name="sending-message-delivery-reports"></a>メッセージ配信レポートの送信

  
  
**適用対象**: Outlook 
  
いくつかの基になるメッセージング システムが配信レポートをサポートし、ないものです。 トランスポート プロバイダーがクライアント アプリケーションにメッセージの配信または配信不能レポートを送信できるかどうかを決定する方法は、個々 のトランスポート プロバイダーに固有の実装の詳細です。 配信レポートは、クライアント アプリケーションに送信できる、トランスポート プロバイダーは 1 つまたは複数の受信者に対する配信の成功または失敗の MAPI を通知するために[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用します。 MAPI では、配信または配信不能レポートが受信者に対応するが生成されます。 トランスポート プロバイダーは、 **StatusRecips**を使用して、MAPI 配信には、メッセージング システムにネイティブな受信の配信と配信不能レポートと配信不能レポートを変換できるも。
  

