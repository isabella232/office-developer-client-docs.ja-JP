---
title: TableDefs.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afe0301153ae5f9e1e0e4fa499c2b27dc7e1c724
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920131"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="c5153-102">TableDefs.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5153-102">TableDefs.Append method (DAO)</span></span>


<span data-ttu-id="c5153-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c5153-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5153-104">新しい **TableDef** を **TableDefs** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="c5153-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5153-105">構文</span><span class="sxs-lookup"><span data-stu-id="c5153-105">Syntax</span></span>

<span data-ttu-id="c5153-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="c5153-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="c5153-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c5153-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c5153-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5153-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5153-109">名前</span><span class="sxs-lookup"><span data-stu-id="c5153-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c5153-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="c5153-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c5153-111">データ型</span><span class="sxs-lookup"><span data-stu-id="c5153-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c5153-112">説明</span><span class="sxs-lookup"><span data-stu-id="c5153-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5153-113">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c5153-113">Object</span></span></p></td>
<td><p><span data-ttu-id="c5153-114">必須</span><span class="sxs-lookup"><span data-stu-id="c5153-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c5153-115"><strong>オブジェクト型 (Object)</strong></span><span class="sxs-lookup"><span data-stu-id="c5153-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="c5153-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="c5153-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c5153-117">注釈</span><span class="sxs-lookup"><span data-stu-id="c5153-117">Remarks</span></span>

<span data-ttu-id="c5153-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="c5153-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="c5153-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5153-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="c5153-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c5153-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="c5153-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="c5153-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

