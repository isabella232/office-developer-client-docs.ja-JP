---
title: 自動クライアントの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: eaa7e53902aa2a862c8f1ff279b05892ad891001
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619450"
---
# <a name="writing-an-automated-client"></a>自動クライアントの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
自動クライアント アプリケーションは、無人で実行されるアプリケーションで、ユーザー インターフェイスは表示されません。
  
 既定では、多くの MAPI インターフェイス メソッドにユーザー インターフェイスが表示されます。 これらのすべてのメソッドには、クライアントがこの表示を許可または抑制できるフラグがあります。 MAPI では、サービス プロバイダーがこれらのフラグを受け入れ、常にこれらの期待を満たしていないプロバイダーがあります。 フラグを尊重しない正当な理由は、ユーザー インターフェイスの抑制を許可しない別のサービスへのサービス プロバイダーの依存です。 自動クライアントを開発する場合は、使用しているサービス プロバイダーと、その構成方法に注意してください。 ユーザー インターフェイスを非表示にするためにすべての呼び出しが成功すると想定していきなさい。 
  
自動化されたクライアントには、プロファイル内の各メッセージ サービスを適切に構成するために必要な情報が必要です。 ログオン時に構成情報を提供するには、次の 2 つの方法があります。
  
- サービス プロバイダーは、プロファイルから情報を取得できます。
    
- サービス プロバイダーは、ユーザーに情報を求めるプロンプトを表示できます。 
    
2 番目のオプションは自動化されたクライアントでは使用できないので、これらのクライアントは最初のオプションを使用する必要があります。 クライアントは、このオプションが常に機能するために、プロファイルを慎重に構成する必要があります。
  
自動クライアントは、MAPILogonEx MAPI_NO_MAILに常にメッセージ フラグを設定して [、MAPI](mapilogonex.md) セッションを開始します。 
  

