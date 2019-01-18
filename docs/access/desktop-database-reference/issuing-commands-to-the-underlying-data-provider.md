---
title: 基になるデータ プロバイダーへのコマンドの発行
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709615"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="60d62-102">基になるデータ プロバイダーへのコマンドの発行</span><span class="sxs-lookup"><span data-stu-id="60d62-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="60d62-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="60d62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60d62-104">図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="60d62-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="60d62-105">これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="60d62-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="60d62-106">これらのコマンドを実行\*しない\***レコード セット**を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60d62-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="60d62-107">たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。</span><span class="sxs-lookup"><span data-stu-id="60d62-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="60d62-108">この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。</span><span class="sxs-lookup"><span data-stu-id="60d62-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

