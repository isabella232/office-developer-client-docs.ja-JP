---
title: Recordset.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3eedbab083807f91ffef78aab25d110db779188
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026086"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="4bac3-102">Recordset.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="4bac3-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="4bac3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4bac3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bac3-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( **Integer** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4bac3-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bac3-106">構文</span><span class="sxs-lookup"><span data-stu-id="4bac3-106">Syntax</span></span>

<span data-ttu-id="4bac3-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="4bac3-107">*expression* .Type</span></span>

<span data-ttu-id="4bac3-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="4bac3-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bac3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="4bac3-109">Remarks</span></span>

<span data-ttu-id="4bac3-110">**Recordset** オブジェクトの場合、設定できる値と戻り値は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4bac3-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bac3-111">定数</span><span class="sxs-lookup"><span data-stu-id="4bac3-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="4bac3-112">レコードセットの種類</span><span class="sxs-lookup"><span data-stu-id="4bac3-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bac3-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="4bac3-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac3-114">テーブル (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="4bac3-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bac3-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="4bac3-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac3-116">動的 (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="4bac3-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="4bac3-117"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4bac3-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="4bac3-118">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4bac3-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bac3-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="4bac3-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac3-120">ダイナセット</span><span class="sxs-lookup"><span data-stu-id="4bac3-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bac3-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="4bac3-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac3-122">スナップショット</span><span class="sxs-lookup"><span data-stu-id="4bac3-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bac3-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="4bac3-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac3-124">前方スクロール</span><span class="sxs-lookup"><span data-stu-id="4bac3-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

