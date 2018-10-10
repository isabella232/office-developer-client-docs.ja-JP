---
title: Indexes.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa0123248781861f51ed4335e0174e654525a8c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476865"
---
# <a name="indexesappend-method-dao"></a><span data-ttu-id="a3845-102">Indexes.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3845-102">Indexes.Append Method (DAO)</span></span>


<span data-ttu-id="a3845-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3845-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3845-104">新しい **Index** を **Indexes** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a3845-104">Adds a new **Index** to the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3845-105">構文</span><span class="sxs-lookup"><span data-stu-id="a3845-105">Syntax</span></span>

<span data-ttu-id="a3845-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="a3845-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="a3845-107">\*式\***インデックス**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a3845-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a3845-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3845-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3845-109">名前</span><span class="sxs-lookup"><span data-stu-id="a3845-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3845-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="a3845-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a3845-111">データ型</span><span class="sxs-lookup"><span data-stu-id="a3845-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a3845-112">説明</span><span class="sxs-lookup"><span data-stu-id="a3845-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3845-113">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a3845-113">Object</span></span></p></td>
<td><p><span data-ttu-id="a3845-114">必須</span><span class="sxs-lookup"><span data-stu-id="a3845-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3845-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="a3845-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="a3845-116">コレクションに追加する項目を表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="a3845-116">An object variable that represents the item being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3845-117">注釈</span><span class="sxs-lookup"><span data-stu-id="a3845-117">Remarks</span></span>

<span data-ttu-id="a3845-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="a3845-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="a3845-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3845-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="a3845-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a3845-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="a3845-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="a3845-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>
