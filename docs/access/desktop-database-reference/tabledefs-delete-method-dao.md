---
title: TableDefs.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e39a1390c9ea26baa83d8203967d603237a3ab1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477904"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="21de7-102">TableDefs.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="21de7-102">TableDefs.Delete Method (DAO)</span></span>


<span data-ttu-id="21de7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="21de7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="21de7-104">指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="21de7-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="21de7-105">構文</span><span class="sxs-lookup"><span data-stu-id="21de7-105">Syntax</span></span>

<span data-ttu-id="21de7-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="21de7-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="21de7-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="21de7-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="21de7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21de7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21de7-109">名前</span><span class="sxs-lookup"><span data-stu-id="21de7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="21de7-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="21de7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="21de7-111">データ型</span><span class="sxs-lookup"><span data-stu-id="21de7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="21de7-112">説明</span><span class="sxs-lookup"><span data-stu-id="21de7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21de7-113">名前</span><span class="sxs-lookup"><span data-stu-id="21de7-113">Name</span></span></p></td>
<td><p><span data-ttu-id="21de7-114">必須</span><span class="sxs-lookup"><span data-stu-id="21de7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="21de7-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="21de7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="21de7-116">削除する TableDef の名前です。</span><span class="sxs-lookup"><span data-stu-id="21de7-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="21de7-117">注釈</span><span class="sxs-lookup"><span data-stu-id="21de7-117">Remarks</span></span>

<span data-ttu-id="21de7-118">**テーブル定義**オブジェクトが新しいし、データベースに追加されていない場合にのみ、または**テーブル定義**の**更新できる**プロパティが**True**に設定すると、Delete メソッドはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="21de7-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

