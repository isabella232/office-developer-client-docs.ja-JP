---
title: Index.Required プロパティ (DAO)
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
ms.openlocfilehash: 71ea383cbf1c55fb15b484fea039c71c44a4e470
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881413"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="613ed-102">Index.Required プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="613ed-102">Index.Required Property (DAO)</span></span>


<span data-ttu-id="613ed-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="613ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="613ed-104">**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="613ed-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="613ed-105">構文</span><span class="sxs-lookup"><span data-stu-id="613ed-105">Syntax</span></span>

<span data-ttu-id="613ed-106">*式*です。必須</span><span class="sxs-lookup"><span data-stu-id="613ed-106">*expression* .Required</span></span>

<span data-ttu-id="613ed-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="613ed-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="613ed-108">注釈</span><span class="sxs-lookup"><span data-stu-id="613ed-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="613ed-p101">[!メモ] <STRONG>Index</STRONG> オブジェクトまたは <STRONG>Field</STRONG> オブジェクトのいずれかにこのプロパティを設定できる場合は、 <STRONG>Field</STRONG> オブジェクトに設定します。 <STRONG>Field</STRONG> オブジェクトのプロパティ設定の妥当性が検査された後、 <STRONG>Index</STRONG> オブジェクトの設定が検査されます。</span><span class="sxs-lookup"><span data-stu-id="613ed-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="613ed-111">**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="613ed-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="613ed-112">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="613ed-113">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="613ed-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="613ed-114"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="613ed-115">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="613ed-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613ed-116"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="613ed-117">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="613ed-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613ed-118"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="613ed-119">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="613ed-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613ed-120"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="613ed-121">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="613ed-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613ed-122"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="613ed-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="613ed-123">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="613ed-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

