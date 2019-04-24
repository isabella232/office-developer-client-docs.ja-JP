---
title: TableDef プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314288"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="8424a-102">TableDef プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="8424a-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="8424a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8424a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8424a-104">**[TableDef](tabledef-object-dao.md)** オブジェクトのレコードの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="8424a-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="8424a-105">取得のみ可能な **Long** 値です。</span><span class="sxs-lookup"><span data-stu-id="8424a-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8424a-106">構文</span><span class="sxs-lookup"><span data-stu-id="8424a-106">Syntax</span></span>

<span data-ttu-id="8424a-107">*式*。RecordCount</span><span class="sxs-lookup"><span data-stu-id="8424a-107">*expression* .RecordCount</span></span>

<span data-ttu-id="8424a-108">\*式\***TableDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="8424a-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8424a-109">注釈</span><span class="sxs-lookup"><span data-stu-id="8424a-109">Remarks</span></span>

<span data-ttu-id="8424a-110">レコードを持たない **Recordset** オブジェクトまたは **TableDef** オブジェクトでは、 **RecordCount** プロパティの設定値が 0 となります。</span><span class="sxs-lookup"><span data-stu-id="8424a-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="8424a-111">リンクされた **TableDef** オブジェクトを使用する場合、**RecordCount** プロパティの設定値は常に -1 となります。</span><span class="sxs-lookup"><span data-stu-id="8424a-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

