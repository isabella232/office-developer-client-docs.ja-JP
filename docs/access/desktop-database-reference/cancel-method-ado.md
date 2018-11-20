---
title: Cancel メソッド (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e817b4310fa1f08d69265691814ac314158e60c
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026128"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="2c1c3-102">Cancel メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="2c1c3-102">Cancel method (ADO)</span></span>

<span data-ttu-id="2c1c3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2c1c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c1c3-104">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="2c1c3-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="2c1c3-105">Syntax</span></span>

<span data-ttu-id="2c1c3-106">*オブジェクト*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="2c1c3-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="2c1c3-107">解説</span><span class="sxs-lookup"><span data-stu-id="2c1c3-107">Remarks</span></span>

<span data-ttu-id="2c1c3-108">非同期メソッド呼び出し (つまり、 **adAsyncConnect** 、 **adAsyncExecute** 、または **adAsyncFetch** オプションを指定して呼び出されたメソッド) の実行を中止するには、 **Cancel** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c1c3-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="2c1c3-109">次の表は、特定の種類のオブジェクトに対して **Cancel** メソッドを使用したときに中止される操作です。</span><span class="sxs-lookup"><span data-stu-id="2c1c3-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="2c1c3-110"><em>object</em> の値</span><span class="sxs-lookup"><span data-stu-id="2c1c3-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="2c1c3-111">最後の非同期呼び出しが中止されるメソッド</span><span class="sxs-lookup"><span data-stu-id="2c1c3-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c1c3-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="2c1c3-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c1c3-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="2c1c3-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> または <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c1c3-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="2c1c3-117"><a href="copyrecord-method-ado.md">CopyRecord</a>、<a href="deleterecord-method-ado.md">DeleteRecord</a>、<a href="moverecord-method-ado.md">MoveRecord</a>、または <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c1c3-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="2c1c3-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c1c3-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="2c1c3-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2c1c3-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

