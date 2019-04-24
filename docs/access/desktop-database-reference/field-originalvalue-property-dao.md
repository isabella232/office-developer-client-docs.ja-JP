---
title: フィールドの originalvalue プロパティ (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293001"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="37746-102">フィールドの originalvalue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="37746-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="37746-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="37746-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="37746-104">構文</span><span class="sxs-lookup"><span data-stu-id="37746-104">Syntax</span></span>

<span data-ttu-id="37746-105">*式*。OriginalValue</span><span class="sxs-lookup"><span data-stu-id="37746-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="37746-106">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="37746-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="37746-107">注釈</span><span class="sxs-lookup"><span data-stu-id="37746-107">Remarks</span></span>

<span data-ttu-id="37746-p101">共有的バッチ更新の実行中に、最初のクライアントがデータを取得してから、最初のクライアントの更新が試行されるまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生する可能性があります。 **OriginalValue** プロパティには、最後のバッチ **Update** が開始された時点のフィールドの値が含まれています。バッチ **Update** によりデータベースに書き込もうとしたときに、この値が実際にはデータベースの値と一致していない場合、競合が発生します。この場合、 **[VisibleValue](field-visiblevalue-property-dao.md)** プロパティを使用してデータベースの新しい値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="37746-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

