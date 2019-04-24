---
title: 転送プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299497"
---
# <a name="handling-a-transport-provider"></a>転送プロバイダーの処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、トランスポートプロバイダーと MAPI スプーラーで提供される状態オブジェクトを通じて、トランスポートプロバイダーと通信します。 クライアントは、 [imapisession:: getstatustable](imapisession-getstatustable.md)を呼び出してステータスオブジェクトにアクセスし、状態テーブルを取得します。 Status オブジェクトは、プロバイダーを構成し、受信および送信メッセージキューをフラッシュする、パスワードを設定する、および状態を検証するための[imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスを実装しています。 状態オブジェクトの詳細については、「 [status Table and status objects](status-table-and-status-objects.md)」を参照してください。


- [必要に応じてメッセージを送信または受信](sending-or-receiving-a-message-on-demand.md)する: 必要に応じてメッセージを送信または受信する方法について説明します。
    
- [トランスポートオーダーの設定](setting-transport-order.md): トランスポート順序を設定する方法について説明します。
    
- [トランスポートプロバイダーの再構成](reconfiguring-a-transport-provider.md): トランスポートプロバイダーを再構成する方法と、設定できるプロパティについて説明します。
    

