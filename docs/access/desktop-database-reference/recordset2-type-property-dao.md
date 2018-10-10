---
title: Recordset2.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee9afcd5367135da2d39fe889d17d089ae6f4c25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476544"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="19ffd-102">Recordset2.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="19ffd-102">Recordset2.Type Property (DAO)</span></span>


<span data-ttu-id="19ffd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="19ffd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19ffd-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( **Integer** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="19ffd-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ffd-106">構文</span><span class="sxs-lookup"><span data-stu-id="19ffd-106">Syntax</span></span>

<span data-ttu-id="19ffd-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="19ffd-107">*expression* .Type</span></span>

<span data-ttu-id="19ffd-108">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="19ffd-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ffd-109">注釈</span><span class="sxs-lookup"><span data-stu-id="19ffd-109">Remarks</span></span>

<span data-ttu-id="19ffd-110">**Recordset** オブジェクトの場合、設定できる値と戻り値は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="19ffd-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19ffd-111">定数</span><span class="sxs-lookup"><span data-stu-id="19ffd-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="19ffd-112">レコードセットの種類</span><span class="sxs-lookup"><span data-stu-id="19ffd-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19ffd-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="19ffd-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="19ffd-114">テーブル (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="19ffd-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19ffd-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="19ffd-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="19ffd-116">動的 (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="19ffd-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="19ffd-p102">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="19ffd-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19ffd-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="19ffd-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="19ffd-120">ダイナセット</span><span class="sxs-lookup"><span data-stu-id="19ffd-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19ffd-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="19ffd-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="19ffd-122">スナップショット</span><span class="sxs-lookup"><span data-stu-id="19ffd-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19ffd-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="19ffd-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="19ffd-124">前方スクロール</span><span class="sxs-lookup"><span data-stu-id="19ffd-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

