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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416539"
---
# <a name="handling-a-transport-provider"></a>転送プロバイダーの処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、トランスポート プロバイダーと MAPI スプーラーによって提供される状態オブジェクトを介してトランスポート プロバイダーと通信します。 クライアントは [IMAPISession::GetStatusTable](imapisession-getstatustable.md) を呼び出して状態オブジェクトにアクセスし、状態テーブルを取得します。 Status オブジェクトは [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) インターフェイスを実装します。このインターフェイスには、プロバイダーの構成、受信メッセージ キューと送信メッセージ キューのフラッシュ、パスワードの設定、および状態の検証のためのメソッドがあります。 状態オブジェクトの詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。


- [メッセージをオンデマンドで送受信する](sending-or-receiving-a-message-on-demand.md): オンデマンドでメッセージを送受信する方法について説明します。
    
- [トランスポートの順序の設定](setting-transport-order.md): トランスポートの順序を設定する方法について説明します。
    
- [トランスポート プロバイダーの再構成](reconfiguring-a-transport-provider.md): トランスポート プロバイダーを再構成する方法と、設定できるプロパティについて説明します。
    

