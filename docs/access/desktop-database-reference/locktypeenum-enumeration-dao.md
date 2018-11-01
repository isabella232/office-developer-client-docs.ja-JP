---
title: LockTypeEnum 列挙 (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0e12f8d60ee3147eb456df302122a5b7eac684d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879929"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="fc9a7-102">LockTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc9a7-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="fc9a7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc9a7-104">レコードセットを開くときに使用されるレコード ロックの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc9a7-105">名前</span><span class="sxs-lookup"><span data-stu-id="fc9a7-105">Name</span></span></p></th>
<th><p><span data-ttu-id="fc9a7-106">値</span><span class="sxs-lookup"><span data-stu-id="fc9a7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fc9a7-107">説明</span><span class="sxs-lookup"><span data-stu-id="fc9a7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc9a7-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="fc9a7-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-109">3</span><span class="sxs-lookup"><span data-stu-id="fc9a7-109">3</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-p101">レコード ID に基づく共有的同時ロック。カーソルは古いレコードと新しいレコードのレコード ID を比較し、そのレコードへのアクセスが最後に行われてから変更が加えられたかどうか判断します。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9a7-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="fc9a7-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-113">5</span><span class="sxs-lookup"><span data-stu-id="fc9a7-113">5</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-114">共有的バッチ更新を可能にします (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc9a7-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="fc9a7-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-116">1</span><span class="sxs-lookup"><span data-stu-id="fc9a7-116">1</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-p102">レコード値に基づく共有的同時ロック。カーソルは古いレコードと新しいレコードのデータ値を比較し、そのレコードへのアクセスが最後に行われてから変更が加えられたかどうか判断します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="fc9a7-p103">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9a7-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="fc9a7-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-122">2</span><span class="sxs-lookup"><span data-stu-id="fc9a7-122">2</span></span></p></td>
<td><p><span data-ttu-id="fc9a7-p104">排他的同時ロック。カーソルは、レコードが更新可能であることを保証するために必要な最低限のロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc9a7-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

