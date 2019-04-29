---
title: メッセージ配信レポートの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433081"
---
# <a name="sending-message-delivery-reports"></a>メッセージ配信レポートの送信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
いくつかの基礎となるメッセージングシステムは、配信レポートをサポートしています。 トランスポートプロバイダーが、メッセージ配信または配信不能レポートをクライアントアプリケーションに送信できるかどうかを判断する方法は、個々のトランスポートプロバイダーに固有の実装の詳細です。 配信レポートをクライアントアプリケーションに送信できる場合、トランスポートプロバイダーは[imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、1人以上の受信者に対して成功した、または失敗した配信を MAPI に通知します。 その後、MAPI は、これらの受信者に対応する配信レポートまたは配信不能レポートを生成します。 また、トランスポートプロバイダーは、メッセージングシステムにネイティブである受信配信レポートと配信不能レポートを、 **StatusRecips**によって MAPI 配信および配信不能レポートに変換することもできます。
  

