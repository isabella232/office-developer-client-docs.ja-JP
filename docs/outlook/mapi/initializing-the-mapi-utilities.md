---
title: MAPI ユーティリティの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420949"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="d78e9-103">MAPI ユーティリティの初期化</span><span class="sxs-lookup"><span data-stu-id="d78e9-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="d78e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d78e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d78e9-105">使用する必要がある MAPI の唯一の部分がユーティリティである場合は、MAPI の MAPIUTIL で宣言されているインターフェイスと関数です。IPropData や **ITableData** などの **H** ヘッダー ファイルは、初期化のために **MAPIInitialize を** 呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d78e9-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="d78e9-106">詳細については [、「IPropData : IMAPIProp](ipropdataimapiprop.md) [、ITableData :](itabledataiunknown.md)IUnknown、MAPIInitialize」 [を参照してください](mapiinitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="d78e9-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="d78e9-107">代わりに **、ScInitMapiUtil 関数を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="d78e9-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="d78e9-108">詳細については [、「ScInitMapiUtil」を参照してください](scinitmapiutil.md)。</span><span class="sxs-lookup"><span data-stu-id="d78e9-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="d78e9-109">**ScInitMapiUtil** を使用すると、クライアント アプリケーションは、MAPI アロケーターを必要とするが、明示的に要求しないユーティリティ関数とメソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d78e9-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="d78e9-110">シャットダウン時に **DeinitMapiUtil** を呼び出して、ユーティリティに接続されているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="d78e9-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="d78e9-111">**MAPIUninitialize を呼び出さない**。</span><span class="sxs-lookup"><span data-stu-id="d78e9-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="d78e9-112">詳細については[、「DeinitMapiUtil」および](deinitmapiutil.md)[「MAPIUninitialize」を参照してください](mapiuninitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="d78e9-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="d78e9-113">ITableData インターフェイスは **、MAPIInitialize** ではなく **ScInitMapiUtil** を呼び出したクライアントのテーブル通知をサポートしません。 </span><span class="sxs-lookup"><span data-stu-id="d78e9-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

