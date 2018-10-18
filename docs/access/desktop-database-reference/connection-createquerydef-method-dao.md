---
title: Connection.CreateQueryDef メソッド (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 35bf71742133b65c2e55583e1c62922cb5bc91e8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606040"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="9a717-102">Connection.CreateQueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a717-102">Connection.CreateQueryDef Method (DAO)</span></span>


<span data-ttu-id="9a717-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a717-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9a717-104">新しい **[QueryDef](querydef-object-dao.md)** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a717-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a717-105">構文</span><span class="sxs-lookup"><span data-stu-id="9a717-105">Syntax</span></span>

<span data-ttu-id="9a717-106">*式*です。CreateQueryDef (***名前***、 ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="9a717-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="9a717-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9a717-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="9a717-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a717-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a717-109">名前</span><span class="sxs-lookup"><span data-stu-id="9a717-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9a717-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="9a717-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="9a717-111">データ型</span><span class="sxs-lookup"><span data-stu-id="9a717-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="9a717-112">説明</span><span class="sxs-lookup"><span data-stu-id="9a717-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a717-113">名前</span><span class="sxs-lookup"><span data-stu-id="9a717-113">Name</span></span></p></td>
<td><p><span data-ttu-id="9a717-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a717-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="9a717-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="9a717-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9a717-116">新しい <strong>QueryDef</strong> の一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="9a717-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a717-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="9a717-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="9a717-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a717-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="9a717-119"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="9a717-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9a717-p101"><strong>QueryDef</strong> を定義する SQL ステートメントを表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。この引数を省略した場合、コレクションへの追加前または追加後に、<strong><a href="querydef-sql-property-dao.md">SQL</a></strong> プロパティを設定して、<strong>QueryDef</strong> を定義できます。</span><span class="sxs-lookup"><span data-stu-id="9a717-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a717-122"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9a717-122"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="9a717-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="9a717-123">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="9a717-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="9a717-124">Return value</span></span>
>>>>>>> <span data-ttu-id="9a717-125">master</span><span class="sxs-lookup"><span data-stu-id="9a717-125">master</span></span>

<span data-ttu-id="9a717-126">QueryDef</span><span class="sxs-lookup"><span data-stu-id="9a717-126">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="9a717-127">注釈</span><span class="sxs-lookup"><span data-stu-id="9a717-127">Remarks</span></span>

<span data-ttu-id="9a717-128">Microsoft Access ワークスペースでは、 **QueryDef** の作成時に名前として長さ 0 の文字列以外を指定すると、作成された **QueryDef** オブジェクトが **[QueryDefs](querydefs-collection-dao.md)** コレクションに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="9a717-128">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="9a717-129">Name で指定されたオブジェクトが既に**QueryDefs**コレクションのメンバーである場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9a717-129">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="9a717-130">一時**クエリ定義**を作成するには、 **CreateQueryDef**メソッドを実行すると、引数 name に長さ 0 の文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a717-130">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="9a717-131">新しく作成した [QueryDef](connection-name-property-dao.md) の \*\*\*\*Name\*\*\*\* プロパティを長さ 0 の文字列 ("") に設定することにより、これを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="9a717-131">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="9a717-132">一時的な **QueryDef** オブジェクトは、 **QueryDefs** コレクション内に新しい永続的オブジェクトを作成せずに動的 SQL ステートメントを繰り返し使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="9a717-132">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="9a717-133">長さ 0 の文字列は永続的な **QueryDef** オブジェクトの有効な名前ではないので、一時的な **QueryDef** をコレクションに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="9a717-133">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="9a717-134">新しく作成した **QueryDef** オブジェクトの **Name** プロパティと **SQL** プロパティはいつでも設定が可能であり、設定後に **QueryDef** を **QueryDefs** コレクションに追加できます。</span><span class="sxs-lookup"><span data-stu-id="9a717-134">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="9a717-135">**QueryDef** オブジェクトで SQL ステートメントを実行するには、 **[Execute](connection-execute-method-dao.md)** メソッドまたは **[OpenRecordset](connection-openrecordset-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a717-135">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="9a717-136">ODBC データベースを使用して SQL パススルー クエリを実行する場合は、 **QueryDef** オブジェクトの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9a717-136">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="9a717-137">Microsoft Access データベース エンジンのデータベースで **QueryDefs** コレクションから **QueryDef** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a717-137">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

