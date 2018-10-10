---
title: Properties.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b9f9c2bdd36f1fc197a22c8866776da6aefe267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477454"
---
# <a name="propertiesappend-method-dao"></a><span data-ttu-id="390aa-102">Properties.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="390aa-102">Properties.Append Method (DAO)</span></span>


<span data-ttu-id="390aa-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="390aa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="390aa-104">新しい **Property** を **Properties** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="390aa-104">Adds a new **Property** to the **Properties** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="390aa-105">構文</span><span class="sxs-lookup"><span data-stu-id="390aa-105">Syntax</span></span>

<span data-ttu-id="390aa-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="390aa-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="390aa-107">\*式\***プロパティ**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="390aa-107">*expression* A variable that represents a **Properties** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="390aa-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="390aa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="390aa-109">名前</span><span class="sxs-lookup"><span data-stu-id="390aa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="390aa-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="390aa-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="390aa-111">データ型</span><span class="sxs-lookup"><span data-stu-id="390aa-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="390aa-112">説明</span><span class="sxs-lookup"><span data-stu-id="390aa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="390aa-113">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="390aa-113">Object</span></span></p></td>
<td><p><span data-ttu-id="390aa-114">必須</span><span class="sxs-lookup"><span data-stu-id="390aa-114">Required</span></span></p></td>
<td><p><span data-ttu-id="390aa-115"><strong>オブジェクト型 (Object)</strong></span><span class="sxs-lookup"><span data-stu-id="390aa-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="390aa-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="390aa-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="390aa-117">注釈</span><span class="sxs-lookup"><span data-stu-id="390aa-117">Remarks</span></span>

<span data-ttu-id="390aa-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="390aa-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="390aa-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="390aa-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="390aa-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="390aa-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="390aa-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="390aa-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>
