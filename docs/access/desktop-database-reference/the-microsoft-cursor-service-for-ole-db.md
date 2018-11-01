---
title: OLE DB 用 Microsoft Cursor Service
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9db5617eecff862ad941a4160c4b92bfa09d4c2d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885921"
---
# <a name="the-microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="4f471-102">OLE DB 用 Microsoft Cursor Service</span><span class="sxs-lookup"><span data-stu-id="4f471-102">The Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="4f471-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4f471-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f471-p101">クライアント側カーソルを選択、つまり **CursorLocation** プロパティを **adUseClient** に設定すると、Microsoft Cursor Service for OLE DB が呼び出されます。"Client Cursor Engine" と呼ばれることもありますが、ADO のコンテキストでは本質的に同じ機能を表します。このサービスは、データ プロバイダーのカーソル サポート機能を補完するものです。その結果、すべてのデータ プロバイダーで、比較的一定した機能を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="4f471-p101">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB. You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO. This service supplements the cursor-support functions of data providers. As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="4f471-p102">Cursor Service for OLE DB により、動的プロパティが使用できるようになり、一部のメソッドの動作が拡張されます。たとえば、動的プロパティの **Optimize** を使用すると、一時的なインデックスを作成して、 **Find** メソッドなど一部の操作を円滑化できます。</span><span class="sxs-lookup"><span data-stu-id="4f471-p102">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods. For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="4f471-p103">Cursor Service を使用すると、あらゆる場合にバッチ更新が実行できるようになります。また、データ プロバイダーが、静的カーソルなど、機能が限定されたカーソルしかサポートしていない場合でも、動的カーソルなど、より高機能な種類のカーソルをシミュレートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4f471-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

