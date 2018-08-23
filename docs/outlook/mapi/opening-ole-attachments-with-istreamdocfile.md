---
title: IStreamDocfile を持つ OLE 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801702"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="e0ed6-103">IStreamDocfile を持つ OLE 添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="e0ed6-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="e0ed6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0ed6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0ed6-105">OLE オブジェクトの添付ファイルを開くときは、 **IStreamDocfile**インターフェイスではなく[IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx)または[IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx)を使用します。</span><span class="sxs-lookup"><span data-stu-id="e0ed6-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="e0ed6-106">**IStreamDocfile**は、構造化ストレージを使用して、コピー操作とオーバーヘッドの削減を実行する必要がなくなるため、オブジェクトへの直接アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e0ed6-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="e0ed6-107">**IStreamDocfile**は、構造化ストレージとして設定することが保証するストリームのコンテンツを含む**IStream**の特定の実装です。</span><span class="sxs-lookup"><span data-stu-id="e0ed6-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="e0ed6-108">**IStreamDocfile**は、メッセージ ストア プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e0ed6-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

