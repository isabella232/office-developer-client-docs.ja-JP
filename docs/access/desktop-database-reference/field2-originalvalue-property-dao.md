---
title: Field2.OriginalValue プロパティ (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a08612076ba138e5e181eec80bec2350fe27ec86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479454"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="a9c7b-102">Field2.OriginalValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9c7b-102">Field2.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="a9c7b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9c7b-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c7b-104">構文</span><span class="sxs-lookup"><span data-stu-id="a9c7b-104">Syntax</span></span>

<span data-ttu-id="a9c7b-105">*式*です。OriginalValue</span><span class="sxs-lookup"><span data-stu-id="a9c7b-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="a9c7b-106">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a9c7b-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c7b-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a9c7b-107">Remarks</span></span>

<span data-ttu-id="a9c7b-p101">共有的バッチ更新の実行中に、最初のクライアントがデータを取得してから、最初のクライアントの更新が試行されるまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生する可能性があります。 **OriginalValue** プロパティには、最後のバッチ **Update** が開始された時点のフィールドの値が含まれています。バッチ **Update** によりデータベースに書き込もうとしたときに、この値が実際にはデータベースの値と一致していない場合、競合が発生します。この場合、 **VisibleValue** プロパティを使用してデータベースの新しい値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a9c7b-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>
