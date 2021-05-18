---
title: IStreamDocfile で OLE 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326230"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="870c6-103">IStreamDocfile で OLE 添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="870c6-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="870c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="870c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="870c6-105">OLE オブジェクト添付ファイルを開く場合は、IStream または [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx)ではなく **IStreamDocfile** インターフェイスを使用します。 [](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="870c6-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="870c6-106">**IStreamDocfile は** 、構造化ストレージを使用してオブジェクトに直接アクセスできます。コピー操作を実行する必要がなくなります。オーバーヘッドを削減します。</span><span class="sxs-lookup"><span data-stu-id="870c6-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="870c6-107">**IStreamDocfile** は **IStream** の特定の実装で、ストリームのコンテンツは構造化ストレージとして書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="870c6-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="870c6-108">**IStreamDocfile は** 、メッセージ ストア プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="870c6-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

