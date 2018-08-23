---
title: トランスポート プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567952"
---
# <a name="handling-a-transport-provider"></a>トランスポート プロバイダーの処理
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントは、MAPI スプーラーとトランスポート プロバイダーによって提供される状態オブジェクトを介してトランスポート プロバイダーと通信します。 クライアントは、状態テーブルを取得するために[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出すことによって状態オブジェクトをアクセスします。 ステータス オブジェクトの実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースのプロバイダーを構成する、フラッシュの受信および送信メッセージのキュー、パスワードの設定、および状態の検証の方法があります。 ステータス オブジェクトの詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。


- [要求時にメッセージを送受信する](sending-or-receiving-a-message-on-demand.md): オン ・ デマンドでメッセージを送受信する方法について説明します。
    
- [トランスポート オーダを設定](setting-transport-order.md): トランスポートの順番を設定する方法について説明します。
    
- [トランスポート プロバイダーを再設定](reconfiguring-a-transport-provider.md): トランスポート プロバイダーを再設定する方法とはどのようなプロパティを設定するのには使用方法について説明します。
    

