---
title: 基になるデータ プロバイダーにコマンドを発行する
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0379d38b6c38145a72d5ab41b7ee0e7ec45531b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889078"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="90570-102">基になるデータ プロバイダーにコマンドを発行する</span><span class="sxs-lookup"><span data-stu-id="90570-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="90570-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="90570-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90570-104">図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="90570-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="90570-105">これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="90570-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="90570-106">これらのコマンドを実行\*しない\***レコード セット**を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90570-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="90570-107">たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。</span><span class="sxs-lookup"><span data-stu-id="90570-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="90570-108">この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。</span><span class="sxs-lookup"><span data-stu-id="90570-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

