---
title: Index プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291700"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="edd62-102">Index プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="edd62-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="edd62-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="edd62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edd62-104">**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="edd62-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd62-105">構文</span><span class="sxs-lookup"><span data-stu-id="edd62-105">Syntax</span></span>

<span data-ttu-id="edd62-106">*式*。必須</span><span class="sxs-lookup"><span data-stu-id="edd62-106">*expression* .Required</span></span>

<span data-ttu-id="edd62-107">\*式\***Index**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="edd62-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd62-108">注釈</span><span class="sxs-lookup"><span data-stu-id="edd62-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="edd62-p101">[!メモ] **Index** オブジェクトまたは **Field** オブジェクトのいずれかにこのプロパティを設定できる場合は、 **Field** オブジェクトに設定します。 **Field** オブジェクトのプロパティ設定の妥当性が検査された後、 **Index** オブジェクトの設定が検査されます。</span><span class="sxs-lookup"><span data-stu-id="edd62-p101">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="edd62-111">**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="edd62-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edd62-112">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="edd62-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="edd62-113">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="edd62-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edd62-114"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="edd62-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="edd62-115">サポートされない</span><span class="sxs-lookup"><span data-stu-id="edd62-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd62-116"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="edd62-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="edd62-117">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="edd62-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd62-118"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="edd62-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="edd62-119">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="edd62-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd62-120"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="edd62-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="edd62-121">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="edd62-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd62-122"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="edd62-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="edd62-123">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="edd62-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

