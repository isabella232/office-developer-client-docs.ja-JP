---
title: Recordset.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 091a8e10-01c0-20af-7230-cd7103c243a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845045(v=office.15)
ms:contentKeyID: 48543116
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19c9539effe5e119cc85dd5eab2f096fe1fd9410
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920194"
---
# <a name="recordsetlastupdated-property-dao"></a><span data-ttu-id="cad3d-102">Recordset.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="cad3d-102">Recordset.LastUpdated property (DAO)</span></span>


<span data-ttu-id="cad3d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cad3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cad3d-p101">ベース テーブルに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cad3d-p101">Returns the date and time of the most recent change made to a base table. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad3d-106">構文</span><span class="sxs-lookup"><span data-stu-id="cad3d-106">Syntax</span></span>

<span data-ttu-id="cad3d-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="cad3d-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="cad3d-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="cad3d-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad3d-109">注釈</span><span class="sxs-lookup"><span data-stu-id="cad3d-109">Remarks</span></span>

<span data-ttu-id="cad3d-110">日付と時刻の設定は、ベース テーブルを作成した、または最後に更新したコンピューターから導出されます。</span><span class="sxs-lookup"><span data-stu-id="cad3d-110">The date and time settings are derived from the computer on which the base table was created or last updated.</span></span>

