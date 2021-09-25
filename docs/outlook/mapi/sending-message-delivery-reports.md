---
title: メッセージ配信レポートの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ef949db447aee54f0e007e1ddbbf104ea2451ef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609440"
---
# <a name="sending-message-delivery-reports"></a>メッセージ配信レポートの送信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部の基になるメッセージング システムは配信レポートをサポートし、一部はサポートしない場合があります。 トランスポート プロバイダーが、メッセージ配信レポートまたは配信以外のレポートをクライアント アプリケーションに送信できるかどうかを決定する方法は、個々のトランスポート プロバイダーに固有の実装の詳細です。 配信レポートをクライアント アプリケーションに送信できる場合、トランスポート プロバイダーは [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを使用して、1 つ以上の受信者の配信が成功または失敗したと MAPI に通知します。 MAPI は、それらの受信者に対応する配信レポートまたは配信以外のレポートを生成します。 トランスポート プロバイダーは **、StatusRecips** を使用して、メッセージング システムにネイティブな受信配信レポートと配信不能レポートを MAPI 配信レポートと配信不能レポートに変換することもできます。
  

