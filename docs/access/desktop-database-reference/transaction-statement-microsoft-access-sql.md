---
title: TRANSACTION ステートメント (Microsoft Access SQL)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314148"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="d3ffa-102">TRANSACTION ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="d3ffa-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="d3ffa-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3ffa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3ffa-104">明示的なトランザクションを開始および終了するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d3ffa-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ffa-105">構文</span><span class="sxs-lookup"><span data-stu-id="d3ffa-105">Syntax</span></span>

<span data-ttu-id="d3ffa-106">**新しいトランザクションを開始します**:</span><span class="sxs-lookup"><span data-stu-id="d3ffa-106">Initiate a new transaction.</span></span>

<span data-ttu-id="d3ffa-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="d3ffa-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="d3ffa-108">**トランザクションの処理中に行われたすべての仕事をコミットして、トランザクションを終了します**:</span><span class="sxs-lookup"><span data-stu-id="d3ffa-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="d3ffa-109">COMMIT \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="d3ffa-109">COMMIT [TRANSACTION | WORK]</span></span>

<span data-ttu-id="d3ffa-110">**トランザクションの処理中に行われたすべての仕事をロールバックして、トランザクションを終了します**:</span><span class="sxs-lookup"><span data-stu-id="d3ffa-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="d3ffa-111">ROLLBACK \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="d3ffa-111">ROLLBACK [TRANSACTION | WORK]</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ffa-112">注釈</span><span class="sxs-lookup"><span data-stu-id="d3ffa-112">Remarks</span></span>

<span data-ttu-id="d3ffa-p101">トランザクションは自動的に開始しません。トランザクションを開始するには、BEGIN TRANSACTION を使用して明示的に開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ffa-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="d3ffa-p102">トランザクションは最大 5 レベルまで入れ子にすることができます。入れ子になったトランザクションを開始するには、既存のトランザクションのコンテキスト内で BEGIN TRANSACTION を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3ffa-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="d3ffa-117">トランザクションはリンク テーブルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d3ffa-117">Transactions are not supported for linked tables.</span></span>

