---
title: Relations.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 51f365ef783fb874b269ac0490b08687ce127475
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477748"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="baabf-102">Relations.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="baabf-102">Relations.Append Method (DAO)</span></span>


<span data-ttu-id="baabf-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="baabf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="baabf-104">新しい **Relation** を **Relations** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="baabf-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="baabf-105">構文</span><span class="sxs-lookup"><span data-stu-id="baabf-105">Syntax</span></span>

<span data-ttu-id="baabf-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="baabf-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="baabf-107">\*式\***関係**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="baabf-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="baabf-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="baabf-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baabf-109">名前</span><span class="sxs-lookup"><span data-stu-id="baabf-109">Name</span></span></p></th>
<th><p><span data-ttu-id="baabf-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="baabf-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="baabf-111">データ型</span><span class="sxs-lookup"><span data-stu-id="baabf-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="baabf-112">説明</span><span class="sxs-lookup"><span data-stu-id="baabf-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baabf-113">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="baabf-113">Object</span></span></p></td>
<td><p><span data-ttu-id="baabf-114">必須</span><span class="sxs-lookup"><span data-stu-id="baabf-114">Required</span></span></p></td>
<td><p><span data-ttu-id="baabf-115"><strong>オブジェクト型 (Object)</strong></span><span class="sxs-lookup"><span data-stu-id="baabf-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="baabf-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="baabf-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="baabf-117">注釈</span><span class="sxs-lookup"><span data-stu-id="baabf-117">Remarks</span></span>

<span data-ttu-id="baabf-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="baabf-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="baabf-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="baabf-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="baabf-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="baabf-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="baabf-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="baabf-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

