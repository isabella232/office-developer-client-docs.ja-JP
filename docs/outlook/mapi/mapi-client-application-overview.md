---
title: MAPI クライアントアプリケーションの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ad2e1f2d-57c3-4fb5-9e0f-db51640df84d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 100d1339ade8e5983c89695afbd85592cc2a4e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318971"
---
# <a name="mapi-client-application-overview"></a><span data-ttu-id="316ad-103">MAPI クライアントアプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="316ad-103">MAPI Client Application Overview</span></span>

  
  
<span data-ttu-id="316ad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="316ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="316ad-105">mapi クライアントアプリケーションは、mapi のプログラミングインターフェイスを使用するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="316ad-105">A MAPI client application is any application that uses the MAPI programming interface.</span></span> <span data-ttu-id="316ad-106">クライアントアプリケーションは、プライマリまたはセカンダリフォーカスのいずれかとしてメッセージングタスクを実装します。</span><span class="sxs-lookup"><span data-stu-id="316ad-106">Client applications implement messaging tasks as either their primary or secondary focus.</span></span> <span data-ttu-id="316ad-107">電子メールを送受信するアプリケーションなどのメッセージングクライアントアプリケーションは、プライマリフォーカスとしてメッセージングを実装します。</span><span class="sxs-lookup"><span data-stu-id="316ad-107">Messaging client applications, such as applications that send and receive email, implement messaging as their primary focus.</span></span> <span data-ttu-id="316ad-108">メッセージング以外のクライアントアプリケーション (インベントリアプリケーション、構成アプリケーションなど) の場合、メッセージングはセカンダリ機能です。</span><span class="sxs-lookup"><span data-stu-id="316ad-108">For non-messaging client applications, such as inventory or configuration applications, messaging is a secondary feature.</span></span>
  
<span data-ttu-id="316ad-109">メッセージングアクティビティには、たとえば、ドキュメントの送信を有効にするための [**ファイル**] メニューに [**送信**] コマンドがあるワードプロセッシングアプリケーション、Microsoft Office Outlook 電子メール、ワークフローオートメーションプログラム、および掲示板サービスなどがあります。</span><span class="sxs-lookup"><span data-stu-id="316ad-109">Messaging activities can include, for example, a word processing application that has a **Send** command on its **File** menu to enable documents to be sent, Microsoft Office Outlook email, work flow automation programs, and bulletin board services.</span></span> 
  
<span data-ttu-id="316ad-110">クライアントアプリケーションには、対話環境を作成するユーザーを含めることも、自動化された環境でユーザーを使用せずに操作することもできます。</span><span class="sxs-lookup"><span data-stu-id="316ad-110">Client applications can either include the user to create an interactive environment or operate without a user in an automated environment.</span></span> <span data-ttu-id="316ad-111">MAPI には、標準のユーザーインターフェイスを備えた一連のコモンダイアログボックスが用意されていますが、クライアントアプリケーションはユーザーインターフェイスを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="316ad-111">Although MAPI supplies a set of common dialog boxes with its standard user interface, client applications are not required to present a user interface.</span></span> <span data-ttu-id="316ad-112">実際には、必要に応じて、すべての処理をアプリケーションで処理することができます。</span><span class="sxs-lookup"><span data-stu-id="316ad-112">In fact, all processing can be handled in the application, if you want.</span></span> <span data-ttu-id="316ad-113">自動化されたクライアントアプリケーションの例として、特定の種類のアイテムを定期的に標準の受信者にルーティングするようにプログラムされた在庫管理アプリケーションがあります。</span><span class="sxs-lookup"><span data-stu-id="316ad-113">An example of an automated client application would be an inventory management application that is programmed to route items of a particular type to standard recipients on a regular basis.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="316ad-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="316ad-114">See also</span></span>



[<span data-ttu-id="316ad-115">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="316ad-115">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

