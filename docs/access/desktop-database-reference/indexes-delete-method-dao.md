---
title: Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291553"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="ba12d-102">Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ba12d-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="ba12d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba12d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba12d-104">指定した **Index** を **Indexes** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="ba12d-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba12d-105">構文</span><span class="sxs-lookup"><span data-stu-id="ba12d-105">Syntax</span></span>

<span data-ttu-id="ba12d-106">*式*。削除 (***名前***)</span><span class="sxs-lookup"><span data-stu-id="ba12d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ba12d-107">\*式\***Indexes**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="ba12d-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba12d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba12d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba12d-109">名前</span><span class="sxs-lookup"><span data-stu-id="ba12d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ba12d-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="ba12d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ba12d-111">データ型</span><span class="sxs-lookup"><span data-stu-id="ba12d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ba12d-112">説明</span><span class="sxs-lookup"><span data-stu-id="ba12d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba12d-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="ba12d-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ba12d-114">必須</span><span class="sxs-lookup"><span data-stu-id="ba12d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ba12d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ba12d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ba12d-116">削除するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba12d-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ba12d-117">注釈</span><span class="sxs-lookup"><span data-stu-id="ba12d-117">Remarks</span></span>

<span data-ttu-id="ba12d-118">**Delete** メソッドは、**Index** オブジェクトが新しく作成されたものであり、まだデータベースに追加されていない場合のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba12d-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

