---
title: コマンドを基になるデータ プロバイダーに発行します。
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944635"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="f7127-102">コマンドを基になるデータ プロバイダーに発行します。</span><span class="sxs-lookup"><span data-stu-id="f7127-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="f7127-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7127-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7127-104">図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="f7127-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="f7127-105">これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="f7127-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="f7127-106">これらのコマンドを実行\*しない\***レコード セット**を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7127-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="f7127-107">たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。</span><span class="sxs-lookup"><span data-stu-id="f7127-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="f7127-108">この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。</span><span class="sxs-lookup"><span data-stu-id="f7127-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

