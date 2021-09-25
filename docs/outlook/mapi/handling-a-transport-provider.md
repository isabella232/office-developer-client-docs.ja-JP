---
title: 転送プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7196800185f2bd4216324ac9a5d65835e61582f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551528"
---
# <a name="handling-a-transport-provider"></a>転送プロバイダーの処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、トランスポート プロバイダーと MAPI スプーラーによって提供される状態オブジェクトを介してトランスポート プロバイダーと通信します。 クライアントは [IMAPISession::GetStatusTable](imapisession-getstatustable.md) を呼び出して状態オブジェクトにアクセスし、状態テーブルを取得します。 Status オブジェクトは [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) インターフェイスを実装します。このインターフェイスには、プロバイダーの構成、受信メッセージ キューと送信メッセージ キューのフラッシュ、パスワードの設定、および状態の検証のためのメソッドがあります。 状態オブジェクトの詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。


- [メッセージをオンデマンドで送受信する](sending-or-receiving-a-message-on-demand.md): オンデマンドでメッセージを送受信する方法について説明します。
    
- [トランスポートの順序の設定](setting-transport-order.md): トランスポートの順序を設定する方法について説明します。
    
- [トランスポート プロバイダーの再構成](reconfiguring-a-transport-provider.md): トランスポート プロバイダーを再構成する方法と、設定できるプロパティについて説明します。
    

