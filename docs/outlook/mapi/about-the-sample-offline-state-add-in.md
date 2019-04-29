---
title: サンプルのオフライン状態アドインについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf8e647af4aba53dfc24880e6ff491985b50a613
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431184"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="44d72-103">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="44d72-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="44d72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44d72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44d72-105">オフライン状態 API は、outlook でのユーザーの接続状態の変更を示すコールバックをサポートします。たとえば、outlook のオンラインからオフラインに至るまで。</span><span class="sxs-lookup"><span data-stu-id="44d72-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="44d72-106">サンプルのオフライン状態アドインは、C++ で作成された COM アドインです。これは、接続状態の変更の通知を受信する方法と、オフライン状態 API を使用して現在の状態を変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="44d72-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="44d72-107">オフライン状態 API の詳細については、[オフライン状態 API について](about-the-offline-state-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44d72-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="44d72-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="44d72-108">In this section</span></span>

- [<span data-ttu-id="44d72-109">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="44d72-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="44d72-110">サンプルのオフライン状態アドインをダウンロードしてインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="44d72-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="44d72-111">オフライン状態アドインのセットアップ</span><span class="sxs-lookup"><span data-stu-id="44d72-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="44d72-112">オフライン状態アドインを使用するために、接続、初期化、およびセットアップ関数を実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="44d72-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="44d72-113">オフライン状態アドインを使用した接続状態変更の監視</span><span class="sxs-lookup"><span data-stu-id="44d72-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="44d72-114">**[hroな offlineobj](hropenofflineobj.md)** 関数を使用して、接続状態を監視および変更するためのオフラインオブジェクトを取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="44d72-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="44d72-115">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="44d72-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="44d72-116">アドインが切断されたときに、オフライン状態アドインを適切に終了してクリーンアップする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="44d72-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44d72-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="44d72-117">See also</span></span>



[<span data-ttu-id="44d72-118">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="44d72-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

