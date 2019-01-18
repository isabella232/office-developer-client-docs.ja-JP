---
title: Recordset.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 091a8e10-01c0-20af-7230-cd7103c243a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845045(v=office.15)
ms:contentKeyID: 48543116
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6ba72c58d40650ec95b859076489d4dc10b4bee
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698226"
---
# <a name="recordsetlastupdated-property-dao"></a><span data-ttu-id="6c862-102">Recordset.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c862-102">Recordset.LastUpdated property (DAO)</span></span>


<span data-ttu-id="6c862-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6c862-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c862-p101">ベース テーブルに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c862-p101">Returns the date and time of the most recent change made to a base table. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c862-106">構文</span><span class="sxs-lookup"><span data-stu-id="6c862-106">Syntax</span></span>

<span data-ttu-id="6c862-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="6c862-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="6c862-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6c862-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c862-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6c862-109">Remarks</span></span>

<span data-ttu-id="6c862-110">日付と時刻の設定は、ベース テーブルを作成した、または最後に更新したコンピューターから導出されます。</span><span class="sxs-lookup"><span data-stu-id="6c862-110">The date and time settings are derived from the computer on which the base table was created or last updated.</span></span>

