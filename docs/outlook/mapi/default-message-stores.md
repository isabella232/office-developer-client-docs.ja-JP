---
title: 既定のメッセージ ストア
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338046"
---
# <a name="default-message-stores"></a><span data-ttu-id="68837-103">既定のメッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="68837-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="68837-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68837-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68837-p101">既定のメッセージ ストアは、クライアント アプリケーションが汎用メッセージング タスクに使用できるものです。既定のメッセージ ストアとしてメッセージ ストア プロバイダーを使用する場合に、メッセージ ストア プロバイダーにとって必要となるいくつかのオプション機能があります。これらは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="68837-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="68837-108">受信トレイ、送信トレイ、および検索結果フォルダーなどの特別なフォルダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="68837-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="68837-109">開封済みレポートと未読レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="68837-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="68837-110">受信メッセージと送信メッセージの送信を許可します。</span><span class="sxs-lookup"><span data-stu-id="68837-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="68837-111">任意のメッセージ クラスのメッセージの作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="68837-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="68837-112">名前付きプロパティと複数値プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="68837-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="68837-113">メッセージ ストア プロバイダーがトランスポート プロバイダーと密接に結合している場合でも、[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="68837-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="68837-p102">関連するコンテンツ テーブルをサポートします。詳細については、[コンテンツ テーブル](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68837-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="68837-116">送信メッセージ キューにメッセージがある場合に、MAPI スプーラーの通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68837-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68837-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="68837-117">See also</span></span>



[<span data-ttu-id="68837-118">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="68837-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

