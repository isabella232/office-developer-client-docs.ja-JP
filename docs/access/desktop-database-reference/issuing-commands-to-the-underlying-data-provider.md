---
title: 基になるデータ プロバイダーにコマンドを発行する
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477289"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="06085-102">基になるデータ プロバイダーにコマンドを発行する</span><span class="sxs-lookup"><span data-stu-id="06085-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="06085-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="06085-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="06085-104">図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。</span><span class="sxs-lookup"><span data-stu-id="06085-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="06085-105">これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="06085-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="06085-106">これらのコマンドを実行\*しない\***レコード セット**を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06085-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="06085-107">たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。</span><span class="sxs-lookup"><span data-stu-id="06085-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="06085-108">この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。</span><span class="sxs-lookup"><span data-stu-id="06085-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

