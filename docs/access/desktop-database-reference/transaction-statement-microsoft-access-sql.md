---
title: トランザクション ステートメント (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886390"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="4c2f4-102">トランザクション ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4c2f4-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4c2f4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c2f4-104">明示的なトランザクションの開始と終了に使用します。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2f4-105">構文</span><span class="sxs-lookup"><span data-stu-id="4c2f4-105">Syntax</span></span>

<span data-ttu-id="4c2f4-106">**新しいトランザクションを開始**します。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="4c2f4-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="4c2f4-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="4c2f4-108">**Conclude は、トランザクションをコミットすることによってすべての作業は、トランザクション中に実行**します。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="4c2f4-109">コミット\[トランザクション。作業\]</span><span class="sxs-lookup"><span data-stu-id="4c2f4-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="4c2f4-110">**Conclude トランザクションをロールバックしてトランザクション中にすべての作業を実行**します。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="4c2f4-111">ロールバック\[トランザクション。作業\]</span><span class="sxs-lookup"><span data-stu-id="4c2f4-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="4c2f4-112">解説</span><span class="sxs-lookup"><span data-stu-id="4c2f4-112">Remarks</span></span>

<span data-ttu-id="4c2f4-p101">トランザクションは自動的に開始されません。トランザクションを始めるためには、BEGIN TRANSACTION 句を使用して明示的に開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="4c2f4-p102">トランザクションは、5 レベルの深さまでネストさせることができます。ネストさせたトランザクションを開始するには、既存のトランザクションのコンテキストの中で、BEGIN TRANSACTION 句を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="4c2f4-117">このトランザクションは、リンク テーブルには対応していません。</span><span class="sxs-lookup"><span data-stu-id="4c2f4-117">Transactions are not supported for linked tables.</span></span>

