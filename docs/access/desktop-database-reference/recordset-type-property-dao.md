---
title: Recordset プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307554"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="ce4d4-102">Recordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ce4d4-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="ce4d4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce4d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce4d4-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ce4d4-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4d4-106">構文</span><span class="sxs-lookup"><span data-stu-id="ce4d4-106">Syntax</span></span>

<span data-ttu-id="ce4d4-107">*式*。種類</span><span class="sxs-lookup"><span data-stu-id="ce4d4-107">*expression* .Type</span></span>

<span data-ttu-id="ce4d4-108">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="ce4d4-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4d4-109">注釈</span><span class="sxs-lookup"><span data-stu-id="ce4d4-109">Remarks</span></span>

<span data-ttu-id="ce4d4-110">**Recordset** オブジェクトの場合、設定できる値と戻り値は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ce4d4-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce4d4-111">定数</span><span class="sxs-lookup"><span data-stu-id="ce4d4-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="ce4d4-112">レコードセットの種類</span><span class="sxs-lookup"><span data-stu-id="ce4d4-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce4d4-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="ce4d4-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4d4-114">テーブル (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="ce4d4-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4d4-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="ce4d4-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4d4-116">動的 (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="ce4d4-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="ce4d4-117"><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ce4d4-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="ce4d4-118">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="ce4d4-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4d4-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="ce4d4-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4d4-120">ダイナセットタイプ</span><span class="sxs-lookup"><span data-stu-id="ce4d4-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4d4-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="ce4d4-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4d4-122">スナップショット</span><span class="sxs-lookup"><span data-stu-id="ce4d4-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4d4-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="ce4d4-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4d4-124">前方のみ</span><span class="sxs-lookup"><span data-stu-id="ce4d4-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

