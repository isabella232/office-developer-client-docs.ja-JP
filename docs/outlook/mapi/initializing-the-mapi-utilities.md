---
title: MAPI ユーティリティの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567672"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="d85cd-103">MAPI ユーティリティの初期化</span><span class="sxs-lookup"><span data-stu-id="d85cd-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="d85cd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85cd-105">MAPI を使用する必要があるの一部にすぎませんが、ユーティリティ、インターフェイス、および機能は、MAPI の MAPIUTIL で宣言されています。H ヘッダー ファイルに**IPropData**や**ITableData**など、初期化するために**生じます**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d85cd-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="d85cd-106">詳細についてを参照してください[IPropData: IMAPIProp](ipropdataimapiprop.md)、 [ITableData: IUnknown](itabledataiunknown.md)と[生じます](mapiinitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="d85cd-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="d85cd-107">代わりに、 **ScInitMapiUtil**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d85cd-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="d85cd-108">詳細については、 [ScInitMapiUtil](scinitmapiutil.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d85cd-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="d85cd-109">**ScInitMapiUtil**は、ユーティリティ関数、および MAPI のアロケーターを必要とすることを要求しないで、明示的にメソッドを使用するクライアント アプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d85cd-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="d85cd-110">シャット ダウン時に、 **DeinitMapiUtil**ユーティリティに接続しているリソースを解放するための呼び出しを確認します。</span><span class="sxs-lookup"><span data-stu-id="d85cd-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="d85cd-111">**MAPIUninitialize**を呼び出さないようにします。</span><span class="sxs-lookup"><span data-stu-id="d85cd-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="d85cd-112">詳細については、 [DeinitMapiUtil](deinitmapiutil.md)と[MAPIUninitialize](mapiuninitialize.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d85cd-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="d85cd-113">**ITableData**インタ フェースが**生じます**ではなく、 **ScInitMapiUtil**を呼び出したクライアント テーブルの通知をサポートしないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="d85cd-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

