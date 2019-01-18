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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705520"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="8b953-102">トランザクション ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8b953-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8b953-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8b953-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b953-104">明示的なトランザクションの開始と終了に使用します。</span><span class="sxs-lookup"><span data-stu-id="8b953-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b953-105">構文</span><span class="sxs-lookup"><span data-stu-id="8b953-105">Syntax</span></span>

<span data-ttu-id="8b953-106">**新しいトランザクションを開始**します。</span><span class="sxs-lookup"><span data-stu-id="8b953-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="8b953-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="8b953-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="8b953-108">**Conclude は、トランザクションをコミットすることによってすべての作業は、トランザクション中に実行**します。</span><span class="sxs-lookup"><span data-stu-id="8b953-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="8b953-109">コミット\[トランザクション。作業\]</span><span class="sxs-lookup"><span data-stu-id="8b953-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="8b953-110">**Conclude トランザクションをロールバックしてトランザクション中にすべての作業を実行**します。</span><span class="sxs-lookup"><span data-stu-id="8b953-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="8b953-111">ロールバック\[トランザクション。作業\]</span><span class="sxs-lookup"><span data-stu-id="8b953-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="8b953-112">解説</span><span class="sxs-lookup"><span data-stu-id="8b953-112">Remarks</span></span>

<span data-ttu-id="8b953-p101">トランザクションは自動的に開始されません。トランザクションを始めるためには、BEGIN TRANSACTION 句を使用して明示的に開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b953-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="8b953-p102">トランザクションは、5 レベルの深さまでネストさせることができます。ネストさせたトランザクションを開始するには、既存のトランザクションのコンテキストの中で、BEGIN TRANSACTION 句を使用してください。</span><span class="sxs-lookup"><span data-stu-id="8b953-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="8b953-117">このトランザクションは、リンク テーブルには対応していません。</span><span class="sxs-lookup"><span data-stu-id="8b953-117">Transactions are not supported for linked tables.</span></span>

